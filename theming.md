---
layout: default
title: Theming
parent: Styling Modern Web Apps
nav_order: 3
---

# Theming

Material UI streamlines the theming process by allowing developers to define the primary and secondary colors of their theme as well as the geometric characteristics of components in a theme file. We will now proceed to define our theme colors as shown below:

## Define the Palette Colors & Border Radius
Start by defining the primary and secondary colors of your theme. The McMaster Digital Brand Standards specify that the primary color should be McMaster Heritage Maroon and the secondary color is McMaster Heritage Gold.

Modify `theme.ts` by adding the following code at the beginning of the `themeOptions` object:
```ts
palette: {  
	primary: {  
		main: "#7a003c"  
	},  
	secondary: {  
		main: "#fdbf57"  
	}  
},
```
In this code snippet, we are defining the primary and secondary colors of our website using the hex values that correspond to the McMaster Heritage Maroon and Heritage Gold colors.

Next, we will set the border radius in the theme to 28 inside `themeOptions`:
```ts
// setting the global border radius for all components
shape: {  
	borderRadius: 28,  
},
```
Note that the shape `borderRadius` sets the global value of the border radius for all MUI components, we will modify the border radius of individual components as needed in future sections of this workshop.

Your `theme.ts` file should now look like this:
```ts
// importing the Roboto and Roboto Condensed fonts from Google Fonts  
import {Roboto, Roboto_Condensed} from "next/font/google";  
  
// specifying the weights and styles of the Roboto font  
const roboto = Roboto({  
    weight: ['400', '900'],  
    style: ['normal', 'italic'],  
    subsets: ['latin'],  
    display: 'swap',  
})  
  
// specifying the weights and styles of the Roboto Condensed font  
const roboto_condensed = Roboto_Condensed({  
    weight: ['400', '700'],  
    style: ['normal', 'italic'],  
    subsets: ['latin'],  
    display: 'swap',  
})  
  
// declaring a custom typography variant  
declare module '@mui/material/Typography' {  
    interface TypographyPropsVariantOverrides {  
        settingTitle: true;  
    }  
}  
  
const themeOptions = {  
    // setting the typography variants  
    typography: {  
        h1: {  
            fontFamily: roboto_condensed.style.fontFamily,  
            fontSize: '50pt',  
            fontWeight: 400,  
        },  
        h2: {  
            fontFamily: roboto_condensed.style.fontFamily,  
            fontSize: '28pt',  
            fontWeight: 400,  
        },  
        h3: {  
            fontFamily: roboto_condensed.style.fontFamily,  
            fontSize: '20pt',  
            fontWeight: 400,  
        },  
        h4: {  
            fontFamily: roboto.style.fontFamily,  
            fontSize: '13pt',  
            fontWeight: 900,  
        },  
        button: {  
            fontFamily: roboto_condensed.style.fontFamily,  
            fontWeight: 700,  
        },  
        settingTitle: {  
            fontFamily: roboto_condensed.style.fontFamily,  
            fontSize: '15pt',  
        },  
    },  
    // setting the global border radius for all components  
    shape: {  
        borderRadius: 28,  
    },  
}  
  
export default themeOptions
```

Save this file and go back to your browser. Your SPA will be automatically updated to use the Heritage Maroon color in lieu of the default MUI blue color. The buttons and the file picker on the main page will now have rounder corners as well:

![color-index](assets/img/color-index.png)

Try navigating to the different pages on this website and notice how the Heritage Maroon color is applied to different components.
