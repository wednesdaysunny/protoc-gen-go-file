# protoc-gen-go-file

小伙伴，有没有发现，现在在使用最新的protoc-gen-go 生成pb文件的时候，struct 中会莫名多出来如下字段

```
XXX_NoUnkeyedLiteral struct{}     `json:"-"`
XXX_unrecognized     []byte       `json:"-"`
XXX_sizecache        int32        `json:"-"`
```
这种字段会引起莫名的问题
在github的protobuf项目的issues里有相关问题，但是没有很好的解决办法
https://github.com/gogo/protobuf 倒是可以解决，也只是没有字段，但还是有方法。

目前也没有一个统一的解决办法，我还是使用的老版本的protoc-gen-go, 不会生成相关字段。
我把这个文件上传了，方便各位需要的下载。
方法也很简单
命令 which protoc-gen-go 可以获取你的文件路径，把下载的文件替换，chmod +x 文件路径即可。
剩下的就可以正常使用了。

