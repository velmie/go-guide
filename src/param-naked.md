# Avoid Naked Parameters

Prefer using (Functional Options)[#functional-options] instead of naked parameters or split your function into a few ones:

<table>
<thead><tr><th>Bad</th><th>Good</th></tr></thead>
<tbody>
<tr><td>

```go
// func getInfo(name string, useCache bool)

getInfo("foo", true)
```

</td><td>

```go
// func getInfo(name string)

// func getInfoUsingCache(name string)

getInfo("foo")
getInfoUsingCache("foo")
```

</td></tr>
</tbody></table>
