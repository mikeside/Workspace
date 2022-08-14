# Workspace
项目工作区、使用docker-compose 可快速构建开发环境服务
包含mysql，redis，mongo，rabbitmq、php、nginx、node、golang等

## 安装教程
```
git clone https://github.com/mikeside/Workspace.git
```

## 使用教程
- 根据需要，编辑docker-compose.yml配置文件
- 运行命令，启动docker-compose
```angular2html
docker-compose up -d
```

## 目录结构介绍
- 每个容器都有自己独立的目录，目录中包括数据和配置子目录


## 问题说明
- 配置文件挂载问题
> 由于docker官方坑爹的设计，导致容器内部配置文件无法反挂载出来

- 解决办法
> 拷贝容器内配置文件到当前工作区的容器config目录下
> 然后开启挂载，并运行 docker-compose up -d 即可！