<template >
<!--Warunek, który pozwoli wyświetlać inne tło dla temperatury powyżej 16 stopni, a inne dla temperatury poniżej 16 stopni-->
<div id="weather" :class="typeof weather.main != 'undefined' && weather.main.temp > 16 ? 'warm' : ''">
    <main class="weather-main">
      <div class="search-box">
        <!--Input, który pozwala wpisać nazwę Miasta (można także nazwę Państwa)-->
        <input 
          type="text" 
          class="search-bar d-none d-sm-flex" 
          placeholder="Wyszukaj Miasto"
          v-model="query"
          @keypress="fetchWeather"
        />
        <input 
          type="text" 
          class="search-bar-mobile d-flex d-sm-none" 
          placeholder="Wyszukaj Miasto"
          v-model="query"
          @keypress="fetchWeather"
        />
      </div>
      <!--Zwraca wpisanę nazwę Miasta (lub Państwa) oraz dzisiejszą datę-->
      <div class="weather-wrap" v-if="typeof weather.main != 'undefined'">
        <div class="location-box">
          <div class="location">{{ weather.name }}, {{ weather.sys.country }}</div>
          <div class="date">{{ dateBuilder() }}</div>
        </div>
        <!--Zwraca temperaturę, która aktualnie jest w danym Mieście (lub Państwie)-->
        <div class="weather-box">
          <div class="temp">{{ Math.round(weather.main.temp) }}°c</div>
          <div class="weather">{{ weather.weather[0].main }}</div>
        </div>
      </div>
    </main>
  </div>
</template>

<!--Scrypt Vue, który zawiera przede wszystkim klucz API potrzebny do pobierania pogody, ale takżę skrypty które pozwolą na pobieranie danych przy użyciu API. Pogoda pobierana jest z OpenWeather.-->
<script>
export default {
  name: 'app',
  data () {
    return {
      api_key: '1840289e8b0f47976cc4f61871aad702',
      url_base: 'https://api.openweathermap.org/data/2.5/',
      query: '',
      weather: {}
    }
  },
  methods: {
    fetchWeather (e) {
      if (e.key == "Enter") {
        fetch(`${this.url_base}weather?q=${this.query}&units=metric&APPID=${this.api_key}`)
          .then(res => {
            return res.json();
          }).then(this.setResults);
      }
    },
    setResults (results) {
      this.weather = results;
    },
    dateBuilder () {
      let d = new Date();
      let months = ["Styczeń", "Luty", "Marzec", "Kwiecień", "Maj", "Czerwiec", "Lipiec", "Siepień", "Wrzesień", "Październik", "Listopad", "Grudzień"];
      let days = ["Niedziela", "Poniedziałek", "Wtorek", "Środa", "Czwartek", "Piątek", "Sobota"];
      let day = days[d.getDay()];
      let date = d.getDate();
      let month = months[d.getMonth()];
      let year = d.getFullYear();
      return `${day} ${date} ${month} ${year}`;
    }
  }
}
</script>

<!--Style CSS + import czocionki-->
<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Segoe UI';
}
#weather{
background: rgb(0,24,36);
background: linear-gradient(90deg, rgba(0,24,36,1) 0%, rgba(9,121,120,1) 36%, rgba(0,211,255,1) 100%);
transition: 0.3s;
}
#weather.warm {
background: rgb(0,24,36);
background: linear-gradient(90deg, rgba(0,24,36,1) 0%, rgba(9,121,58,1) 35%, rgba(0,255,154,1) 100%);
}
main {
  min-height: 42vh;
  padding: 25px;
  
}
.search-bar-mobile{
 display: block;
  width: 145%;
  padding: 15px;
  margin-left:-25px;
  
  color: #313131;
  font-size: 20px;
  appearance: none;
  border:none;
  outline: none;
  background: none;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  background-color: white;
  border-radius: 0px 16px 0px 16px;
  transition: 0.4s;
  
}
.search-box {
  width: 35%;
  margin-left:33%;
  float:center;
  margin-bottom: 30px;
}
.search-box .search-bar {
  display: block;
  width: 100%;
  padding: 15px;
  
  color: #313131;
  font-size: 20px;
  appearance: none;
  border:none;
  outline: none;
  background: none;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  background-color: white;
  border-radius: 0px 16px 0px 16px;
  transition: 0.4s;
}
.search-box .search-bar:focus {
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.75);
  border-radius: 16px 0px 16px 0px;
}
.location-box .location {
  color: #FFF;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
}
.location-box .date {
  color: #FFF;
  font-size: 20px;
  font-weight: 300;
  font-family: 'Segoe UI';
  text-align: center;
}
.weather-box {
  text-align: center;
}
.weather-box .temp {
  display: inline-block;
  padding: 10px 25px;
  color: #FFF;
  font-size: 102px;
  font-weight: 900;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
  background-color:rgba(255, 255, 255, 0.25);
  border-radius: 16px;
  margin: 30px 0px;
  box-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}

.weather-box .weather {
  color: #FFF;
  font-size: 48px;
  font-weight: 700;
  font-family: 'Segoe UI';
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}
</style>