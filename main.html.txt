<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calories Coach</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #ffff;
      color: #333;
    }

    /* Sidebar styles */
    #mySidenav a {
      position: absolute;
      left: -80px;
      transition: 0.3s;
      padding: 15px;
      width: 120px;
      text-decoration: none;
      font-size: 18px;
      color: white;
      border-radius: 0 5px 5px 0;
    }

    #mySidenav a:hover {
      left: 0;
    }

    /* Link specific styles */
    #home { top: 60px; background-color: #e9c46a; }
    #aboutus { top: 140px; background-color: #f4a261; }
    #target { top: 220px; background-color: #e76f51; }
    #faqs { top: 300px; background-color: #2a9d8f; }
    #contactus { top: 380px; background-color: #287271; }

    /* Page content */
    .content {
      margin-left: 140px;
      padding: 20px;
    }

    .header {
      background-color: #2594a3;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .intro {
      margin-top: 20px;
      font-size: 18px;
      line-height: 1.6;
    }

    /* Image transition styles */
    .image-container {
      text-align: center;
      margin-top: 20px;
    }

    .image-container img {
      width: 800px;
      height: 400px;
      border-radius: 10px;
      -webkit-transition: all 0.1s ease;
      -moz-transition: all 0.1s ease;
      -ms-transition: all 0.1s ease;
      -o-transition: all 0.1s ease;
      transition: all 0.1s ease;
    }

    /* Small round button styles */
    .button-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      max-width: 800px;
      margin: 20px auto;
    }

    .small-round-button {
      background-color: #fff;
      border: 2px solid black;
      border-radius: 50%;
      width: 120px;
      height: 120px; 
      margin: 20px 10px;
      cursor: pointer;
      position: relative;
      overflow: hidden; 
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .small-round-button img {
      width: 100%;
      height: 100%; 
      object-fit: cover; 
      border-radius: 50%; 
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity 0.3s ease;
      border-radius: 50%;
    }

    .small-round-button:hover .overlay {
      opacity: 1;
    }
  </style>
</head>
<body>
  <!-- Sidebar -->
  <div id="mySidenav" class="sidenav">
    <a href="#" id="home">Home</a>
    <a href="#" id="aboutus">About Us</a>
    <a href="#" id="target">Target</a>
    <a href="#" id="faqs">FAQs</a>
    <a href="#" id="contactus">Contact Us</a>
  </div>

  <!-- Header -->
  <div class="header">
    <h1>Welcome to Calories Coach</h1>
    <p>Your partner in maintaining a healthy lifestyle!</p>
  </div>

  <!-- Image with Transition -->
  <div class="image-container">
    <img id="slideshow" src="health5.jpg" alt="Health Tips">
  </div>

  <!-- Small Round Buttons -->
  <div class="button-container">
    <button class="small-round-button">
      <img src="calculator_img.jpg" alt="Calculator">
      <div class="overlay">Calculator</div>
    </button>
    <button class="small-round-button">
      <img src="exercise.jpg" alt="Exercise">
      <div class="overlay">Exercise</div>
    </button>
    <button class="small-round-button">
      <img src="diet.jpg" alt="Diet">
      <div class="overlay">Diet</div>
    </button>
    <button class="small-round-button">
      <img src="sleep.jpg" alt="Sleep">
      <div class="overlay">Sleep</div>
    </button>
    <button class="small-round-button">
      <img src="medicare.jpg" alt="Medicare">
      <div class="overlay">Medicare</div>
    </button>
    <button class="small-round-button">
      <img src="recipes.jpg" alt="Recipes">
      <div class="overlay">Recipes</div>
    </button>
  </div>

  <script>
    // Array of image sources
    const images = [
      "pic1.jpg", "pic2.jpg", "pic3.jpg", "pic4.jpg", "health4.jpg", "pic5.jpg",
    ];

    let currentIndex = 0;

    // Function to change the image
    function changeImage() {
      const imgElement = document.getElementById("slideshow");
      currentIndex = (currentIndex + 1) % images.length; // Loop back to start
      imgElement.src = images[currentIndex];
    }

    // Set interval to change the image every 3 seconds
    setInterval(changeImage, 3000);
  </script>
</body>
</html>
