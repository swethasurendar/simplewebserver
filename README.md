# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>

<body>
    <div style="display: flex;">
        <div style="width: 30%;"></div>
        <div style="width: 70%;">

            <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-indicators">
                    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0"
                        class="active" aria-current="true" aria-label="Slide 1"></button>
                    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
                        aria-label="Slide 2"></button>
                    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
                        aria-label="Slide 3"></button>
                    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3"
                        aria-label="Slide 4"></button>
                    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="4"
                        aria-label="Slide 5"></button>
                </div>
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="saveetha.0076.jpeg" class="d-block w-100" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="Screenshot 2023-10-19 192835.png" class="d-block w-100" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="Screenshot 2023-09-21 212845.png" class="d-block w-100" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="Screenshot 2023-10-19 204754.png" class="d-block w-100" alt="...">
                    </div>
                    <div class="carousel-item">
                        <img src="Screenshot 2023-09-21 205744.png" class="d-block w-100" alt="...">
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators"
                    data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators"
                    data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>
        </div>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
            integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
            crossorigin="anonymous"></script>
</body>

</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title><link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <style>
    .icon {
            color:brown;
            font-size: 25px;
            padding: 5px;
        }
        i:hover {
            color:grey
        }
        .menu{
            color:red;
            font-size: 20px;
            padding:5px;
        }
    </style><link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

</head>
<body>
    <div class="row border border-3 bgc">
    <div class="col-5">
        <i class="bi bi-youtube icon"></i>
        <i class="bi bi-twitter icon"></i>
        <i class="bi bi-whatsapp icon"></i>
        <i class="bi bi-instagram icon"></i>
    </div>
    <div class="col-5">
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNavDropdown">
            <ul class="navbar-nav">
              <li class="nav-item">
                <a class="nav-link menu" aria-current="page" href="#">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link menu" href="#">Alumini</a>
              </li>
              <li class="nav-item">
                <a class="nav-link menu" href="#">Events</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle menu" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  Department
                </a>
                <i class="bi bi-three-dots-vertical"></i>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item menu" href="#">computer networks</a></li>
                  <li><a class="dropdown-item menu" href="#">web application</a></li>
                  <li><a class="dropdown-item menu" href="#">information technology</a></li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>

</body>
</html>
class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 8000)
httpd = HTTPServer(server_address, MyHandler)

print("my webserver is running...")
httpd.serve_forever()

## OUTPUT:
[Screenshot 2024-03-29 223533.pdf](https://github.com/swethasurendar/simplewebserver/files/14807465/Screenshot.2024-03-29.223533.pdf)


## RESULT:
The program for implementing simple webserver is executed successfully.
