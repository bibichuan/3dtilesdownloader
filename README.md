# 项目说明
项目来源：https://github.com/elfc2000/3dtilesdownloader, 主要就是从这个项目基础上进行了改进，把原先的python2代码，改为了python3代码

类似案例：https://github.com/junyuz/3dtiles_downloader

相关文章：
1.[3dTiles测试数据下载](https://blog.csdn.net/zipack/article/details/116036352)


# 使用说明

参数:

   -u --url  必选，需要下载的3d tiles 地址

   -d --dir  必选，需要保存的目录

   -s --start 可选，默认为0，有时候会下载失败，重新执行的时候可以通过此参数跳过前多少个

示例：
```sh
python3 downloader.py -u http://data.mars3d.cn/3dtiles/max-shihua/tileset.json -d ./data
```

这个数据里有 119 个b3dm，如果下载第100个出错，下次可以从第100个开始重新下载

```sh 
python3 downloader.py -u http://data.mars3d.cn/3dtiles/max-shihua/tileset.json -d ./data -s 100
```