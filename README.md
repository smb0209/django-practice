# Django 샘플 튜토리얼<br/>Django Sample Tutorial
### 이 레포는 Django 프로젝트 하위의 연습용 앱이다 <br/>This is an app located below A Django project.
## Folder Structure 
***
```
${PROJECT_ROOT}
├── ${PROJECT}
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
├── ${THIS_APP}
│   ├── migrations
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   ├── views.py
└── db.sqlite3
└── manage.py
```

***

You can also reference other repositories as follows:
https://github.com/smb0209/docker-django

1. 모델생성 및 디비에 마이그레이션 <br/>Define Models and Migrate to Database
   1. ./models.py 에 클래스로 생성 (ORM 이라고 생각하면 쉬움) <br/>Define relation in ./models.py file as a Class (just think it as a ORM then it feels easier)
   2. python manage.py makemigrations ${app_name}
   3. python manage.py sqlmigrate ${app_name} ${generated_migration_number}
      1. 출력되는 DML 확인 <br/>check printed DML
   4. python manage.py migrate ${app_name}
   5. 언제든 모델 파일을 수정 후 makemigrations 를 실행하면 수정할 수 있다. <br/>Whenever you can make a migration file by editing class in ./models.py  