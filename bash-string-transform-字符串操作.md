## lowercase 变小写
```
$ string="A FEW WORDS"
$ echo "${string,}"  # 第一个字母小写
a FEW WORDS
$ echo "${string,,}" # 全小写
a few words
$ echo "${string,,[AEIUO]}"
a FeW WoRDS

$ string="A Few Words"
$ declare -l string
$ string=$string; echo "$string"
a few words

# 或用awk中的函数
echo $string|awk "{ print tolower($0) }"
```

## uppercase 变大写
```
$ string="a few words"
$ echo "${string^}"
A few words
$ echo "${string^^}"
A FEW WORDS
$ echo "${string^^[aeiou]}"
A fEw wOrds

$ string="A Few Words"
$ declare -u string
$ string=$string; echo "$string"
A FEW WORDS
```




