#react-native-radio-form
=================================================
react-native-radio-form is a simple Radio’s form, it’s a pure JS's component and it could used for the Android and iOS


##Installation
```bash
npm install react-native-radio-form --save
```
**Note**: The radio-form is based on ECMAScript6, if you use React Native < `v0.13`, maybe it don't run


##Usage
```javascript
import React, { Component } from 'react';
import { StyleSheet, View } from 'react-native';
import RadioForm from 'react-native-radio-form';
const mockData = [
    {
        label: 'label1',
        value: 'fi'
    },
    {
        label: 'label2',
        value: 'se'
    },
    {
        label: 'label3',
        value: 'th'
    }
];

export default class PRNRadioForm extends Component {

    _onSelect = ( item ) => {
      console.log(item);
    };

  render() {
    return (
      <View style={styles.container}>
        <View style={{ marginVertical: 10 }} >
          <RadioForm
              style={{ width: 350 - 30 }}
              dataSource={mockData}
              itemShowKey="label"
              itemRealKey="value"
              circleSize={16}
              initial={1}
              formHorizontal={true}
              labelHorizontal={true}
              onPress={(item) => this._onSelect(item)}
          />
        </View>
      </View>
    );
  }
}
```
##Properties
| Prop  | Default  | Type | Description |
| :------------ |:---------------:| :---------------:| :-----|
| style | - | `object` | Specify the style of the radio-form, eg. width, height...  |
| dataSource | - | `array` | Specify the display date of radio-form. `array` type value must match the specified format and it's required |
|itemShowKey | 'label' | `string` | The item's property what should display in the pages of `date`, `datetime` and `time` |
| itemRealKey | 'value' | `string` | Specify the display format of the date, which using [moment.js](http://momentjs.com/). The default value change according to the mode. |
| circleSize | 20 | `number` | Specify the text of confirm btn in ios. |
| initial | 0 | `number | string` | Specify the text of cancel btn in ios. |
| onPress | - | `function` | Specify the icon. Same as the `source` of Image, always using `require()` |
| formHorizontal | false | `boolean` |  |
| labelHorizontal | true | `boolean` | Restricts the range of possible date values. |
| outerColor | '#2f86d5' | `string` | Restricts the range of possible date values. |
| innerColor | '#2f86d5' | `string` | Restricts the range of possible date values. |


##Licence
(MIT)


