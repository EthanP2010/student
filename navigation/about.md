---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Cool places in my life:
<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - forever"},
        {"flag": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAARMAAAC3CAMAAAAGjUrGAAAAkFBMVEX////tKTnsFSr2q6/tJzfsHC/tIDLtJDXsAB/+8/TtITPsDyfzhYzsGS3sAB7sCCTxb3f96On0kpj84OL1naL60dPvR1PyeH/6y87wW2X5xcjtLDz4ubz97e7zgIf+9/fuPUvuN0XsABf72Nr2pKn4u7/wYGnvUFv0kZfxaHHuOkf3srbvS1f84+T1m6H0i5F8OTSOAAAGfUlEQVR4nO2ca3eqOBSGAyaA3OLdo3jX1nrs5f//uyFalSQEaVdnapj3+TBDJWctfCTJ3jsB4gAV8tsX8IDAiQ6c6MCJDpzowIkOnOjAiQ6c6HzbCc35yQt5IL7hhHpJxLnLmMt5lHjNM/NVJ74bOIferN+dt9vzbv9ptxg1TsqXnNAkHe36pMh08ff/7MSPskFXFtLh0f+579BodZSEkOOaN1CIU98JY4qRpyzy1UYNMVTPCU3HS8lId8J1AdRvhpRaTsLkSb5JZoFX0iyaRT98db9DHSfJ61xWMg7KbgiakZXWnWykhhP3WTay3Lul7VhMBskPX96vcN9JNJaVtFesvCEfkrf0hy/vV7jrxO0oStb6UOJ7OczJz64ScWh5D7rnhE1kJWRUomQy7nQ6h0F+tnXIj8bPdku548T/qyh5Lhkx6Hootemv7J6Tq51Q/iYreeelzTYfhTa91G4ld5xwJXgdlkRqJ9zXSyY031sfpFQ68ZRZmGTGgSIMzndUl5dFc3ZR6SSV02DyXh6YCCj/bNOA6luVE7cnK5lvzG09EcWInOjDEL1YRIUT6sl5HxlLX5eGxb+iKSHHdCeGnOLHoY13TYWTRLlNutIAS9edghSaENLhlD8vCSu0Cg82TstmJzRpy04W0m3C4mlhgvHGfUecZmz4UmjmHm3MgMxOPCXPWTLpJ+d/SHD7y5+45ymJ8klhbgra/cCxDrOT/EtLPElxB/WX5FCYdv2SI8ff59O3fZ3H6ISGSmzyfBk+xGoXZfldNIuoceXrdMbNx9yPxNzoQTE6YQul61zLAJlIfdN8nmlzlh85Wcm/zkQjFuTxzXYjmmdljR4Vo5NIKTf+ucyx4Y60c8Rnp/8PS3oHzaZyo2OotXlcjE5Spd7Yu04gXBp8d1FpHZK/FxvFpjzpITE5oY4ynExuv3SSba896tn0baP9VerbypwTPCImJ6Ga/hXXKfx0cP5w6Jkjec+dnhsdU8tKTCYn6hDblkL2S8LcqqoLXNKlsW0ZkMlJspOd9CUnlwF4XhWRpW/K6GwLJieuUk3aFr8Y5Xl2OIvzj/fmbuGvxMjcyv9j1QDrmJ0Yp2KBdxDrXtGoS1rm0TN5J/NJFHSW1nUeo5Op7ESK7KOnt3U+NYfubGnuPLw7TfLgn2XboWXVyLr3STEJdvzeeU8BDRavpn5BVx/nFVQ/6Fm24cDoZCY7kUtF1xS5YgMKvfYYZpeS742xDcc4F2tFtv/0sn4VkxNPWSYmpWlNMzE58UeKk7+mSMRQP/mRq/sdjDkgV5yYggx/XZoXr20qDigYawVcXhcns/LozN+XVqFZz+K9BUYnybvspFu+3SYZlJ7g26Nd9YEiRieivixR2kecoF9WhaZOdXr42Jjr9oGx0FZAJHolJ0SloSI9fHDMTly1WqD88B7L4T1RhRZHn8EqPR1v/hCyC8SRjTutzU602Xgk//DxRxzHC1EjiQUvp+cz6Orl9NeSkPlCHHw0aX1HX/SayavjE3nptHeeq1ksfbo8WLgdpcJJqG7vk3/ysJg6d0eXaSZZFx5mmXoWKqncf5JuZSdHOeeh6XVR47gprI1urgNRvLGv4zjVTu6NKI772WAnf/f05fzxxLJa0oXKvVu8JTvZKuHZZfCQiyvXGt27hfssBJVOtC0osRycnuJ/0UR6SIUG5LyNq2/pTvPqvaCeGsyOiqkdzXIjkyifnuJigijKDFs66uahr51h25191FHV/q286+QTCw1e5M6Tz0cD7ofuzNbOc2+/faDWqgt7H6PhuQwdvbYLG0xoOJ+IAhQNFn07i3P3nNCNUjM43gaJbPV5H4Re4SFjuso+g5JkZdOukxt3n1WhrhKlDG4Ped0OpDFWP28X959poq4S4x/tjMTqU+PZNxooaz3TwOLCYg3qPCNJU2XjxS27aST1ni92R8pzPLFt+2y+Qs3n0EOuBCrbEW+slbrP5lM3U1ZLZ+umWqn/XgsaZUf5QY3ZKLBtebwWX3n/CY38WI7gtvFaf5OD9XztPTmUcdppbYu3y5O99XkTX36fEvVcnrr7zuKlF48nXuo2Tsk337tFfY+xhHkNebmHAt7PpgMnOnCiAyc6cKIDJzpwogMnOnCiQ1ygQlpAhQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAIB/jX8ALhudv2T+wSIAAAAASUVORK5CYII=", "greeting": "Ni Hao", "description": "Favorite vacation"},
        {"flag": "b/be/Flag_of_England.svg", "greeting": "Alright mate", "description": "England - 2 years"},
        {"flag": "e/ef/Flag_of_Hawaii.svg", "greeting": "Aloha", "description": "Hawaii - 2 years"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

My childhood:

- I was born in 2010 and went to Design 39 when I was 4 years old 🏫
- I attended D39 all the way through 8th grade and made great friends along the way 👨‍💻
- I traveled a lot throughout my childhood. My favorite was going to Singapore ✈️
- I always enjoyed going skiing and snowboarding with my family. We usually went to Big Bear but Mammoth is my favorite resort 🏂
- I went from D39 to Del Norte and, obviously, still attend Del Norte 🎓

### Fun Facts 😊:

- I am 15 years old (1111)
- I have two older sisters
- I have lived in San Diego my whole life
- I have been to 6 continents
- I have broken 5 bones
- I wrestle at Del Norte
- I enjoy building LEGOs

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/missionary.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/john_tamara.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/tamara_fam.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/surf.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/john_lora.jpg" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/lora_fam.jpg" alt="Image 6">
  <img src="{{site.baseurl}}/images/about/lora_fam2.jpg" alt="Image 7">
  <img src="{{site.baseurl}}/images/about/pj_party.jpg" alt="Image 8">
  <img src="{{site.baseurl}}/images/about/trent_family.png" alt="Image 9">
  <img src="{{site.baseurl}}/images/about/claire.jpg" alt="Image 10">
  <img src="{{site.baseurl}}/images/about/grandkids.jpg" alt="Image 11">
  <img src="{{site.baseurl}}/images/about/farm.jpg" alt="Image 12">
</div>
