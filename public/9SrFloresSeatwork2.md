# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.


### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
*Compared to the default static positioning, the position of the sidebar changed slightly depending on the values and the direction of the css given. Static positioning follows the natural flow of the page*

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
*When you scroll the page, the footer just stays in the same position at the bottom of the page and would still be visible in the viewport despite scrolling up or down. The footer behaves differently from position relative because its position is fixed.*

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
*The effect of position: absolute on an element is that it changes the position of the element to a position that is relative to its nearest positioned ancestor. It is different from fixed because a fixed positioned element would stay visible on the screen even after scrolling, while an absolute positioned element would move with the page content as you scroll and disappear from viewport.*

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
*The notice appears on top of the content because it is a higher z-index than the content. An element with higher z-index will cover an element with a lower z-index. If we swap their z-index values, the content will cover the notice.*

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    ```css
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
      position: absolute; top: 66px; left: 200px;
      z-index: 1;
    
    }
    .notice {
    position: absolute; top: 66px; left: 430px;
    background: orange;
    padding: 10px;
    z-index: 2;

    }
    ```
    ```html
    </html>
      </head>
        <body>
          <div class="header">Header</div>
          <div class="sidebar">Sidebar</div>
          <div class="content">Main Content</div>
          <div class="footer">Footer</div>
          <div class="notice">Notice!</div>
        </body>
    </html>
    ```
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    *When the position of .contect is changed to relative while keeping the top and left values, .content is placed to its original position but is moved 66px down and 200px to the right. On the other hand, when changed to fixed, it is placed at the same position as it was when the position was set to absolute. However, since the position is fixed, .content will always stay on the viewport in the same position.*

    * What do you observe on about the effect of z-index on .notice and .content boxes?
    *The z-index layers the elements to each other. Element with a higher z-index will be placed on top of the one with a lower z-index.*

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)?
    *Static position places the element on its default position, ignoring other properties. Relative position places the element relative to its original position. Absolute position places the element relative to its nearest positioned ancestor. Fixed position places the element relative to the screen and stays in the same spot even when scrolling.*

    b. How does absolute positioning depend on its parent element?
    *Absolute positioning uses the parent element as an anchor instead of the whole browser viewport.*

    c. How do you differentiate sticky from fixed (you can research on sticky)?
    *When an element is in fixed positioning, it stays in its same position on the viewport at all times even when scrolling. When an element is in sticky positioning, it behaves like relative positioning or scrolls normally until it reaches a specific scroll position, and that's when it will behave like fixed positioning, but only within its parent container.*

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
    *Applying positioning for a webpage would be very helpful in making the page look organize, neat, and easy to follow. For example, sticky positioning can be applied on the header of a long webpage that would serve as a navigation menu. Another example is using absolute positioning in overlaying text or icons as labels on an image or video without affect the rest of the layout.*
