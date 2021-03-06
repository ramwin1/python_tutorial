**Xiang Wang @ 2021-01-06 10:07:52**


### [pathlib](https://docs.python.org/3/library/pathlib.html)
```
from pathlib import Path
p = Path('.')
```

* iterdir(): 返回一个包含子文件的generator
```
import re
def get_number(name):
    '785e321f-7855-42a8-8365-2cd82488d581-2.png'
    return int(re.match("\S+-(\d+).png", name).groups()[0])
sorted(
    path.iterdir(),
    key=lambda i: 
)
```
* glob(pattern): 返回匹配的文件或者目录名
```
glob("*.pdf")
glob("**/*.pdf")
```
* mkdir(exist_ok=False): 创建目录
* stem: 最后的目录(排除后缀)
```
>>> PurePosixPath('my/library.tar.gz').stem
'library.tar'
>>> PurePosixPath('my/library.tar').stem
'library'
>>> PurePosixPath('my/library').stem
'library'
```
* as_posix(): 返回绝对路径
* joinpath(str|path): 合并路径
```
dirpath = Path("缓存")
cache_path = dirpath.join("运行缓存.json")
```
* name: 返回文件名
* suffix: 返回最后一个后缀名
```
>>> Path("README.md").suffix
'.md'
```
* suffixes: 返回后缀名列表
* unlink: 删除文件或者链接
* write_text: 写入文字然后关闭
