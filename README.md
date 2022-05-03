# NBear```go
go run main.go

go mod init bitcoin 
```



pip install   -i https://pypi.douban.com/simple/  

文章从中国云厂商的角度，指出：1.中国云集体减速，原因是国内是Iaas占比大，Paas与Saas占比小，国外则是服务生态成熟。但国内已开始转型。

2.政企客户偏向云巨头扮演总集成商角色，需要“信创，自主可控”，与互联网市场“数据智能”不同，国家队崛起。

3.在IT支出结构方面，国内硬件大于软件和服务，国外相反。国内软件厂商处于云转型的中前期，服务模式未软件定制，项目集成为主，而非SaaS。国内云也开始注重业务健康度，明确自营产品和托管类产品比例。

4.中国云厂商的发展需要思考新的增长路径。国内正实现从“国家电力公司”到下游厂商的重新定位，集成、咨询、软件会占较大比重。

image（图纸），container（别墅），Service（别墅区），Swarm（土地）





```
10.101.15.27-29
```

Python3安装：

```
tar -zxvf Python-3.7.10.tgz
mkdir /usr/lib/python3.7
cd Python-3.7.10
./configure --prefix=/usr/lib/python3.7 --with-ssl
make && make install
rm -rf /usr/bin/python3 /usr/bin/pip3 /usr/bin/pip /usr/bin/python
ln -s /usr/lib/python3.7/bin/python3.7 /usr/bin/python3
ln -s /usr/lib/python3.7/bin/pip3.7 /usr/bin/pip3
ln -s /usr/bin/pip3 /usr/bin/pip
rm -f /usr/bin/python
ln -s /usr/bin/python3 /usr/bin/python
ll /usr/bin/ |grep python
python --version

vi /usr/bin/yum
vi /usr/libexec/urlgrabber-ext-down
```

安装Ray

```
pip install   -i https://pypi.douban.com/simple/  ray
find / -name ray
ln -s /usr/lib/python3.7/bin/ray /usr/bin

```

创建Ray Cluster

```
ray start --head --port=6379
ray start --address='10.101.15.27:6379' --redis-password='5241590000000000'

import ray
ray.init(address='10.101.15.27:6379', _redis_password='5241590000000000')

import ray
ray.init(address='ray://<head_node_ip_address>:10001')

ray stop

4. 检查结点是否加入
  （1） 可以在head结点使用ray status命令查看，用哪个取决于ray版本
  （2） 可以在worker节点使用ps aux | grep ray查看是否有对应进程
  （3） 如果下载了ray的整个项目，可以运行doc/kuernetes/example.py进行测试
```

运行python script

```
python ray_server_init.py
```

安装Helm

```
1.安装docker
2.安装kubelet、kubeadm、kubectl
3.创建集群
kubeadm join cluster-endpoint:6443 --token ho85r2.jr5pgds9qd1wkzh1     --discovery-token-ca-cert-hash sha256:2cc097c7f131586aedf6ccb619ddec791421f1ac26453efd1c69cdc116d5a8e0 
4.安装helm（chart&release）
5.Ray Helm chart.
 查询当前集群有哪些 chart 库 :helm repo list
 查看安装的应用 : helm list
 自定义Chart：ray6
```









4.16

Q：全局调度与本地调度关系， 执行流程（框架图解决）

​       蚂蚁 ray（调查)

​	   colmap



Reading：

Ray 的生态？开源的生态？

混合任务调度？



4.30

hi 像analytics zoo，infore，ray, Rheem你

![image-20220503125824511](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20220503125824511.png)



![image-20220503125834908](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20220503125834908.png)

5.7
