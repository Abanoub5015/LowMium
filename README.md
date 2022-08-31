
## LowMium E-commerce Online Shopping By Abanoub Magdy

### LowMium E-commerce Online Shopping made by (Flutter) for (Web, Android, iOS). Along with some styling.
* In total 10 screens,
* 7 models,
* 7 states(GetxController(to get data such as Services_Component(angular))),
* 5 firebase-references,
* 3 view_models-wz-imp(to Implement functions),
* 6 widgets (to make the project more organizable) and some (string, utils files (to define texts in the app))

# About The Project
## [Demo]
| [![]()]() | [![]()]() |
|:---:|:---:|
| [0]*Home*   | [1]*Menu* |
| [![screenShot_LowMium](https://i.ibb.co/6yxvfMX/image.png)](https://lowmium.ml/) |[![screenShot_LowMium](https://i.ibb.co/MpshPmh/image.png)](https://lowmium.ml/)
| *2.Cart [2.1.Place Order Screen]*  | *2.2.GoogleMap (Map Pick-location)* |
| [![screenShot_LowMium](https://i.ibb.co/02NwcWz/image.png)](https://lowmium.ml/) |[![screenShot_LowMium](https://i.ibb.co/k01KPxN/image.png)](https://lowmium.ml/)



# 👉🏻[Here's the website [lowmium.ml]](https://lowmium.ml/)

## [Screens]

* [0]*Home*
  * 0.1.MostPopularWidget
  * 0.2.BestDealsWidget

* [1]*Menu*
  * 1.*Categories*
    * 1.1.list Screen
    * 1.2.detail Screen

  * 2.*Cart*
    * *2.1.Place Order Screen*
        * *2.2.GoogleMap*

  * 3.*Order History*
    * *3.1.Order History view detail Screen*

  * 4.*Login*



## [Roadmap]

#### [*Categories*]
- [ ]  1.add [Categories] to [Home-screen]

----
#### [*Home*]
- [ ]  1.Make [app] looks like a (modern & cool website)
- [ ]  2.add [login-btn & profile-pic] to [Home-screen] beside [cart-btn in the top right corner]

----
#### [*Order History*]
- [ ]  1.add [tracking order[state of order]] (order tracking process [1.order placed - 2.shipping - 3.delivered] )
- [ ]  2.fix [order-total(color)] => [3.1.Order History view detail Screen]

----
 #### [*Cart*]
- [ ]  1.add fav btn to [Cart] (to make it easy for user to fetch any item when placing an order)
----




## [Built With]
 [for 👉🏼(e.g.)]
* [google_fonts] [for 👉🏼GoogleFonts.jetBrainsMono(color: Colors.white,fontSize: 18),)]
* [cached_network_image] [for 👉🏼CachedNetworkImage(imageUrl: widget.cartStateController.getCart()[index].image,fit: BoxFit.fill,errorWidget: (context, url, err) => Center(child: Icon(Icons.image),),]
* [firebase_core] [for 👉🏼(FirebaseApp app = await Firebase.initializeApp();)]
* [firebase_database] [for 👉🏼(var source = await FirebaseDatabase.instance.ref().child('Restaurant').child('restauranta').child(BEST_DEAL_REF).orderByKey().once();)]
* [get] [for 👉🏼( final cartStateController = Get.put(CartStateController()); | return GetMaterialApp( ... ))]
* [auto_animated] [for 👉🏼[LiveList( ... ]]
* [carousel_slider] [for 👉🏼( return CarouselSlider(items: lstBestDeal.map((e) => Builder(builder: (BuildContext context) { )]
* [flutter_zoom_drawer] [for 👉🏼( style: DrawerStyle.defaultStyle,///styles )]
* [flutter_elegant_number_button] [for 👉🏼( Center(child: ElegantNumberButton(initialValue: widget.cartStateController.getCart()[index].quantity, )]
* [flutter_rating_bar] [for 👉🏼(  RatingBar.builder(initialRating: 5, minRating: 1, direction: Axis.horizontal, allowHalfRating: false, )]
* [badges] [for 👉🏼(Badge( ... ) |  position: BadgePosition(top: -1,end: -2), |  animationType: BadgeAnimationType.scale, )]
* [get_storage] [for 👉🏼(  await GetStorage.init(); //for cart_state (to read cart-list-data in the box) |final box = GetStorage(); )]


* [intl] [for 👉🏼(NumberFormat numberFormat = NumberFormat("#,##0", "en_US"); //thousand separators [1000000 => 1000,000] )]
* [flutter_slidable] [for 👉🏼( child:SlidableAutoCloseBehavior( //to close(the previous one) when another [Slidable] widget with the same [groupTag] opens. |  ,itemBuilder: (context,index)=> Slidable()]


* [firebase_auth] [for 👉🏼( if(FirebaseAuth.instance.currentUser != null) { )]
* [flutter_auth_ui] [for 👉🏼( FlutterAuthUi.startUi( items: [ AuthUiProvider.phone, )]


* [//firedart] [for 👉🏼(for desktop app )]
* [//http] [for 👉🏼(for desktop app )]

* [form_validator] [for 👉🏼(TextFormField( controller: widget.NameController, validator: ValidationBuilder(requiredMessage: '$NameText $isRequiredText',).required().build(), )]

* ### [place_order_screen]
  #### 1.get user current location(lat & lang)
  * [geolocator] [for 👉🏼(await Geolocator.isLocationServiceEnabled(); | LocationPermission permission; | Future<Position> _determinePosition() async {)]
  #### 2.and this get the address of user (name of address)
  * [geocoding] [for 👉🏼( List<geocoding.Location> locationFromAddress = []; |  List<geocoding.Placemark> placeMark = await geocoding.placemarkFromCoordinates(position.latitude, position.longitude); |  geocoding.Placemark place = placeMark[1]; )]

  #### 3.(flutter-toast) for permission if its deniedForever => openAppSettings
  * [fluttertoast] [for 👉🏼(Fluttertoast.showToast(msg: deniedForeverMessageTitle, )]

  #### 4.Test if location services are enabled.
  * [location] [for 👉🏼(locator.Location location = new locator.Location();)]

  #### 5.select location from maps
  * [map_pin_picker] [for 👉🏼(MapPickerController mapPickerController = new MapPickerController(); |  MapPicker( showDot: true, showDotcolor: )]

  #### 6.(CameraPosition(target: LatLng(0, 0)) and (cameraPosition.target.latitude... so on) //ANDROID IOS
  * [google_maps_flutter] [for 👉🏼( GoogleMap( MinMaxZoomPreference(6,20), GoogleMapController controller) ... ) | Completer<GoogleMapController> _controller = Completer(); |   MapType _defaultMapType = MapType.normal; |  _mapController.animateCamera(CameraUpdate.newCameraPosition(CameraPosition(target: LatLng(lat, long), zoom: 19,),),); )]
---

* [msix] [for 👉🏼(to create .msiX (setup file of app))]



* ## [installation]
```
0.check [environment-variables]
0.flutter doctor
0.flutter --version 
0.flutter --v

1.flutter upgrade
  2.additional run args --no-sound-null-safety [map_pin_picker cuz it deprecated now]
  2.flutter run --no-sound-null-safety

*.flutter clean

last-thing... u must update(map_pin_picker.dart) in flutterSDK [D:\aFlutterSDK\flutter\.pub-cache\hosted\pub.dartlang.org\map_pin_picker-0.0.1\lib\map_pin_picker.dart]
🌟🌠imp - dependency(package)🌠🌟 => u will find updated(map_pin_picker.dart)
```


* ## 1.git Commands [// means once]
```
//git init
//git add README.md
  git add *
  [
  fatal: unsafe repository ('D:/Apps/lowmium' is owned by someone else) To add an exception for this directory, call:

        git config --global --add safe.directory D:/Apps/lowmium

  ]
  git commit -m "publish project"
//git branch -m main
//git remote add origin https://github.com/Abanoub5015/LowMium.github.io
  git push origin main
git pull origin main
```

* ## 2.git (deploy-page) Commands
```
[1] flutter build web => then [drag & drop this web-folder to github(in gh-page)]
```


* ## 3.after every update:
```
-----------------------------
git add *
git commit -m "update commit"
git push origin main

flutter build web => then [drag & drop this web-folder to github(in gh-page)]
-----------------------------
```


[google_fonts]: https://pub.dev/packages/google_fonts
[cached_network_image]: https://pub.dev/packages/cached_network_image
[firebase_core]: https://pub.dev/packages/firebase_core
[firebase_database]: https://pub.dev/packages/firebase_database

[get]: https://pub.dev/packages/get
[auto_animated]: https://pub.dev/packages/auto_animated
[carousel_slider]: https://pub.dev/packages/carousel_slider
[flutter_zoom_drawer]: https://pub.dev/packages/flutter_zoom_drawer
[flutter_elegant_number_button]: https://pub.dev/packages/flutter_elegant_number_button
[flutter_rating_bar]: https://pub.dev/packages/flutter_rating_bar
[badges]: https://pub.dev/packages/badges
[get_storage]: https://pub.dev/packages/get_storage


[intl]: https://pub.dev/packages/intl
[flutter_slidable]: https://pub.dev/packages/flutter_slidable


[firebase_auth]: https://pub.dev/packages/firebase_auth
[flutter_auth_ui]: https://pub.dev/packages/flutter_auth_ui

[//firedart]: https://pub.dev/packages/firedart
[//http]: https://pub.dev/packages/http

[form_validator]: https://pub.dev/packages/form_validator

[geolocator]: https://pub.dev/packages/geolocator
[geocoding]: https://pub.dev/packages/geocoding


[fluttertoast]: https://pub.dev/packages/fluttertoast
[location]: https://pub.dev/packages/location
[map_pin_picker]: https://pub.dev/packages/map_pin_picker
[google_maps_flutter]: https://pub.dev/packages/google_maps_flutter

[msix]: https://pub.dev/packages/msix
