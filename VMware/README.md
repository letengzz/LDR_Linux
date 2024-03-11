# VMware

## 新建虚拟机

**操作步骤**：

1. 打开VMware，选择"文件" -> "新建虚拟机"

   ![image-20240311100053742](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111000003.png)

2. 选择配置类型("典型"即可)：

   ![image-20240311100256269](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111003484.png)

3. 选择镜像文件(后缀为Minimal)：

   **镜像下载地址**：https://buildlogs.centos.org/centos/7/isos/x86_64

   ![image-20240311132647328](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111326985.png)

4. 给虚拟机起名称(VMware显示名称)并设置虚拟机存放位置：

   ![image-20240311103248994](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928037.png)

5. 默认即可：

   ![image-20240311103320235](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928109.png)

6. 自定义硬件信息：(建议设置2G4核)

   ![image-20240311103405630](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928169.png)

7. 选择中文

   ![image-20240311133023363](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929014.png)

8. 设置时区为Asia/Shanghai：

   ![image-20240311133150539](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111928952.png)

9. 打开网络：

   ![image-20240311133352072](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929910.png)

10. 设置root密码：

    ![image-20240311133433039](https://cdn.jsdelivr.net/gh/letengzz/tc2/img202403111929997.png)

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