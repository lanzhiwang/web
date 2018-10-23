# First Web Applications Framework By Go

#### 开发环境说明

```bash
$ echo "PATH=${PATH}:/usr/local/go/bin" >> /etc/profile
$ mkdir -p ~/work/go_workspace
$ export GOPATH=/home/lanzhiwang/work/go_workspace
$ mkdir -p ~/work/go_workspace/src
$ cd ~/work/go_workspace
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ tree src
src
└── web
    ├── examples
    │   ├── arcchallenge.go
    │   ├── cookie.go
    │   ├── hello.go
    │   ├── logger.go
    │   ├── multipart.go
    │   ├── multiserver.go
    │   ├── params.go
    │   ├── secure_cookie.go
    │   ├── streaming.go
    │   └── tls.go
    ├── fcgi.go
    ├── helpers.go
    ├── LICENSE
    ├── Readme.md
    ├── scgi.go
    ├── secure_cookie.go
    ├── server.go
    ├── ttycolors.go
    ├── web.go
    └── web_test.go

2 directories, 20 files
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$

package path
(from $GOROOT) -> (from $GOPATH)

lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go get -u golang.org/x/crypto
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go get -u golang.org/x/net
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go get -u golang.org/x/sys
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go run src/web/examples/hello.go
string // /(.*)
func(string) string // 0x743eb0
2018/10/23 14:09:02 web.go serving [::]:9999

```

#### 重要的 go 基础

* 接口类型以及接口类型变量赋值
* reflect
    * type Type interface {}
    * type Value struct {}

* net/http

[感谢](https://github.com/hoisie/web)
