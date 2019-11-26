<template>
  <div>
    <h2 class="page__title"> Контакты</h2>
    <div id="map"></div>   
  </div>
</template>

<style lang="scss">
#map{
  min-height: 70vh;
  border: 1px solid #fff;
  border-radius: 5px;
  box-shadow: 0 0 2px rgba(0,0,0,.3);
}
</style>

<script>

export default {
  data() {
    return {
      myMap: {},
      objectManager: {}   
    }
  },
  methods: {
    init() {
      this.myMap = new ymaps.Map('map', {
        center:[43.26414732288554,76.92991844041444],
        zoom: 12
      });
      this.objectManager = new ymaps.ObjectManager();
      this.objectManager.add({
        "type" : "FeatureCollection",
        "features": [
          {
            "type" : "Feature",
            "id": 0,
            "geometry": {
              "type": "Point",
              "coordinates": [43.26414732288554,76.92991844041444]
            },
            "properties" : {
              "balloonContent": "Мега Парк",
              "hintContent": "ТРЦ Мега Парк"
            },
          },
          {
            "type" : "Feature",
            "id": 1,
            "geometry": {
              "type": "Point",
              "coordinates": [43.23053604152807,76.945977]
            },
            "properties" : {
              "hintContent": "Нурлы-Тау"              
            },
            "options": {
              "iconLayout": "default#image",
              "iconImageHref": '/point.png',
              "iconImageSize": [30,38]
            }
          }
          
        ]
      });
      this.myMap.geoObjects.add(this.objectManager);
    }
  },
  mounted(){
    ymaps.ready(this.init);
  }
}
</script>