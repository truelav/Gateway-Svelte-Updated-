<script>

</script>


<div class="container">
  <ul class="slides">
    <li id="slide1"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw1.jpg" alt="" /></li>
    <li id="slide2"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw2.jpg" alt="" /></li>
    <li id="slide3"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw3.jpg" alt="" /></li>
    <li id="slide4"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw4.jpg" alt="" /></li>
    <li id="slide5"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw5.jpg" alt="" /></li>
  </ul>

  <ul class="thumbnails">
    <li>
      <a href="#slide1"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw1.jpg" /></a>
    </li>
    <li>
      <a href="#slide2"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw2.jpg" /></a>
    </li>
    <li>
      <a href="#slide3"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw3.jpg" /></a>
    </li>
    <li>
      <a href="#slide4"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw4.jpg" /></a>
    </li>
    <li>
      <a href="#slide5"><img src="https://cdn.rawgit.com/huijing/filerepo/gh-pages/lw5.jpg" /></a>
    </li>
  </ul>
</div>

<style>
  html {
    box-sizing: border-box;
    height: 100%;
  }

  *,
  *::before,
  *::after {
    box-sizing: inherit;
    margin: 0;
    padding: 0;
  }

  .container {
    display: flex;
    justify-content: center;
  }

  .thumbnails {
    display: flex;
    flex-direction: column;
    line-height: 0;
  }
  .thumbnails li {
    flex: auto;
  }
  .thumbnails a {
    display: block;
  }
  .thumbnails img {
    width: 30vmin;
    height: 20vmin;
    -o-object-fit: cover;
      object-fit: cover;
    -o-object-position: top;
      object-position: top;
  }

  .slides {
    overflow: hidden;
    width: 75vmin;
    height: 100vmin;
  }
  .slides li {
    width: 75vmin;
    height: 100vmin;
    position: absolute;
    z-index: 1;
  }
  .slides img {
    height: 100vmin;
    -o-object-fit: cover;
      object-fit: cover;
    -o-object-position: top;
      object-position: top;
  }

  .slides li:target {
    z-index: 3;
    -webkit-animation: slide 1s 1;
  }

  .slides li:not(:target) {
    -webkit-animation: hidden 1s 1;
  }

  @-webkit-keyframes slide {
    0% {
      transform: translateY(-100%);
    }
    100% {
      transform: translateY(0%);
    }
  }

  @keyframes slide {
    0% {
      transform: translateY(-100%);
    }
    100% {
      transform: translateY(0%);
    }
  }
  @-webkit-keyframes hidden {
    0% {
      z-index: 2;
    }
    100% {
      z-index: 2;
    }
  }
  @keyframes hidden {
    0% {
      z-index: 2;
    }
    100% {
      z-index: 2;
    }
  }
</style>