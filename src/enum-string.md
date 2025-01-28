# String() for enums

Prefer to implement the `String()` method for custom enum types.

```go
type CardType int

const (
    CardType_UNDEFINED CardType = iota
    CardType_PLASTIC
    CardType_VIRTUAL
)

func (s CardType) String() string {
    switch s {
    case CardType_PLASTIC:
        return "plastic"
    case CardType_VIRTUAL:
        return "virtual"
    }
	
    return "undefined"
}

```

---
**NOTE**

You also can use the package <https://github.com/abice/go-enum>.

---
