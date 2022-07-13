React version of login widget creates connection to Port app (using QR code, magnet link or simple copy-paste function).


## Installation

Just run:
```
npm install browser-link-for-port-apps-react-component
```

## Prerequirements

Create [dynamic link ](https://firebase.google.com/docs/dynamic-links/create-links) with one of four options on the Firebase platform. You don't need to create an entire dynamic link, only a dynamic_link URL is required. Other parameters are created by script in this repository.


## Implementation

1. Include library on the top of your file:

```
import {PortWidget} from "browser-link-for-port-apps-react-component";
```

2. Call the render script:

```html
function App() {
   var androidData = {"apn":"<apn>",
                      "afl":"<link_to_play_store>",
                  "version":"<min_sdk_version>"};

  var iosData = {"ibi":"<apple_store_id>",
                 "isi":"<link_to_app_store>",
                 "imv":<min_ios_version_integer>}

  var shortLinkURL = "<short_link>";
  var deepLinkURL = "<deep_link>";
 
  var linkOtherPlatforms = 'https://port.link/';

  var buttonXpressedFunc = () => {
        alert("Button X was pressed.");
    }

  return (
      <div>
        <PortWidget androidData={androidData}
                                iosData={iosData}
                                shortLinkURL={shortLinkURL}
                                deepLinkURL={deepLinkURL}
                                linkOtherPlatforms={linkOtherPlatforms}
                                config={config}
                                callbackFunction={buttonXpressedFunc}/>
      </div>
        );
}

```
## Acknowledgment 
QR window design inspired by [Anchor Link](https://github.com/greymass/anchor-link)

## License

[MIT](https://choosealicense.com/licenses/mit/)
