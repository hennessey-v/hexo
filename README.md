## 内置环境

hexo 5.4.0

nodejs 12.22.6

npm 6.14.15

hexo-deployer-git 3.0.0

hexo-theme-fluid 1.8.13 [内置了hexo主题fluid 1.8.13]

## 使用镜像

#### 1.docker部署

```
docker run -dit \
  -v $PWD/hexo:/root/hexo \
  -p 4000:4000 \
  --name hexo \
  --hostname hexo \
  --restart unless-stopped \
  hennessey/hexo:latest
```

#### 2.docker-compose 部署
```shell
#待完善
```

## 配置

#### github+hexo模式环境配置

设置github变量
```shell
git config --global user.name "yourname" 
git config --global user.email "youremail"
(yourname是github用户名，youremail是注册github的邮箱)
```
检查是否正确，输入命令
```
git config user.name
git config user.email
```
#### SSH密钥

生成SSH密钥添加到GitHub

输入命令，创建SSH,一路回车
```
ssh-keygen -t rsa -C "youremail"
```

[**详细步骤请移步我的个人博客**](https://www.hennessey.xyz/2021/08/17/TermuxLinux%E6%90%AD%E5%BB%BAHexo%E5%8D%9A%E5%AE%A2/)
