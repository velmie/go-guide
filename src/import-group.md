# Import Group Ordering

There should be two import groups:

- Standard(builtin) library
- External packages
- Internal packages

This is the grouping applied by goimports by default.

<table>
<thead><tr><th>Bad</th><th>Good</th></tr></thead>
<tbody>
<tr><td>

```go
import (
  "fmt"
  "os"
  "go.uber.org/atomic"
  "golang.org/x/sync/errgroup"
  "your-project/internal/package"
)
```

</td><td>

```go
import (
  "fmt"
  "os"

  "go.uber.org/atomic"
  "golang.org/x/sync/errgroup"

  "your-project/internal/package"
)
```

</td></tr>
</tbody></table>
