# Ex.08 Design of Interactive Image Gallery

# Name :  Mohamed Faizal M
# Reg No : 212223243002
## Date:

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

gallery.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>INTERACTIVE GALLERY</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@700&display=swap" rel="stylesheet">
</head>
<body>
  <div class="container">
    <h1>✨INTERACTIVE GLOWING GALLERY✨</h1>
    <div class="gallery">
      <div class="card"><img src="i1.jpeg" alt="Image 1" /></div>
      <div class="card"><img src="i1.jpg" alt="Image 2" /></div>
      <div class="card"><img src="i2.jpeg" alt="Image 3" /></div>
      <div class="card"><img src="i3.webp" alt="Image 4" /></div>
      <div class="card"><img src="i4.jpg" alt="Image 5" /></div>
      <div class="card"><img src="i5.webp" alt="Image 6" /></div>
      <div class="card"><img src="i6.jpg" alt="Image 7" /></div>
      <div class="card"><img src="i7.jpeg" alt="Image 8" /></div>
      <div class="card"><img src="i8.jpg" alt="Image 9" /></div>
      <div class="card"><img src="i9.jpg" alt="Image 10" /></div>
      <div class="card"><img src="i10.jpeg" alt="Image 11" /></div>
      <div class="card"><img src="i11.jpg" alt="Image 12" /></div>
    </div>

    <div class="signature">
      <p>✨ DONE BY <strong>YASHWANTH K</strong> (212224040369) ✨</p>
    </div>
  </div>

  <!-- Modal popup for image enlarge -->
  <div id="modal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="modalImage">
  </div>

  <!-- JavaScript for interaction -->
  <script>
    const modal = document.getElementById("modal");
    const modalImg = document.getElementById("modalImage");
    const closeBtn = document.getElementsByClassName("close")[0];

    document.querySelectorAll('.card img').forEach(img => {
      img.addEventListener('click', () => {
        modal.style.display = "block";
        modalImg.src = img.src;
      });
    });

    closeBtn.onclick = function() {
      modal.style.display = "none";
    };

    window.onclick = function(event) {
      if (event.target == modal) {
        modal.style.display = "none";
      }
    };
  </script>
</body>
</html>
```

style.css

```
body {
  margin: 0;
  padding: 0;
  background: linear-gradient(to bottom, #0f2027, #203a43, #2c5364);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: white;
}

.container {
  text-align: center;
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
  font-size: 2.5rem;
  color: #00f5ff;
  text-shadow: 0 0 15px #00f5ff, 0 0 25px #00f5ff;
  margin-bottom: 40px;
  font-family: 'Exo 2', sans-serif;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* Fixed 4 columns per row */
  gap: 20px;
}

.card {
  background-color: #1e2f3f;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 0 15px rgba(0, 255, 255, 0.2);
  transition: transform 0.3s ease;
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 0 25px rgba(0, 255, 255, 0.6);
}

.signature {
  margin-top: 60px;
  padding: 20px;
  text-align: center;
  font-size: 1.6rem;
  font-family: 'Exo 2', sans-serif;
  background: linear-gradient(90deg, #ff0080, #7928ca, #00ffff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% auto;
  animation: colorChange 3s ease-in-out infinite;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
}

@keyframes colorChange {
  0% {
    background-position: 0% 50%;
  }
  100% {
    background-position: 100% 50%;
  }
}

/* Responsive for small screens (phones/tablets) */
@media (max-width: 992px) {
  .gallery {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .gallery {
    grid-template-columns: 1fr;
  }
}
```

## OUTPUT

<img width="971" height="461" alt="image" src="https://github.com/user-attachments/assets/68cd2504-b675-4bd8-9722-90229cff3ff5" />

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
