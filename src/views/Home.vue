<template>
  <l-map style="height: 95vh" :zoom="zoom" :center="center">
    <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle.loc"
      :radius="circle.radius"
    ></l-circle>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng2"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle2.loc"
      :radius="circle2.radius"
    ></l-circle>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng3"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle3.loc"
      :radius="circle3.radius"
    ></l-circle
    ><l-marker color="#ff00ff" :lat-lng="markerLatLng4"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle4.loc"
      :radius="circle4.radius"
    ></l-circle>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng5"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle5.loc"
      :radius="circle5.radius"
    ></l-circle>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng6"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle6.loc"
      :radius="circle6.radius"
    ></l-circle>
    <l-marker color="#ff00ff" :lat-lng="markerLatLng7"></l-marker>'
    <l-circle
      color="#ff00ff"
      :lat-lng="circle7.loc"
      :radius="circle7.radius"
    ></l-circle>
    <l-polyline :lat-lngs="polygon.latlngs" color="#ff00ff"></l-polyline>
  </l-map>
</template>

<script>
import { Icon } from "leaflet";
import { LMap, LTileLayer, LMarker, LCircle, LPolyline } from "vue2-leaflet";
delete Icon.Default.prototype._getIconUrl;
Icon.Default.mergeOptions({
  iconRetinaUrl: require("leaflet/dist/images/marker-icon-2x.png"),
  iconUrl: require("leaflet/dist/images/marker-icon.png"),
  shadowUrl: require("leaflet/dist/images/marker-shadow.png"),
});
export default {
  name: "Home",
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LCircle,
    LPolyline,
  },
  data() {
    return {
      url: "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
      attribution:
        '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      zoom: 15,
      center: [-3.716797488613226, -38.6056858424101],
      markerLatLng: [-3.716797488613226, -38.6056858424101],
      circle: {
        loc: [-3.716797488613226, -38.6056858424101],
        radius: 200,
      },
      markerLatLng2: [-3.7152562247098957, -38.596633219896994],
      circle2: {
        loc: [-3.715225100169137, -38.59662337039545],
        radius: 200,
      },
      markerLatLng3: [-3.717335866742238, -38.55753913173632],
      circle3: {
        loc: [-3.717335866742238, -38.55753913173632],
        radius: 200,
      },
      markerLatLng4: [-3.7337358290813283, -38.49590624241987],
      circle4: {
        loc: [-3.7337358290813283, -38.49590624241987],
        radius: 200,
      },
      markerLatLng5: [-5.150421298981283, -38.09977895587379],
      circle5: {
        loc: [-5.150421298981283, -38.09977895587379],
        radius: 200,
      },
      markerLatLng6: [-3.8950418782040304, -38.61957093452946],
      circle6: {
        loc: [-3.8950418782040304, -38.61957093452946],
        radius: 200,
      },
      markerLatLng7: [-3.722244431976655, -38.575140379102926],
      circle7: {
        loc: [-3.722244431976655, -38.575140379102926],
        radius: 200,
      },
      polygon: {
        latlngs: [
          [-3.716797488613226, -38.6056858424101],
          [-3.7152562247098957, -38.596633219896994],
          [-3.717335866742238, -38.55753913173632],
          [-3.7337358290813283, -38.49590624241987],
          [-5.150421298981283, -38.09977895587379],
          [-3.8950418782040304, -38.61957093452946],
          [-3.722244431976655, -38.575140379102926],
        ],
      },
    };
  },
};
</script>
