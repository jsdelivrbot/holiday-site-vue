<template>
<div id="app">

  <!--wrapper-->
  <div id="wrapper">

    <!--header-->
    <header>
      <!---contact number-->
      <aside class="contact">
        <span class="tele">
						<img v-bind:src="'src/assets/images/images/Telephone.png'" >
						<a href="tel:0208-000-1452" id="contact-number">{{phoneNumber}}</a>
					</span>
        <span id="opening-time">{{openTime}}</span>
      </aside>

      <!---logo-->
      <figure id="logo">
        <img v-bind:src="'./src/assets/images/travel-agency-website-logo.png'">
      </figure>


      <!---primary navigation-->
      <nav>

        <aside id="language-box">
          <form>
            <label>Language:</label>
            <select name="language">
							<option value="empty"></option>
							<option value="United_Kingdom"></option>
							<option value="Germany"></option>
							<option value="United_States"></option>
							<option value="Jamaica"></option>
							<option value="France"></option>
							<option value="Spain"></option>
						</select>
          </form>

        </aside>

        <button v-on:click="testerFunction" id="toggle-menu">Menu</button>

        <ul id="navi" class="hide" v-if="testerFunction">
          <li>
            <router-link to="/" class="nav-item r-item">Home</router-link>
          </li>
          <li>
            <router-link to="/HolidayPackages" class="nav-item r-item">HolidayPackages</router-link>
          </li>
          <li>
            <router-link to="/BestDeal" class="nav-item r-item">BestDeal</router-link>
          </li>
          <li>
            <router-link to="/Services" class="nav-item r-item">Services</router-link>
          </li>
          <li>
            <router-link to="/AboutUs" class="nav-item r-item">AboutUs</router-link>
          </li>
          <li>
            <router-link to="/Contact" class="nav-item r-item">Contact</router-link>
          </li>
        </ul>

      </nav>
      <!---primary navigation end-->
    </header>

    <transition name="router-anim">

      <!--view-->
      <router-view/>

    </transition>

  </div>

  <!--footer-->
  <footer>
    <ul>
      <li>
        <router-link to="/" class="nav-item r-item">Home</router-link>
      </li>
      <li>
        <router-link to="/BestDeal" class="nav-item r-item">BestDeal</router-link>
      </li>
      <li>
        <router-link to="/AboutUs" class="nav-item r-item">AboutUs</router-link>
      </li>
      <li>
        <router-link to="/HolidayPackages" class="nav-item r-item">HolidayPackages</router-link>
      </li>
      <li>
        <router-link to="/Contact" class="nav-item r-item">Contact</router-link>
      </li>
      <li>
        <router-link to="/Services" class="nav-item r-item">Services</router-link>
      </li>
    </ul>
  </footer>

</div>
</template>

<script>
export default {
  name: 'app',
  methods: {

    testerFunction: function() {

      //console.log(event);

      event.preventDefault();

      var el = document.getElementById("navi");

      var box = el.getAttribute("class");

      if (box == "hide") {

        el.setAttribute("class", "show");

      } else {
        el.setAttribute("class", "hide");

      }

    }

  },
  data() {

    return {

      phoneNumber: '0208-365-1452',
      openTime: 'Everyday 8am - 9pm',


    }
  }

}
</script>

<style lang="scss">

@import 'main.scss';

.router-anim-enter-active {

    animation: coming 1s;
    animation-delay: 1s;
    opacity: 0;
}

.router-anim-leave-active {

    animation: going 1s;
}

@keyframes coming {
    from {
        transform: translateX(-50px);
        opacity: 0;
    }
    to {
        transform: translateX(0px);
        opacity: 1;
    }

}

@keyframes going {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(-50px);
        opacity: 0;
    }

}


</style>
