# Django 샘플 튜토리얼 ( Django Sample Tutorial)
### 이 레포는 Django 프로젝트 하위의 연습용 앱이다 (This repo is located Django project and an app for practice)
1. 모델생성 및 디비에 마이그레이션 ( Define Models and Migrate to Database)
   1. ./models.py 에 클래스로 생성 (ORM 이라고 생각하면 쉬움) - Define relation in ./models.py file as a Class (just think it as a ORM then it feels easier)
   2. python manage.py makemigrations ${app_name}
   3. python manage.py sqlmigrate ${app_name} ${generated_migration_number}
      1. 출력되는 DML 확인 - check printed DML
   4. python manage.py migrate ${app_name}
   5. 언제든 모델 파일을 수정 후 makemigrations 를 실행하면 수정할 수 있다. - Whenever you can make a migration file by editing class in ./models.py  