# README

[![Build status](https://github.com/kenyon-wong/anki-sync-server-docker/workflows/Docker%20Image%20CI/badge.svg)](https://github.com/kenyon-wong/anki-sync-server-docker/actions)

用自编译 Rust 二进制可执行程序作为服务组件来封装的Anki 自托管同步服务器项目



## 编译镜像

### 手动编译

修改配置文件中的版本号之后，执行编译

```bash
docker build -t anki/syncd:v24.06.2 .
```

### GitHub action 自动编译

在仓库的 GitHub Actions 设置中，新增 `GITEA_USER`、`GITEA_TOKEN `和 `GITEA_SERVICE ` 这三个 secrets 键值对，然后手动运行 GitHub Actions 即可。

> `GITEA_USER`、`GITEA_TOKEN `和 `GITEA_SERVICE ` 这三个 secrets 键值对可以考虑任意兼容 docker pull 的包仓库对应参数，如果不需要使用包仓库也可以注释 GitHub Actions 中对应部分

关于 anki-sync-server 的版本更新方式：

在 `.github/VERSION.txt` 中的版本号，GitHub Actions 会自动运行编译。


## 参考资料

- [3 分钟为英语学习神器 Anki 部署一个专属同步服务器](https://www.cnblogs.com/ryanyangcs/p/17508044.html)
- [搭建 Anki 自托管同步服务器](https://blog.gazer.win/essay/build-anki-self-hosted-sync-server.html)
