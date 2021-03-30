# redblacktree
red black tree

### Use         
```go
package main

import (
	"github.com/koomox/redblacktree"
	"fmt"
)

func main() {
	tree := redblacktree.NewWithIntComparator()
	tree.Put(1, "hello world")
	fmt.Println(tree.ToJSON())
}
```