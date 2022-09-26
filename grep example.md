## 匹配单个关键字
grep keyword file_path
ls -l|grep keyword
git log|grep keyword

## 匹配多个关键字（或）
grep 'keyword_1\|keyword_2' file_path
grep -E 'keyword_1|keyword_2' file_path
grep -e 'keyword_1' -e 'keyword_2' file_path

## 过滤所有以.py结尾的结果 (用引号是个好习惯）
git ls-files|grep '.py$'

## 忽略大小写
-i 选项

## 关键字完整匹配，而不是whole
-w 选项

## 整行匹配
-x 选项

## 显示匹配的个数而非内容
-c 选项

## 显示不匹配的
-v 选项


## Manual
https://man7.org/linux/man-pages/man1/grep.1.html
