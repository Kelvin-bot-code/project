# Project Responsive Web Design using Bootstrap
# Date:
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
## index.html:
```html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>nivlek</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Static CSS -->
    <link rel="stylesheet" href="{% static 'css/styles.css' %}">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">nivlek</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="{% url 'sign_up' %}">Sign Up</a></li>
                    <li class="nav-item"><a class="nav-link" href="{% url 'sign_in' %}">Sign In</a></li>
                </ul>                
            </div>
        </div>
    </nav>

    <header class="bg-dark text-white text-center py-5">
        <div class="container">
            <h1 class="display-4">What are you working on?</h1>
            <p class="lead">nivlek is the go-to for creatives to show and tell their designs.</p>
            <a href="#" class="btn btn-primary btn-lg me-2">Learn More</a>
            <a href="sign-up.html" class="btn btn-pink btn-lg">Sign Up</a>
        </div>
    </header>

    <section class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="card">
                        <img src="{% static 'img/1.jpg' %}" class="card-img-top" alt="Sample Design">
                        <div class="card-body">
                            <h5 class="card-title">1</h5>
                            <p class="card-text">HELL RIDE</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card">
                        <img src="{% static 'img/2.jpg' %}" class="card-img-top" alt="Sample Design">
                        <div class="card-body">
                            <h5 class="card-title">2</h5>
                            <p class="card-text">KILL BILL</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card">
                        <img src="{% static 'img/31.png' %}" class="card-img-top" alt="Sample Design">
                        <div class="card-body">
                            <h5 class="card-title">3</h5>
                            <p class="card-text">oNCe uPoN a TiMe IN HoLLYWooD</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-dark text-white text-center py-3">
        <p>Designed by kelvin</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
## sing_in:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign In</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="index.html">nivlek</a>
        </div>
    </nav>

    <div class="container py-5">
        <h2 class="text-center mb-4">Sign In</h2>
        <form class="mx-auto" style="max-width: 400px;">
            <div class="mb-3">
                <label for="email" class="form-label">Email address</label>
                <input type="email" class="form-control" id="email" placeholder="Enter your email">
            </div>
            <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input type="password" class="form-control" id="password" placeholder="Enter your password">
            </div>
            <button type="submit" class="btn btn-primary w-100">Sign In</button>
            <p class="text-center mt-3">Don't have an account? <a href="{% url 'sign_up' %}">Sign Up</a></p>
        </form>
    </div>
</body>
</html>
```
## sign_up:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="index.html">nivlek</a>
        </div>
    </nav>

    <div class="container py-5">
        <h2 class="text-center mb-4">Sign Up</h2>
        <form class="mx-auto" style="max-width: 400px;">
            <div class="mb-3">
                <label for="name" class="form-label">Full Name</label>
                <input type="text" class="form-control" id="name" placeholder="Enter your full name">
            </div>
            <div class="mb-3">
                <label for="email" class="form-label">Email address</label>
                <input type="email" class="form-control" id="email" placeholder="Enter your email">
            </div>
            <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input type="password" class="form-control" id="password" placeholder="Create a password">
            </div>
            <button type="submit" class="btn btn-primary w-100">Sign Up</button>
            <p class="text-center mt-3">Already have an account? <a href="{% url 'sign_in' %}">Sign In</a></p>
        </form>
    </div>
</body>
</html>
```
# OUTPUT:
## index
![Screenshot 2024-12-23 104514](https://github.com/user-attachments/assets/dd45c6c3-a25c-4fcf-8c4a-0ca843ef852a)
## sign_up
![Screenshot 2024-12-23 104651](https://github.com/user-attachments/assets/91440fc7-17ff-4e0d-9b70-ecfb959d09c0)
## sign_in
![Screenshot 2024-12-23 104723](https://github.com/user-attachments/assets/2378a24e-fc04-461f-83a9-b21bbddde110)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
