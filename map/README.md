使用方法

```
docker build -t map:latest .
docker rm -f map
docker run -d --name map -p 80:80 map:latest
```
