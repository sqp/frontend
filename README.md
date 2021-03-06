# frontend

a Ponzu addon to create a web frontend for your CMS.

### To install:

[![GoDoc](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat)](https://godoc.org/github.com/bosssauce/frontend)
[![Go Report Card](https://goreportcard.com/badge/github.com/bosssauce/frontend)](https://goreportcard.com/report/github.com/bosssauce/frontend)

from within your Ponzu project, run:
```bash
$ ponzu add github.com/bosssauce/frontend
```
Usage: 

```go
// content/song.go

package content

import (
    // import the frontend addon
    "github.com/bosssauce/frontend"
    ...
)

type Song struct {
    title   string  `json:"title"`
    ...
}

func init() {
    // add routes/handlers to the frontend Router, which embeds a *mux.Router
    frontend.Router.HandleFunc("/songs", func(res http.ResponseWriter, req *http.Request) {
        // GET /api/contents?type=Song
        ...
    })
}
```
