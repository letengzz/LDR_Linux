# Linux 卸载 Docker

1. 杀死Docker中的所有容器：

   ```sh
   docker kill $(docker ps -a -q)
   ```

2. 删除所有docker容器：

   ```sh
   docker rm $(docker ps -a -q)
   ```

3. 删除所有docker镜像：

   ```sh
   docker rmi $(docker images -q)
   ```

4. 停止 docker 服务：

   ```sh
   systemctl stop docker
   ```

5. 删除docker相关存储目录(分别进行执行以下四个命令)：

   ```sh
   rm -rf /etc/docker
   rm -rf /run/docker
   rm -rf /var/lib/dockershim
   rm -rf /var/lib/docker
   ```

   如果删除不掉，则先umount，然后再重新执行1~4步骤：

   ```sh
   umount /var/lib/docker/devicemapper
   ```

6. 查看系统已经安装了哪些docker包：

   ```sh
   yum list installed | grep docker
   ```

7. 卸载相关包：接着会出现选择提示，直接输入“y”然后回车就可以。

   ```sh
   yum remove containerd.io.x86_64 docker-ce.x86_64 docker-ce-cli.x86_64 docker-ce-rootless-extras.x86_64 docker-scan-plugin.x86_64 docker-buildx-plugin.x86_64 docker-compose-plugin.x86_64
   ```

8. 再次查看，不再出现相关信息，证明删除成功：

   ```sh
   yum list installed | grep docker
   ```

9. 再看看docker命令：

   ```sh
   docker version
   ```

   