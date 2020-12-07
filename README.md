## GitBook电子书

### 通过npm安装

```shell
npm install gitbook-cli -g
```

### 创建两个文件

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

### 使用插件

创建 book.json 文件

```json
{
    "title": "GitBook",
    "author" : "echo",
	"output.name": "site",
    "description" : "电子书",
    "language" : "zh-hans",
	"gitbook" : "3.2.3",
	"root": ".",
	"links" : {
        "sidebar" : {
            "Home" : "http://zhangjikai.com"
        }
    },
    "styles": {
		"website": "styles/website.css",
		"ebook": "styles/ebook.css",
		"pdf": "styles/pdf.css",
		"mobi": "styles/mobi.css",
		"epub": "styles/epub.css"
	},
    "plugins": [
        "-lunr",
		"-search",
		"-highlight",
		"search-plus",
		"expandable-chapters",
		"chapter-fold",
		"splitter",
		"prism",
		"prism-themes",
		"github",
		"github-buttons",
		"tbfed-pagefooter",
		"edit-link",
		"copy-code-button",
		"simple-page-toc",
		"anchor-navigation-ex"
    ],
    "pluginsConfig": {
		"theme-default": {
			"showLevel": false
		},
		"prism": {
            "css": [
                "prism-themes/themes/prism-base16-ateliersulphurpool.light.css"
            ]
        },
		"github": {
			"url": "https://github.com/zhx2020"
		},
		"github-buttons": {
            "repo": "zhx2020/mybook",
            "types": [
                "star",
                "watch",
                "fork"
            ],
            "size": "small"
        },
		"tbfed-pagefooter": {
			"copyright":"Copyright &copy zhx2020.github.io 2020",
			"modify_label": "该文件修订时间：",
			"modify_format": "YYYY-MM-DD HH:mm:ss"
		},
		"edit-link": {
			"base": "https://github.com/USER/REPO/edit/BRANCH",
			"label": "Edit This Page"
		},
		"simple-page-toc": {
            "maxDepth": 3,
            "skipFirstH1": true
        },
		"anchor-navigation-ex": {
            "isRewritePageTitle": false,
            "isShowTocTitleIcon": false,
            "tocLevel1Icon": "fa fa-hand-o-right",
            "tocLevel2Icon": "fa fa-hand-o-right",
            "tocLevel3Icon": "fa fa-hand-o-right"
        }
    }
}
```

安装插件

```shell
gitbook install
```