# fix-nastool-douban
修复豆瓣想看无法获取数据的问题

## docker 安装修复方法

1. 将修复后的webapi.py上传到服务器
2. 拷贝修复后的webapi.py文件路径 例如(/root/project/webapi.py)
3. 执行以下命令

```shell
# 备份源文件到/root目录下
docker cp 容器id:/nas-tools/app/media/doubanapi/webapi.py /root
# 拷贝修复后的webapi.py覆盖到nastool容器内
docker cp /root/project/webapi.py 容器id:/nas-tools/app/media/doubanapi/webapi.py
# 重启容器（替换容器id为你的容器id）
docker restart 容器id
```
4. 重启完毕后登陆nastool - > 服务 - > 豆瓣想看
5. 打开实时日志查看是否恢复
6. ![image-20230819020154718](http://file.92coco.cn/markdown_img/4828f8a306a541d5a10cbb4e7b56f60d.png)
