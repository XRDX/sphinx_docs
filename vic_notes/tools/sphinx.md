# Sphnix使用手册

## 安装

1. 安装Python，建议使用Python 3


2. 安装Sphnix

```shell
pip install Sphnix
```

3. 安装md支持及主题

```shell
pip install recommonmark
pip install sphinx_rtd_theme
```

## 使用

创建一个新目录，在目录下执行命令
```shell
sphnix-quickstart
```
默认

修改conf.py文件
```python
# 添加md支持, 添加以下配置
from recommonmark.parser import CommonMarkParser

source_parsers = {
    '.md': CommonMarkParser,
}

# 修改以下配置
source_suffix = ['.rst', '.md']

# 修改主题
html_theme = 'sphinx_rtd_theme'
```

修改index.rst文件
```rst

```