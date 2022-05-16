<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <h2>{{currentDate()}}</h2>

    <ul>
      <li style="color:red"><b>{{daytime1}}</b></li>
      <li style="color:coral"><b>{{description1}}</b></li>
      <li style="color:coral">{{task1}}</li>
    </ul>

    <ul>
      <li style="color:red"><b>{{daytime2}}</b></li>
       <li style="color:coral"><b>{{description2}}</b></li>
      <li style="color:coral">{{task2}}</li>
    </ul>

    <ul>
      <li style="color:red"><b>{{daytime3}}</b></li>
       <li style="color:coral"><b>{{description3}}</b></li>
      <li style="color:coral">{{task3}}</li>
    </ul>

    <footer>
      <img 
        src="./assets/logo-zh.png"
        width = 230px:
        
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
  data() {
    return {
      title: "Welcome to Opportunity",
      description1: "Basisbeschäftigung Besuch",
      description2: "Gruppenarbeit",
      description3: "Abschluss",
      daytime1: "08.30" + " Uhr",
      daytime2: "13.30" + " Uhr",
      daytime3: "16.30" + " Uhr",
      task1: "Interessierte für den zweiten Kurs werden uns besuchen",
      task2: "Workshop",
      task3: "Wrap-Up",
    }
  },
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}.${current.getMonth()+1}.${current.getFullYear()}`;
      return date;
    }
  }
};
  
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
