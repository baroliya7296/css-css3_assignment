Q-3. Describe how viewport settings affect mobile displays.

ans:-

1. Scaling of Content
   - The viewport is developers to control the scaling of content on smaller screens.

     ```html
     <meta name="viewport" content="width=device-width, initial-scale=1">
``
      This ensures that the width of the viewport matches the device’s screen width, meaning the page will adjust to fit the screen.
`
     This ensures that the page is initially scaled at 100%, meaning no zooming in or out when the page loads.

 2. **Zoom Control**
   
     ```html
     <meta name="viewport" content="width=device-width,">
     ```
   
   Disabling zoom might cause accessibility issues, as users with visual impairments might find it difficult to interact with the page.
 3. **Content Screen Size**

   - Viewport settings help ensure that content adapts to different screen sizes. Without these settings, elements could appear too large or too small, requiring horizontal scrolling or awkward zooming.

 4. **Horizontal Scrolling**

   - If the content’s width exceeds the viewport, users would have to scroll horizontally, which is generally undesirable on mobile devices. 

5. **Font and Text Sizing**

   - Mobile browsers may adjust the text size to make it more readable by default. However, you can control this using viewport settings in combination with responsive CSS to ensure that text sizes scale across devices.