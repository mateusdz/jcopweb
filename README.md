# About this website

This website was created using [Jekyll](https://jekyllrb.com/) and hosted using GitHub Pages.

The source can be found at [https://github.com/eu-jcop/eu-jcop.github.io](https://github.com/eu-jcop/eu-jcop.github.io).

Additions/corrections/suggestions are welcome.

## How to run the website on your local computer

- Make sure to install [Jekyll](https://jekyllrb.com/) on your computer using the [instructions](https://jekyllrb.com/docs/) provided on their website.
- In the Terminal, run this command to check if Jekyll is installed. It is recommended to install v4.1.1 and above.
```
jekyll -v
```
- Clone the JCOP Website repo [https://github.com/eu-jcop/eu-jcop.github.io](https://github.com/eu-jcop/eu-jcop.github.io) to your computer.

```bash
cd mateusdz.github.io

jekyll serve
```
- Running ```jekyll serve``` creates a folder called ```_site``` under the folder ```mateusdz.github.io```. Jekyll uses this folder content to serve the website locally. The folder ```_site``` should not be checked into the repository.

- Browse the website by going to this URL. Make sure to stop the server and run again each time a change is made to the ```_config.yml``` file.

```
http://127.0.0.1:4000/index.html
```
## Website Structure

```
.
+-- _includes
|   -- footer.html                  # Contains code to include Back to Top button and JavaScript used in this website.
|   -- header.html                  # Contains code to include Stylesheets used in this website.
|   -- navbar.html                  # Contains code to display top level and mobile navigation including website search.
+-- _layouts
|   -- default.html                 # Contains HTML and Jekyll code to implement a re-usable page layout. (Used for index.html)
|   -- page.html                    # Imports the layout used for default.html and adds extra layout to present inner HTML pages.
+-- _sass
|   +-- main.scss                   # Contains re-usable SASS properties for the website.
+-- assets
|   +-- css
|       -- main.scss                # Imports the re-usable SASS properties for the website.
|       -- style.css                # Contains CSS for each section of the website.
|   +-- img   
|   +-- js
|       -- main.js                  # Contains JavaScript used for this website.
|   +-- vendor
|       +-- animate.css             # Supports Basic animations like Fade up, Fade Down etc.
|       +-- aos                     # To animate HTML elements when a user slides down a page.
|       +-- bootstrap
|       +-- boxicons
|       +-- icofont
|       +-- jquery-sticky
|       +-- jquery.easing
|       +-- jquery
+-- content
|   +-- homepage
|       +-- carousel
|           -- slide1.html           # HTML imported for First Slide of the Carousel in index.html
|           -- slide2.html           # HTML imported for Second Slide of the Carousel in index.html
|           -- slide3.html           # HTML imported for Third Slide of the Carousel in index.html
|       -- paragraph1.md             # Markdown imported as paragraph1 with figure in index.html
|       -- paragraph2.md             # Markdown imported as paragraph2 with figure in index.html
|       -- paragraph3.md             # Markdown imported as paragraph3 with figure in index.html
|       -- paragraph4.md             # Markdown imported as paragraph4 with figure in index.html
+-- _site                            # Folder generated locally when jekyll serve is run. This should not be checked in to the repo.
-- 404.html                          # Invalid URLs point to this page.
-- CNAME                             # Contains Domain name of the JCOP website.
-- _config.yml                       # Jekyll configuration for this website. Requires Server Restart each time it's changed.
-- faq.html                          # Frequently asked Questions (hidden, but the content exitst also in the index.html file in the bottom.)
-- favicon.ico
-- index.html                        # HomePage of this website.
-- partners.html                     # JCOP partners.
-- project.html                      # Information about JCOP project.
-- timeline.html                     # JCOP timeline.
-- README.md                         # Documentation on how to use/contribute to this website.

```

## How to add/remove slides in the carousel on the homepage?
```index.html``` is the homepage and it uses [Bootstrap Carousel](https://getbootstrap.com/docs/4.0/components/carousel). Please refer to it's documentation to learn more about it.

To add a new slide to the carousel, create a HTML content file in ```content/homepage/carousel``` folder similar to other ```slide-*.html``` files

Open ```index.html``` and add the HTML code inside the ```carousel-inner``` section to reflect the following change.

```
        <!-- Slide 4 -->
        <div class="carousel-item">
          <div class="carousel-container">
            <div class="carousel-content container">
            <!-- Include slide5.html using Jekyll's include_relative tag. 
            See here for more info: https://jekyllrb.com/docs/includes 
            -->
            </div>
          </div>
        </div>
```

To remove unwanted slides, delete the HTML code and content file for the unused slide.

## How to change the timeline in "JCOP timeline" page?
```timeline.html``` is the page where a timeline is present.

To add or remove cards in the timeline, Open ```timeline.html``` and find the date you would like to insert a new card and copy paste this HTML. Please make sure to change the Date and Link as necessary.

```
<div class="timecard" data-aos="fade-up">
    <div class="content">
        <h6>June 06, 2020</h6>.  <!-- This section has the date of the entry -->
            <p> <!-- This section has the content of the entry -->
               <a rel="noopener noreferrer" target="_blank" href="https://codesync.global/media/making-iot-safer-with-beam-otp-cbf20/">
              Making IoT safer with BEAM OTP
              </a>
            </p>
     </div>
</div>
```

## Contributing
Pull requests are welcome. To request changes, please open an issue first to discuss what you would like to change.

