# Django - Basi complete

### Start

#### O.S. Linux


[Start](https://github.com/pasqualeclarizio83/django/blob/main/start.png)



#### Ambiente virtuale. COme lo chiamo? venv.
#### Dipende dalla versione di python

```python

python -m venv venv | python3.10 -m venv venv

cd venv
cd bin
source activate

```
#### Ambiente virtuale attivo. è importante

```python
(venv)
```


[Ambiente Virtuale](https://github.com/pasqualeclarizio83/django/blob/main/venv.png)

#### E' bene installare il modulo del Framework Django

```python
pip install Django==3.2.15
```

[Installato Django](https://github.com/pasqualeclarizio83/django/blob/main/django_install.png)

#### Verificare che i pip siano installati?

```python
pip list
```

[pip list](https://github.com/pasqualeclarizio83/django/blob/main/pip_list.png)

#### Creamo il primo progetto. L'ho chiamato "nuovo_progetto"

```python
django-admin startproject nuovo_progetto
```

#### Creerà una nuova directory con la struttura di base di Django

[Django Creazione Progetto](https://github.com/pasqualeclarizio83/django/blob/main/django_creato.png)

#### Entrare nella cartella del progetto

```python
cd nuovo_progetto
```
#### Per la creazione di una Nuova App

```python
python manage.py startapp nuova_app
```

[Creata App](https://github.com/pasqualeclarizio83/django/blob/main/creata_app.png)

#### Questo creerà una nuova directory chiamata nuova_app all'interno del tuo progetto, contenente i file necessari per la tua applicazione.

#### Dopo aver creato la nuova Applicazione


[Struttura Progetto](https://github.com/pasqualeclarizio83/django/blob/main/struttura.png)

#### Apri il file nuovo_progetto/settings.py con un editor di testo e aggiungi 'nuova_app' alla lista INSTALLED_APPS:

[Settings è importante](https://github.com/pasqualeclarizio83/django/blob/main/settings.png)

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    'nuova_app',
```

[Struttura](https://github.com/pasqualeclarizio83/django/blob/main/settings.png)

#### Lanciando il seguente comando

```python
python3.10 manage.py runserver
```

[Runserver](https://github.com/pasqualeclarizio83/django/blob/main/runserver.png)

#### Apparirà una schermata simile a questa

[Home](https://github.com/pasqualeclarizio83/django/blob/main/home.png)

#### 1. Creo una tabella: Clienti
#### 2. Creo il modello, quindi il model
#### 3. Creo il Layout e tutto il resto

#### Andiamo passo passo.

#### Apri il file models.py della tua app (nuova_app/models.py) e aggiungi la seguente classe:

```python
from django.db import models

class Cliente(models.Model):
    nome = models.CharField(max_length=100)
    cognome = models.CharField(max_length=100)
    email = models.EmailField(unique=True)
    telefono = models.CharField(max_length=20, blank=True, null=True)
    indirizzo = models.TextField(blank=True, null=True)
    data_creazione = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return f"{self.nome} {self.cognome}"
```

[Models](https://github.com/pasqualeclarizio83/django/blob/main/models.png)

#### Dopo aver creato il model, è bene applicare le modifiche! Integrarle!

```python
python manage.py makemigrations
```

[Cosa appare?](https://github.com/pasqualeclarizio83/django/blob/main/models.png)

#### E dopo

[Models dove](https://github.com/pasqualeclarizio83/django/blob/main/models_dove.png)

```python
python manage.py migrate
```

#### Lanciato il seguente comando, tutte le rispettive Entità, ovvero i Models
#### saranno creati all'interno del DB. In questo caso è SQLLite. Il Db di Default di Django

[migrate](https://github.com/pasqualeclarizio83/django/blob/main/cmd_migrate.png)

#### settings per il database? SQlLite?

#### nuovo_progetto -> settings.py

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

[SqlLite](https://github.com/pasqualeclarizio83/django/blob/main/sqllite.png)

### DB: MySQL

#### E' necessario sicuramente, creare prima il database su MySQL DB

#### Accediamo

[MySQLDB](https://github.com/pasqualeclarizio83/django/blob/main/mysqldb.png)

#### Creare il database: example

[Example Db](https://github.com/pasqualeclarizio83/django/blob/main/mysql_db.png)

#### nuovo_progetto -> settings.py




