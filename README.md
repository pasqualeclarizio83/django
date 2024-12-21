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