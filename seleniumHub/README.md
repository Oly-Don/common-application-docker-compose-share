## 应用介绍-product introduce
- 1. registry  默认版本:2.6.0


## 使用要求
- 1.  端口号为5000,不可被占用

### 优化内容-optimize index
- 1. chrome最大实例,由默认的5改为20      - NODE_MAX_INSTANCES=20
默认vnc端口 由默认的5900改为10001;      - "10001:5900"
- 2. firefox,由默认的5改为10      - NODE_MAX_INSTANCES=10
默认vnc端口 由默认的5900改为10001;      - "10002:5900"
- 3. 浏览器超时时间,由默认的600改为180:      - GRID_BROWSER_TIMEOUT="180"  用于快速释放浏览器资源
- 4. 块释放的时间,由默认的1800改为300:      - GRID_TIMEOUT="300"           用于快速释放浏览器资源

### 连接
- 1. selenium grid hub:  宿主IP+4444  , 无需验证,仅限局域网使用;如需验证,请使用harbor;
- 2. selenium grid chrome node VNC:  宿主IP+10001  , 用户密码: root secret
- 3. selenium grid firefox node VNC:  宿主IP+10002  , 用户密码: root secret