## 部署

### 步骤

1. 登录Okteto云，点击Deploy


2. 复制本项目的git地址 `https://github.com/ivanphz/okvv.git`
3. 点击Git URL，粘贴git地址，点击`Deploy`

![](https://img.misaka.sbs/imgs/20210919162442.png)

okteto-docker-compose.yaml
services:
  okvv:
    build: .
    shm_size: 2.6gb
    ports:
      - "443:443"


| 变量 | 默认值 | 说明 |
| :--- | :--- | :--- |
| `ID` | `c156b24b-d468-41ba-c801-4d4755520051` | VLESS 用户 ID，用于身份验证，为 UUID 格式 |
| `WSPATH` | `/wsokteto` | WebSocket 所使用的 HTTP 协议路径 |
