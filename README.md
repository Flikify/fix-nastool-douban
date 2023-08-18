# fixed-nastool-douban
修复豆瓣想看无法获取数据的问题

## docker 安装修复方法

1. 将修复后的webapi.py上传到服务器
2. 拷贝修复后的webapi.py文件路径 例如(/root/project/webapi.py)
3. 执行以下命令

```shell
# 备份源文件到/root目录下
docker cp nas-tools:/nas-tools/app/media/doubanapi/webapi.py /root
# 拷贝修复后的webapi.py覆盖到nastool容器内
docker cp /root/project/webapi.py nas-tools:/nas-tools/app/media/doubanapi/webapi.py
```

