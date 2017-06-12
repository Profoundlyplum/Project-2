# Project-2
The second challenge

The brief for tutorial:
1 - Make the header and navigation HTML
2 - Style the header with CSS
3 - Add responsive design + "like" button
4 - Build your own blog theme

For this project I used flexgrid and I'm struggling with:
- Aligning text in menu bar
- When screen is shrinked, the search bar is in the way of the open menu (flexy nav)
- The top two rows shrink in proportion, but the third row doesn't. I think this is to with the images.
- It would be nice for the rows to shrink to just one showing per row
- The text size and buttons aren't responsive, SO BIG!
- Hover effect over the 'read more' button (plus change the colour, but that's fine)


<!DOCTYPE html>
<link href="https://fonts.googleapis.com/css?family=Abril+Fatface|Annie+Use+Your+Telescope|Roboto+Condensed:700" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link href="/normalize.css" rel="stylesheet">
<head>
  
  <style>
  
  header {
    background: salmon;
    width:100%;
    text-align:center;
  }
   img {
      display:inline-block;
      margin: 0 auto;
      border: 7px solid white;
      border-radius: 20px;
    }
  a {
      color: #2A2A2A;
  }
  h1 {
    font-family: 'Annie Use Your Telescope', cursive;
    font-size: 70px;
   text-align: center;
   color: white;
  }
  h2 {
    font-family: 'Abril Fatface', cursive;
    color: #70e1a9;
  }
  p {
    color: grey; 
  }
     
input,
button {
  
  box-shadow: none;
  background: #fba69c;
  padding: 10px;
  font-size: 15px;
  border: 4px solid #afeecf;
  border-radius: 80px;
  margin: 0px 0px 40px 0px;

}

button {
  cursor: pointer;
}

.fa {
    padding: 10px;
    font-size: 25px;
    width: 25px;
    text-align: center;
    text-decoration: none;
    border-radius: 50%;
}

.fa:hover {
    opacity: 0.7;
}
.fa-facebook {
    background: #3B5998;
    color: white;
}
.fa-twitter {
    background: #55ACEE;
    color: white;
}
.fa-instagram {
    background: #fb3958;
    color: white;
}
.fa-flickr {
  background: #fb0084;
    color: white;
}

.flexy-nav {
  display: flex;
  flex-direction: column;
  font-family: 'Roboto Condensed', sans-serif;
}



.flexy-nav__items {
  display: none;
  flex: 1;
  flex-direction: column;
  list-style: none;
  margin: 0 0 40px 0;
  padding: 4px;
  text-align: center;

}

.flexy-nav__items--visible {
  display: flex;
}

.flexy-nav__item {
  font-size: 20px;
  border-bottom: solid 5px #e7e7e7;
}

.flexy-nav__item:last-child {
  border-bottom: 0;
}

.flexy-nav__link {
  padding: 8px;
  display: block;
}


.flexy-nav__toggle {
  margin: 0 0 4px 0;
  padding: 4px;
  color: #fff;
  font-size: 25px;
  background-color: salmon;
  border: ;
}

.flexy-nav__toggle:hover,
.flexy-nav__toggle:focus {
  outline: none;
  background-color: #fcbfb8;
}

.flexy-nav__form {
  height: 110px;
}

.flexy-nav__search {
  display: block;
  margin: 0;
  padding: 0 4px;
  width: 100%;
  height: 48px;
  color: #6d6d6d;
  background-color: #fff;
  border: solid 4px #e7e7e7;
}

.flexy-nav__search:focus {
  outline: none;
  border: solid 2px #6d6d6d;
}

.grid {
  border: solid px #e7e7e7;
}

.grid__row {
  display: flex;
  
}

.grid__item {
  flex: 1;
  background: ;
  padding: 20px;
  margin: 5px 10px 5px 10px;
  border: solid 1px #e7e7e7;
}


@media all and ( min-width: 480px ) {

  .grid__row--sm {
    flex-direction: row;
  }

}

@media all and ( min-width: 720px ) {

  .grid__row--md {
    flex-direction: row;
  }
  

}

@media all and ( min-width: 960px ) {

  .grid__row--lg {
    flex-direction: row;
  }

}

@media all and (min-width: 768px) {
  .flexy-nav {
    flex-direction: row;
  }

  .flexy-nav__items {
    display: flex;
    flex-direction: row;
    margin: 0;
    padding: 0;
    height: 48px;
  }

  .flexy-nav__item {
    flex: 1;
    margin-right: 4px;
    border-bottom: none;
  }

  .flexy-nav__link {
    padding: 0;
    line-height: 48px;
  }

  .flexy-nav__toggle {
    display: none;
  }

  .flexy-nav__form {
    flex: none;
  }

  .flexy-nav__search {
    width: 240px;
    transition: width 0.3s;
  }

  .flexy-nav__search:focus {
    width: 360px;
  }
}
  



  </style>
  
  <header>
  <nav class="flexy-nav">
  <button id="flexy-nav__toggle" class="flexy-nav__toggle">Menu</button>
  <ul id="flexy-nav__items" class="flexy-nav__items">
    <li class="flexy-nav__item"><a href="#" class="flexy-nav__link">POSTS</a></li>
    <li class="flexy-nav__item"><a href="#" class="flexy-nav__link">GALLERY</a></li>
    <li class="flexy-nav__item"><a href="#" class="flexy-nav__link">ABOUT ME</a></li>
    <li class="flexy-nav__item"><a href="#" class="flexy-nav__link">CONTACT</a></li>
  </ul>
  <form action="" class="flexy-nav__form">
    <input class="flexy-nav__search" type="text" placeholder="Type search terms and hit enter...">
  </form>
</nav>

    <img src="http://imgur.com/ms7CdKc.jpg">
   <h1> This little blog of mine</h1>
   </header>
  
  <div class="grid">
  <div class="grid__row">
    <div class="grid__item"><h2>Noodle's weekend visit</h2>
    <p>No day is complete without bumping into a dog, so to my delight I was asked to dog-sit for a lovely boy called Noodle. He's the sweetheart of the office and can melt hearts with one blink of his exceptionally long eyelashes. 'Don't let him on the bed' was Jamie, the owner's last words... Said with a wink and a sigh, knowing full well this was never going to be a reasonable request.</p></br>
    <button>Read more</button>
    <a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a></div>
    <div class="grid__item"><h2>Colour Obstacle Rush</h2>
    <p>A 5km 'marathon' interspersed with large adult only inflatables. I'm not into running, or jogging or generally anythiing relatively active but this was immensely fun. Throw in the idea of being splashed with rainbow coloured powder and dressing like you're in an Eighties music video, and you start to get an idea of what it was all about.</p></br>
    <button>Read more</button>
    <a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a>
    </div>
  </div>
  <div class="grid__row">
    <div class="grid__item"><h2>Spring has sprung!</h2>
    <p>And the garden is in bloom. It reminds me of a favourite poem of mine by Robert Louis Stevenson - Summer Sun.</br></br>
    
<i>Great is the sun, and wide he goes</br> 
Through empty heaven with repose;</br> 
And in the blue and glowing days</br> 
More thick than rain he showers his rays.</i></br></p>
    <button>Read more</button>
    <a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a>
</div>
    <div class="grid__item"><h2>Coding and chaos</h2>
    <p>It's happened! All those months of planning and dreaming. I've finally done it, finally started the exciting journey of becoming a programmer, a developer, a coder! It's been an intense journey so far and hopefully will get even more intense soon if I get accepted onto the web developement intensive course at <a href="https://generalassemb.ly/">General Assembly.</a></p>
    <button>Read more</button>
    <a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a></div>
    <div class="grid__item"><h2>Panto season</h2>
    <p>In July?! I know, it doesn't seem entirely right but then isn't that the great art of panto? Rehearsals are in full swing ready for our second performance of Goldilocks And The Four Bears. Being an entirely inclusive amdram group of course we have the usual motley crew and once again I'll be donning the cap of Mother Bear. <i> He's behind you!</i></p>
    <button>Read more</button>
    <a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a></div>
  </div>
  
  <div class="grid__row">
    <div class="grid__item"><img src="http://imgur.com/KrJfWpH.png"></br>
    <p>"You may feed me now"</p>
       <a href="#" class="fa fa-facebook"></a>
      <a href="#" class="fa fa-twitter"></a>
      <a href="#" class="fa fa-instagram"></a>
      <a href="#" class="fa fa-flickr"></a></div>
    <div class="grid__item"><img src="http://imgur.com/qi2GTnP.png"></br>
      <p>"In bloom"</p>
      <a href="#" class="fa fa-facebook"></a>
      <a href="#" class="fa fa-twitter"></a>
      <a href="#" class="fa fa-instagram"></a>
      <a href="#" class="fa fa-flickr"></a></div>
    <div class="grid__item"><img src="http://imgur.com/Hiz5lFJ.png"></br>
      <p>"The colour hop"</p>
      <a href="#" class="fa fa-facebook"></a>
      <a href="#" class="fa fa-twitter"></a>
      <a href="#" class="fa fa-instagram"></a>
      <a href="#" class="fa fa-flickr"></a></div>
  <div class="grid__item"><img src="http://imgur.com/uZza0iu.png"></br>
    <p>"And the epic tan lines"</p>
    <a href="#" class="fa fa-facebook"></a>
    <a href="#" class="fa fa-twitter"></a>
    <a href="#" class="fa fa-instagram"></a>
    <a href="#" class="fa fa-flickr"></a></div>
  </div>
</div>


<script>
(function() {
  var toggle = document.querySelector("#flexy-nav__toggle");
  var nav = document.querySelector("#flexy-nav__items");
  toggle.addEventListener("click", function(e) {
    e.preventDefault();
    nav.classList.contains("flexy-nav__items--visible") ? nav.classList.remove("flexy-nav__items--visible") : nav.classList.add("flexy-nav__items--visible");
  });
})();
</script>
  
