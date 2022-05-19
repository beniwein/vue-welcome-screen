<template>
  <div id="app">
    
    <h1>{{ title }}</h1>
    <h2>{{currentDate()}}</h2>

    <ul 
      v-if="entries"
        class="entry-list">     
      <li        
        class="entry-item"
        v-for="entry in entries"      

        :key="entry.id"
      >
        <span class="entry-daytime" style="color:red"><b>{{entry[0]}}, {{entry[1].replaceAll("/", ".")}}</b></span><br />
        <h3 class="entry-title" style="color:coral">{{entry[2]}}</h3>
        <span class="entry-description" style="color:coral">{{entry[3]}}</span><br />
        
        </li>
      </ul>

      <h1 v-else>No Items available</h1>
      
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
import axios from "axios";
export default {
  name: 'App',
  data() {
    return {
      title: "Welcome to Opportunity",
      sheet_id: "1a81aI0Y8ViZO0tI92h2YSMqVQJ8hmNNMyMylXgvwiU4",
      api_token: "AIzaSyA-qeDXOhEeQDA0vQf7LgkF7DQtGnAtmAU",
      entries: [],
    }
  },
  computed: {
    gsheet_url() {
      return `https://sheets.googleapis.com/v4/spreadsheets/${this.sheet_id}/values:batchGet?ranges=A2%3AE100&valueRenderOption=FORMATTED_VALUE&key=${this.api_token}`;
    },
  },
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}.${current.getMonth()+1}.${current.getFullYear()}`;
      return date;
      },
    getData() {
      axios.get(this.gsheet_url).then((response) => {
      this.entries = response.data.valueRanges[0].values;
      });
    },
    refreshData() {
      this.currentDate();
      this.getData();
    }
  },  
  mounted() {
    this.refreshData();
      setInterval(
        this.refreshData,
      1800000);
      },
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
h3, span, li {
   background-color: #0F05A0;
   display: block;
   list-style-type: none; 
   list-style-type: none;    
   font-size: 28px;
   margin: 10px;
   padding-top: 10px;
   padding-left: 40px;
}
footer {
  background: white;
  position: fixed;
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