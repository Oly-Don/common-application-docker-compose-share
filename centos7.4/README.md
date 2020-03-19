## 应用介绍-product introduce
- Centos 7.4.1708

### 优化内容-optimize index
- 1. 优化时区
- 2. 更新yum,不再需要yum update更新
- 3. 更改默认端口  shell 10022 (已开启); http 10080 (未开启,预留)
- 4. 预设用户;
```
(不存在sudoers文件,目前无法提权)
useradd appuser  && \
echo u6hCwUvd0w7uwjloHEPgVhwej65HTw | passwd --stdin appuser  && \
sed -i "appuser ALL=(ALL) NOPASSWD:ALL"  /etc/sudoers && \
```

### 连接使用
- 1 . Shell: 宿主 IP+10022 , 默认用户,密码: appuser u6hCwUvd0w7uwjloHEPgVhwej65HTw,未提权;
