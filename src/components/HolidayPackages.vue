<template>
<div class="HolidayPackages">

  <button v-on:click="leftsideFunction" id="side-bar-btn">SIDE</button>


  <!---leftside2-->
  <aside id="leftside2" class="hide" v-if="leftsideFunction">
    <br/>
    <h1>Filter By Season</h1>
    <ul>
      <li v-for="(data,index) in seasons" :key='index'>
        <a href="">{{data.season}}</a>
      </li>

    </ul>
    <br/>
    <br/>
    <h1>Filter By Location</h1>
    <ul>
      <li v-for="(data,index) in locations" :key='index'>
        <a href="">{{data.location}}</a>
        </li>

    </ul>
    <br/>
    <br/>
    <h1>Filter By Price</h1>
    <ul>
      <li v-for="(data,index) in prices" :key='index'>
        <a href="">{{data.price}}</a>
      </li>

    </ul>
    <br/>
    <br/>
    <h1>Filter By Rating</h1>
    <ul>
      <li v-for="(data,index) in ratings" :key='index'>
        <a href="">{{data.rating}}</a>
      </li>

    </ul>
    <br/>
  </aside>

  <!---main content-->
  <main id="content2">

    <article class="holiday_details" v-for="(data,index) in count" :key='index'>

      <h1>{{title}}</h1>
      <span class="holidayprice">from <span class="offerbox-price">{{pricesmall}}</span></span>

      <figure>
        <img v-bind:src="url" />
        <figcaption>
          <p>Location : {{place}}</p>
          <p>{{text}}</p>
          <a href="">View Details</a>

        </figcaption>

      </figure>


    </article>


  </main>

  <div class="clearfix"></div>

</div>
</template>

<script>
export default {

  methods: {

    leftsideFunction: function() {

      console.log(event);

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

  name: 'HolidayPackages',

  data() {

    return {

      show: 'true',

      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",

      url: "src/assets/images/page2grandcanyon_03.jpg",

      title: 'Lorem ipsum dolor sit amet.',

      pricesmall: '$399 - $599',

      place: 'Yellowstone',

      month: 'June',

      seasons: [

        {
          "season": "Winter"
        },
        {
          "season": "Summer"
        },
        {
          "season": "Spring"
        },
        {
          "season": "Autumn"
        }

      ],

      locations: [

        {
          "location": 'London'
        },
        {
          "location": 'Paris'
        },
        {
          "location": 'Madrid'
        },
        {
          "location": 'Rome'
        },
        {
          "location": 'Dubai'
        }

      ],

      prices: [

        {
          "price": '$100 - $500'
        },
        {
          "price": '$500 - $1000'
        },
        {
          "price": '$1000 - $1500'
        },
        {
          "price": '$1500 - $2000'
        },
        {
          "price": '$2000 +'
        }

      ],

      ratings: [

        {
          "rating": '1 Star'
        },
        {
          "rating": '2 Star'
        },
        {
          "rating": '3 Star'
        },
        {
          "rating": '4 Star'
        },
        {
          "rating": '5 Star'
        }

      ],

      holiday: [],

      count: 10
    }

  }



}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" >




</style>
