# CGenerator

A color generator that will give the user a random color &amp; hex #

# Technology Used

* HTML
* CSS
* JavaScript
* jQuery

# Into The Code

The Below code is how we obtain the randomly generator hex number.
`````
  function getRandomColor() {

            var letters = "0123456789ABCDEF".split('');
            var color = "#";
            for (var i = 0; i < 6; i++) {
            color += letters[Math.round(Math.random() * 15)];
        }
            return color;
        }
`````
We first split the string by using the .split() method. We then create a variable for the "#" sign. Into the create loop that wil loop up to 6 characters(Since a hex # contains 6 characters.) We then use the Math.round/Math.random to generate a random number and to round it to a whole number. 

So now that we have our generate hex #, we need to change the background color to the changed color.

var randomColor = getRandomColor;
`````
                    $("button").click(function(getRandomColor) {

                    $('#hex').addClass('animated infinite pulse');

                      $("body").css({
                        background: randomColor
                      });

                      $("h1").text(randomColor);

                    });
`````

This part of the code is pretty straight forward, we simply create a .click() event. I used animate.css to give the text a little bit of life. We chang the background with .css() to randomColor which is our function to generate the random hex #. We also change our text to display the color in a hex # code.
