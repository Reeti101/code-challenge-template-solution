# Code Challenge Template
# Technology used
- Django
- Django Rest Framework
- SQLite for database

<br>

# Structure
- wx_data --> Weather data
- yld_data --> Yeild data
- src --> Source Code
- answers --> output.log


# Steps to run the program

- Create and run the virtual environment using commands: <br>
  pip install virtualenv <br>
  virtualenv env<br> <br> To activate virtual environment :<br>
  env/Scripts/activate (in Windows) <br>
  source env/bin/activate (in Linux and Mac)

- Navigate to "src/coding_test/" directory using command cd in terminal
- Install all the requirements using command <br> 
  pip install -r "requirements.txt"
- Migrate the models: <br>
  python manage.py makemigrations <br>
  python manage.py migrate
- Create superuser <br>
  python manage.py createsuperuser <br>
- Run the python server using command: <br>
  python manage.py runserver <br>
- Ingesting the data:<br>
  Run shell in another terminal using command: <br>python manage.py shell <br> <br>
  Run following commands:<br>
  from app.helper import import_weather, import_yield, Get_all_data_info<br>
  import_weather()<br>
  import_yield()<br>
  Get_all_data_info()

- Now all the data is uploaded, and it can be seen by accessing admin panel by visiting localhost: <br>
  http://127.0.0.1:8000/admin/login/?next=/admin/

- And other functionalities can be accessed through these API links: <br>
http://127.0.0.1:8000/api/weather<br>
http://127.0.0.1:8000/api/yield <br>
http://127.0.0.1:8000/api/weather/stats/

- With query params it can also be accessed such as : <br>
  http://127.0.0.1:8000/api/weather/?date=20100101

<br><br>
- To run the unittest you can run the command: <br>
  python manage.py test
