https://flutter.dev/docs/get-started/web

1、flutter channel stable
2、flutter upgrade
3、flutter devices
4、flutter create myapp & cd myapp
5、flutter run -d chrome
6、flutter build web

坑1: 找到了index.html,用浏览器打开一片空白
这个属于正常的, 这个不像前端web ,html css js那套,点击index.html就能访问的. 在flutter里面是不能直接访问的,一定要放到容器里面去才能访问,如:tomcat等

坑2: 已经放到tomcat了,用浏览器打开还是一片空白
那是因为文件路径引用不对.解决办法有2种
方法1:
用编辑器打开index.html,能看到源文件,把<base href="/">,改成<base href="">

方法2:
用编辑器打开index.html,能看到源文件,把<base href="/">,改成你服务器的路径比喻说:<base href="http://192.168.1.80:3350/web/">