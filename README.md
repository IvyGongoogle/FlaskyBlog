运行前的准备：
==============
0.安装virtualenv 虚拟环境
    apt-get install virtualenv
1.安装Flask
    apt-get install Flask
2.导入Flask必需的插件
    pip install -r requirements.txt

配置
===============
（示例代码中已经包含了data-dev.sqlite数据库文件）
初始化数据库迁移脚本
python manage.py db init

创建数据库，类似于db.create_all()，以后每一次更新数据模型，都要运行
python manage.py db migrate -m "init migration"

把更新后的数据模型应用到数据库
python manage.py db upgrade

运行网站
python manage.py runserver


测试用户
----------
用户名 john@example.com 密码 cat
用户名 sam@example.com 密码 sam