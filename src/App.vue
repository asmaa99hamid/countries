<template>
      <div class="container">
        <div class="row">
          <div class="col-md-12">
            <nav>
              <router-link :to="{ name: 'CountriesList'}">Countries</router-link> |
              <router-link :to="{ name: 'about' }">About</router-link>               
            </nav>
          </div>
        </div>
      </div>
  <router-view />
</template>

<style src="@/assets/css/bootstrap.min.css"></style>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}
h1,
h1 span,
h2,
h3,
h4,
h5,
h6,
ul.office-details li {
  font-family: 'Circe Rounded', sans-serif;
}
*,
:after,
:before,
h1,
h2,
h3,
h4,
h5,
h6,
p {
  margin: 0;
  padding: 0;
}
body,
html {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}
strong::-moz-selection {
  color: #212126;
}
strong::selection {
  color: #212126;
}
img {
  max-width: 100%;
}
a,
button,
p,
span {
  font-family: 'Gill Sans', sans-serif;
}
p {
  font-size: 18px;
  color: #777;
  line-height: 30px;
  font-weight: 400;
}
a:focus,
a:hover {
  text-decoration: none;
  outline: 0;
}
.content-box-md {
  padding: 100px 0;
}
.btn-general{
    font-weight: 400;
  text-transform: uppercase;
}
.btn-general,
.btn-general:before{
    -webkit-transition: 0.4s;
  -o-transition: 0.4s;
  transition: 0.4s;
}
.btn-general {
  position: relative;
  font-size: 13px;
  background: 0;
  color: #55b9a6 !important;
  line-height: 1 !important;
  padding: 13px 46px;
  border: 2px solid;
  overflow: hidden;
  z-index: 1;
}
.btn-general:before {
  content: ' ';
  position: absolute;
  background: #55b9a6;
  width: 0;
  height: 100%;
  left: -50%;
  top: 0;
  -webkit-transform: skew(50deg);
  -ms-transform: skew(50deg);
  transform: skew(50deg);
  -webkit-transform-origin: top left;
  -ms-transform-origin: top left;
  transform-origin: top left;
  z-index: -1;
}
.btn-general:hover:before {
  width: 150%;
}
.btn {
  outline: 0 !important;
  -webkit-box-shadow: none !important;
  box-shadow: none !important;
}
.btn-blue {
  border-color: #55b9a6;
}
.btn-blue:hover {
  color: #fff !important;
}
nav {
  padding: 30px;
  text-align: center;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a:hover {
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #55b9a6;
}
</style>
