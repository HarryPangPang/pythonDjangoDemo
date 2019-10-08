# pythonDjangoDemo
a samll django demo 

1. （venv）$ pip freeze>requirements.txt 依赖项
2. venv\Scripts\activate 激活虚拟环境
3. python manage.py runserver 启动
4. venv\Scripts\deactivate.bat 关闭虚拟环境

部署:
1. git clone
2. virtualenv venv -p python3.6 打开虚拟环境
3. source venv/bin/activate 初始化虚拟环境
4. pip install -r django-beginners-guide/requirements.txt 安装依赖
5. pip install gunicorn psycopg2