Prototype interface for examining core files.
The goal is to build a tool for understanding OOMs.
This is a WIP. See corefile/doc.go for known bugs and TODOs.


Quick start:

```
$ cd examples
$ ulimit -c unlimited
$ go build -o httpleak httpleak.go
$ GOTRACEBACK=crash ./httpleak
$ cd ../heapcheck && go run main.go /home/ebytes/go/src/github.com/tombergan/goheapdump/examples/core /home/ebytes/go/src/github.com/tombergan/goheapdump/examples/httpleak
$ cd ../heapview && go run main.go ./core ./httpleak
```
