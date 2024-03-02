#guide #example 

###### Package
```sh
yarn add @eva-design/eva @ui-kitten/components @ui-kitten/eva-icons
yarn expo install react-native-svg
```
>If you use Expo, you should use `expo install react-native-svg@9.13.6` to install svg package.

###### Generate Eva Design
https://colors.eva.design/
https://akveo.github.io/eva-icons/
Export as json
Drop it to project

###### Apps
```tsx
import { default as myMapping } from "./src/constant/mapping.json";
...

export default () => {  
  return (  
    <SafeAreaProvider>
	  <ApplicationProvider {...eva} theme={theme === "light"  
	  ? { ...eva.light, ...customTheme, ...lightTheme }  
	  : { ...eva.dark, ...customTheme, ...darkTheme }} 
	  customMapping={myMapping}>  
        <AppContainer />  
      </ApplicationProvider>  
    </SafeAreaProvider>  
  );  
}
```


###### Custom Fonts
`yarn add expo-font`
```tsx
import * as Font from 'expo-font';

export const loadFonts = async () => {
  await Font.loadAsync({
    // Specify the name and path of your custom font files
    'CustomFont-Regular': require('./assets/fonts/CustomFont-Regular.ttf'),
    'CustomFont-Bold': require('./assets/fonts/CustomFont-Bold.ttf'),
  });
};

```

>app.tsx
```tsx
import {loadFonts} from "./src/assets/ExpoFonts";

export default () => {  
  const [fontsLoaded, setFontsLoaded] = useState(false);  
  
  useEffect(() => {  
    const loadApp = async () => {  
      await loadFonts();  
      setFontsLoaded(true);  
    };    loadApp().then();  
  }, []);  
  
  if (!fontsLoaded) {  
    // Return a loading state or placeholder while fonts are being loaded  
    return null;  
  }  
  
  return (...)
}
```