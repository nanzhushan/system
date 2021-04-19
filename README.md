## 采集linux指标, 可用于监控(以下内容只适合采集Linux不适合windows)

覆盖如下几类:
* cpu
* 内存
* io状态
* 磁盘占用
* 负载
* 内、外网卡的流入、流出流量等

## 使用
go get github.com/nanzhushan/system

```go
package main

import(
	"github.com/nanzhushan/system"
)

func main() {
    mem := &system.Mem{}
    mem.Collect()
    println("used:", mem.MemUsedFunc(""), "kb")
    println("free:", mem.MemFreeFunc(""), "kb")
}
```

更多监控项请参考源码注释.
