# TASK-1-Landing-page
creating an landing page using HTML and CSS

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="styles.css">
    <title>Document</title>
    
<!-- Include this CDN for using icons     -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">

</head>



<body>
    <!-- header section starts  -->
    

    <header>
<!--  This will contain the navigation menu -->
     
    </header>

    <!-- header section ends -->
    

    <!-- hero section starts  -->
<!-- This will contain the brief description about our product (here, restaurant)  -->

<!--  hero section ends -->


</body>

</html>

2. Adding the Basic CSS
The below code includes the necessary CSS. We have imported a Google font and created a dark background.

 @import url("https://fonts.googleapis.com/css2?family=Jacques+Francois+Shadow&display=swap");
    * {
        font-family: "Nunito", sans-serif;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        outline: none;
        border: none;
        text-decoration: none;
        text-transform: capitalize;
        transition: all 0.2s linear;
    }
    
    html {
        font-size: 62.5%;
        overflow: hidden;
    }
    
    body {
        background: #212531;
        margin: 0;
    }
    
    header {
        margin: 0px;
    }

   <!-- header section starts  -->

    <header>

        <section class="nav">
            <!-- We can also insert any logo here     -->

            <!-- We can also insert any logo here     -->
            <div class="logo">
                <a href="#"><i class="fas fa-utensils"></i>food</a>
            </div>

            <!--  checkbox to control the icon's state    -->
            <input id="menu-toggle" type="checkbox" />
            <label class='menu-button-container' for="menu-toggle">
                <div class='menu-button'></div>
              </label>
            <!--  main menu    -->
            <ul class="menu">
                 <li><a href="#home">Home</a></li>
                <li><a href="#speciality">About</a></li>
                <li> <a href="#popular">Popular</a></li>
                <li> <a href="#review">Contact</a></li>
                <li> <a href="#order" class="order">Menu</a></li>
            </ul>
        </section>




    </header>

    <!-- header section ends -->

    a {
        text-decoration: none;
        color: #000;
    }
    
    ul {
        list-style: none;
    }
    
/* styling the logo  */

    .logo {
        font-size: 2.5rem;
        font-weight: bolder;
        color: #666;
        display: inline-block;
    }
    
    .logo i {
        padding-right: 2rem;
        color: black;
    }
    
    .order {
        text-shadow: -1px -1px 0 yellow, 1px -1px 0 yellow, -1px 1px 0 yellow, 1px 1px yellow;
    }

/* Stying the navbar container */
    
    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        background: white;
        color: black;
        height: 65px;
        padding: 1em;
        font-size: 25px;
    }
    
    .menu li:hover {
        cursor: pointer;
        transform: scale(1.2);
    }
    
    .menu {
        display: flex;
        flex-direction: row;
        list-style-type: none;
        margin: 0;
    }
    
    .menu>li {
        margin: 0 1rem;
        overflow: hidden;
    }
    /*Container for menu button  */
    
    .menu-button-container {
        display: none;
        height: 100%;
        width: 30px;
        cursor: pointer;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    #menu-toggle {
        display: none;
    }
    /*  Creating the hamburger menu button  */
    
    .menu-button,
    .menu-button::before,
    .menu-button::after {
        display: block;
        background-color: black;
        position: absolute;
        height: 6px;
        width: 32px;
        border-radius: 3px;
        color: white;
    }
    
    .menu-button::before {
        content: "";
        margin-top: -8px;
    }
    
    .menu-button::after {
        content: "";
        margin-top: 8px;
    }

 /*  Adding Functionality to the Hamburger Menu with CSS  */
    
    #menu-toggle:checked+.menu-button-container .menu-button::before {
        margin-top: 0px;
        transform: rotate(45deg);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button {
        background: rgba(255, 255, 255, 0);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button::after {
        margin-top: 0px;
        /*  transforms the hamburger icon into a cross  */
        transform: rotate(-45deg);
    }
    
 /* media queries  */
    
    @media (max-width: 991px) {
        html {
            font-size: 55%;
        }
        header {
            padding: 2rem;
        }
        section {
            padding: 2rem;
        }
    }
    
    @media (max-width: 768px) {
        .menu-button-container {
            display: flex;
        }
        .menu {
            position: absolute;
            top: 0;
            margin-top: 50px;
            left: 0;
            flex-direction: column;
            width: 100%;
            justify-content: center;
            align-items: center;
            padding: 2rem
        }
        .menu li:hover {
            transform: scale(1);
        }
        #menu-toggle~.menu li {
            height: 0;
            margin: 0;
            padding: 0;
            border: 0;
        }
        #menu-toggle:checked~.menu li {
            border: 1px solid #9f9a9a;
            height: 2.5em;
            padding: 0.5em;
        }
        .menu>li {
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0.5em 0;
            width: 100%;
            color: black;
            background-color: #e8e8e8;
        }
        .menu>li:not(:last-child) {
            border-bottom: 1px solid #444;
        }
    }
