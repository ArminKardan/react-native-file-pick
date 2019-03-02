# react-native-file-pick

### Installation

```bash
npm i --save react-native-file-pick
react-native link react-native-file-pick
```


## Example
```javascript
import { DocumentPicker, DocumentPickerUtil } from 'react-native-file-pick';

// iPhone/Android
DocumentPicker.show({
      filetype: [DocumentPickerUtil.images()],
    },(error,res) => {
      // Android
      console.log(
         res.uri,
         res.type, // mime type
         res.fileName,
         res.fileSize
      );
    });

// iPad
const {pageX, pageY} = event.nativeEvent;

DocumentPicker.show({
  top: pageY,
  left: pageX,
  filetype: ['public.image'],
}, (error, url) => {
  alert(url);
});

```
