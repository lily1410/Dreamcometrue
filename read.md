perspective: 1000px;

This is set on the parent container (.flip-card).

It controls how “deep” the 3D effect looks.

A smaller value (e.g. 200px) makes the 3D effect more dramatic (stronger tilt).

A larger value (e.g. 2000px) makes it look flatter (less tilt).
👉 In short: it tells the browser how far the viewer’s eye is from the object.

🔹 transition: transform 0.8s;

This makes the flip animation smooth.

0.8s = duration of the flip (slower flip = larger number).
👉 Without this, the card would instantly snap instead of animating.

🔹 transform-style: preserve-3d;

Tells the browser to keep the 3D effect for child elements.

If you don’t set this, the front/back won’t look like separate 3D planes.
👉 It allows the front and back faces to exist in 3D space.

🔹 transform: rotateY(180deg);

This rotates the element around the Y-axis (left → right).

180deg flips it to the opposite side.
👉 That’s how we “see the back of the card” when hovered/clicked.

🔹 backface-visibility: hidden;

By default, when an element flips, the back side is still visible through the front (like glass).

Setting this to hidden makes the hidden side invisible.
👉 Ensures only one face is shown at a time.

🔹 transform: translateX(-50%);

Moves an element 50% of its own width to the left.

This is usually combined with left: 50% to perfectly center horizontally.
👉 That’s why your overlay text is centered on the image.

🔹 background: linear-gradient(135deg, #1e3c72, #2a5298);

Creates a gradient background.

135deg = the angle of the gradient.

Colors = from #1e3c72 (dark blue) → #2a5298 (lighter blue).
👉 This gives the card back a smooth, modern color effect instead of plain solid color.

⚡ So basically:

perspective + transform-style = 3D setup

rotateY + backface-visibility = flipping logic

transition = smooth animation

translateX = centering text

linear-gradient = stylish background







 <div class="button">
    <div class="box">H</div>
    <div class="box">E</div>
    <div class="box">L</div>
    <div class="box">L</div>
    <div class="box">O</div>
  </div>


.button {
  display: flex;
  align-items: center;
  justify-content: center;
  /* height: 100vh; */
}

.box {
  width: 35px;
  /* height: 40px; */
  padding: 15px;
  display: flex;
  justify-content: center;
  font-size: 15px;
  font-weight: 700;
  color: #fff;
  transition: all .8s;
  cursor: pointer;
  position: relative;
  background: rgb(55, 115, 165);
  overflow: hidden;
}

.box:before {
  content: "W";
  position: absolute;
  top: 0;
  background: #0f0f0f;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: translateY(100%);
  transition: transform .4s;
}

.box:nth-child(2)::before {
  transform: translateY(-100%);
  content: "O";
}

.box:nth-child(3)::before {
  content: "R";
}

.box:nth-child(4)::before {
  transform: translateY(-100%);
  content: "L";
}

.box:nth-child(5)::before {
  content: "D";
}

.button:hover .box:before {
  transform: translateY(0);
}
.products{
  display: flex;
}































@media only screen and (max-width: 768px) {

  * {
    padding: none !important;
    margin: none !important;
  }

  nav {
    width: 285px !important;
  }

  /* Navbar */
  .nav-link {
    font-size: 16px;
  }

  .navbar {
    /* width: 300px !important; */
  }

  .navbar-brand {
    font-size: 1rem !important;
  }

  /* Hero Section */
  .hero-img {
    height: 30vh;
  }

  .hero-carousel {
    width: 285px !important;
  }

  .carousel-caption h1 {
    font-size: 1.5rem !important;
  }

  .carousel-caption h1 {
    font-size: 2rem;
  }

  .carousel-caption p {
    font-size: 1rem;
  }

  .carousel-caption .btn {
    padding: 8px 20px;
    font-size: 14px;
  }

  /* About Section */
  .about-img img {
    height: 250px !important;
    width: 250px !important;
  }

  .about-text p {
    font-size: 1rem;
  }


  .about-section .about {
    width: 300px !important;
    align-items: center !important;
    justify-content: center !important;
  }

  .about-section .about-text {
    width: 300px !important;

  }

  .about-section .about-text h2 {
    font-size: 1.8rem !important;
  }

  .about-section .about-text p {
    width: 250px !important;
    font-size: 15px !important;
  }

  .main-section {
    width: 285px !important;
  }
  .products{
     width: 290px !important;
  }
 .products p{
  font-size:  15px !important;
 }
  .section-title {
    font-size: 1.6rem;
  }

  /* Flip Cards / Services */
  .flip-card {
    height: 250px;
  }

  .overlay-text {
    font-size: 16px;
  }

  /* Product Cards */
  .product-card img {
    height: 200px;
  }

  .product-card .card-title {
    font-size: 1rem;
  }

  .price-tag {
    font-size: 14px;
    padding: 5px 12px;
  }

  .star {
    /* width: 20px !important; */
    display: flex !important;
    align-items: center !important;
    justify-content: center !important;
    text-align: center !important;
  }

  /* Retreat Section */
  .retreat {
    height: 200px;
  }

  .retreat img {
    width: 320px !important;
    height: 250px !important;
  }

  .retreat .healing {
    font-size: 1rem !important;
    align-items: center !important;
    justify-content: center !important;
    text-align: center;
  }

  /* Additional Images */
  .img2 img {
    width: 140px;
    height: 30vh;
  }

  /* Notify Section */
  .notify-title {
    font-size: 1.4rem;
  }
  .notify-section{
    width: 280px !important;
  }

  .notify-card {
    padding: 12px;
    font-size: 0.9rem;
  }

  /* General padding adjustments */

}