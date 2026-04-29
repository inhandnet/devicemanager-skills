# 远程隧道管理

通过 Device Manager 平台建立远程隧道，访问设备或设备背后的服务。

## 概念

- **隧道（Tunnel）**：平台与设备之间的安全通道，用于远程访问设备上的服务
- **协议（Proto）**：隧道支持的协议类型（TCP/UDP 等）
- **本地端口（Local Port）**：设备上的目标端口

## 创建隧道

```bash
devicemanager tunnel create \
  --name "Web管理" \
  --device-id <device-id> \
  --local-port 80 \
  --proto tcp \
  --local-address 127.0.0.1
```

## 管理隧道

```bash
# 列出所有隧道
devicemanager tunnel list

# 按设备过滤
devicemanager tunnel list --device-id <device-id>

# 连接隧道
devicemanager tunnel connect <tunnel-id>

# 断开隧道
devicemanager tunnel disconnect <tunnel-id>

# 更新隧道名称
devicemanager tunnel update <tunnel-id> --name "新名称"

# 删除隧道
devicemanager tunnel delete <tunnel-id>
```

## 典型场景

### 远程访问设备 Web 管理页面

```
步骤 1：创建隧道指向设备 80 端口
  devicemanager tunnel create --name "Web" --device-id <id> --local-port 80

步骤 2：连接隧道
  devicemanager tunnel connect <tunnel-id>

步骤 3：通过平台提供的访问地址打开浏览器
  （连接成功后平台会返回访问 URL）

步骤 4：使用完毕后断开
  devicemanager tunnel disconnect <tunnel-id>
```

### 远程 SSH 到设备

```
步骤 1：创建隧道指向设备 22 端口
  devicemanager tunnel create --name "SSH" --device-id <id> --local-port 22

步骤 2：连接隧道
  devicemanager tunnel connect <tunnel-id>

步骤 3：通过返回的地址 SSH 连接
```

### 访问设备背后的内网服务

```
步骤 1：创建隧道，local-address 指向内网 IP
  devicemanager tunnel create --name "内网服务" --device-id <id> \
    --local-address 192.168.1.100 --local-port 8080

步骤 2：连接并访问
  devicemanager tunnel connect <tunnel-id>
```

## 注意事项

- 设备必须在线才能创建和连接隧道
- 使用完毕后及时断开隧道，释放资源
- 不需要的隧道应及时删除
- 隧道名称建议包含用途说明，便于管理
