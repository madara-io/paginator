# paginator
[![go report card](https://goreportcard.com/badge/github.com/madara-io/paginator "go report card")](https://goreportcard.com/report/github.com/madara-io/paginator)
[![GoDoc](https://godoc.org/github.com/madara-io/paginator?status.svg)](https://godoc.org/github.com/madara-io/paginator)

## Usage

```bash
go get github.com/madara-io/paginator
```

```go
type Post struct {
    ID    int
    Title string
    Body  string
}

var posts []Post
db = db.Where("id > ?", 0)

pagination.Paging(&pagination.Param{
    DB:      db,
    Page:    1,
    Limit:   10,
    OrderBy: []string{"id desc"},
}, &posts)
```