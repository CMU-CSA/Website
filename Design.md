# Design Document

updated: 07/30/2015 by Langxuan Su

## Basic Info

- Language: Python
- Framework: Django 
- Server: Gunicorn
- System: Linux?
- Database: MySQL/SQLite3
- Platform: GoDaddy
- Test Server: Heroku

## Installed Dependencies

- Python v2.7
- Django v1.8.3 
- gunicorn v19.3.0
- wheel v0.24.0
- whitenoise v2.0.2

## Installed Apps

- mainpage

## Models

##### mainpage:
- `models.py`

## View Controllers

##### mainpage:
- `views.py`:
    - `home` renders the home page
    - `contact` renders the contact page
    - `aboutus` renders the about us page
    - `activities` renders the activity list page (currently)

## Routes
*All relative to root*

- `/` redirects to `/home`

##### mainpage:
- `/home` calls `views.home`
- `/home/contact` calls `views.contact`
- `/home/aboutus` calls `views.aboutus`
- `/home/activities` calls `views.activities`

## Templates

##### mainpage:
- `base.html` the base html frame | include: `navbar.html`, `footer.html` | block: `navbar`, `content`
- `navbar.html` the navigation bar of home page
- `footer.html` the footer of home page
- `home.html` the home page | extends: `base.html` | block: `navbar`, `content`
- `contact.html` the contact page | extends: `base.html` | block: `content`
- `aboutus.html` the about us page | extends: `base.html` | block: `content`
- `activities` the activity list page | extends: `base.html` | block: `content `

## Static Files

##### mainpage:
- `style.css` styles for all pages | loaded in `base.html`
- `home.js` behaviors for all pages | loaded in `base.html`
