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

	it := tree.Iterator()
	for it.Next() {
		value := it.Value().(string)
		fmt.Printf("%v, %v\n", it.Key(), value)
	}

	rbtree := redblacktree.NewWithStringComparator()
	rbtree.Put("1", "hello world")
	it = tree.Iterator()
	for it.Next() {
		value := it.Value().(string)
		fmt.Printf("%v, %v\n", it.Key(), value)
	}
}
```