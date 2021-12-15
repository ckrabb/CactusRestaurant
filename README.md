# CactusRestaurant

<div class="rotating-content" style=" max-height: auto;">
                        <img class="mySlides" src="homePage1.jpeg" style="width:100%">
                        <img class="mySlides" src="homePage2.jpeg" style="width:100%">
                        <img class="mySlides" src="homePage3.jpeg" style="width:100%">
                        <img class="mySlides" src="homePage4.jpeg" style="width:100%">
                        <img class="mySlides" src="homePage5.jpeg" style="width:100%">

                        <button class="button-display-left" style="height:40px;width:40px;" onclick="plusDivs(-1)">&#10094;</button>
                        <button class="button-display-right" style="height:40px;width:40px;" onclick="plusDivs(1)">&#10095;</button>
                    </div>

        <!-- JS rotating slideshow function -->
        <script>
        var myIndex = 0;
        carousel();

        function carousel() {
          var i;
          var x = document.getElementsByClassName("mySlides");
          for (i = 0; i < x.length; i++) {
            x[i].style.display = "none";
          }
          myIndex++;
          if (myIndex > x.length) {myIndex = 1}
          x[myIndex-1].style.display = "block";
          setTimeout(carousel, 9000); //9 second rotation
        }
        </script>

        <!-- JS function for next/previous image selectors on home page-->
        <script>
var slideIndex = 1;
showDivs(slideIndex);

function plusDivs(n) {
  showDivs(slideIndex += n);
}

function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("mySlides");
  if (n > x.length) {slideIndex = 1}
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
  x[slideIndex-1].style.display = "block";
}
</script>

/* CSS for slideshow button left */
.button-display-left {
  color: #fff!important;
  background-color: #000000!important;
  position: sticky;
  top: 35%;
  left: 0%;
  right: 100%;
  transform: translate(0%, -700%);
}

/* CSS for slideshow button right */
.button-display-right {
  color: #fff!important;
  background-color: #000000!important;
  position: sticky;
  top: 35%;
  left: 100%;
  right: 0%;
  transform: translate(0%,-700%);
  }
