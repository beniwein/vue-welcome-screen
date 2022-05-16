<template>
  <div id="app">
    <h1>Welcome to Opportunity</h1>
    <h2>Datum-Placeholder</h2>

    <ul>
      <li style="color:red"><b>Uhrzeit</b></li>
      <li style="color:coral"><b>Basisbeschäftigung Besuch</b></li>
      <li style="color:coral">Interessierte für den zweiten Kurs werden uns besuchen</li>
    </ul>

    <ul>
      <li style="color:red"><b>Uhrzeit</b></li>
       <li style="color:coral"><b>Basisbeschäftigung Besuch</b></li>
      <li style="color:coral">Interessierte für den zweiten Kurs werden uns besuchen</li>
    </ul>

    <ul>
      <li style="color:red"><b>Uhrzeit</b></li>
       <li style="color:coral"><b>Basisbeschäftigung Besuch</b></li>
      <li style="color:coral">Interessierte für den zweiten Kurs werden uns besuchen</li>
    </ul>

    <footer>
      <img
        src="./assets/logo-zh.png"
        width = 230px;
        
      >  
      <img 
        src="./assets/logo-opportunity.png"
        width = 296px;
                      
      >  
      <img
        src="./assets/logo-sag.png"
        width = 273px;
              
      >  
    </footer>
    
  </div>
  
</template>

<script>

export default {
  name: 'App',
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap');
#app {
  font-family: 'Inter', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  margin-top: 60px;
}
h1 {
  font-family: 'Inter';
  font-size: 62px;
  margin-left: 60px;
}
h2 {
  font-family: 'Inter';
  font-size: 62px;
  color: #9AA7B1;
  margin-left: 60px;
}
body {
  background-color: #E8EFF4;
  display:flex; 
  flex-direction:column; 
}
ul {
   background-color: #0F05A0;
   display: block;
   list-style-type: none; 
   list-style-type: none;    
   font-size: 28px;
   margin: 60px;
   padding-top: 37px;
   padding-bottom: 37px;
   padding-left: 40px;
}

footer {
  background: white;
  position: absolute;
  margin-left: 0px;
  margin-right: 0px;
  bottom: 0px;
}  
img {
  margin-top: 43px;
  margin-bottom: 43px;
  margin-left: 40px;
  margin-right: 50px;
    
}

</style>
