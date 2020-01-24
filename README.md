<div align="center">
<h1>  react-native-actions-sheet</h1>
</div>
<div
align="center"
style="width:100%;"
>
<img href="https://github.com/ammarahm-ed/react-native-actions-sheet/pulls" src="https://img.shields.io/badge/PRs-welcome-green"/>
<img href="https://www.npmjs.com/package/react-native-actions-sheet" src="https://img.shields.io/npm/v/react-native-actions-sheet?color=green"/>
<img href="https://www.npmjs.com/package/react-native-actions-sheet" src="https://img.shields.io/npm/dt/react-native-actions-sheet?color=green"/>
</div>
<p align="center">
A highly customizable cross platform ActionSheet for react native. 
</p>
<p align="center">
<img src="https://raw.githubusercontent.com/ammarahm-ed/react-native-actions-sheet/master/gifs/preview1.png"/>
</p>

<div align="center">
<h2>Screenshots</h2>
</div>

<img
width='44%'
height:600
src="https://github.com/ammarahm-ed/react-native-actions-sheet/blob/master/gifs/2020_01_12_14_16_30_trim.gif"
/><img
width='40%'
height:500
src="https://github.com/ammarahm-ed/react-native-actions-sheet/blob/master/gifs/screen-recording-1.gif"
/>

<div align="center">
<h2>Features</h2>
</div>
<p align="center">
 ❶ Native Animations & Performance  ❷ Cross Platform (iOS and Android)
 ❸ Identical Working on Android and iOS
❹ Gesture Control
 ❺  Raw ActionSheet - You can Add Anything
❻ Allow ActionSheet to be partially shown when opened
❽ Support TextInputs
 ❿ Cool bounce effect on open.
</p>
 
 

<div align="center">
<h2>Run Example</h2>
</div>
To run the example app clone the project

    git clone https://github.com/ammarahm-ed/react-native-actions-sheet.git

      

   then run ` yarn or npm install` in the example folder and finally to run the example app:
       
   
    react-native run-android

<div align="center">
<h2>Installation Guide</h2>
</div>

    npm install react-native-actions-sheet --save
or if you use yarn:

    yarn add react-native-actions-sheet

<div align="center">
<h2>Usage Example</h2>
</div>
For complete usage, see the example project.

```jsx
      
      <View
        style={{
          justifyContent: 'center',
          flex: 1,
        }}>
        <TouchableOpacity
          onPress={() => {
            actionSheet.setModalVisible();
          }}>
          <Text>
            Open ActionSheet
          </Text>
        </TouchableOpacity>

        <ActionSheet
          ref={ref => (actionSheet = ref)}
          children={YOUR CUSTOM COMPONENT INSIDE THE ACTIONSHEET}
        />
        
      </View>
    

```

<div align="center">
<h2>ActionSheet Props</h2>
</div>

|Name|Type|Description|Default Value|
|--|--|--|--|
|children|React.Component|Your custom component to render inside ActionSheet|`<View/>`
|containerStyle|object|Any custom styles you want to add to the container|
|CustomHeaderComponent|React.Component|Your custom header component, it will hide the indicator.|
|CustomFooterComponent|React.Component|A footer component if you want to add some info at the bottom. Always remember to **give footer a fixed height and provide the actionSheet the `footerHeight` prop with same value.** If you have added margins etc, add those values to `footerHeight` also. |
|footerStyle|object|A custom style to modify the footer|
|footerHeight|number|The height of the footer|80
|headerAlwaysVisible|object|Setting this to true keeps the header always visible, even when gestures are disabled|false
|footerAlwaysVisible|object|Should the footer always be visible? Currently when you overdraw, the footer appears, however you can change this by setting this to `true`.|false
|animated |boolean| Enable or disable animation of Modal|`true`
|openAnimationDuration |number| Duration of opening animation|`200`
|closeAnimationDuration |number| Duration of closing animation|`300`
|gestureEnabled|boolean| Enable gestures to control ActionSheet|`false`
|bounceOnOpen|boolean| Bounce the actionSheet on open|`false`
|bounciness|number| How much you want the view to bounce from the actual position on drag end.|`8`
|springOffset|number| When touch ends and user has not moved farther from the set springOffset, the ActionSheet will return to previous position. |`50`
|initialOffsetFromBottom|number|Use if you want to show the ActionSheet Partially on Opening. **Requires `gestureEnabled=true`**|`1`
|closeOnPressBack|boolean| BackHandler Controls the ActionSheet|`true`
|elevation|number| Elevation of ActionSheet|`0`
|indicatorColor|string| Color of gestureEnabled indicator|`gray`
|overlayColor|rgba string| Color of background Overlay.
|defaultOverlayOpacity| number 0 - 1| Opacity of background Overlay| `0.3`
|onClose|function| Function Called on Close
|onOpen|function| Function Called on Open

<div align="center">
<h2>ActionSheet Methods</h2>
</div>
ActionSheet can be opened or closed using its ref.
```jsx
// First create a ref on your <ActionSheet/> Component.

<ActionSheet
ref={ref => this.actionSheet = ref}
/>

// then later in your function to open the ActionSheet:

this.actionSheet.setModalVisible();



```
#

### MIT Licensed

