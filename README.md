<!DOCTYPE html>
<html lang ="en">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="./assets/CSS/style.css">

    <link href='https://unpkg.com/boxicons@2.0.7/css/boxicons.min.css' rel='stylesheet'>

    <title>Karuga Mbugua</title>
    <style type="text/css">
        *{
            margin: 0;
        }
        #home__img {
            position: absolute;
            width: 100%;
            height: 100vh;
            right: 0;
            bottom: 0;
        }
        @media screen and (min-width: 768px){
            .home__img{
                size: 0.1;
            }
        }

    </style>
</head>
<body>

    <header class="l-header">
        <nav class="nav bd-grid">
            <div>
                <a href="#" class="nav__logo">Karuga Mbugua</a>
            </div>
            <div class="nav__menu" id="nav-menu">
                <ul class="nav__list">
                    <li class="nav__item"><a href="#home" class="nav__link active">Home</a></li>
                    <li class="nav__item"><a href="#about" class="nav__link">Know Me</a></li>
                    <li class="nav__item"><a href="#services" class="nav__link">Services</a></li>
                    <li class="nav__item"><a href="#contact" class="nav__link">Contact</a></li>
                    
                </ul>
            </div>
            <div class="nav__toggle" id="nav-toggle">
                <i class='bx bx-menu-alt-right'></i>
            </div>
        </nav>
    </header>



    <main class="1-main">

    <section class="home bd-grid" id="home">
        <div id="home__img">
            <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r134/three.min.js"></script>
            <script src="https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.globe.min.js"></script>
            <script>
            VANTA.GLOBE({
            el: "#home__img",
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            minHeight: 50,
            minWidth: 50,
            scale: 1.00,
            scaleMobile: 1,
            color: 0x3fa7ff,
            backgroundColor: 0x10001,
            size: 0.3
            })
            </script>
        </div>
        <div class="home__data">
            <h1 class="home__title">Hello, <br>My Name is  <span class="home__title-color">Karuga Mbugua</span><br>A Software Engineer</h1>
            <a href=tel:+254798713962 class="button">Contact</a>

        </div>

        <div class="home__social">
            <a href="#" class="home__social-icon"><i class='bx bxl-linkedin-square'></i></a>
            <a href="#" class="home__social-icon"><i class='bx bxl-instagram-alt' ></i></i></a>
            <a href="#" class="home__social-icon"><i class='bx bxl-facebook' ></i></i></i></a>
        </div>


    </section>

    <section class="about section" id="about">
        <h2 class="section-title">Know Me</h2>
        <div class="about__container bd-grid">
            <div class="about__img">
                <img src="assets/img/keny.webp">
            </div>
            <h2 class="about__subtitle">Who I am<div><span class="all__">
                I am an individual with a great passion for tech. I want to achieve a lot as a software engineer. 
                I want to be a part of the team 
                that designs and develops new applications. I also want to contribute to improving existing applications. 
                I want to work on projects that are challenging and interesting, 
                and that have a positive impact on people’s lives.
            </span></div><a href="sample.pdf" class="button">Download My CV</a>
        </h2>
        </div>

    </section>

    <section class="skills section" id="services">
        <h2 class="section-title">Areas Of Focus</h2>
        <div class="skills__container bd-grid">
            <div>
                <h2 class="skills__subtitle">Professional Skills</h2>
                <p class="skills__text">"Software never was perfect and won’t get perfect. 
                    But is that a license to create garbage? The missing ingredient is our 
                    reluctance to quantify quality "
                </p>

                <div class="skills__data">
                    <div class="skills__names">
                        <i class='bx bx-laptop skills__icon' ></i>
                      <span class="skills__name">Web Development</span>  
                    </div>
                    <div>
                        <span class="skills__percentage">100%</span>
                    </div>
                    <div class="skills__bar skills__video"></div>
                </div>

                <div class="skills__data">
                    <div class="skills__names">
                        <i class='bx bx-laptop skills__icon'></i>
                      <span class="skills__name">Mobile Development</span>  
                    </div>
                    <div>
                        <span class="skills__percentage">100%</span>
                    </div>
                    <div class="skills__bar skills__html"></div>
                </div>

                <div class="skills__data">
                    <div class="skills__names">
                        <i class='bx bx-laptop skills__icon'></i>
                      <span class="skills__name">Website Penetration Testing</span>  
                    </div>
                    <div>
                        <span class="skills__percentage">80%</span>
                    </div>
                    <div class="skills__bar skills__html"></div>
                </div>
            </div>

            <div>
                <img src="assets/img/Area.png" class="skill__img">
            </div>
        </div>
    </section>


    <section class="contact section" id="contact">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact__container bd-grid">
            <form onSubmit="sendEmail(); reset(); return false;" class="contact__form">
                <input type="text" placeholder="Name" id="name" class="contact__input">
                <input type="email" id="email" placeholder="Email" class="contact__input">
                <textarea name="" id="message" cols="0" rows="10" class="contact__input"></textarea>
                <button type="submit" class="contact__button button">Submit</button>
            </form>
        </div>
        <script src="https://smtpjs.com/v3/smtp.js"></script>
        <script>
            function sendEmail(){
            
            Email.send({
            Host : "smtp.elasticemail.com",
            Username : "karugakenn@gmail.com",
            Password : "D63E8F32B465B1D265ECCE60826CB9D5255E",
            From : 'karugakenn@gmail.com',
            To : 'wanderiflorence05@gmail.com',
            Subject : "Client Enquiry",
            Body : "Name:" + document.getElementById("name").value 
                    + "<br> Email:" + document.getElementById("email").value
                    + "<br> Message:" + document.getElementById("message").value
            }).then(
                message => alert("Message sent")
            );
            }
        </script>
    </section>

    </main>

    <footer class="footer">
        <p class="footer__title">KARUGA MBUGUA</p>
        <div class="footer__social">
            <a href="#" class="footer__icon"><i class='bx bxl-instagram-alt'></i></a>
            <a href="#" class="footer__icon"><i class='bx bxl-facebook-circle'></i></a>
            <a href="#" class="footer__icon"><i class='bx bxl-linkedin'></i></a>
        </div>
        <p>&#169; 2023 copyright all rights reserved</p>
    </footer>


    

    <script src="https://unpkg.com/scrollreveal">
    </script>

    <script src="assets/js/main.js"></script>
    
</body>

</html>

