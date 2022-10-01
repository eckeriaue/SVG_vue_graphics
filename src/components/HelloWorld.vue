<template>

  <!-- <div class="wrapper">

    <div>
      <figure>
        <svg viewBox="0 0 63.6619772368 63.6619772368">
          <circle class="pie1" cx="31" cy="31" r="15" :style="`stroke-dasharray: 55, 40, 30, 70;`" />
          <circle class="pie2" cx="31" cy="31" r="15" :style="`stroke-dasharray: 5, 50, 35, 0;`" />
        </svg>
      </figure>
    </div>

  </div> -->

  <div style="display: flex; column-gap: 30px; position: sticky; z-index: 30; background-color: #fff; padding: 10px; top: 0;">
    <div style="border: 1px solid; border-radius: 20px; padding: 10px 20px; font-family: sans-serif;">
      blue
    <input style="display: block" type="range" v-model="blue1" />
    <pre> stroke-dasharray: {{ `${100 - blue1}, ${blue1}` }}</pre>

  </div>
  <div style="border: 1px solid; border-radius: 20px; padding: 10px 20px; font-family: sans-serif;">
    green
    <input style="display: block" type="range" v-model="green1" />

    <pre> stroke-dasharray: {{ `${100 - green1}, ${green1}` }}</pre>

  </div>
</div>




  <div class="wrapper" style="display: flex; flex-wrap: wrap">


    <div class="scene">
      <svg xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="300" height="300" viewBox="0 0 50 50" style="transform: rotate(-15deg)">

        <circle class="pie1" cx="25" cy="25" r="15"  ></circle>
        <circle class="pie2" cx="25" cy="25" r="15"  ></circle>
     
     
      </svg>
    </div>
    <div class="scene">
      <svg xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="300" height="300" viewBox="0 0 50 50" style="transform: rotate(-15deg)">

        <circle class="pie1_v1" cx="25" cy="25" r="15"  ></circle>
        <circle class="pie2_v1" cx="25" cy="25" r="15"  ></circle>
     
     
      </svg>
    </div>




    <div class="scene">
      <svg xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="300" height="300" viewBox="0 0 50 50" style="transform: rotate(-15deg)">

        <circle class="pie1_v2" cx="25" cy="25" r="15"  ></circle>
        <circle class="pie2_v2" cx="25" cy="25" r="15"  ></circle>
     
     
      </svg>
    </div>


    <div class="scene">
      <svg width="300" height="300" viewBox="0 0 50 50">

        <circle cx="25" cy="25" r="15" fill="none" stroke="#E1E1E1" stroke-width="8"/>
          <circle cx="25" cy="25" r="15" fill="none" stroke-dashoffset="314" stroke-dasharray="0, 314"  stroke="purple" stroke-width="8" >
          <animate attributeName="stroke-dasharray" dur="4s" begin="svg1.click" values="0,314;314,0" fill="freeze" /> 
     </circle>
     <text  x="50%" y="50%" fill="red" style="font-family: sans-serif;" text-anchor="middle" dy="7" font-size="20">error</text>
      </svg>
    </div>



    <div class="scene">
      <svg xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="300" height="300" viewBox="0 0 50 50" style="transform: rotate(-15deg)">

        <text x="20%" y="-5%" fill="green" style="font-family: sans-serif;" text-anchor="middle" dy="7" font-size="5">control</text>

        
        <circle stroke="#C4F2A9" cx="25" cy="25" r="15" :stroke-dasharray="`${100 - green1}, ${green1}`" ></circle>
        <circle  stroke="#79A4FF" cx="25" cy="25" r="15" :stroke-dasharray="`${100 - blue1}, ${blue1}`"  ></circle>
     
     
      </svg>
    </div>


    <div class="scene">
      <svg  xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"   
        width="100%" height="100%" viewBox="0 0 50 50"
      >  
        
        <circle cx="25" cy="25" r="15" transform="rotate(-90 25 25)" stroke-dasharray="0, 314"  stroke="#79A4FF"  stroke-width="10">
         <animate attributeName="stroke-dasharray" dur="4s"  :values="`0, 314; ${60 * 3.14}, ${40 * 3.14}`" fill="freeze" /> 
        </circle>
        
     <text id="count" x="50%" y="50%" fill="red" style="font-family: sans-serif;" text-anchor="middle" dy="7" font-size="20">error</text>

        
     
      </svg> 
    </div>


    
  

  </div>
  <div style="display: flex; column-gap: 30px; position: sticky; z-index: 30; background-color: #fff; padding: 10px; top: 0;">
    <div style="border: 1px solid; border-radius: 20px; padding: 10px 20px; font-family: sans-serif;">
      blue
    <input style="display: block" type="range" v-model="blue.val" />
    <input style="display: block;" type="range" v-model="blue.val2" /> 
     <input style="display: block;" type="range" v-model="blue.val3" /> 
     <input style="display: block;" type="range" v-model="blue.val4" />
    <div style="display: flex;">
      <span>stroke-dasharray:</span>
      <input type="number" style="max-width: 40px" v-model="blue.val">,
      <input type="number" style=" max-width: 40px" v-model="blue.val2">,
      <input type="number" style=" max-width: 40px" v-model="blue.val3">,
      <input type="number" style=" max-width: 40px" v-model="blue.val4">,
    </div>
  </div>
  <div style="border: 1px solid; border-radius: 20px; padding: 10px 20px; font-family: sans-serif;">
    green
    <input style="display: block" type="range" v-model="green.val" />
    <input style="display: block" type="range" v-model="green.val2" />
    <input style="display: block" type="range" v-model="green.val3" />
    <input style="display: block" type="range" v-model="green.val4" /> 

    <div style="display: flex;">
      <span>stroke-dasharray:</span>
      <input type="number" style="max-width: 40px" v-model="green.val">,
      <input type="number" style="max-width: 40px;" v-model="green.val2">,
      <input type="number" style="max-width: 40px;" v-model="green.val3">,
      <input type="number" style="max-width: 40px;" v-model="green.val4">,
    </div>

  </div>
</div>
  


<div class="wrapper" style="display: flex; flex-wrap: wrap">

  <div class="scene">
      <svg xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="300" height="300" viewBox="0 0 50 50" style="transform: rotate(-15deg)">
        <text x="20%" y="-5%" fill="green" style="font-family: sans-serif;" text-anchor="middle" dy="7" font-size="5">control</text>

        <circle stroke="#C4F2A9" cx="25" cy="25" r="15" :stroke-dasharray="`${green.val}, ${green.val2}, ${green.val3}, ${green.val4}`" ></circle>
        <circle  stroke="#79A4FF" cx="25" cy="25" r="15" :stroke-dasharray="`${blue.val}, ${blue.val2}, ${blue.val3}, ${blue.val4}`"  ></circle>
     
     
      </svg>
    </div>

</div>

</template>

<script>

export default {
  data() {
    return {
      blue1: 50,
      green1: 0,
      blue: {
        val:  40,
        val2:  40,
        val3:  35,
        val4:  0,
      }, 

      green: {
        val:  0,
        val2:  50,
        val3:  35,
        val4:  0,
      }
    }
  }
}

</script>

<style>

.wrapper {
  width: 100%;
  max-width: 1200px;
  margin: 20px auto;
}
.scene{
  margin: 10px;
  background: rgba(0, 0, 0, 0.064);
}
circle {
	fill:rgba(0,0,0,0);
  stroke-width: 10;
  stroke-dashoffset: 25;
  /* animation: pie1 6s  ease both; */
}
.pie1 {
  animation: pie1 2s ease-out both;
  stroke:#C4F2A9;
}
.pie2 {
  stroke:#79A4FF;
  animation: pie2 2s ease-out both;
}


.pie1_v1 {
  animation: pie1_v1 2s ease-in-out both;
  stroke:#C4F2A9;
}
.pie2_v1 {
  stroke:#79A4FF;
  animation: pie2_v1 2s ease-out both;
}
.pie1_v2 {
  animation: pie1_v2 2s ease-in-out both;
  stroke:#C4F2A9;
}
.pie2_v2 {
  stroke:#79A4FF;
  animation: pie2_v2 2s ease-out both;
}


@keyframes pie1 {
  0% {
    stroke-dasharray:0, 130
  }
  100% {
    stroke-dasharray:100, 0
  }
}
@keyframes pie2 {
  0% {
    stroke-dasharray: 0, 130
  }
  100% {
    stroke-dasharray:60, 40
  }
}





@keyframes pie1_v1 {
  0% {
    stroke-dasharray:20, 90
  }
  100% {
    stroke-dasharray:100, 0
  }
}
@keyframes pie2_v1 {
  0% {
    stroke-dasharray: 20, 80
  }
  100% {
    stroke-dasharray:60, 40
  }
}




@keyframes pie1_v2 {
  0% {
    stroke-dasharray:0, 100
  }
  100% {
    stroke-dasharray:100, 0
  }
}
@keyframes pie2_v2 {
  0% {
    stroke-dasharray: 0, 100
  }
  30% {
    stroke-dasharray:60, 40
  }
  100% {
    stroke-dasharray:60, 40
  }
}


</style>