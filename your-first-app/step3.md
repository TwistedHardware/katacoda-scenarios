# Writing the app

Look in the tree view of your files for `main.go` and click on it.

In the code editor, add this code:

```golang
package main

import "github.com/uadmin/uadmin"

type Task struct {
    uadmin.Model
    Name string
    Done bool
}

func main() {
    uadmin.Register(Task{})
    uadmin.StartServer()
}
```

Finally, we will let golang initialize our modules and name the app `todo`. Run this in the terminal:

`go mod init todo`{{execute}}

Then run this to collect your dependencies:

`go mod tidy`{{execute}}