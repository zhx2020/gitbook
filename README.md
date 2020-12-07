## GitBook电子书

### 通过npm安装

```shell
npm install gitbook-cli -g
```

### 创建 README.md 和 SUMMARY.md 两个文件

**Introduction.md**

```md
# Introduction
说明文档
```

**SUMMARY.md**

```md
# Summary

* [Introduction](README.md)
* [section1](section1/README.md)
    * [example1](section1/example1.md)
    * [example2](section1/example2.md)
* [section2](section2/README.md)
    * [example1](section2/example1.md)
    * [example2](section2/example2.md)
```

### 初始化目录文件

```shell
gitbook init
```

### 预览书籍

```shell
gitbook serve
```

### 编译文件

```shell
gitbook build
```