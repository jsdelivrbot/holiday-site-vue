<template>

  <div class="HolidayPackages">
		
<button v-on:click="show = !show" id="side-bar-btn">SIDE</button>

<!---Leftside-->
<transition name="fade">
<aside id="leftside2" v-if="!show">
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
</transition>

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
	
	 data(){
  
		return{

			show :'true',
			
			text:"raymond thompson",
			
			url: "src/assets/images/page2grandcanyon_03.jpg",
			
			title:'Lorem ipsum dolor sit amet.',
			
			pricesmall:'$399 - $599',
							
			place:'Yellowstone',
			
			month:'June',
		
			season :[
			
				{title:'Winter'},
				{title:'Summer'},
				{title:'Spring'},
				{title:'Autumn'}
			
			],
			
			location :[
			
				{title:'London'},
				{title:'Paris'},
				{title:'Madrid'},
				{title:'Rome'},
				{title:'Dubai'}
			
			],
			
			price :[
			
				{title:'$100 - $500'},
				{title:'$500 - $1000'},
				{title:'$1000 - $1500'},
				{title:'$1500 - $2000'},
				{title:'$2000 +'}
			
			],
			
			rating :[
			
				{title:'1 Star'},
				{title:'2 Star'},
				{title:'3 Star'},
				{title:'4 Star'},
				{title:'5 Star'}
			
			],
			
			holiday :[
			],
			count: 10
		}
	
	}	
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>




</style>