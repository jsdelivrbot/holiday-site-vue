<template>
<div class="BestDeal">
  <button id="side-bar-btn" v-on:click="leftsideFunction">SIDE</button>

  <!--Leftside-->

  <aside id="leftside2" class="hide" v-if="leftsideFunction">
    <br/>
    <h1>Filter By Season</h1>
    <ul>
      <li v-for="season in season" :key="season"><a href="">{{season.title}}</a></li>

    </ul>
    <br/><br/>
    <h1>Filter By Location</h1>
    <ul>
      <li v-for="location in location" :key="location"><a href="">{{location.title}}</a></li>

    </ul>
    <br/><br/>
    <h1>Filter By Price</h1>
    <ul>
      <li v-for="price in price" :key="price"><a href="">{{price.title}}</a></li>

    </ul>
    <br/><br/>
    <h1>Filter By Rating</h1>
    <ul>
      <li v-for="rating in rating" :key="rating"><a href="">{{rating.title}}</a></li>

    </ul>
    <br/>
  </aside>


  <main id="content2">

    <article class="holiday_details_small" v-for="count in count" :key="count">

      <h1>{{title}}</h1>
      <figure>

        <img :src="url" />

        <figcaption>
          <span class="holidayprice">From <span class="offerbox-price">{{pricesmall}}</span></span>
          <p>Location: {{place}}.</p>
          <p> Available: {{month}}.</p>
          <a href="">View Details</a>
        </figcaption>

      </figure>

    </article>

    <br/>

  </main>

  <div class="clearfix"></div>
</div>
</template>

<script>
export default {

  

  methods: {

    leftsideFunction: function() {

      //console.log(event);

      event.preventDefault();

      var el = document.getElementById("leftside2");

      var box = el.getAttribute("class");

      if (box == "hide") {

        el.setAttribute("class", "show");

      } else {

        el.setAttribute("class", "hide");

      }
    }

  },

  name: 'BestDeal',

  data() {

    return {

      show: 'true',

      url: "src/assets/images/page2grandcanyon_03.jpg",

      title: 'Lorem ipsum dolor sit amet.',

      pricesmall: '$399 - $599',

      place: 'Yellowstone',

      month: 'June',

      season: [

        {
          title: 'Winter'
        },
        {
          title: 'Summer'
        },
        {
          title: 'Spring'
        },
        {
          title: 'Autumn'
        }

      ],

      location: [

        {
          title: 'London'
        },
        {
          title: 'Paris'
        },
        {
          title: 'Madrid'
        },
        {
          title: 'Rome'
        },
        {
          title: 'Dubai'
        }

      ],

      price: [

        {
          title: '$100 - $500'
        },
        {
          title: '$500 - $1000'
        },
        {
          title: '$1000 - $1500'
        },
        {
          title: '$1500 - $2000'
        },
        {
          title: '$2000 +'
        }

      ],

      rating: [

        {
          title: '1 Star'
        },
        {
          title: '2 Star'
        },
        {
          title: '3 Star'
        },
        {
          title: '4 Star'
        },
        {
          title: '5 Star'
        }

      ],

      holiday: [],

      count: 10
    }

  }

}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss">



</style>
