# Start Enums at One

The standard way of introducing enumerations in Go is to declare a custom type
and a `const` group with `iota`. Since variables have a 0 default value, you
should usually start your enums on a non-zero value.

<table>
<thead><tr><th>Bad</th><th>Good</th></tr></thead>
<tbody>
<tr><td>

```go
type Operation int

const (
  Add Operation = iota
  Subtract
  Multiply
)

// Add=0, Subtract=1, Multiply=2
```

</td><td>

```go
type Operation int

const (
  Add Operation = iota + 1
  Subtract
  Multiply
)

// Add=1, Subtract=2, Multiply=3
```

</td></tr>
</tbody></table>

There are cases where using the zero value makes sense, for example when the
zero value case is the desirable default behavior.

Example 1:

```go
type LogOutput int

const (
  LogToStdout LogOutput = iota
  LogToFile
  LogToRemote
)

// LogToStdout=0, LogToFile=1, LogToRemote=2
```

Example 2:

```go
type CardType int

const (
  CardType_UNDEFINED CardType = iota
  CardType_PLASTIC
  CardType_VIRTUAL
)

// CardType_UNDEFINED=0, CardType_PLASTIC=1, CardType_VIRTUAL=2
```

---
**NOTE**

You also can use the package <https://github.com/abice/go-enum>.

---
