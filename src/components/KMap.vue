<script>
export default{
  name: "Kakaomap",
  data(){
    return {
      map:null
    };
  },
  setup() {},
  created() {},
  mounted() {
    if (window.kakao && window.kakao.maps){
      this.loadMap();
    }else{
      this.loadScript();
    }
  },
  unmounted() {},
  methods: {
    loadScript(){
      const script = document.createElement("script");
      script.src =
        "//dapi.kako.com/v2/maps/sdk.js?appkey=112dbb83c174d4ca84a3e232efea83a8&autoload=false";
      script.onload = () => window.kakao.maps.load(this.loadMap);
    
      document.head.appendChild(script);
    },
    loadMap(){
      const container = document.getElementByID("map");
      const options = {
        center: new window.kakao.maps.LatLng(33.450701, 126.570667),
        level: 3,
      };
      this.map = new window.kakao.maps.Map(container, options);
      this.loadMaker()
    },
    loadMaker() {
      const markerPosition = new window.kakao.maps.LatLng(33.450701, 126.570667)
      const marker = new window.kakao.maps.Marker({
        position: markerPosition
      })
      marker.setMap(this.map)
    }
  },
};
</script>

<template>
  <div>
    <h2>카카오 맵 보기</h2>
    <div id="map"></div>
  </div>
</template>

<style scope>
#map {
  width : 100%;
  height : 400px;
}
</style>