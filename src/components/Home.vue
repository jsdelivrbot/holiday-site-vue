<template>
  <div class="Home">

<!--Leftside-->
<aside id="leftside">

<!---Search form-->
<section class="leftsidebox">

<h2>Holiday Search</h2>

<form id="search_form">
	<ul>
	<li>
	<label>Where are you going?</label>
	<select name="destination" class="destination1">
	<option value="Antigua">Antigua</option>
	<option value="Belgium">Jamaica</option>
	<option value="United Kingdom">India</option>
	<option value="United Kingdom">United States</option>
	<option value="United Kingdom">United Kingdom</option>
	</select>
	</li>

	<li class="time">
	<label >When are you going?</label>
	<select name="date" class="time_1">
	<option value="1">1</option>
	<option value="2">2</option>
	<option value="3">3</option>
	<option value="4">4</option>
	<option value="5">5</option>
	</select>

	<select name="month" id="time_2">
	<option value="January">January</option>
	<option value="February">February</option>
	<option value="March">March</option>
	<option value="April">April</option>
	<option value="May">May</option>
        <option value="January">June</option>
	<option value="February">July</option>
	<option value="March">August</option>
	<option value="April">September</option>
	<option value="May">October</option>
        <option value="May">November</option>
        <option value="May">December</option>
	</select>

	<select name="year" class="time_1">
	<option value="2014">2014</option>
	<option value="2015">2015</option>
	<option value="2016">2016</option>
	</select>
	</li>

	<li>
	<label> Duration</label>
	<select name="duration" class="destination1">
	<option value="One Day">One Day</option>
	<option value="One Week">One Week</option>
	<option value="One Month">One Month</option>
	<option value="Six Months">Six Months</option>
	<option value="One Year">One Year</option>
	</select>
	</li>


	<li class="misc_inner">
	<label> Board</label>

	<select name="board" class="misc">
	<option value="Half">Half</option>
	<option value="Full">Full</option>

	</select>
	</li>
	<li class="misc_inner">
	<label> Star</label>
	<select name="star" class="misc">
	<option value="1 Star">1 Star</option>
	<option value="2 Star">2 Star</option>
	<option value="3 Star">3 Star</option>
	<option value="4 Star">4 Star</option>
	<option value="5 Star">5 Star</option>
	</select>
	</li>

	<li class="misc_inner">
	<label>Adults</label>
	<select name="adults" class="misc">
	<option value="1">1</option>
	<option value="2">2</option>
	<option value="3">3</option>
	<option value="4">5</option>
	<option value="5">6</option>
	</select>
	</li>
	<li class="misc_inner">
	<label>Children 0-17</label>
	<select name="children" class="misc">
	<option value="14">1</option>
	<option value="15">2</option>
	<option value="16">3</option>
	<option value="">4</option>
	<option value="">5</option>
	</select>
	</li>
	</ul>
	<input type="submit" value="Find Holiday" id="searchbtn">
</form>

</section>

<!--Destinations-->
<section class="leftsidebox">
<h2>Top Destinations</h2>

<div class="destinations">
<figure>
<img v-bind:src="'src/assets/images/travel-agency-website-eiffel-tower-image.jpg'" >

<figcaption>
<h3>Paris</h3>
<p>France</p>
<p>1,399 Hotels</p>
</figcaption>

</figure>
</div>

<div class="destinations">
<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-tower-of-london-image.jpg'" >
	
<figcaption>
<h3>London</h3>
<p>England</p>
<p>1,912 Hotels</p>
</figcaption>

</figure>
</div>

<div class="destinations">
<figure>
<img v-bind:src="'src/assets/images/travel-agency-website-bangkok-image.jpg'" >
<figcaption>
<h3>Bangkok</h3>
<p>	Thailand</p>
<p>1,542 Hotels</p>
</figcaption>

</figure>
</div>

<div class="destinations">
<figure>
<img v-bind:src="'src/assets/images/travel-agency-website-istanbul-image.jpg'" >

<figcaption>
<h3>Istanbul</h3>
<p>Turkey</p>
<p>504 Hotels</p>
</figcaption>

</figure>
</div>

<div class="destinations">
<figure>
<img v-bind:src="'src/assets/images/travel-agency-website-hong-kong-image.jpg'" >

<figcaption>
<h3>Hong Kong</h3>
<p>China</p>
<p>504 Hotels</p>
</figcaption>

</figure>
</div>

<a href="">View All</a>

</section>

<br/>
<br/>
<br/>
</aside>

<main id="content">

<figure id="banner">
<img v-bind:src="'src/assets/images/travel-agency-website-banner-image.jpg'" >

</figure>

<section id="offers">

<h2>Featured Holiday Package</h2>

<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-spanish-villa-image.jpg'" >

	<figcaption>
		<p>Lorem Ipsum Dolen sit.</p>
		<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>

	</figure>
</div>
<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-taj-mahal-image.jpg'" >

	<figcaption>
	<p>Lorem Ipsum Dolen sit.</p>
	<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>
	</figure>
</div>
<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-gold-coast-image.jpg'" >

	<figcaption>
	<p>Lorem Ipsum Dolen sit.</p>
	<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>
	</figure>

	<div class="clearfix"></div>
</div>
<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-dubai-image.jpg'" >

	<figcaption>
	<p>Lorem Ipsum Dolen sit.</p>
	<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>
	</figure>
</div>
<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-singapore-image.jpg'" >
		
	<figcaption>
	<p>Lorem Ipsum Dolen sit.</p>
	<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>
	</figure>
</div>
<div class="offerbox">
	<figure>
	<img v-bind:src="'src/assets/images/travel-agency-website-toronto-image.jpg'" >
		

	<figcaption>
	<p>Lorem Ipsum Dolen sit.</p>
	<p>from only <span class="offerbox-price">&pound;339</span> per person</p>
	</figcaption>
	</figure>
</div>

<div class="clearfix"></div>
</section>


</main>

<div class="clearfix"></div>
  </div>
</template>



<!--scripting-->
<script>
export default {
  name: 'Home',
 
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>




</style>
