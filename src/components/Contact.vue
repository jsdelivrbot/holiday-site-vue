<template>
  <div class="Contact">
    <button v-on:click="show = !show" id="side-bar-btn">SIDE</button>
<!--Leftside-->
<transition name="fade">
<aside id="leftside3" v-if="!show">

<ul id="contact-details" >
	<li><span><img :src= "'src/assets/images/images/Telephone.png'" ></span>Phone: <br/>123 436 7890</li>
	<li><span><img :src="'src/assets/images/images/envelope.png'" ></span>Mail: <a href="">info@travelagency.com</a></li>
	<li><span><img :src="'src/assets/images/images/Address.png'" ></span>Address:<br/> Lorem Ipsum 1234 Dolo Sit Amet</li>
</ul>
<div class="clearfix"></div>
</aside>
</transition>
<main id="content2">
<h1>Lorem ipsum dolor sit amet, consectetur</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. <br/>
Enim odit dolor sequi voluptatem esse doloribus libero commodi ea debitis id nostrum odio velit impedit vitae tenetur voluptates vero beatae excepturi.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. <br/>
Enim odit dolor sequi voluptatem esse doloribus libero commodi ea debitis id nostrum odio velit impedit vitae tenetur voluptates vero beatae excepturi.</p>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. <br/>
Enim odit dolor sequi voluptatem esse doloribus libero commodi ea debitis id nostrum odio velit impedit vitae tenetur voluptates vero beatae excepturi.</p>
<div class="clearfix"></div>
<br/>

<form id="contactform" >
<ul>
<li>
<label>First name</label>
<input  id="firstname" type="text" name="firstname" >
</li>
<li>
<label>Last name</label>
<input type="text" id="lastname" name="lastname">
</li>
<li>
<label>Email</label>
<input type="text" id="email" name="email"  >
</li>
<li>
<label>Phone</label>
<input type="text" id="phone" name="phone" >
</li>
<li>
<label>Message</label>
<textarea name="message" id="message" class="required" cols="50" rows="10" > ..</textarea>
</li>
<li>
<input type="submit" value="submit" id="contactbtn">
</li>
</ul>

</form>

</main>
<div class="clearfix"></div>

  </div>
</template>

<script>
export default {
  name: 'Contact',
  data(){
  
		return{

			show :'true',
						
		}
	
	}
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>



</style>