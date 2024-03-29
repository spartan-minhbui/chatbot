## Chatbot - Reacjs, Django, Postgresql

### Frontend: Reactjs

- Chatbot base template: [React-simple-chatbot](https://github.com/LucasBassetti/react-simple-chatbot)
- Dockerfile contain commands to install packages for using in frontend.

### Backend: Django

- requirement.txt file contains library used in backend folder.

```
    Django>=3.0,<4.0
    psycopg2-binary>=2.8
    djangorestframework==3.7.7
    psycopg2==2.8.5
    django-cors-headers
    tensorflow
    bogo
    regex
    pandas
```

### NLP Model: RNN-LSTM

- Model :[BiLSTM](https://colab.research.google.com/drive/1qEfA7PqEmsjhy0hz653zzOsTGeOGQZPr?usp=sharing)
- Test accuracy: 0.937

### Install and setup environment for docker.

- [Docker](https://docs.docker.com/get-started/)

### Deploy chatbot.

- Run: `docker-compose up --build`

- Then, open new terminal in the same directory and type: `docker exec -it django_backend /bin/bash`

- Then, create superuser:

```
    python manage.py migrate
    python manage.py migrate --run-syncdb
    python manage.py createsuperuser
```

- Use the account you just created to login django admin backend at [Localhost](http://localhost:8000/admin/).
- Access [chatbot](http://localhost:3000) to use chatbot.
