# [Datta Able Flask](https://appseed.us/product/datta-able/flask/)

Open-source **Flask Dashboard** generated by `AppSeed` op top of a modern design. **[Datta Able](https://appseed.us/generator/datta-able/)** Bootstrap Lite is the most stylised Bootstrap 4 Lite Admin Template, around all other Lite/Free admin templates in the market. It comes with high feature-rich pages and components with fully developer-centric code. Before developing Datta Able our key points were performance and design.

- 👉 [Datta Able Flask](https://appseed.us/product/datta-able/flask/) - `Product page`
- 👉 [Documentation](https://docs.appseed.us/products/flask-dashboards/datta-able) - `Learn how to use and update the product`
- 🚀 Free [support](https://appseed.us/support/) for **registered users** (Email & `Discord`) 

<br />

> Built with [App Generator](https://appseed.us/generator/), timestamp `2022-09-18 20:26`

- `Up-to-date dependencies`
- Database: `sqlite`
- `DB Tools`: SQLAlchemy ORM, Flask-Migrate (schema migrations)
- Session-Based authentication (via **flask_login**), Forms validation
- `Dark Mode` (enhancement)
  - Persistent via browser `local storage`
  
<br />

![Datta Able (enhaced with dark mode) - Open-Source Seed project generated by AppSeed.](https://user-images.githubusercontent.com/51070104/176118649-7233ffbc-6118-4f56-8cda-baa81d256877.png)

<br />




## ✨ How to use it

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/appseed-projects/f0e4f2e8-5e75-4586-8814-7bbffa4c6694.git
$ cd f0e4f2e8-5e75-4586-8814-7bbffa4c6694
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ # CMD 
$ set FLASK_APP=run.py
$ set FLASK_ENV=development
$
$ # Powershell
$ $env:FLASK_APP = ".\run.py"
$ $env:FLASK_ENV = "development"
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:5000/register`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:5000/login`

<br />

## ✨ Code-base structure

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- routes.py                  # Define app routes
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- routes.py                  # Define authentication routes  
   |    |    |-- models.py                  # Defines models  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |    |    |-- includes/                  # HTML chunks and components
   |    |    |    |-- navigation.html       # Top menu component
   |    |    |    |-- sidebar.html          # Sidebar component
   |    |    |    |-- footer.html           # App Footer
   |    |    |    |-- scripts.html          # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # App Dependencies
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />

## ✨ Deploy APP with HEROKU

> The set up

- [Create a FREE account](https://signup.heroku.com/) on Heroku platform
- [Install the Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-python#set-up) that match your OS: Mac, Unix or Windows
- Open a terminal window and authenticate via `heroku login` command
- Clone the sources and push the project for LIVE deployment

<br />

> **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ # Get the code
$ git clone https://github.com/appseed-projects/<YOUR_BUILD_ID>.git
$ cd <YOUR_BUILD_ID>
```

<br />

> **Step 2** - Connect to `HEROKU` using the console

```bash
$ # This will open a browser window - click the login button (in browser)
$ heroku login
```
<br />

> **Step 3** - Create the `HEROKU` project

```bash
$ heroku create
```

<br />

> **Step 4** - Push Sources to `HEROKU`

```bash
$ git push heroku HEAD:master
```

<br />

> **Step 5** - Srt up the APP Environemnt in `HEROKU` (`.env` file is ignored by the platform)

- `DEBUG`=True
- `FLASK_APP`=run.py
- `FLASK_ENV`=development
- `ASSETS_ROOT`=/static/assets

![AppSeed - HEROKU Set UP](https://user-images.githubusercontent.com/51070104/171815176-c1ca7681-38cc-4edf-9ecc-45f93621573d.jpg)

<br />

> **Step 6** - Visit the app in the browser

```bash
$ $ heroku open
```

At this point, the APP should be up & running. 

<br />

> **Step 7** (Optional) - Visualize `HEROKU` logs

```bash
$ heroku logs --tail
```

<br />


## PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

Designed for those who like bold elements and beautiful websites, **Datta Able** is the most stylish Bootstrap 4 Admin Template compare to all other Bootstrap admin templates. It comes with high feature-rich pages and components with fully developer-centric code. 

- 👉 [Flask Datta PRO](https://appseed.us/product/datta-able-pro/flask/) - product page
  - ✅ `Enhanced UI` - more pages and components
  - ✅ `Improved Authentication`, Password Strength Checker
  - ✅ `Automatic User Suspension` on multiple failed logins
  - ✅ `Extended User profile`
  - ✅ `Users Management` (restricted to admins) 

<br >

![Datta Able PRO - Full-Stack Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/170474361-a58da82b-fff9-4a59-81a8-7ab99f478f48.png)

<br />

---
[Datta Able](https://appseed.us/generator/datta-able/) Flask - Open-source starter generated by **[AppSeed Generator](https://appseed.us/generator/)**.
