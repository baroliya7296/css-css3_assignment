Q-2Explain the role of media queries in responsive design.

ans:-

 1. Conditional CSS Application

 This means you can write different CSS rules that only apply if certain criteria are met, allowing the design to adjust according to the device's characteristics.

   Example:
   ```css

   body {
       font-size: 16px;
   }
   @media screen and (max-width: 600px) {
       body {
           font-size: 14px;
       }
   }

   @media screen and (min-width: 1200px) {
       body {
           font-size: 18px;
       }
   }
   ```

2. Adapting to Different Viewport Sizes
   One of the most common uses of media queries is to adjust the layout of a web page based on the width of the viewport. For example, a multi-column layout may work well on a large screen but may need to switch to a single column on a small mobile screen.

   Example:
   ```css

   .container {
       display: grid;
       grid-template-columns: 1fr 1fr;
   }

   @media screen and (max-width: 768px) {
       .container {
           grid-template-columns: 1fr;
       }
   }


3. Targeting Specific Device Features
   Media queries can also target specific device features, such as screen resolution (density), orientation (portrait or landscape), and even color depth or screen contrast. This helps tailor the design for devices with different display capabilities.

   Example:
   ```css
   
   @media screen and (min-200px) {
       .logo {
           background-image: url('logo@2x.png');
       }
   }

   @media screen and (orientation) {
       .container {
           flex-direction: row;
       }
   }


5. Grids and Layouts
   Media queries can be used to modify grid systems and layouts at different breakpoints. This ensures that elements like columns, images, and other content adapt to fit the width of the screen device.

   Example:
   ```css

   .grid {
       display: grid;
       grid-template-columns: 1fr 1fr 1fr;
   }

   @media screen and (max-width: 768px) {
       .grid {
           grid-template-columns: 1fr;
       }
   }
