
#### 安装

```shell
npm install -g pm2
```
或者
```shell
cnpm install -g pm2
```

#### 启动进程

```shell
pm2 start app.js --name my_service
```
或者不同版本可以这样启动
```shell
pm2 start bin/www --name my_service
```
 > --name 参数指定启动之后的进程名
 
#### 查看所有进程
 
```shell
pm2 list
```
 
#### 查看日志
 
```shell
pm2 logs
```
查看指定进程的日志
```shell
pm2 logs my_service //通过指定进程的名称查看
 
pm2 logs 6 //通过进程id查看
```
 
#### 重启服务

```shell
pm2 restart <name or id>
```

#### 停止服务

```shell
pm2 stop <name or id>
```

#### 删除服务

```shell
pm2 delete <name or id>
```

#### 参数传递

例如下面的一个启动命令
```shell
node --expose-gc bin/www arg1 arg2 arg3
```
改成pm2之后启动
```shell
pm2 start bin/www --node-args="--expose-gc" -- arg1 arg2 arg3
```
**所有v8引擎参数均应放到-node-args中，所有的脚本参数放到-之后**

#### 重设id

 > 如果想到重新设置服务的id和顺序，可以通过pm2 kill 命令开重启pm2。
 
 **注意：重启pm2之后需要检查所有服务是否都启动了，重启机器同理。**
 
#### 参考

 - [How to reset the id of pm2?](https://stackoverflow.com/questions/30784548/how-to-reset-the-id-of-pm2)
 - [How to pass node v8 args and script args to pm2?](https://stackoverflow.com/questions/27690980/how-to-pass-node-v8-args-and-script-args-to-pm2)

