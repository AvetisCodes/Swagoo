# Swagoo
Mobile-First Responsive Design Framework With Pure CSS & Funky Swag.

## Setup Instructions

### #1

You need to download Swagoo. In order to do that please go to the GitHub page and click on the Clone or Download green button at the top right corner.

If you don't know how to use GIT then go ahead and click Download ZIP button. Otherwise if you have GIT setup and know how to use it - go ahead and run the following command to clone the remote repository down to your local drive.

`git clone https://github.com/AvetisG/Swagoo.git`
    
### #2

Now you need to build the Framework to produce the CSS file which you can include in your project.

There are many SASS compilers out there but our recoemmendaiton is to download/install Visual Studio Code and then go ahead and download an extension for Visual Studio Code called Live Sass Compiler.

Once everything is setup all you would need to do is open up Swagoo, navigate to scss folder and open swagoo-theme.scss.

Once the file is open, go ahead and click on Watch Sass button at the bottom of Visual Studio Code editor. This will compile the SCSS into CSS file.

Once you have swagoo-theme.css you can go ahead and include that in your project as follows (below code is assuming you have placed swagoo-theme.css in a folder called css):

`<link rel="stylesheet" type=text/css href="./css/swagoo-theme.css">`
    
### #3

Now that you have all of the files setup and included we can learn how to customize the styles to match your needs.

Recommended way is to create a sass file called site.sass (you can call it anything you want, our default name is site.sass).

The rest is simple. All you need to do is re-declare existing variables from the list below and assign a new value to them.

Once all of your variables have been declared go ahead and import swagoo-theme.scss at the very bottom.

You can look at the code below to help you get an idea.

```
$swagoo-seed-color: rgb(144, 13, 245) !default;

@import "../scss/swagoo-theme.scss";
```

Below are all of the available variables which you can override:

| Variable Name   |      Description      |
|----------|:-------------:|
| $tablet-size: 767px !default; | You can override the media query breakpoint for tablet devices. |
| $desktop-size: 1000px !default; | You can override the media query breakpoint for desktop devices. |
| $large-device-font-size: 1.414 !default; | Current Typography scale for large devices (desktop, laptop) is set to Augmented Fourth but you can change the value. |
| $small-device-font-size: 1.250 !default; | Current Typography scale for small devices (tablet, mobile) is set to Major Third but you can change the value. |
| $root-element-font-size: 16px !default; | This is the root element font-size which you can override as well. In the mobile media query the font-size is automatically calculated to be equal to 80% of the $root-element-font-size. |
| $serif-font-file: url([path towards font]) !default; | You can replace the current serif font using the following variable. |
| $sans-serif-file: url([path towards font]) !default; | You can replace the current sans-serif font using the following variable. |
| $swagoo-seed-color: hsla(211, 100%, 50%, 1) !default; | You can override the theme seed color which will recalculate all of the primary, complementary and analogous colors. |
