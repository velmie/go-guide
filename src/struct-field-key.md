# Use Field Names to Initialize Structs

You should almost always specify field names when initializing structs. This is
now enforced by [`go vet`].

  [`go vet`]: https://pkg.go.dev/cmd/vet

<table>
<thead><tr><th>Bad</th><th>Good</th></tr></thead>
<tbody>
<tr><td>

```go
k := User{"John", "Doe", true}
```

</td><td>

```go
k := User{
    FirstName: "John",
    LastName: "Doe",
    Admin: true,
}
```

</td></tr>
</tbody></table>

Exception #1: Field names *may* be omitted in test tables when there are 3 or
fewer fields.

```go
tests := []struct{
  op Operation
  want string
}{
  {Add, "add"},
  {Subtract, "subtract"},
}
```

Exception #2: Field names *should* be omitted in function-constructor

<table>
<thead><tr><th>Bad</th><th>Good</th></tr></thead>
<tbody>
<tr><td>

```go

type Consumer struct {
  logger string
  svc    string
}

func NewConsumer(logger string, svc string) *Consumer {
  return &Consumer{
    logger: logger,
    svc: svc,
  }
}

```

</td><td>

```go
type Consumer struct {
  logger string
  svc    string
}

func NewConsumer(logger string, svc string) *Consumer {
  return &Consumer{
    logger,
    svc,
  }
}
```

</td></tr>
</tbody></table>
