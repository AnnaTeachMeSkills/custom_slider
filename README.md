# custom_slider
*Universal carousel with the necessary user settings.*

## Example using 

To get started you need to download files __*custom_slider.js*__ and __*custom_slider.css*__.

Just add the links to the css file in your <head>:
  
  ```html
  <!-- Add the custom_slider.css to use default styling --> 
  <link rel="stylesheet" href="./css/custom_slider.css">  
  <!-- Add the style.css to use your styles -->   
  <link rel="stylesheet" href="./css/style.css">
  ```
  
  Then, before your closing `<body>` tag add:
  
  ```html
  <script src="./js/custom_slider.js"></script>
  <!-- Also you should add your script-->
  <script src="./js/script.js"></script>
  ```
  
  Each slide turns into a `<div>`, inside which there can be any picture:
  
  ```html
  <div class="custom_slider">
        <div><img src="./img/cat1.jpg" alt="cat1"></div>
        <div><img src="./img/cat2.jpg" alt="cat2"></div>
        <div><img src="./img/cat3.jpg" alt="cat3"></div>
        <div><img src="./img/cat4.jpg" alt="cat2"></div>
        <div><img src="./img/cat5.jpg" alt="cat3"></div>
   </div>
  ```
  In the file __*script.js*__, you need to call the method __customSlider()__, where you can pass the desired settings.
  
  ```js
  let main = document.querySelector('.main');
main.customSlider({
    maxSlides: 1,
    slideWidth: 300,
    slideHeight: 200,
    navs: true,
    loop: true,
    autoplay: true,
    timeout: 2000,
});

```

    
   Settings
   -----------
If called without parameters, the default values will be set.

  | Option      | Type           | Default | Description |
| ------------- |:------------------:| :-----:| --------:|
| maxSlides     | number    | 1 | Number of active slides|
| slideWidth     | number |   300 | Width of picture|
| slideHeight | number         |    auto |Height of picture|
| navs     | boolean   | true | Enable Next/Prev arrows|
| loop     | boolean    | true | Infinite looping|
| autoplay     | boolean    | true | Enables auto play of slides|
| timeout    | number    | 2000 | Auto play change interval|
| dots    | boolean    | true | Current slide indicator dots|
| margin    | number    | 10 | External indent of slide|
| onHover    | boolean    | true | Pauses autoplay on hover|
