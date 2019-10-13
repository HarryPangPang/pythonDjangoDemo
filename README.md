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


#### 附使用
# 安装virtualenv
pip install virtualenv


# 创建虚拟环境
virtualenv venv


# 进入虚拟环境
venv\Scripts\activate

# 安装django
pip install django

# 创建project
django-admin startproject mysite


# 创建app
python manage.py startapp uploader


# 启动
python manage.py runserver


# 数据迁移-生成建表语句
python manage.py makemigrations


# 数据迁移-查看建表语句
python manage.py sqlmigrate polls 0001

    BEGIN;
    --
    -- Create model Question
    --
    CREATE TABLE "polls_question" ("id" integer NOT NULL PRIMARY KEY AUTOINCREMENT, "question_text" varchar(200) NOT NULL, "pub_date" datetime NOT NULL);

    --
    -- Create model Choice
    --
    CREATE TABLE "polls_choice" ("id" integer NOT NULL PRIMARY KEY AUTOINCREMENT, "choice_text" varchar(200) NOT NULL, "votes" integer NOT NULL, "questio
    n_id" integer NOT NULL REFERENCES "polls_question" ("id") DEFERRABLE INITIALLY DEFERRED);
    CREATE INDEX "polls_choice_question_id_c5b4b260" ON "polls_choice" ("question_id");
    COMMIT;


# 数据迁移-执行建表语句
python manage.py migrate

# 创建管理员
python manage.py createsuperuser
