# map

In this project, we display a map on the map so that we can display the desired address graphically

## Usage
First, we need to enter the CDN and API address to connect

```javascript
<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyC1r0WGwV_MRE_l1hCBvxGhBg5C0fVmgzQ&callback=myMap"></script>
```


```javascript
function myMap() {
  var myCenter = new google.maps.LatLng(35.700145, 51.337115);
    var mapCanvas = document.getElementById("map");
    var mapOptions = {
      center: myCenter, 
      zoom: 15,
      // mapTypeId: google.maps.MapTypeId.HYBRID
      mapTypeId: google.maps.MapTypeId.ROADMAP
    }

  var map = new google.maps.Map(mapCanvas, mapOptions); 
  google.maps.event.addListener(map,'click',function() {click1();});
  
  
  var p1 = new google.maps.LatLng(35.800145, 51.437115);
  var marker = new google.maps.Marker({position: p1,  icon: { url: "1.png", scaledSize: new google.maps.Siz(50, 
50), 
  origin: new google.maps.Point(0,0), 
  anchor: new google.maps.Point(50, 50)}  });
      
  marker.setMap(map);
  
  var infoWindow = new google.maps.InfoWindow();
  google.maps.event.addListener(marker, 'click', function () {
      var markerContent = '<button> click </button> Majid Tejenjari <br><br> توضیحات دلخواه';
      infoWindow.setContent(markerContent);
      infoWindow.open(map, this);
  });
}
function click1(){
}
```


## Result

This project was written by Majid Tajanjari and the Aiolearn team, and we need your support!❤️

# نقشه

در این پروژه نقشه ای را روی نقشه نمایش می دهیم تا بتوانیم آدرس مورد نظر را به صورت گرافیکی نمایش دهیم

## نحوه استفاده
ابتدا باید آدرس CDN و API را برای اتصال وارد کنیم

```javascript
<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyC1r0WGwV_MRE_l1hCBvxGhBg5C0fVmgzQ&callback=myMap"></script>
```


```javascript
function myMap() {
  var myCenter = new google.maps.LatLng(35.700145, 51.337115);
    var mapCanvas = document.getElementById("map");
    var mapOptions = {
      center: myCenter, 
      zoom: 15,
      // mapTypeId: google.maps.MapTypeId.HYBRID
      mapTypeId: google.maps.MapTypeId.ROADMAP
    }

  var map = new google.maps.Map(mapCanvas, mapOptions); 
  google.maps.event.addListener(map,'click',function() {click1();});
  
  
  var p1 = new google.maps.LatLng(35.800145, 51.437115);
  var marker = new google.maps.Marker({position: p1,  icon: { url: "1.png", scaledSize: new google.maps.Siz(50, 
50), 
  origin: new google.maps.Point(0,0), 
  anchor: new google.maps.Point(50, 50)}  });
      
  marker.setMap(map);
  
  var infoWindow = new google.maps.InfoWindow();
  google.maps.event.addListener(marker, 'click', function () {
      var markerContent = '<button> click </button> Majid Tejenjari <br><br> توضیحات دلخواه';
      infoWindow.setContent(markerContent);
      infoWindow.open(map, this);
  });
}
function click1(){
}
```


## نتیجه

این پروژه توسط مجید تجن جاری و تیم Aiolearn نوشته شده است و ما به حمایت شما نیازمندیم!❤️