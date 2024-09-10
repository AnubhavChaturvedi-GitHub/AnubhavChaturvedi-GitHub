# Day 2: **Learning CSS Basics**

Welcome to **Day 2** of my **100 Days of Full-Stack Development** challenge. Today, I started exploring CSS (Cascading Style Sheets) and its role in enhancing the appearance and layout of web pages. Below is a summary of what I learned and the resources I used. 

## 📘 **Resources Used**:
- **Tutorials Point CSS PDF**: [Download/View PDF](https://github.com/AnubhavChaturvedi-GitHub/AnubhavChaturvedi-GitHub/blob/main/Full-Stack%20100%20Days/Day%202/css_tutorial.pdf)
- **CSS Cheat Sheet**: [Download/View CheatSheet](https://github.com/AnubhavChaturvedi-GitHub/AnubhavChaturvedi-GitHub/blob/main/Full-Stack%20100%20Days/Day%202/css-cheatsheet.pdf)
- **W3Schools CSS Tutorial**: [Explore W3Schools](https://www.w3schools.com/html/html_css.asp)

---

## 🧠 **Concepts Learned**:

### 1️⃣ **Ways to Add CSS**:
CSS can be applied to HTML documents in **three different ways**:
- **Inline CSS**: Using the `style` attribute directly inside HTML elements.
- **Internal CSS**: Using the `<style>` tag within the `<head>` section of your HTML.
- **External CSS**: Linking an external CSS file using the `<link>` element.

```html
<!-- Inline CSS Example -->
<p style="color:blue;">This is a blue paragraph.</p>

<!-- Internal CSS Example -->
<head>
  <style>
    p { color: red; }
  </style>
</head>

<!-- External CSS Example -->
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

### 2️⃣ **CSS Properties Explored**:

- **Colors**: You can set text color using the `color` property.
- **Fonts**: Define font styles with the `font-family` property.
- **Sizes**: Control text size using the `font-size` property.

```css
/* Color Example */
p { color: #606c38; }

/* Font Example */
h1 { font-family: 'Arial', sans-serif; }

/* Font Size Example */
p { font-size: 16px; }
```

### 3️⃣ **Borders, Padding, and Margins**:

- **Border**: You can add borders around elements using the `border` property.
- **Border Radius**: Use `border-radius` to create rounded borders.
- **Padding**: Defines space between the content and the border.
- **Margin**: Defines space around an element (outside the border).

```css
/* Border Example */
div { border: 2px solid black; }

/* Border Radius Example */
div { border-radius: 10px; }

/* Padding Example */
div { padding: 20px; }

/* Margin Example */
div { margin: 15px; }
```

### 4️⃣ **Links (href) and Images (src)**:
You can style links and images using CSS properties like `color`, `text-decoration`, and dimensions like `width` and `height`.

```html
<!-- Hyperlink with styled color -->
<a href="https://example.com" style="color: #dda15e;">Visit Example</a>

<!-- Image with defined width and height -->
<img src="image.jpg" style="width: 100px; height: auto;">
```

### 5️⃣ **CSS Backgrounds**:
CSS allows customization of backgrounds with properties like `background-color`, `background-image`, and `background-size`.

```css
/* Background Color */
body { background-color: #fefae0; }

/* Background Image */
body { background-image: url('background.jpg'); background-size: cover; }
```

### 6️⃣ **Transparency and Opacity**:
CSS provides properties like `opacity` and `rgba` to control transparency.

- **Opacity**: Defines the transparency of an element.
- **RGBA**: Allows setting color with transparency (alpha value).

```css
/* Opacity Example */
div { opacity: 0.8; }

/* RGBA Example */
p { color: rgba(255, 0, 0, 0.5); }
```

### 7️⃣ **Images**:
Visualizing the effects of transparency and backgrounds can be tricky, but here’s a glimpse of what I explored:

- **Transparency using RGBA**:
![image](https://github.com/user-attachments/assets/02f958ac-3a15-4fb0-b82a-a1800f730272)

- **CSS Backgrounds**:
![image](https://github.com/user-attachments/assets/92f41a63-b44e-454e-a13c-370043fbcc1f)

---

## ✍️ **Next Steps**:
I will dive in to Develop projects 
---

## 🛠 **Tools**:
- **Editor**: Visual Studio Code
- **Browser**: Chrome Developer Tools

# Project 1 :- Login paga only using HTML + CSS



