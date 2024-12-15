# Ex.08 Design of Interactive Image Gallery
## Date:15/12/2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background: #f4f4f9;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        h1 {
            margin: 20px 0;
            color: #444;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            max-width: 1200px;
            padding: 20px;
        }

        .gallery-item {
            width: 200px;
            height: 400px;
            border-radius: 8px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: filter 0.3s;
        }

        .gallery-item:hover img {
            filter: brightness(0.7);
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item .caption {
            position: absolute;
            bottom: 0;
            width: 100%;
            text-align: center;
            background: rgba(0, 0, 0, 0.6);
            color: #fff;
            padding: 10px 0;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .gallery-item:hover .caption {
            opacity: 1;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 10;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox .close {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #fff;
            font-size: 28px;
            cursor: pointer;
        }

        footer {
            margin-top: 20px;
            width: 100%;
            background: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
        }
    </style>
</head>
<body>
    <h1>Photo Gallery</h1>
    <div class="gallery">
        <div class="gallery-item">
            <img src="photo1.jpg" alt="Photo 1">
            <div class="caption">Tony Stark</div>
        </div>
        <div class="gallery-item">
            <img src="photo2.jpg" alt="Photo 2">
            <div class="caption">T'Challa</div>
        </div>
        <div class="gallery-item">
            <img src="photo3.jpg" alt="Photo 3">
            <div class="caption">Thor</div>
        </div>
        <div class="gallery-item">
            <img src="photo4.jpg" alt="Photo 4">
            <div class="caption">Petter Parkar</div>
        </div>
        <div class="gallery-item">
            <img src="photo5.jpg" alt="Photo 5">
            <div class="caption">Wanda</div>
        </div>
    </div>

    <div id="lightbox">
        <span class="close">&times;</span>
        <img src="" alt="Enlarged">
    </div>

    <footer>
        <p>&copy; 2024 Interactive Gallery Designed by Harish S</p>
    </footer>

    <script>
        const galleryImages = document.querySelectorAll('.gallery-item img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = lightbox.querySelector('img');
        const closeBtn = lightbox.querySelector('.close');

        galleryImages.forEach(img => {
            img.addEventListener('click', () => {
                lightbox.style.display = 'flex';
                lightboxImg.src = img.src;
            });
        });

        closeBtn.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });

        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) {
                lightbox.style.display = 'none';
            }
        });
    </script>
</body>
</html>


```

## OUTPUT:
![image](https://github.com/user-attachments/assets/2cbe1004-f7c9-4cc8-a200-c97376658335)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
