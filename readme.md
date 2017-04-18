

## 功能
```
1. 将文件上传（spss类型文件）并获取数据写入数据库
2. 获取内容生成spss文件
```

## 过程
1. 读取文件，得到列名和类型
2. 创建表
3. 存入数据--注意对时间的处理和指标签和说明 确定对mysql的处理
4. 读取数据返回web  暂缓
5. 日志
6. 异步处理


## 注意事项:
    1. 在存入库的时候将unicode的字符串进行了json(类型为VARCHAR)
    2. 时间模块存库的时候是字符串,不是json
    3. 字典, key为int, value为字符串时候,进行json, key会变成float, 反解的时候不能变成int, 重点是valueLables
    4. 对汉字的处理, savwrite的时候: ioutf-8, 看用途吧
    5. 对时间的处理 暂时只支持这两种b = "2016-11-15"  c = u'2016-09-21 13:37:34'


## 删除所有.pyc文件的命令
```find 绝对路径  -type f -name  "*.pyc"  | xargs -i -t rm -f {}```

## git上传命令
```
git add .
git commit -m ""
git push origin master
```