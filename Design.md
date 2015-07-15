# Design Document

updated: 07/16/2015 by Langxuan Su

## Basic Info

- Language: Python
- Framework: Django 
- Server: Apache?
- System: Linux?
- Database: MySQL/SQLite3
- Platform: GoDaddy
- Test Server: Heroku?

## Installed Dependencies

- Python v2.7

- Django v1.8 installed with **pip**
    
        $ pip sudo install Django

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

## Routes

##### mainpage:
- `/home` calls `views.home`
- `/home/contact` calls `views.contact`
- `/home/aboutus` calls `views.aboutus`

## Templates

##### mainpage:
- `base.html` the base html frame | include: `navbar.html`, `footer.html` | block: `navbar`, `content`
- `navbar.html` the navigation bar of home page
- `footer.html` the footer of home page
- `home.html` the home page | extends: `base.html` | block: `navbar`, `content`
- `contact.html` the contact page | extends: `base.html` | block: `content`
- `aboutus.html` the about us page | extends: `base.html` | block: `content`

## Static Files

##### mainpage
- `style.css` styles for all pages | loaded in `base.html`
