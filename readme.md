# bh-go-pagination

捕获科技 pagination 工具

## dev environment

go version

> go version go1.12 darwin/amd64 & go module enable

mysql version

> 5.7

## protobuf

run command

```bash
protoc -I. -I$GOPATH/src --go_out=. ./*.proto
```

## test 

run test

```bash

go test -v .
# === RUN   TestGetOptionCollection
# --- PASS: TestGetOptionCollection (0.00s)
#     pagination_test.go:13: 
#          GetOptionCollection result : &{PagingMode:1 GotoPageNumber:1 PageSize:15 CursorColumn:"id" CursorDirection:"desc"  15 0 [] [] false}
# === RUN   TestInitPagingOption
# --- PASS: TestInitPagingOption (0.00s)
#     pagination_test.go:26: 
#          InitPagingOption PagingMode:1 GotoPageNumber:1 PageSize:15 CursorColumn:"id" CursorDirection:"desc" 
# === RUN   TestNewCursorValue
# --- PASS: TestNewCursorValue (0.00s)
#     pagination_test.go:48: 
#          DefaultCursorValueHandler result : 0
# === RUN   TestCursorColumnExistInModel
# --- PASS: TestCursorColumnExistInModel (0.00s)
#     pagination_test.go:66: 
#          DefaultCursorColumnHandler result : true
# === RUN   TestToCamelString
# --- PASS: TestToCamelString (0.00s)
#     utils_test.go:16: 
#          snakeString(xx_yy) => camelString(XxYy)
# PASS
# ok      github.com/buhuoxinxi/bh-go-pagination  0.006s

```