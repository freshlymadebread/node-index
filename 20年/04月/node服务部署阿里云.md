  前天波仔找我玩耍，又提到了他导师给的任务，我发现最近学习了一段时间后，以前解决不了的问题，现在又有了思路，于是使用爬虫打算搞一下。
  然后准备自己买一个服务器，将一个简单的爬数据并将其返回前端的项目，部署到服务器。
1. 首先，购买阿里云服务器。这里我买的是学生版9.5元/月的云服务器。系统是centOS。
2. 然后，安装node，npm以及pm2，并使用ln /usr/local/nodejs/bin/node /usr/local/bin/ 等将他们加入到环境变量。这里我使用node官网的.tar.xz文件进行解压安装，.tar.xz文件需要解压两次，首先解压xz，然后tar。
3. 将项目放到 /usr/local/deployment/ 下，然后运行 pm2 start ./bin/www -name goods 即可。
4. 因为防火墙原因，外部不能访问，因此设置安全组。在入规则中 将3000/3000 设置为0.0.0.0/0（所有ip）使用TCP均可访问的。