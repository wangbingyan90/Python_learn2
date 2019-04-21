# django 学习

安装

    pip3 install django

查看

    python -m django --version

创建项目(名称避免使用 django或test会出现冲突)

    django-admin startproject mysite
    创建目录结构
    mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        wsgi.py

外部mysite：根目录只是项目的容器。它的名字对Django来说无关紧要; 你可以将它重命名为你喜欢的任何东西。
manage.py：一个命令行实用程序，允许您以各种方式与此Django项目进行交互。
内部mysite：目录是项目的实际Python包。它的名称是您需要用来导入其中任何内容的Python包名称（例如mysite.urls）。
mysite/__init__.py：一个空文件，告诉Python该目录应该被视为Python包。如果您是Python初学者，请阅读官方Python文档中有关包的更多信息。
mysite/settings.py：此Django项目的设置/配置。 Django设置将告诉您有关设置如何工作的所有信息。
mysite/urls.py：这个Django项目的URL声明; 您的Django支持的站点的“目录”。您可以在URL调度程序中阅读有关URL的更多信息。
mysite/wsgi.py：与WSGI兼容的Web服务器的入口点，用于为您的项目提供服务。有关更多详细信息，请参阅如何使用WSGI进行部署。

PHP（没有使用现代框架），将代码放在Web服务器的文档根目录下（在某个地方/var/www）。使用Django，你不会这样做。将任何此Python代码放在​​Web服务器的文档根目录中并不是一个好主意，因为它可能会使人们可能通过Web查看您的代码。这对安全性不利。
将您的代码放在文档根目录之外的某个目录中，例如 /home/mycode。

启动 django-admin runserver [addrport]
    
    cd mysite
    python manage.py runserver

添加应用

    python manage.py startapp polls
    应用的目录结构
    polls/
        __init__.py
        admin.py
        apps.py
        migrations/
            __init__.py
        models.py
        tests.py
        views.py

