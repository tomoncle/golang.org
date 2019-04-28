# golang.org
go语言关于golang.org包的常用依赖

## 如何使用？
* 常见异常 1：
```
/usr/local/go/bin/src/github.com/sirupsen/logrus/terminal_check_notappengine.go:9:2: cannot find package "golang.org/x/crypto/ssh/terminal" in any of:
	/usr/local/go/src/golang.org/x/crypto/ssh/terminal (from $GOROOT)
	/home/liyuanjun/GolandProjects/src/golang.org/x/crypto/ssh/terminal (from $GOPATH)
	/home/liyuanjun/src/golang.org/x/crypto/ssh/terminal
	/usr/local/go/bin/src/golang.org/x/crypto/ssh/terminal
```

* 常见异常 2 :
```
..\src\github.com\sirupsen\logrus\terminal_check_notappengine.go:9:2: cannot find package "golang.org/x/crypto/ssh/terminal" in any of:
	C:\Go\src\golang.org\x\crypto\ssh\terminal (from $GOROOT)
	D:\WorkSpaces_ide\go_space\src\golang.org\x\crypto\ssh\terminal (from $GOPATH)
..\src\github.com\prometheus\common\log\eventlog_formatter.go:22:2: cannot find package "golang.org/x/sys/windows/svc/eventlog" in any of:
	C:\Go\src\golang.org\x\sys\windows\svc\eventlog (from $GOROOT)
	D:\WorkSpaces_ide\go_space\src\golang.org\x\sys\windows\svc\eventlog (from $GOPATH)
```

* 解决
```
$ cd $GOROOT/src
$ git clone --depth=1 https://github.com/tomoncle/golang.org.git golang.org
$ rm -rf $GOROOT/src/golang.org/.git
```

## 备注
> 所有的包(模块)，都在 https://github.com/golang 社区中存在，clone 到 `$GOROOT/golang.org/x` 包下即可.


