# Live Project

## Introduction
For the last two weeks of my time at the Tech Academy, I worked in a team environment developing a full scale Hobby Inventory Application in Python. It was a great opportunity to learn by adding requested features, fixing bugs, and cleaning up code. There were some big changes that could have been a large time sink, but we used what we had to deliver what was needed on time. I saw how a good developer works with what they have to make a quality product. I worked on several [front end stories](#front-end-stories) that I am very proud of. Because much of the site had already been built, there were also a good deal of front end stories and UX improvements that needed to be completed, all of varying degrees of difficulty. Everyone on the team had a chance to work on front end and back end stories.
  
Below are descriptions of the stories I worked on, along with code snippets, screenshots and navigation links. I also have some full code files in this repo for the larger functionalities that was implemented.

**View Repository**: [**Hobby Inventory**](https://github.com/nguyenmarvin8/Hobby-Inventory-Project)

# Front End Stories
* [Ship Wheel Animation](#Ship-Wheel-Animation)
* [Hidden Image Map Easter Egg](#Hidden-Image-Map-Easter-Egg)
* [Hovering Slide Effect on Social Media Icons](#Hovering-Slide-Effect-on-Social-Media-Icons)
* [Bouncing Buttons](#Bouncing-Buttons)

## Ship Wheel Animation
I was tasked to create a hover effect for when the mouse over the wheels, it would create a spinning effect.

![Ship Wheel Animation](https://imgur.com/1tQ0M0G.jpg)

### HTML
      <div id="buttonList" class="collapse col-12 mx-auto">
        <div class="wheelButtons col mx-auto">
          <a href="{% url 'footy' %}">
              <figure class="col">
                <img src="{% static 'images/shipswheel.png' %}" alt="Footy App" class="rotateWheel">
                <figcaption>Footy App</figcaption>
              </figure>
          </a>
      </div>

### CSS
        .wheelButtons .rotateWheel {
            -webkit-transition: transform -webkit-transform .8s ease-in-out;
            transition: transform .8s ease-in-out;
        }

        .wheelButtons .rotateWheel:hover {
            -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
        }

## Hidden Image Map Easter Egg
I create a hidden Easter Egg of an image map on the soccer ball that links to a Rick Rolled Youtube video.

![Hidden Image Map Easter Egg](https://imgur.com/1KtjLRT.jpg)

### HTML
      <section>
          <div id="footyPic">
              <img src="{% static 'images/footy_home.jpg' %}" usemap="#image-map"> <!-- added image mapping -->
              <span class="footy_center">
                  <strong>Welcome to the Footy Demo App</strong>
                  <br/>
                  A collection manager app for a major soccer fan! There's a database to manage a
                  collection of jerseys, an API for recent soccer scores, and recent news stories scraped from
                  the MLS website. Take a look.
              </span>
              <br />
              <a class="footy_caption" href="https://unsplash.com/@davidclarke?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge" target="_blank" rel="noopener noreferrer" title="Download free do whatever you want high-resolution photos from david clarke"><span>photo by david clarke</span></a>
              <!--Soccer ball Easter egg image mapping-->
              <map name="image-map">
                  <area target="_blank" alt="Click if you dare! (;" title="Click if you dare! (;" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" coords="740,265,120" shape="circle">
              </map>
          </div>
      </section>

## Hovering Slide Effect on Social Media Icons
I created a hovering effect on the social media icons so that when its hovered over, it will expand and slide out.

![Hovering Slide Effect on Social Media Icons](https://imgur.com/UISpxdy.jpg)

### HTML
      <div class="icons">
          <ul>
              <a href="#"><li class="facebook"><i class="fab fa-facebook-f"></i></li></a>
              <a href="#"><li class="twitter"><i class="fab fa-twitter"></i></li></a>
              <a href="#"><li class="snapchat"><i class="fab fa-snapchat"></i></li></a>
              <a href="#"><li class="instagram"><i class="fab fa-instagram"></i></li></a>
              <a href="#"><li class="youtube"><i class="fab fa-youtube"></i></li></a>
          </ul>
      </div>

### CSS
      .icons {
          top: 80%;
          left: 0;
          transform: translateY(-50%);
          position: fixed;
          z-index: 100;
      }
     .icons ul {
          padding: initial;
      }
      .icons ul li {
          height: 40px;
          width: 30px;
          list-style-type: none;
          padding-left: 20px;
          padding-top: 10px;
          padding-right: 27px;
          margin-top: 5px;
          border-top-right-radius: 20px;
          border-bottom-right-radius: 20px;
          color: white;
          text-align: center;
      }
      .facebook {
          background-color: #2c80d3;
      }
      .twitter {
          background-color: #53c5ff;
      }
      .snapchat {
          background-color: #fffc00;
      }
      .instagram {
          background-color: #833AB4;
      }
      .youtube {
          background-color: #fa0910;
      }
      .icons ul li:hover {
          padding-left: 30px;
          width: 80px;
          transition: .5s;
      }

## Bouncing Buttons
I also created an ongoing bouncing animation effect on the buttons to add some life to the page.

![Bouncing Buttons](https://imgur.com/hw1oLie.jpg)

### HTML
      <section>
          <div class="flex-container wrapper">
              <h5 class="button1 bouncy" style="animation-delay:0.07s">Footy Demo Application</h5>
              <a class='button1 bouncy' href="{% url 'footy' %}">Footy Home Page</a>
              <a class='button1 bouncy' href="{% url 'listJerseys' %}" style="animation-delay:0.14s">Jersey Collection</a>
              <a class='button1 bouncy' href="{% url 'footyApi' %}" style="animation-delay:0.21s">Footy API Service</a>
              <a class='button1 bouncy' href="{% url 'MLSNews' %}" style="animation-delay:0.30s">News from the MLS</a>
          </div>
      </section>
        
 ### CSS
      .bouncy {
          animation:bouncy 5s infinite linear;
          position:relative;
      }
      @keyframes bouncy {
          0%{top:0em}
          40%{top:0em}
          43%{top:-0.9em}
          46%{top:0em}
          48%{top:-0.4em}
          50%{top:0em}
          100%{top:0em;}
      }

*Jump to: [Front End Stories](#front-end-stories), [Other Skills](#other-skills-learned), [Page Top](#live-project)*


## Other Skills Learned
* Working with a group of developers to identify front and back end bugs to the improve usability of an application.
* Improving project flow by communicating about who needs to check out which files for their current story.
* Learning new efficiencies from other developers by observing their workflow and asking questions.
* Practice with team programming/pair programming when one developer runs into a bug they cannot solve.
    
*Jump to: [Front End Stories](#front-end-stories), [Other Skills](#other-skills-learned), [Page Top](#live-project)*
