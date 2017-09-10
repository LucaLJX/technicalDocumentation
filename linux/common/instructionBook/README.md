
 > 参考： [linux命令大全](http://man.linuxde.net/)

### 文件目录管理

#### 目录操作

 - cd : 切换目录

```shell
cd /root/data/    #进入xxx目录
cd ../   #回到上一层目录
```

 - ls & dirs
    - ls : 显示目录内容列表
    - dirs : 显示目录记录
    
 - mkdir : 创建目录
 
 - mv: 移动或者重命名文件或目录

```shell
 $ mv file_test.txt /home/public/test  #将文件从当前目录移动到指定目录
 #移动多个文件
 $ mv file_test1 file_test2 /home/public/test
```

 - rm:删除目录或文件，一般形式为：rm [选项]... 目录
    - -d --directory 删除可能仍有数据的目录 (只限超级用户)
    - -f --force  略过不存在的文件，不显示任何信息
    - -i --interactive 进行任何删除操作前必须先确认
    - -r/R --recursive 同时删除该目录下的所有目录层
    - -v --verbose 详细显示进行的步骤
    - -v --help 显示此帮助信息并离开
    - -v --version 显示版本信息并离开

 - rmdir： 删除空目录
 
#### 文件处理

 - iconv：转换文件的编码方式
 
 - touch：创建新的空文件
 
 - cat： 链接文件并打印到标准输出设备上