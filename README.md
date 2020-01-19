# kiwi linter x

基于kiwi linter修改，增加了i18nType配置项， 以满足覆盖方式为 ts('I18N.xx..', { val1, ... }).
注意：使用方式和kiwi linter 完全相同，自定义写入的键值也为I18N.xx.xx,  配置i18nType后会自动改变覆盖值为ts('I18N.xxx').

## 如何使用

> VS Code 插件搜索 kiwi linter 安装

> 推荐与[🐤 Kiwi-国际化全流程解决方案](https://github.com/alibaba/kiwi)结合使用


![演示](https://img.alicdn.com/tfs/TB1EYENfTnI8KJjy0FfXXcdoVXa-1006-368.gif)

![展示](https://img.alicdn.com/tfs/TB1pzAIC4YaK1RjSZFnXXa80pXa-884-308.png)

## 配置项

### vscode-i18n-linter.i18nType

default: `kiwi-intl`

重写中文的方式， 默认为I18N.xx.xxx； 设为react-intl，写入类型则为 ts('I18N.xx.xxx')

### vscode-i18n-linter.langPrefix

default: `.kiwi/zh-CN/`

多语言文件的位置, kiwi linter将根据目录内的多语言文件提取对应语言(默认为中文`zh-CN`)高亮.
可以参考的目录结构如下:
![示例目录结构](https://github.com/alibaba/kiwi/raw/master/kiwi-linter/assets/i18n-folder-structure.gif)

### vscode-i18n-linter.i18nFilesPattern

default: `**/src/**/ts*`

待扫描的文件类型，可以基于 [minimatch](https://github.com/isaacs/minimatch) 规则进行自定义。

### vscode-i18n-linter.markStringLiterals

default: `true`

是否标红中文字符串，默认开启。

### vscode-i18n-linter.showOverviewRuler

default: `true`

右侧滚动条中，是否显示对应的待提取中文高亮。

![](https://img.alicdn.com/tfs/TB1CHZRrxGYBuNjy0FnXXX5lpXa-1088-568.png)

### vscode-i18n-linter.markColor

default: `#ff4400`

待提取文字，高亮颜色。

### vscode-i18n-linter.enableReplaceSuggestion

default: `true`

是否开启一键提取中文功能。

## VS code 命令

### 在全部代码库中查找国际化文案
默认快捷键是 `cmd + ctrl + r`.


### 在当前文件中查找国际化文案
默认快捷键是 `cmd + ctrl + f`.

![](https://img.alicdn.com/tfs/TB1dzf8rpOWBuNjy0FiXXXFxVXa-1256-700.png)

## Changelog

### 1.1.4

-  优化国际化文案提示

### 1.1.2

- 支持 HTML 文件

### 1.0.0

- 支持国际化 Key 值显示
- 支持对应国际化文案的搜索
