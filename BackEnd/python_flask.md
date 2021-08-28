[Node]: ./node_express.md
[SQL]: ./sql.md
[CP]: ../copy_pasta.md

# Python Flask Notes

### Table of Contents
1. [Installing Packages](#installing-packages)
2. [Python Notes](#python-notes)
    * [Run Unittest](#run-unittests)
3. [Flask Notes](#flask-notes)
    * [Run Flask](#run-flask)
    * [Blueprint](#blueprint)
4. [Postgres Notes](#postgres)
    * [Start Server](#start-postgres-server)
    * [Init VENV](#init-venv)
    * [Activate VENV](#activate-venv)
    * [Run Flask](#run-flask)
5. [Springboard Notes](#springboard-notes)

Other Files:
1. [Node Express][Node]
2. [SQL][SQL]
3. [Copy Pasta][CP]

---

# Installing Packages

#### Axios
    npm install axios

#### Install Flask
    pip3 install flask

#### Install flask-alchemy
    pip3 install psycopg2-binary
    pip3 install flask-sqlalchemy

#### Install flask-WTForm
    pip3 install flask-wtf

---

# Python Notes

#### Run unittests
    $ python3 -m unittest <fileName>

---

# Flask Notes

#### Run Flask
    flask run

---
# Blueprint
Blueprint is a handy way to link files in python-flask

#### ./app.py
    from routes.route_file import routes_name

    app = Flask(__name__)

    app.register_blueprint(routes_name)

#### ./routes/route_file.py
    from flask import Blueprint, render_template

    routes_name = Blueprint('routes_name', __name__)

    @routes_name.route("/")
    def rout_function():
        """THis is a normal route"""

        return render_template("index.html")

---

# Postgres

#### Start Postgres server
    sudo service postgresql start

#### Init VENV
    python3 -m venv venv

#### Activate VENV
    source venv/bin/activate

---

# Springboard Notes

*  #### [Intro To Python (18.1)](http://curric.rithmschool.com/springboard/lectures/python-intro/)

* #### [Python Data Structures (18.2)](http://curric.rithmschool.com/springboard/lectures/python-ds/)

* #### [Python Tools & Techniques (18.3)](http://curric.rithmschool.com/springboard/lectures/python-tools/)

* #### [Python Object Orientation (18.4)](http://curric.rithmschool.com/springboard/lectures/python-oo/)

* #### [Flask Intro (19.1)](http://curric.rithmschool.com/springboard/lectures/flask-intro/)

* #### [Templates & Jinja (19.2)](http://curric.rithmschool.com/springboard/lectures/flask-jinja/)

* #### [Flask Tools (19.3)](https://curric.rithmschool.com/springboard/lectures/flask-tools/)

* #### [Cookies & Sessions (19.4)](http://curric.rithmschool.com/springboard/lectures/flask-session/)

* #### [Flask Testing (19.5)](http://curric.rithmschool.com/springboard/lectures/flask-testing/)

* #### [WTForms (24.1)](http://curric.rithmschool.com/springboard/lectures/flask-wtforms/)

* #### [Flask with External Web APIs (24.2)](http://curric.rithmschool.com/springboard/lectures/flask-ext-apis/) 

* #### [REST and JSON APIs (24.3)](http://curric.rithmschool.com/springboard/lectures/flask-rest-json-api/)

* #### [Hashing and Login (24.5)](http://curric.rithmschool.com/springboard/lectures/flask-hashing-login/)

* #### [Flask Wrap-Up (24.6)](http://curric.rithmschool.com/springboard/lectures/flask-wrapup/)

* #### [Python Wrap-Up (24.7)](http://curric.rithmschool.com/springboard/lectures/python-wrapup/)

* #### [Deployment with Heroku (24.8)](http://curric.rithmschool.com/springboard/lectures/flask-heroku/)
