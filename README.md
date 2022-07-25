# Event Fundraising Website

An event fundraising website where individuals can create personal pages, set goals and raise money for the overall goal.



## Features

* Fully responsive website that supports phones, tablets and computers
* Individuals can create custom fundraising pages with a photo, message and fundraising goal
* Email notifications to the fundraiser whenever a donation is received

## Installing

### Prerequisites

* [Python 3.7](https://www.python.org/)
* [git](https://git-scm.com/)

### Local installation

1. (optional) Create and activate a [virtualenv](https://virtualenv.pypa.io/) to have an isolated environment.
2. Clone this repository:

 
   `cd fundraising-website`

3. Install dependencies:

   `pip install -r requirements.txt`

4. Copy .env.example to .env:

   `cp .env.example .env`

5. Edit .env and add a SECRET_KEY value, a long (32 chars or more) random string.

6. Create a database:

   `python3 ./manage.py migrate`

7. Create a superuser - please use a strong password:

   `python3 ./manage.py createsuperuser`

8. Load test data into the database from fixtures:

   `python3 ./manage.py loaddata startingdata`

9. If everything installed, you should be able to start the Django development server:

   `python3 ./manage.py runserver localhost:8000`

10. You can browse to [http://localhost:8000/team_fundraising/](http://localhost:8000/team_fundraising/)

### Email

In order to send out emails when someone registers, makes a donation or receives a donation, you need to provide a mail server. A Gmail account can be used for this. Edit the .env file and add EMAIL_HOST, EMAIL_PORT, EMAIL_HOST_USER and EMAIL_HOST_PASSWORD.

## Built with

* [Python 3.7](https://docs.python.org/3/) - Primary language
* [Django 2.2](https://docs.djangoproject.com/en/2.2/) - Web Framework
* [Bootstrap 4](https://getbootstrap.com/docs/4.0/getting-started/introduction/) - Interface
