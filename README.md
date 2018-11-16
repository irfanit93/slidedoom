# slidedoom
A responsive slide library for webpages
Dont forget to add Slidedoom.css. It is needed inorder to display the slides correctly. 
Visit https://irfanit93.github.io for the implementation

Example page:



<!DOCTYPE html>

<head>

    <meta name="viewport" content="width=device-width, initial-scale=1">

    <script>
        // Assumed you have created Totally 18 Slides in the single webpage, 
        //mention in the backgrounds array what each and every slide background should be.
        // The Order of the background color is respected.
        // If you want to specify background image instead of background color, specify it as
        // object with property name set to the image name along with the extenstion.
        var backgrounds = [
            "rgba(0,0,0,0.8)",//Slide0 background
            "#687792",//Slide1 background
            "#121212",//Slide2 background
            "#888eee",//Slide3 background
            "#a77756",//Slide4 background
            "#444777",//Slide5 background
            "#2558ee",//Slide6 background
            "#874562",//Slide7 background
            "#456285",//Slide8 background
            "#aa5623",//Slide9 background
            { name: "tree1.jpg" },//Slide10 background
            { name: "tree0.jpg" },//Slide11 background
            "#445566",//Slide12 background
            "#a5a5a5",//Slide13 background
            "#786856",//Slide14 background
            "#377666",//Slide15 background
            "#222222",//Slide16 background
            "#333333"//Slide17 background
        ],
            // Concept: 
            // 1. A single container mentioned by div with css class 'slidecontainer'. There may be many slidecontainers in a single page, each having different number of slides.
            // 2. Then inside of that div with 'slidecontainer' css class, place another div with css class as 'slidezimple'
            // 3.Inside the div with css class 'slidezimple', we are going to create few slides.
            // 4. Create a div with css classes 'slides slide0' inside the 'slidezimple' div.This completes our first slide.
            // 5. Create a div with css classes 'slides slide1' inside the same 'slidezimple' div.This completes our second slide.
            // 6. You can add as many slides you can by repeating the step4 or step5 again.
            // The basic structure looks like this:
            /*
            <div class='slidecontainer'> ---- Step1
        
                <div class="slidezimple"> ---- Step2
        
                        <div class="slides slide0"> ----Step4
        
                        <div>
        
                        <div class="slides slide1"> ----Step5
        
                        <div>
        
                </div>
        
            </div>
                    //Another slidecontainer with few slides in it
        
            <div class='slidecontainer'> ---- Step1
        
                <div class="slidezimple"> ---- Step2
        
                        <div class="slides slide0"> ----Step4
        
                        <div>
        
                        <div class="slides slide1"> ----Step5
        
                        <div>
        
                </div>
        
            </div>
            */

            //array of slidecontainer Height in proportion to Browser Client Height
            // first slidecontainer height is 1/2 =50%  of Browser Client Height
            // second slidecontainer height is 1/2 =50%  of Browser Client Height
            // third slidecontainer height is 1/2 =50%  of Browser Client Height
            // fourth slidecontainer height is 1/2 =50%  of Browser Client Height
            // fifth slidecontainer height is 1/2 =50%  of Browser Client Height
            aspectRatioHeight = [2, 2, 2, 2, 2],
            //array of slidecontainer width in proportion to Browser Client Width
            // first slidecontainer width is 1/1= 100%  of Browser Client Width
            // second slidecontainer width is 1/2= 50%  of Browser Client Width
            // third slidecontainer width is 1/2= 50%  of Browser Client Width
            // fourth slidecontainer width is 1/1= 100%  of Browser Client Width
            // fifth slidecontainer width is 1/1= 100%  of Browser Client Width
            aspectRatioWidth = [1, 2, 2, 1, 1],

            //Till now we have specified what each slidecontainer width and height

            //Now we are going to  merge the slidecontainers and put it row wise
            // First row contains only 1 slidecontainer
            // Second row contains two slidecontainer
            // Third row contains 1 slidecontainer
            //Fourth row contains 1 slidecontainer
            slidesgroup = [1, 2, 1, 1],

            //used only for css
            //specify the maximum number of slides you are going to use in a single slidecontainer.
            maxSlides = 7;

    </script>
    <style>
        .aboutslidedoom {
            text-align: center;
            padding: 3%;
            font-size: 90%;
        }
    </style>
    <link href="Slidedoom.min.css" rel="stylesheet" />
</head>

<body>
    <div style="background:#231562;padding:1%;font-size:20px;color:white;text-align:center;font-style:italic;position:fixed;width:100%;z-index:1001;top:0px;"
        class="headadjust">
        <span style="float:left;top:40%;position:absolute;line-height:10px;left:1px;">
            Menu
        </span>
        <h1>Slidedoom</h1>
    </div>
    <div class="headadjust" style="background:#377ee0;padding:10%;font-size:30px;color:white;text-align:center;clear:right;clear:left;">
        Slidedoom is a lightweight and ease of use carousel library.
    </div>
    <div class="slidecontainer">
        <div class="leftarrow">
            <span style="display:inline-block;">&lt;&lt;</span>
        </div>
        <div class="slidezimple">
            <div class="slides slide0">
                <h3>Slide0</h3>
                <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel
                    library.Slidedoom is a lightweight and ease of use carousel library.
                </div>
            </div>
            <div class="slides slide1">
                <div class="glassy">

                </div>
                <div class="afterglassy">
                    <h3>Slide1</h3>
                    <div class="aboutslidedoom">
                        <img src="tree1.jpg" style="height:25%;width:25%;" />
                    </div>
                    <div class="aboutslidedoom">
                        Image Sliders, Text Sliders, Gallery, can be made using slidedoom
                    </div>
                </div>
            </div>
            <div class="slides slide2">
                <div class="glassy">

                </div>
                <div class="afterglassy">
                    <h3>Slide2</h3>
                    <div class="aboutslidedoom">
                        Image Sliders, Text Sliders, Gallery, can be made using slidedoom
                    </div>
                    <div class="aboutslidedoom">
                        <img src="tree0.jpg" style="height:25%;width:25%;" />
                    </div>
                </div>
            </div>
            <div class="slides slide3">
                <div class="glassy">

                </div>
                <div class="afterglassy">
                    <h3>Slide3</h3>
                    <div class="aboutslidedoom">
                        <img src="tree2.jpg" style="height:25%;width:25%;" />
                    </div>
                    <div class="aboutslidedoom">
                        Image Sliders, Text Sliders, Gallery, can be made using slidedoom
                    </div>
                </div>
            </div>
            <div class="slides slide4">
                <h3>Slide4</h3>
            </div>
        </div>
        <div class="rightarrow">
            <span style="display:inline-block;">&gt;&gt;</span>
        </div>
    </div>
    <div class="slidecontainer">
        <div class="leftarrow">
            <span style="display:inline-block;">&lt;&lt;</span>
        </div>
        <div class="slidezimple">
            <div class="slides slide0">
                <h3>Slide5</h3>
            </div>
            <div class="slides slide1">
                <h3>Slide6</h3>
                <div class="aboutslidedoom">
                    Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
                    is a lightweight and ease of use carousel library.
                </div>
            </div>
            <div class="slides slide2">
                <h3>Slide7</h3>
            </div>
        </div>
        <div class="rightarrow">
            <span style="display:inline-block;">&gt;&gt;</span>
        </div>
    </div>
    <div class="slidecontainer">
        <div class="leftarrow">
            <span style="display:inline-block;">&lt;&lt;</span>
        </div>
        <div class="slidezimple">
            <div class="slides slide0">
                <h3>Slide8</h3>
            </div>
            <div class="slides slide1">
                <h3>Slide9</h3>
                <div class="aboutslidedoom">
                    Cross Browsers Support tOO Cross Browsers Support tOO Cross Browsers Support tOO Cross Browsers Support tOO Cross Browsers
                    Support tOO
                </div>
            </div>
            <div class="slides slide2">
                <div class="glassy">

                </div>
                <div class="afterglassy">
                    <h3>Slide10</h3>
                    <div class="aboutslidedoom">Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use
                        carousel library.Slidedoom is a lightweight and ease of use carousel library.
                    </div>
                    <div class="aboutslidedoom">
                        <img src="tree2.jpg" style="height:50%;width:50%;" />
                    </div>
                </div>
            </div>
            <div class="slides slide3">
                <div class="glassy">

                </div>
                <div class="afterglassy">
                    <h3>Slide11</h3>
                </div>
            </div>
        </div>
        <div class="rightarrow">
            <span style="display:inline-block;">&gt;&gt;</span>
        </div>
    </div>
    <div class="slidecontainer">
        <div class="leftarrow">
            <span style="display:inline-block;">&lt;&lt;</span>
        </div>
        <div class="slidezimple">
            <div class="slides slide0">
                <h3>Slide12</h3>
                <div class="aboutslidedoom">
                    Mobile,Desktop,Tablet and Whatever Its fully responsive.
                </div>
            </div>
            <div class="slides slide1">
                <h3>Slide13</h3>
            </div>
            <div class="slides slide2">
                <h3>Slide14</h3>
            </div>
        </div>
        <div class="rightarrow">
            <span style="display:inline-block;">&gt;&gt;</span>
        </div>
    </div>
    <div class="slidecontainer">
        <div class="leftarrow">
            <span style="display:inline-block;">&lt;&lt;</span>
        </div>
        <div class="slidezimple">
            <div class="slides slide0">
                <div class="aboutslidedoom" style="color:black !important;">
                    Slide15 Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
                    is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel
                    library.Slidedoom is a lightweight and ease of use carousel library.
                </div>
            </div>
            <div class="slides slide1">
                <div class="aboutslidedoom">
                    Slide16 Integrate easy with autosliding.
                </div>
            </div>
            <div class="slides slide2">
                <div class="aboutslidedoom">
                    Slide17 Multiple Slide feature is available and Its responsive.
                </div>
            </div>
        </div>
        <div class="rightarrow">
            <span style="display:inline-block;">&gt;&gt;</span>
        </div>
    </div>
    <div class="aboutslidedoom" style="background:#377ee0;padding:10%;font-size:30px;color:white;text-align:center;clear:left;">
        Slidedoom is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.Slidedoom
        is a lightweight and ease of use carousel library.Slidedoom is a lightweight and ease of use carousel library.
    </div>
    <script src="Slidedoom.min.js"></script>
</body>

</html>
