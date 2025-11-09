# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f4f4f4;
        }

        .gallery {
            padding: 50px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .thumbnail-container {
            display: flex;
            justify-content: center;
            gap: 100px;
            flex-wrap: wrap;
        }

        .thumbnail {
            width: 500px;
            height: 350px;
            object-fit: cover;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .thumbnail:hover {
            transform: scale(1.1);
        }

        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .lightbox-img {
            max-width: 80%;
            max-height: 80%;
            margin: 20px 0;
            border: 2px solid white;
            box-shadow: 0 0 10px black;
        }

        .caption {
            color: white;
            text-align: center;
            font-size: 18px;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body background="background.jpg">
    <h1 align="center"><font face="Kunstler Script" size="7">Beautiful Places of India</font></h1>
    <div class="gallery">
        <div class="thumbnail-container">
            <img src="tag.jpg" class="thumbnail" alt="Taj Mahal, Agra">
            <img src="mysorepalace.jpg" class="thumbnail" alt="City Palace, mysore">
            <img src="kerela.jpg" class="thumbnail" alt="Backwaters, Kerala">
            <img src="ladak.jpg" class="thumbnail" alt="Leh-Ladakh, Jammu & Kashmir">
            <img src="meenakishiamman temple.jpg" class="thumbnail" alt="Meenakshi Temple, Madurai">
        </div>
        <div class="lightbox">
            <span class="close">&times;</span>
            <img class="lightbox-img" src="" alt="">
            <div class="caption"></div>
        </div>
    </div>
    <script>
        const thumbnails = document.querySelectorAll('.thumbnail');
        const lightbox = document.querySelector('.lightbox');
        const lightboxImg = document.querySelector('.lightbox-img');
        const caption = document.querySelector('.caption');
        const closeBtn = document.querySelector('.close');

       
        thumbnails.forEach(thumbnail => {
            thumbnail.addEventListener('click', () => {
                lightbox.style.display = 'flex';
                lightboxImg.src = thumbnail.src;
                caption.textContent = thumbnail.alt;
            });
        });

       
        closeBtn.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });

        
        lightbox.addEventListener('click', (e) => {
            if (e.target !== lightboxImg) {
                lightbox.style.display = 'none';
            }
        });
    </script>
</body>
</html>
```

## OUTPUT
![alt text](<Screenshot 2025-11-09 181336.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
