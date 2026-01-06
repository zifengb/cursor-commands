# Docker 日志追踪

追踪 Docker 容器日志以检查错误并监控应用程序行为。

## 说明

当用户请求查看容器日志时：

1. **发现运行中的容器**：首先，列出所有运行中的容器以查看可用的容器：

   ```bash
   docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Image}}"
   ```

2. **询问用户哪些容器**：展示列表并询问他们想监控哪些容器

3. **使用适当的命令**：根据他们的需求运行带有合适参数的 `docker logs`

## 常用命令

### 列出运行中的容器

```bash
docker ps --format "table {{.Names}}\t{{.Status}}\t{{.Image}}"
```

### 追踪特定容器的日志

```bash
docker logs -f <container_name>
```

### 带时间戳追踪日志

```bash
docker logs -f --timestamps <container_name>
```

### 追踪最后 N 行

```bash
docker logs -f --tail 100 <container_name>
```

### 查看特定时间以来的日志

```bash
docker logs -f --since 5m <container_name>
```

### 查看所有容器的日志（使用 docker compose）

```bash
docker compose logs -f
```

### 查看特定服务的日志

```bash
docker compose logs -f <service1> <service2>
```

### 过滤错误

```bash
docker logs <container_name> 2>&1 | grep -i error
```

## 使用流程

1. 运行 `docker ps` 发现可用容器
2. 向用户展示容器列表
3. 询问他们想追踪哪些容器
4. 询问是否需要任何过滤器（仅错误、最后 N 行、从某时间开始等）
5. 执行适当的 `docker logs` 命令

