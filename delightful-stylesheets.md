# [fit] Delightful
# [fit] **Stylesheets**

---

# [fit] ''CSS is **hard**''
#### - me, many times
#### - also, the internet

^ no error reporting
^ browser compatibility
^ specificity

---

## ~~CSS is hard~~
### [fit] **but it doesn't have to be**

---

# **The Cascade**

### (it's a feature, not a 🐞)

^ CSS is doing exactly what it was meant to do
make the cascade work for you, don't fight against it

---

### **The cascade**
## **1.** Source Order
## **2.** Specificity
## **3.** Importance

---

### The cascade
## **1. Source Order**
## **2.** Specificity
## **3.** Importance


![fit right](images/source-order2.png)

^ elements within same file, but also the order in which files are included

---

### The cascade
## **1.** Source Order
## **2. Specificity**
## **3.** Importance

![fit right](images/specificity-order2.png)

^ certain selectors will override others

---

### The cascade
## **1.** Source Order
## **2. Specificity**
## **3.** Importance

![fit right](images/specificity2.png)

---

### The cascade
## **1.** Source Order
## **2.** Specificity
## **3. Importance**

![fit right](images/important.png)

^ if you do end up with the exact same specificity and importance,
source order wins out

---

![](images/nuclear.jpg)
# [fit] !important

^ overrides all source order and specifity
throws our our capability to write clean and predictable CSS
makes things super hard to change later
yes it makes things work, but it causes a lot more work to get around it in the future

---

### The cascade
## 1. **Source Order**
## 2. **Specificity**
## 3. **Importance**

^ so that's the cascase, the thing that makes css css
^ bad css happens when we ignore the cascade and the rules of css
^ this makes your codebase not predictable, scalable or maintainable
costs more to update, both in money and time and headaches

---

### _So what now?_
### **What can we do to save us from ourselves?**

![inline](images/what-to-do.gif)

^ so what now? What can we do to save us from ourselves?

---

# [fit] _Organization_ **&**
# [fit] Componentization

---
### **Organization with**
# ITCSS

### *by Harry Roberts*

---

# [fit] **Inverted**
# [fit] *Triangle*
# [fit] CSS

^ a way to organize your css so that the cascade works for you
ITCSS can be used with or without preprocessors and
is compatible with CSS methodologies like BEM, SMACSS or OOCSS.

---

# [fit] **Philosophy**
# [fit] NOT *A*
# [fit] *Framework*

^ no code to download, just simply a way of thinking differently

---

![inline](images/itcss-reach.png)

---

![inline](images/itcss-layers.png)

^ we break up the triangle in to separate layers

---

![fit left](images/itcss-layers.png)

## **Variables**

## contain fonts, colors, measurements, etc

^ only needed when using CSS preprocessors like SCSS or Less

---

![fit left](images/itcss-layers.png)

## **Tools**
## globally used mixins and functions

^ also optional - only needed when using preprocessors

---

![fit left](images/itcss-layers.png)

## **General**
## reset and/or normalize styles, box-sizing definition

^ This is the first layer which generates actual CSS

---

![fit left](images/itcss-layers.png)

## **Base Elements**
## styling for HTML elements
## ``` h1, a, p, input```

---

![fit left](images/itcss-layers.png)

## **Components**
## specific components unique to the design
## ```.panel, .form ```

^ this is where the majority of our work takes place

---

![fit left](images/itcss-layers.png)

## **Utilities**
## utilities and helper classes with ability to override
## ```.is--hidden```

^ the _only_ place where !important should exist

---

![inline](images/txi-example.png)

---

# [fit] **What does this buy us?**

---

# [fit] Reusabe & Scalable

---

# [fit] Reduce specificity

---

# [fit] Less waste, smaller files

---

![inline](images/delightful.gif)
# More **delightful**

---

# [fit] _Organization_ **&**
# [fit] Componentization

---

# [fit] discrete
# [fit] **self-contained**
# [fit] *reusable*

^ discrete, reusable components that are combined to build up different pieces of UI

---

![inline](images/mockup2.png)

---

## **Set up base styles first**
- fonts
- colors
- sizing & measurements
- layout

![fit right](images/mockup2.png)

---

![inline](images/variables-example.png)

---

![inline](images/typography-example.png)

---

![inline](images/layout-example.png)

---

![inline](images/components-step1.png)

---

**1. text components** </br>

- section header
- title & subtitle

</br>

**2. entry components**</br>

- entry
- image
- content
- featured entry

![fit right](images/mockup2.png)

---

![inline](images/text-components.png)

^ text components

---

![inline](images/components-step2.png)

^ what page looks like with text components applied

---

Next is the entry components

![inline](images/components-step3.png)

---

![inline](images/entry-components.png)

^ entry html
^ talk about BEM a little bit

---

![inline](images/entry-components-scss.png)

^ entry-scss
^ call out nesting - increases specificity

---

![inline](images/components-step4.png)

^ what page looks like with entry compoonents applied

---

# **Almost done!**

- Featured entry styling
- Responsiveness

![fit right](images/mockup2.png)

---

![inline](images/featured-entry-scss.png)

^ featured entry scss

---

![inline](images/fillmurray.gif)

^ gif of page showing featured & responsive

---

# [fit] _Organization_ **&**
# [fit] Componentization

---


![inline fit](images/footer-example.png)

^ less than 15 lines of css specific to the footer

---

![inline](images/footer-scss.png)

---

![inline](images/footer-haml.png)

---

![inline](images/footer-example.png)

---

![inline](images/cat-computer.gif)

---

# *Aly Fluckey*
## ![inline]() @**wtfluckey**
![right 100%](images/tablexi-logo.png)
