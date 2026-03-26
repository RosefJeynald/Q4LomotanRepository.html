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

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
- Answer: The rectangle containing the text "Sidebar" moved depending on the amount of px added in the values of top and left. When position: relative was removed in the   CSS, the rectangle moved in its original state.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- Answer: When the page is scrolled, the footer is fixed to the page and stays in the same position the entire time. It behaves differently because position fixed fixes the object to the page, while position relative makes the object have a position relative to the page.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- Answer: It positions the object relative to the nearest element with a position css on it. It is different since it locks on to another element.

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
- Answer: It appears on top of the content since it is positioned relative to it and the values of top and left allow it to be positioned on where it's at. When the z-index is swapped, the notice box goes behind the content box.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    - Answer: The left: 400px will have to be changed into left" 430px.
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    - Answer: When the position of .content was changed to relative, it moved relative to the page. When it changed to fixed, it returned to it's place near the sidebar.
    * What do you observe on about the effect of z-index on .notice and .content boxes?
    - Answer: It moves the position of the boxes back or forward, where the higher z-index gets to be on top of the lower z-index box.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 
    - Answer: Static – Follows normal page flow. 
              Relative – Moves relative to its original spot. 
              Absolute – Positioned based on nearest positioned parent.
              Fixed – Stays in the same spot on the screen. (even when scrolling)

    b. How does absolute positioning depend on its parent element?
    - Answer: It uses the nearest parent's position as it's reference, then moves off that.

    c. How do you differentiate sticky from fixed (you can research on sticky)?
    - Answer: Sticky acts normal, then sticks to the page when you scroll to a certain point. Fixed always stays at the same position even when scrolling.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
    - Answer: Using fixed for a top navigation bar so it's always visible, same with the footer. Not only that, I can use relative to alter the positioning of images and text better and for the design to be more eye catching and appealing to the viewer.