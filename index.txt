<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Divya Ayodhya</title>
    <link rel="stylesheet" href="Assets/css/index.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <!-- fontswesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    
</head>
<body>

<nav class="navbar navbar-expand-lg header">
  <div class="container headerContainer">
  <button class="bg-transparent border-0 d-md-flex d-lg-none">  <img style="height:20px" src="Assets/Images/circle-user-regular.svg"> </button>
    <a class="navbar-brand" href="#">
     <img src="Assets/Images/image 301.png">
    Divya Ayodhya</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    
    <div class="collapse navbar-collapse " id="navbarNav">
      <ul class="navbar-nav ms-auto" id="navbarItems">
        <!-- List items will be dynamically changed based on screen width. if need to change something chech update function below-->
      </ul>
      
    </div>
  </div>
  <ul class="navbar-nav subNav d-md-flex d-lg-none">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="stay-in-ayodhya">Homestay</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="tour-package">Tour Packages</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="souvenir">Souvenir</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="about.php">Cabs</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="login">Tour Guide</a>
        </li>
      </ul>
</nav>

<!-- hero Section -->
 <div class="container-fluid p-0 heroSection ">
 <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="Assets/Images/Banner 1.png" class="d-block w-100" alt="first slide">
    </div>
    <div class="carousel-item">
      <img src="Assets/Images/Banner 1.png" class="d-block w-100" alt="second slide">
    </div>
    <div class="carousel-item">
      <img src="Assets/Images/Banner 1.png" class="d-block w-100" alt="third slide">
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>

<!-- utility section -->
<div class="utilitySection" >
<div>
  <img src="Assets/images/honey_moon.png.png" >
  <h6> Homestays </h6>
</div>
<div>
  <img src="Assets/images/honey_moon.png.png" >
  <h6> Cabs </h6>
</div>
<div>
  <img src="Assets/images/honey_moon.png.png" >
  <h6> Tour Packages </h6>
</div>
<div>
  <img src="Assets/images/honey_moon.png.png" >
  <h6> Souvenir </h6>
</div>
<div>
  <img src="Assets/images/honey_moon.png.png" >
  <h6> Book Guide </h6>
</div>
</div>
 </div>


<!-- homestay section -->
<div class="container homeStaySection">
    <h2 class="textMaroon">Book Trending <span class="text-warning1">Homestays</span></h2>
    <p class=" textMaroon">Book best stays in Ayodhya at reasonable prices for your visit.</p>

    <div class="row homeStayRow">
        <?php
        $homestays = [
            [
                'image' => 'Assets/Images/image.png',
                'name' => 'Amar Villa',
                'location' => '5/8/90, Amaniganj Ram Path, Ayodhya',
                'price' => 3500,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image (1).png',
                'name' => 'Nandigram Eco Friendly Villa',
                'location' => 'Nandigram, Bharatkund, Ayodhya',
                'price' => 1400,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image (2).png',
                'name' => 'Shri Ram Kripa Kunj Homestay',
                'location' => 'Agnikund, Ayodhya',
                'price' => 2000,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image (3).png',
                'name' => 'Shree Hanumant Place',
                'location' => 'Balu Ghat Ayodhya',
                'price' => 1500,
                'rating' => 3.8,
            ],
        ];
        // <i class="fa-solid fa-star" ></i>
        foreach ($homestays as $homestay) {
            echo "
            <div class='col-md-3 homestayCol'>
                <div class='card homeStayCard '>
                    <img src='{$homestay['image']}' class='card-img-top' alt='{$homestay['name']}'>
                    <div class='card-body'>
                     <span class=''><i class='fas fa-star' style='color: #FEA330'></i> {$homestay['rating']}</span><br>
                        <h5 class='card-title homeStayCardTitle'>{$homestay['name']}</h5>
                        <p class='card-text homeStayCardText'>
                           <i class='fa-solid fa-location-dot' style='color: #E4821C;'></i>
                            {$homestay['location']}<br>
                            <span class='text-danger'>Rs {$homestay['price']}.00 /person</span>
                        </p>
                    </div>
                </div>
            </div>
            ";
        }
        ?>
    </div>
</div>

<!-- mid hero section -->
<div class="container midHeroSection "> 
  <picture> 
    <source media="(max-width:992px)" srcset="Assets/Images/malaysia-banner-mob.png.png">
    <img src="Assets/Images/malaysia-banner-sp.png.png" alt="Malaysia Banner">
  </picture>
</div>


<!-- Home services Section -->
<div class="container hServSection ">
    <h2 class="textMaroon">Divya Ayodhya<span class="text-warning1"> Services</span></h2>
    <p class=" textMaroon mb-5">Explore the services offered by Divya Ayodhya.</p>

  <!-- Scroll Button -->
  <button id="scrollRightBtn" class="btnRight"> <i class="fa-solid fa-arrow-right" style="color: #000000;"></i> </button>
    <!-- <button id="scrollLeftBtn" class="btn btn-primary mb-3">Scroll Left</button> -->


    <div id="hServContainer" class="row hServRow">
        <?php
        $homestays = [
            [
                'image' => 'Assets/Images/Rectangle 1075.png',
                'name' => 'Amar Villa',
                'location' => '5/8/90, Amaniganj Ram Path, Ayodhya Nandigram, Bharatkund, Ayodhya',
               
            ],
            [
                'image' => 'Assets/Images/image (a).png',
                'name' => 'Nandigram Eco Friendly Villa',
                'location' => 'Nandigram, Bharatkund, Ayodhya Nandigram, Bharatkund, Ayodhya',
               
            ],
            [
                'image' => 'Assets/Images/image (b).png',
                'name' => 'Shri Ram Kripa Kunj Homestay',
                'location' => 'Agnikund, Ayodhya Nandigram, Bharatkund, Ayodhya',
                
            ],
            [
                'image' => 'Assets/Images/image (c).png',
                'name' => 'Shree Hanumant Place',
                'location' => 'Balu Ghat Ayodhya Nandigram, Bharatkund, Ayodhya',
                
            ],
            [
              'image' => 'Assets/Images/image-aa.png',
              'name' => 'Amar Villa',
              'location' => '5/8/90, Amaniganj Ram Path, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/image (5).png',
              'name' => 'Nandigram Eco Friendly Villa',
              'location' => 'Nandigram, Bharatkund, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/image (6).png',
              'name' => 'Shri Ram Kripa Kunj Homestay ',
              'location' => 'Agnikund, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/image (7).png',
              'name' => 'Shree Hanumant Place',
              'location' => 'Balu Ghat Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
            'image' => 'Assets/Images/image (8).png',
            'name' => 'Amar Villa',
            'location' => '5/8/90, Amaniganj Ram Path, Ayodhya Nandigram, Bharatkund, Ayodhya',
           
        ],
        [
            'image' => 'Assets/Images/image (a).png',
            'name' => 'Nandigram Eco Friendly Villa',
            'location' => 'Nandigram, Bharatkund, Ayodhya Nandigram, Bharatkund, Ayodhya',
            
        ],
        
        ];
        // <i class="fa-solid fa-star" ></i>
        foreach ($homestays as $homestay) {
            echo "
            <div class='col-md-3 hServCol'>
                <div class='card hServCard '>
                    <img src='{$homestay['image']}' class='card-img-top' alt='{$homestay['name']}'>
                    <div class='card-body'>
                        <h5 class='card-title hServCardTitle'>{$homestay['name']}</h5>
                        <p class='card-text hServCardText'>
                            {$homestay['location']}<br>
                            
                        </p>
                    </div>
                </div>
            </div>
            ";
        }
        ?>
    </div>
</div>

<!-- tour package section -->
<div class="container tourSection">
    <h2 class="textMaroon">Trending<span class="text-warning1"> Tour Packages & Intercity cabs</span></h2>
    <p class=" textMaroon mb-5">Explore the services offered by Divya Ayodhya.</p>
    <div id="" class="row tourRow">
        <?php
        $homestays = [
           
            [
              'image' => 'Assets/Images/Link.png',
              'name' => 'Amar Villa',
              'location' => '5/8/90, Amaniganj Ram Path, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/Link (1).png',
              'name' => 'Nandigram Eco Friendly Villa',
              'location' => 'Nandigram, Bharatkund, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/Link (2).png',
              'name' => 'Shri Ram Kripa Kunj Homestay ',
              'location' => 'Agnikund, Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
              'image' => 'Assets/Images/Link (3).png',
              'name' => 'Shree Hanumant Place',
              'location' => 'Balu Ghat Ayodhya Nandigram, Bharatkund, Ayodhya',
              
          ],
          [
            'image' => 'Assets/Images/Link (4).png',
            'name' => 'Amar Villa',
            'location' => '5/8/90, Amaniganj Ram Path, Ayodhya Nandigram, Bharatkund, Ayodhya',
           
        ],
        [
            'image' => 'Assets/Images/Link (5).png',
            'name' => 'Nandigram Eco Friendly Villa',
            'location' => 'Nandigram, Bharatkund, Ayodhya Nandigram, Bharatkund, Ayodhya',
            
        ],
        
        ];
        // <i class="fa-solid fa-star" ></i>
        foreach ($homestays as $homestay) {
            echo " 
            <a class='col-md-4 tourCol'>
                <div class='card tourCard '>
               
                    <img src='{$homestay['image']}' class='' alt='{$homestay['name']}'>
               
                </div>
            </a>
            ";
        }
        ?>
    </div>
</div>

<!-- visit section -->

    <div class="container visitSection ">
    <h2 class="textMaroon"><span class="text-warning1"> Take memories</span> from Ayodhya visit</h2>
    <p class=" textMaroon mb-5">Purchase authentic souvenirs from Ayodhya</p>

    <div class="row visitRow">
        <?php
        $homestays = [
            [
                'image' => 'Assets/Images/image 29.png',
                'name' => 'Amar Villa',
                'location' => '5/8/90, Amaniganj Ram Path, Ayodhya',
                'price' => 3500,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image 29.png',
                'name' => 'Nandigram Eco Friendly Villa',
                'location' => 'Nandigram, Bharatkund, Ayodhya',
                'price' => 1400,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image 29.png',
                'name' => 'Shri Ram Kripa Kunj Homestay',
                'location' => 'Agnikund, Ayodhya',
                'price' => 2000,
                'rating' => 3.8,
            ],
            [
                'image' => 'Assets/Images/image 29.png',
                'name' => 'Shree Hanumant Place',
                'price' => 1500,
                
            ],
            [
              'image' => 'Assets/Images/image 29.png',
              'name' => 'Shree Hanumant Place',
              'price' => 1500,
              
          ],
        ];
        // <i class="fa-solid fa-star" ></i>
        foreach ($homestays as $homestay) {
            echo "
            <div class='col-md-2 visitCol'>
                <div class='card visitCard '>
                    <img src='{$homestay['image']}' class='card-img-top' alt='{$homestay['name']}'>
                    <div class='card-body'>
                        <h6 class='card-title visitCardTitle'>{$homestay['name']} <i class='fa-regular fa-heart' style='color: #000000;'></i> </h6>
                        <h6 class='card-text visitCardText'>
                            <span class=''>&#8377; {$homestay['price']}</span>
                        </h6>
                    </div>
                </div>
            </div>
            ";
        }
        ?>
    </div>
</div>

<!-- end hero section -->
<div class="container endHeroSection"> 
  <picture> 
    <!-- <source media="(max-width:992px)" srcset="Assets/Images/malaysia-banner-mob.png.png"> -->
    <img src="Assets/Images/image 32.png" alt="">
  </picture>
</div>

<!-- Email Section -->
 <div class = "container emailContainer" > 


 <div class=" pt-5 emailContentWrapper ">
        <div> 
        <h2 class="fw-bold">Explore the spiritual land of <br> Lord Ram, Ayodhya</h2>
        <h5 class="mt-4">Access over 30 popular Attractions, </br> Live Events & Activities in Ayodhya </br> City and so much more.</h5>
        
        <div class="input-group my-4 ">
            <input type="text" class="form-control" placeholder="Enter your Mobile Number" aria-label="Enter your Mobile Number">
            <button class=" redBtn" type="button">Send Link</button>
        </div>
        
       <div class="smallImgWrapper">
       <div class=" qr-code ">
            <img src="Assets/Images/Frame.png" alt="QR Code" class="img-fluid">
        </div>
        
        <div class="app-links mt-3">
            <a href="#"><img src="Assets/Images/App Store Black.png" alt="Download on the App Store" class="img-fluid me-3"></a>
            <a href="#"><img src="Assets/Images/Google Play Black.png" alt="Get it on Google Play" class="img-fluid"></a>
        </div>  
      </div>
    
      </div>
    </div>  


 <div class= " emailImgWrapper ">
<img src="Assets/Images/Group 49.png" >  
</div>
</div>


<!-- footer section -->
<footer class="footer">
    <div class="container">
        <div class="row">
            <div class="col-lg-4 col-md-6 logoCol">
                <div class="logo">
                    <img src="Assets/Images/image 298.png" alt="Logo 1">
                    <img src="Assets/Images/image 299.png" alt="Logo 2">
                    <img src="Assets/Images/image 300.png" alt="Logo 3">
                </div>
            </div>
            <div class="col-lg-3 col-md-6 footerCol">
                <h5>Services</h5>
                <ul>
                    <li><a href="#">Tourist places</a></li>
                    <li><a href="#">Aarti Pass</a></li>
                    <li><a href="#">Donation To Ram Mandir</a></li>
                    <li><a href="#">Events in Ayodhya</a></li>
                    <li><a href="#">Parkings in Ayodhya</a></li>
                    <li><a href="#">Emergency</a></li>
                </ul>
            </div>
            <div class="col-lg-2 col-md-6  footerCol">

                <ul>
                    <li><a href="#">FAQs</a></li>
                    <li><a href="#">Trip routes</a></li>
                    <li><a href="#">Hotels in Ayodhya</a></li>
                    <li><a href="#">E-Bus</a></li>
                    <li><a href="#">Wheelchair</a></li>
                </ul>
            </div>
            <div class="col-lg-3 col-md-6 footerCol">
                <h5>Important Links</h5>
                <ul>
                    <li><a href="#">Ayodhya Development Authority</a></li>
                    <li><a href="#">Disclaimer</a></li>
                    <li><a href="#">Terms and Conditions</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">Sitemap</a></li>
                </ul>
            </div>
        </div>
        <div class="row copyrightWrapper">
            <div class="col-md-8  text-end mt-3">
              <h6>  &copy; 2023 All rights reserved.   </h6>
            </div>
            <div class="col-md-4  text-end  social-icons">
                <a href="#"><i class="fab fa-youtube"></i></a>
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
            </div>
        </div>
    </div>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>

<script>
// Function to update the navbar items based on window width
function updateNavbar() {
    const navbarItems = document.getElementById('navbarItems');
    navbarItems.innerHTML = ''; // Clear existing items

    if (window.innerWidth <= 768) {
        navbarItems.innerHTML = `
            <li class="nav-item">
                <a class="nav-link active" href="stay-in-ayodhya">Home 0</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="tour-package">Home 1</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="souvenir">Home 2</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="about">Home 3</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="login">Home 4</a>
            </li>`;
    } else {
        navbarItems.innerHTML = `
            <li class="nav-item">
                <a class="nav-link active" href="stay-in-ayodhya">Stays in Ayodhya</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="tour-package">Tour Packages</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="souvenir">Souvenir</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="about">About Ayodhya</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="login">Login</a>
            </li>`;
    }
}

// Call the function on page load
updateNavbar();

// Update navbar items when window is resized
window.addEventListener('resize', updateNavbar);

// single slider in service section
document.addEventListener('DOMContentLoaded', function () {
    const container = document.getElementById('hServContainer');
    const scrollRightBtn = document.getElementById('scrollRightBtn');
    // const scrollLeftBtn = document.getElementById('scrollLeftBtn');

    // Scroll Right Button Click Event
    scrollRightBtn.addEventListener('click', function () {
        container.scrollBy({ left: 300, behavior: 'smooth' });
    });

    // Scroll Left Button Click Event
    // scrollLeftBtn.addEventListener('click', function () {
    //     container.scrollBy({ left: -300, behavior: 'smooth' });
    // });
});


// 
</script>

</body>
</html>
