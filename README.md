# Ex.08 Design of Interactive Image Gallery
## Date:13-12-2024

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
<html>
<head>
  <title>Interactive Photo Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f0f0f0;
      text-align: center;
    }

    h1 {
      background-color: #333;
      color: white;
      padding: 1rem;
      margin: 0;
    }

    .gallery {
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 20px;
    }

    .photo {
      display: inline-block;
      margin: 10px;
      border: 2px solid #ccc;
      border-radius: 10px;
      overflow: hidden;
    }

    .photo img {
      width: 200px;
      height: 150px;
      object-fit: cover;
    }

    #popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.7);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #popupContent {
      background: white;
      padding: 20px;
      border-radius: 10px;
      text-align: center;
    }

    #popupContent img {
      max-width: 100%;
      height: auto;
    }

    .close-btn {
      background-color: red;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 10px;
    }
  </style>
   <script>
    function openPopup(imageSrc, imageAlt) {
      var popup = document.getElementById("popup");
      var popupImage = document.getElementById("popupImage");

      popupImage.src = imageSrc;
      popupImage.alt = imageAlt;

      popup.style.display = "flex";
    }

    function closePopup() {
      var popup = document.getElementById("popup");
      popup.style.display = "none";
    }
  </script>
</head>
<body>
  <h1>Interactive Photo Gallery</h1>

  <div class="gallery">
    <div class="photo">
      <img src="food2.jpeg" alt="Photo 1" onclick="openPopup('food2.jpeg', 'Photo 1')" />
    </div>
    <div class="photo">
      <img src="food3.jpeg" alt="Photo 2" onclick="openPopup('food3.jpeg', 'Photo 2')" />
    </div>
    <div class="photo">
      <img src="food4.jpeg" alt="Photo 3" onclick="openPopup('food4.jpeg', 'Photo 3')" />
    </div>
  </div>

  <div id="popup">
    <div id="popupContent">
      <img id="popupImage" src="" alt="" />
      <br />
      <button class="close-btn" onclick="closePopup()">Close</button>
    </div>
  </div>

</body>
</html>


```
## OUTPUT:

![alt text](<Screenshot (67).png>)
![alt text](<Screenshot (68).png>) 

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
