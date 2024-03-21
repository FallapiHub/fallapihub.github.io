[**Home**](https://fallapihub.github.io)
[**Tierlists**](https://fallapihub.github.io/tierlists)
[**WebTech**](https://fallapihub.github.io/webtechleren)

# webtech leerlijst:
-------------------
## Week 1:
~~HTML~~ 

~~CSS~~

Bootstrap:

gedownload nu alleen nog leren en oefenen

hulp vragen aan olivier

https://www.youtube.com/watch?v=-qfEOE4vtxE&ab_channel=freeCodeCamp.org




-------------------
## ~~Week 2:~~
~~OOP Python~~

-------------------
## Week 3:
Databasebeheer in Python

SQLite basis

Muziek database ?

SQL in Python

SQL injections

Exceptions





-------------------
## ~~Week 4:~~
~~Flask~~

https://www.digitalocean.com/community/tutorials/how-to-create-your-first-web-application-using-flask-and-python-3#step-3-running-the-application




-------------------
## Week 5:
~~Flask Forms~~

~~WTFlask, WTF forms~~





-------------------
## Week 6:
Flask en SQL




-------------------
## Week 8:
Flask login







# GITTINGLIST
![image](https://github.com/FallapiHub/fallapihub.github.io/assets/158185370/2c99be46-300d-4982-97a6-c86c94faa8cc)

Ik weet ongeveer wat git is

Ik begrijp de github site

Ik weet ongeveer wat een repository is

Ik kan deze .md documentatie schrijven



### nog te leren:
hoe doe ik meerdere sites?:

https://www.youtube.com/watch?v=Q-YA_dA8C20 




~~Static markdown:~~

~~https://harrywang.medium.com/how-to-host-static-markdown-web-pages-using-github-pages-61f80a3a5136~~

















#SQL in python Standaard text


from flask import Flask
import os
from flask_sqlalchemy import SQLAlchemy

basedir = os.path.abspath(os.path.dirname(__file__))

app = Flask(__name__)

app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///' + os.path.join(basedir, 'data.sqlite')
app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False

db = SQLAlchemy(app)

class Cursist(db.Model):
    # __tablename__ = 'cursisten'
    id = db.Column(db.Integer, primary_key=True)
    naam = db.Column(db.Text)
    leeftijd = db.Column(db.Integer)

    def __init__(self, naam, leeftijd):
        self.naam = naam
        self.leeftij = leeftijd

    def __repr__(self):
        return f'Cursist {self.naam} is {self.leeftijd} jaar oud'


