# slidedoom
A responsive slide library for webpages
Dont forget to add Slidedoom.css. It is needed inorder to display the slides correctly. 
Visit https://irfanit93.github.io for the implementation
Visit https://www.npmjs.com/package/slidedoom for the package details

Installation:

npm i slidedoom --save

Use Slidedoom.min.js for regular websites.

Use Slidedoom.ang.min.js for Angular2+ .

Features:
1. Its Small. 4kb Javascript and 2Kb CSS.
2. No External Dependencies.
2. Integrate Slides to Your app in seconds.
3. Easy Integration.
4. Cross Browser Support
5. Responsive
6. Mobile browsers Support and Tablets Too
7. Set Background images for slide using any colors, local image url or remote image url. Its that easy. (In backgrounds array just set any array element value as object literal {name:"<REMOTE_URL or LOCAL_URL>"}. For background colors for slide, in background array just set string as "#789564 or rgb(7,7,7)")

Example:

var backgrounds = [
            { name: "https://storage.googleapis.com/cdn.magloft.com/blog/2017/02/responsive-design-1280x640.jpg" },//Slide0 background
            { name: "https://www.w3schools.com/css/img_temp_band.jpg" },//Slide1 background
            "#121212",//Slide2 background
            "#888eee",//Slide3 background
            "#a77756",//Slide4 background
            "#444777"//Slide5 background
        ]
For more info, refer Documentation or source code at Github https://github.com/irfanit93/slidedoom

Tip:

If you want some cool glassy effect for your slide add two css classes 'glassy' and 'afterglassy': Do it like below:

            <div class="slides slide0">
                <div class="glassy" style="opacity:0.7"></div><!--set opacity from 0 to 1 to increase or decrease the glassy effect.-->
                <div class="afterglassy"><!-- this class will make the glassy effect possible -->
                    <h3>Slide0</h3>
                    <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use
                        carousel library.Slidedoom is a lightweight and ease of use carousel library.
                    </div>
                </div>
            </div>

Note: Apply a background image to the slide to see the effect visually.

=============================================================================================================

For Angular 2+,

Refer the following sample code:

app.component.ts:


import { Component, OnInit } from '@angular/core';


import slidedoom from "slidedoom/Slidedoom.ang.min.js";

 //Note that its Slidedoom.ang.min.js file for angular  ( slidedoom.js file is only for regular website or webpage)

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})

export class AppComponent implements OnInit {
  
title = 'app';
  
backgrounds = [
    "rgba(0,0,0,0.8)",//Slide0 background
   
 "#687792",//Slide1 background
    
"#121212",//Slide2 background
    
"#888eee",//Slide3 background
   
 "#a77756",//Slide4 background
    
"#444777"//Slide5 background
  ];
  

  
//array of slidecontainer Height in proportion to Browser Client Height
 
 // first slidecontainer height is 1/1 =100%  of Browser Client Height
 
 aspectRatioHeight = [1];
 
 //array of slidecontainer width in proportion to Browser Client Width
  // first slidecontainer width is 1/1= 100%  of Browser Client Width
  aspectRatioWidth = [1];

  
//Till now we have specified what each slidecontainer width and height

  //Now we are going to  merge the slidecontainers and put it row wise
  // First row contains only 1 slidecontainer
 
 slidesgroup = [1];

 
 //used only for css
  //specify the maximum number of slides you are going to use in a single slidecontainer.
  
maxSlides = 6;
  
ngOnInit() {
    
//call slidedoom method as imported at the top  with the following arguments
slidedoom(this.backgrounds, this.aspectRatioHeight, this.aspectRatioWidth, this.slidesgroup, this.maxSlides);



}

}


app.component.css
=================
@import url("slidedoom/Slidedoom.min.css");

app.component.html
=================
(Same as in previous slidedoom version)

<div class="slidecontainer">
  
<div class="slidezimple">

    <div class="slides slide0">
   
   <h3>Slide0</h3>
 
     <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
     
 </div>
  
  </div>

    <div class="slides slide1">
      <h3>Slide1</h3>
      <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
      </div>
    </div>
    <div class="slides slide2">
      <h3>Slide2</h3>
      <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
      </div>
    </div>
    <div class="slides slide3">
      <h3>Slide3</h3>
      <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
      </div>
    </div>
    <div class="slides slide4">
      <h3>Slide4</h3>
      <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
      </div>
    </div>
   
 <div class="slides slide5">
     
 <h3>Slide5</h3>
      <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.
      
</div>
   
 </div>
  
</div>

</div>

<router-outlet></router-outlet>

Have Fun with it ! :)
