<template>

  <div class="HolidayPackages">
		
		<button v-on:click="bestvalueFunction" id="side-bar-btn">SIDE</button>

<!---Leftside-->
<aside id="leftside2" class="hide" v-if="bestvalueFunction">
<br/>
<h1>Filter By Season</h1>
<ul>
	<li v-for="season in season"><a href="">{{season.title}}</a></li>

</ul>
<br/>
<br/>
<h1>Filter By Location</h1>
<ul>
	<li v-for="location in location"><a href="">{{location.title}}</a></li>

</ul>
<br/>
<br/>
<h1>Filter By Price</h1>
<ul>
	<li v-for="price in price"><a href="">{{price.title}}</a></li>

</ul>
<br/>
<br/>
<h1>Filter By Rating</h1>
<ul>
	<li v-for="rating in rating"><a href="">{{rating.title}}</a></li>

</ul>
<br/>

</aside>

<main id="content2">

<article class="holiday_details" v-for="count in count">

<h1>{{title}}</h1>
<span class="holidayprice">from <span class="offerbox-price">{{pricesmall}}</span></span>

<figure>
	<img :src="url"/>
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

	
	name: 'HolidayPackages',

 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>




</style>