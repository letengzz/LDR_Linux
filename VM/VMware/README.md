# VMware

## 新建虚拟机

打开VMware，选择"文件" -> "新建虚拟机"，一个虚拟机软件可以创建多个虚拟机，一个虚拟机就代表一台新的电脑。

![image-20240311100053742](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111000003.png)

## 典型配置

选择配置类型("典型"即可)：

![image-20240311100256269](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111003484.png)

选择镜像文件(后缀为Minimal)：

**镜像下载地址**：https://buildlogs.centos.org/centos/7/isos/x86_64

![image-20240311132647328](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111326985.png)

给虚拟机起名称(VMware显示名称)并设置虚拟机存放位置：

![image-20240311103248994](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928037.png)

默认即可：

![image-20240311103320235](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928109.png)

自定义硬件信息：(建议设置2G4核)

![image-20240311103405630](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928169.png)

选择中文

![image-20240311133023363](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929014.png)

设置时区为Asia/Shanghai：

![image-20240311133150539](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928952.png)

打开网络：

![image-20240311133352072](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929910.png)

设置root密码：

![image-20240311133433039](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929997.png)

## 自定义配置

选择配置类型("自定义"即可)：

![image-20240519103325401](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191033052.png)

选择硬件兼容性 (默认选项即可)：

![image-20240519103949149](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191039955.png)

稍后安装操作系统，只创建一台裸机：

![image-20240519104023193](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191040034.png)

选择操作系统类型：

![image-20240519104652816](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191046192.png)

选择名称并存放位置：

![image-20240519104833520](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191048534.png)

设置电脑的CPU数量：

![image-20240519105011941](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191050712.png)

设置内存大小：

![image-20240519105059131](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191051202.png)

指定网络连接方式为NAT：

![image-20240519105203455](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191052672.png)

在创建虚拟机时，网络连接模式有桥接模式和NAT模式，应该根据个人实际需求来选择。

- 桥接模式：虚拟机会直接接入宿主机网络中，相当于虚拟机相当于网络中的一个普通计算机，有自己的ip地址和MAC地址，可以访问网络上其他的设备。适用于需要虚拟机与宿主机处于同一网段的场景，如测试、网络应用开发等。 
- NAT模式：虚拟机通过虚拟化的NAT网络与宿主机连接，宿主机向虚拟机提供网络访问能力，虚拟机之间不能相互访问。NAT模式适用于虚拟机需要访问外部网络，但只有一个公共IP地址的情况下使用。 

总之，根据个人实际需求来选择适合自己的网络连接模式，有需要虚拟机与宿主机处于同一网段的情况选桥接模式，有需要虚拟机访问外部网络的情况选NAT模式。

选择IO控制器类型 (默认即可)：

![image-20240519105238333](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191052591.png)

选择硬盘类型 (默认即可)：

![image-20240519105327373](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191440856.png)

选择创建新的虚拟磁盘：

![image-20240519105407101](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191054548.png)

指定硬盘容量：

![image-20240519105448724](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191440886.png)

指定硬盘对应的文件：

![image-20240519105947407](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191059340.png)

查看电脑的配置，点击下图自定义硬件进行修改配置，点击完成即可：

![image-20240519110034012](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191440576.png)

下载操作系统的镜像文件：https://www.centos.org/download/

![image-20240519112207005](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191122249.png)

文件其实就相当于现实生活中的系统盘（光盘）。把这个文件放到虚拟机的DVD当中：

![image.png](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191212347.webp)

![image-20240519140017445](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191400254.png)

开启此虚拟机：

![image-20240519140128796](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191401527.png)

按上下键，移动到：Install CentOS Stream 9，然后回车。
**注意**：从虚拟机中释放鼠标的组合键是ctrl + alt

![image-20240519140335673](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191403429.png)

语言选择：简体中文，英文不错的话，可以使用英文，都可以

![image-20240519140612467](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191440183.png)

安装目的地，默认即可，点击完成：

![image-20240519141540949](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191415571.png)

设置root密码时允许root远程SSH登录：

![image-20240519141631353](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191416609.png)

软件选择：

![image-20240519141737193](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191417541.png)

点击开始安装：

![image-20240519141802810](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191418612.png)

安装完成后，点击右下角的重启系统即可：

![image-20240519143521635](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191435918.png)

配置操作系统：

![image-20240519143636254](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191436030.png)

设置定位服务，这属于隐私，可以打开，也可以关闭：

![image-20240519143658363](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191437874.png)

设置在线账号，这里跳过：

![image-20240519143730296](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191437430.png)

开启除了root管理员之外，开启的其他账户：

![image-20240519143803621](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191438229.png)

设置密码：

![image-20240519143831166](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191438073.png)

完成，点击开始使用：

![image-20240519143903475](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191439770.png)

查看一下网络是否正常：

![image-20240519143958674](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202405191440296.png)

## 修改bogon问题

如果提示符显示`root@bogon`，需要修改：

1. 查看ip地址：

   ```sh
   ip a
   ```

2. 修改host：

   ```
   vi /etc/hosts
   ```

3. 将 `ip localhost`放入到host即可

   ![image-20240311150513773](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111930032.png)

4. 重启网络：

   ```sh
   systemctl restart network
   ```

5. exit退出登录，重新再次登录即可

## 删除虚拟机

首先先关机，直接点击管理-彻底删除 即可。  

![image-20240311164026731](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929720.png)

## 克隆虚拟机

点击管理-克隆：

![image-20240311164124673](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929301.png)

选择虚拟机中的当前状态：

![image-20240311164251137](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929321.png)

选择完整克隆，否则会指向同一虚拟机：

![image-20240311164348552](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929459.png)

重新更改MAC地址，防止和之前的ip地址一致：

![image-20240311164620820](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929187.png)

重新启动即可

## 修改主机名

查看主机名：

```sh
more /etc/hostname
```

修改主机名：

```sh
hostnamectl set-hostname 新主机名
```

**例**：

```sh
# 修改
hostnamectl set-hostname localhost.localdomain
# 再次查看
more /etc/hostname
```

## 修改域名和IP

通过命令行修改IP地址：

1. 安装：

   ```sh
   yum install net-tools
   ```

2. 使用ifconfig命令查看当前网络接口名称，例如eth0。

3. 使用ifconfig命令将网络接口eth0关闭，例如执行命令：

   ```sh
   sudo ifconfig eth0 down
   ```

4. 使用ifconfig命令设置新的IP地址、子网掩码和网关，例如执行命令：

   ```sh
   sudo ifconfig eth0 192.168.0.100 netmask 255.255.255.0
   ```

5. 使用ifconfig命令将网络接口eth0重新启用，例如执行命令：

   ```
   sudo ifconfig eth0 up
   ```
