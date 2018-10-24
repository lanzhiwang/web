# First Web Applications Framework By Go

#### 开发环境说明


```bash
$ echo "PATH=${PATH}:/usr/local/go/bin" >> /etc/profile
GOROOT=/usr/local/go # 将安装包中的 bin 目录加到 $PATH 里，系统会自动推导出 GOROOT 的值
$ mkdir -p ~/work/go_workspace
$ export GOPATH=/home/lanzhiwang/work/go_workspace
$ export GOBIN=${GOPATH}/bin  # go install 或者 go build
$ export PATH=${PATH}:${GOPATH}/bin
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
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go fmt src/web/examples/hello.go
src/web/examples/hello.go
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go run src/web/examples/hello.go
string // /(.*)
func(string) string // 0x743eb0
2018/10/23 14:09:02 web.go serving [::]:9999

lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ go install src/web/examples/hello.go
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ ll
total 16
drwxrwxr-x 4 lanzhiwang lanzhiwang 4096 10月 24 11:47 ./
drwxrwxr-x 6 lanzhiwang lanzhiwang 4096 10月 23 12:59 ../
drwxrwxr-x 2 lanzhiwang lanzhiwang 4096 10月 24 11:47 bin/
drwxrwxr-x 4 lanzhiwang lanzhiwang 4096 10月 23 14:06 src/
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ ldd bin/hello
	linux-vdso.so.1 (0x00007ffdc77a3000)
	libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f4dcdac5000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f4dcd6d4000)
	/lib64/ld-linux-x86-64.so.2 (0x00007f4dcdce4000)
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$
lanzhiwang@lanzhiwang-desktop:~/work/go_workspace$ readelf -a bin/hello

```

#### 重要的 go 基础

* 接口类型以及接口类型变量赋值
* reflect
    * type Type interface {}
    * type Value struct {}

* net/http

#### 框架基本架构

![](https://github.com/lanzhiwang/web/blob/master/go_web_01.jpg)

![](https://github.com/lanzhiwang/web/blob/master/go_web_02.jpg)



[感谢](https://github.com/hoisie/web)
