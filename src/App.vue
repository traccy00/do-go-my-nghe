<template>
  <div id="app">
    <div class="nav">
      <!-- <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link> -->
    </div>
  </div>
  <router-view />
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-weight: 700;
}

body {
  background-color: #fff;
  font-family: "Roboto", sans-serif;
  line-height: 1;
  font-size: 16px;
}

img {
  display: block;
  max-width: 100%;
}

a {
  text-decoration: none;
}

/* CONTAINER */

.container {
  margin: 0 auto;
}

.intro {
  margin: 0 auto;
  height: 80vh;
}

.advertise {
  display: flex;
  justify-content: space-between;
  padding: 10px 200px;
  background-color: #e7e7e7;
  margin-bottom: 2px;
}

.advertise-text {
  text-transform: uppercase;
}

.menu {
  display: flex;
  justify-content: space-around;
  list-style: none;
  margin-left: auto;
}

.menu-item {
  padding: 0 20px;
}

.menu-link {
  color: #000;
}

.header {
  width: 100%;
  height: 100px;
  padding: 0 100px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  top: 0;
  z-index: 2;
  background-color: #e7e7e7;
}

.logo {
  max-width: 35%;
  cursor: pointer;
}

.search-box input {
  line-height: 20px;
  outline: none;
  border-radius: 5px;
  padding: 8px;
}

.hotline {
  font-size: 20px;
  display: flex;
  align-items: center;
}

.fas {
  font-size: 30px;
}

.hotline p {
  padding: 10px;
}

.category {
  display: flex;
  list-style: none;
  margin-left: 300px;
  align-items: center;
  padding: 10px;
}

.category-item:not(:first-child) {
  padding-left: 55px;
}

.category-link {
  color: #000;
  text-transform: uppercase;
}

/* SLIDER */

.slider {
  width: 100%;
  background-color: #e7e7e7;
}

.myslider {
  display: none;
  overflow: hidden;
  background-position: center;
}

.panel {
  background-size: auto 100%;
  background-position: center;
  background-repeat: no-repeat;
  height: 80vh;
  color: #fff;
  cursor: pointer;
  flex: 0.5;
  position: relative;
  transition: flex 0.7s ease-in;
}

.prev,
.next {
  position: absolute;
  top: 50%;
  transform: translate(0, -50%);
  margin: 20px;
  cursor: pointer;
  color: #fff;
  transition: 0.1s;
  user-select: none;
}

.prev:hover,
.next:hover {
  color: #3498db;
}

.next {
  right: 0;
}

.dotsbox {
  position: absolute;
  left: 50%;
  transform: translate(-50%);
  bottom: 30px;
  cursor: pointer;
}

.dot {
  display: inline-block;
  width: 15px;
  height: 15px;
  background-color: rgba(0, 0, 0, 0.6);
  border-radius: 50%;
  margin: 0 10px;
  cursor: pointer;
}

.active,
.dot:hover {
  background-color: rgba(0, 0, 0, 1);
}

.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {
    opacity: 0.8;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade {
  from {
    opacity: 0.8;
  }
  to {
    opacity: 1;
  }
}

.txt {
  position: absolute;
  color: #fff;
  letter-spacing: 2px;
  line-height: 35px;
  top: 40%;
  left: 15%;
  -webkit-animation-name: posi;
  -webkit-animation-duration: 2s;
  animation-name: posi;
  animation-duration: 2s;
  z-index: 1;
}

@-webkit-keyframes posi {
  from {
    left: 25%;
  }
  to {
    left: 15%;
  }
}

@keyframes posi {
  from {
    left: 25%;
  }
  to {
    left: 15%;
  }
}

.txt h1 {
  color: rgb(160, 100, 28);
  margin: 20px;
}

.txt p {
  font-weight: bold;
  font-size: 20px;
}

@media screen and (max-width: 800px) {
  .myslider {
    height: 500px;
  }
  .txt {
    line-height: 25px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    -webkit-animation-name: posi2;
    -webkit-animation-duration: 2 s;
    animation-name: posi2;
    animation-duration: 2 s;
  }
  @-webkit-keyframes posi2 {
    from {
      top: 35%;
    }
    to {
      top: 50%;
    }
  }
  @keyframes posi2 {
    from {
      top: 35%;
    }
    to {
      top: 50%;
    }
  }
  .txt h1 {
    font-size: 40px;
  }
  .txt p {
    font-size: 13px;
  }
}

@media screen and (max-width: 520px) {
  .txt h1 {
    font-size: 30px;
  }
  .sign {
    margin-right: 20px;
  }
  .sign a {
    font-size: 12px;
  }
}

/* PRODUCT */

.main {
  max-width: 1190px;
  margin: 0 auto;
  margin-top: 20px;
}

.list {
  --spacing: 5px;
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
}

.list-item {
  margin: 0 var(--spacing) 15px var(--spacing);
  width: calc(25% - var(--spacing) * 2);
}

.list-image {
  border-radius: 5px;
  border: 2px solid rgba(0, 0, 0, 0.1);
  padding: 1px;
}

.caption {
  display: flex;
  justify-content: center;
  padding: 20px;
}

.tab-caption {
  margin: 0 20px;
}

.head-title {
  text-transform: uppercase;
  font-size: 20px;
  font-weight: 400;
  border: 2px;
}

.tab-selected {
  border-bottom: 1px solid #000;
  padding-bottom: 3px;
}

.head-selected {
  font-weight: 700;
}

.sale-price {
  padding-right: 10px;
  text-decoration: line-through;
}

.sale-price,
.price {
  font-weight: 400;
  padding-top: 20px;
  padding-bottom: 20px;
}

.list-title {
  margin-top: 10px;
}

.list-desc {
  display: flex;
}

.list-evaluate {
  /* margin: 0 var(--spacing) 15px var(--spacing);
  width: calc(33.33% - var(--spacing) * 2); */
}

.evaluate-container {
  background-color: #e7e7e7;
}

.customer-evaluate {
  padding: 20px 0;
}

form {
  margin: 0 auto;
  width: 70%;
}

.form-row {
  padding: 5px;
}

.form-row input,
.form-row textarea,
.form-row select,
.infor-desc input {
  width: 70%;
  margin: 10px 0;
  border-radius: 4px;
  padding: 5px;
  outline: none;
}

.form-row label {
  width: 400px;
}

.infor {
  padding: 40px;
  background-color: rgba(60, 55, 55, 1);
  color: #fff;
  display: flex;
  justify-content: space-around;
  margin-top: 10px;
}

.infor-desc {
  margin-top: 10px;
}

.infor-desc p {
  line-height: 20px;
  padding: 5px;
}

.product-category .caption {
  padding-left: 5px;
  padding-right: 5px;
  display: block;
  text-align: center;
}

.list-sub-category {
  display: flex;
  list-style: none;
  align-items: flex-start;
}

.sub-category-item {
  padding-right: 40px;
}

.sub-category-link {
  color: #000;
  font-weight: 400;
}

.active-sub {
  border-bottom: 1px solid black;
  padding-bottom: 2px;
  font-weight: 700;
}
</style>
