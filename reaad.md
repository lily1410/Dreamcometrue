
  <div class="div"></div>
.div {
  /* margin: 6rem 12rem; */
  height: 100vh;
  width: 100%;
  object-fit: cover;
  background-size: 100% 100%;
  box-shadow: 20px 20px 10px gray;
  animation: slider 10s linear infinite;
}

@keyframes slider {
  0% {
    background-image: url(/assets/img/darkcupoftea.jpg);
  }

  25% {
    background-image: url(/assets/img/book1.jpg);
  }

  50% {
    background-image: url(/assets/img/developer.jpg);
  }

  75% {
    background-image: url(/assets/img/darkcupoftea.jpg);
  }

 100% {
    background-image: url(/assets/img/darkcupoftea.jpg);
  }

}