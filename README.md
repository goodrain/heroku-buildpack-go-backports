# Heroku Buildpack for Go![travis ci](https://travis-ci.org/heroku/heroku-buildpack-go.svg?branch=master)

云帮 Go 语言项目的源码构建核心部分是基于[Heroku buildpack for java](http://devcenter.heroku.com/articles/buildpack) 来实现的。

## 工作原理

当buildpack检查您的应用含有如下情况时，您的应用被识别为Go应用：

- 在根目录的`/Godeps`目录下有`Godeps.json`文件，标识应用由[godep](https://devcenter.heroku.com/articles/go-dependencies-via-godep)管理。
- 在根目录的`/vendor`目录下有`Govendor.json`文件，标识应用由[govendor](https://devcenter.heroku.com/articles/go-dependencies-via-govendor)管理。
- 在根目录的`/src`目录下包含`<文件名>.go`文件，标识应用由[gb](https://devcenter.heroku.com/articles/go-dependencies-via-gb)管理。

## 文档

以下文章了解更多：

- [云帮支持Go](http://www.rainbond.com/docs/stable/user-lang-docs/go/lang-go-overview.html)
- [使用Beego等框架](http://www.rainbond.com/docs/stable/user-lang-docs/go/lang-go-beego.html)

## 配置

### Go Tools版本

- Glide 默认支持版本v0.12.3
- Govendor 默认支持版本1.0.8
- GB 默认支持版本 0.4.3
- PkgErrors 默认支持版本 0.8.0
- HG 默认支持版本3.9

## 授权

根据 MIT 授权证获得许可。 请参阅LICENSE文件