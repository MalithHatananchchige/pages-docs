# Maps

Maps in Pages will only support Google maps. The premium plugin "Mapplic" will not be included in the angular package as it only supports jQuery. However you could still use it from the HTML version and import it to Angular package. 

{% hint style="warning" %}
Note that using jQuery will cause unwanted increase in package size and will be a bad practice for templating causing unwanted issues. 
{% endhint %}

{% embed url="https://github.com/ng2-ui/map" %}

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { NguiMapModule} from '@ngui/map';
@NgModule({
  imports: [NguiMapModule.forRoot({apiUrl: 'https://maps.google.com/maps/api/js?key=YOUR_KEY_HERE'}),...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<ngui-map  [zoom]="zoomLevel" [styles]="styles" [center]="center" [disableDefaultUI]="disableDefaultUI"></ngui-map>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
import { Component, OnInit } from '@angular/core';
import { pagesToggleService } from '../../@pages/services/toggler.service'
import { Subscriber } from 'rxjs/Subscriber'

@Component({
  selector: 'google-map-page',
  templateUrl: './google.component.html',
  styleUrls: ['./google.component.scss']
})
export class GoogleMapPage implements OnInit {
  zoomLevel = 11;
  center  = {lat: 40.6700, lng: -73.9400};
  disableDefaultUI = true;
  styles = [{
    featureType: 'water',
    elementType: 'all',
        stylers: [{
            hue: '#e9ebed'
        }, {
            saturation: -78
        }, {
            lightness: 67
        }, {
            visibility: 'simplified'
        }]
    }, {
        featureType: 'landscape',
        elementType: 'all',
        stylers: [{
            hue: '#ffffff'
        }, {
            saturation: -100
        }, {
            lightness: 100
        }, {
            visibility: 'simplified'
        }]
    }, {
        featureType: 'road',
        elementType: 'geometry',
        stylers: [{
            hue: '#bbc0c4'
        }, {
            saturation: -93
        }, {
            lightness: 31
        }, {
            visibility: 'simplified'
        }]
    }, {
        featureType: 'poi',
        elementType: 'all',
        stylers: [{
            hue: '#ffffff'
        }, {
            saturation: -100
        }, {
            lightness: 100
        }, {
            visibility: 'off'
        }]
    }, {
        featureType: 'road.local',
        elementType: 'geometry',
        stylers: [{
            hue: '#e9ebed'
        }, {
            saturation: -90
        }, {
            lightness: -8
        }, {
            visibility: 'simplified'
        }]
    }, {
        featureType: 'transit',
        elementType: 'all',
        stylers: [{
            hue: '#e9ebed'
        }, {
            saturation: 10
        }, {
            lightness: 69
        }, {
            visibility: 'on'
        }]
    }, {
        featureType: 'administrative.locality',
        elementType: 'all',
        stylers: [{
            hue: '#2c2e33'
        }, {
            saturation: 7
        }, {
            lightness: 19
        }, {
            visibility: 'on'
        }]
    }, {
        featureType: 'road',
        elementType: 'labels',
        stylers: [{
            hue: '#bbc0c4'
        }, {
            saturation: -93
        }, {
            lightness: 31
        }, {
            visibility: 'on'
        }]
    }, {
        featureType: 'road.arterial',
        elementType: 'labels',
        stylers: [{
            hue: '#bbc0c4'
        }, {
            saturation: -93
        }, {
            lightness: -2
        }, {
            visibility: 'simplified'
        }]
    }];
  
  constructor(private toggler:pagesToggleService) { }

  ngOnInit() {
    this.toggler.setBodyLayoutClass("no-header");
    this.toggler.toggleFooter(false);
    this.toggler.setPageContainer("full-height");
    this.toggler.setContent("full-width full-height overlay-footer");
    this.toggler.setHeaderClass("transparent");
  }

  zoomIn(){
      this.zoomLevel++;
  }

  zoomOut(){
    this.zoomLevel--;
  }

}
```
{% endtab %}
{% endtabs %}

