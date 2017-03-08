# [fit] Delightful
# [fit] **Stylesheets**

---

# [fit] CSS is **hard**

---

## **No error reporting**

^ by nature, css doesn't have a way to tell you when you've messed up

---

## **Browser Compatibility**

---

## **Specificity**

---

## ~~CSS is hard~~
### [fit] **but it doesn't have to be**

---

# The Cascade

^ You can't talk about specificity without first talking about the cascade.
The cascade is CSS's biggest strength but also its biggest complexity.
The cascade is the thing we end up debugging.

---

## **1. Source Order**
## **2.** Specificity
## **3.** Importance

---

![inline](images/cascade.png)

^ elements within same file, but also the order in which files are included

---

![inline](images/txi-file-order.png)

---

## **1.** Source Order
## **2. Specificity**
## **3.** Importance

^ certain selectors will override others

---

# [fit] **```IDs```**
# [fit] Classes
# [fit] *Elements*

---

![inline](images/specificity-order.png)

---

## **1.** Source Order
## **2.** Specificity
## **3. Importance**

---

![](images/nuclear.jpg)
# [fit] !important

^ !important throws our our capability to write clean and predictable CSS
it overrides all source order and specifity
yes it makes things work, but it causes a lot more work to get around it in the future
txi code audit example

---

![inline](images/source-order.png)

^ if you do end up with the exact same specificity and importance,
source order wins out

---

# **!important**
### overrides all specificity and source order
### decreases our ability to write clean & predictable CSS

^ makes things super hard to change later

---
# bootstrap
![inline](images/bootstrap-specificity.png)

---

![inline](images/bootstrap-spikes.png)

^ https://jonassebastianohlsson.com/specificity-graph/

^ if you include bootstrap first and add on, you're setting
yourself up for the specificity wars

---

![](images/geometry-wars.jpg)
# [fit] Specificity Wars

^ when your CSS codebase is not predictable, scalable or maintainable
costs more to update, both in money and time and headaches
talk about experience as a rails dev, spent most of my time battling spec. wars

---

![inline](images/mind-blown.gif)

---

# [fit] Organization **&**
# [fit] Componentization

---

# ITCSS

### *Harry Roberts*

---

# [fit] **Inverted**
# [fit] *Triangle*
# [fit] CSS

^ ITCSS stands for Inverted Triangle CSS and it helps 
you to organize your project CSS files in such way that 
you can better deal with (not always easy-to-deal with) CSS

^ 
ITCSS can be used with or without preprocessors and
is compatible with CSS methodologies like BEM, SMACSS or OOCSS.

---

# [fit] **Philosophy**
# [fit] NOT *A*
# [fit] *Framework*

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

![](images/group-happiness.jpg)
# [fit] More **delightful**

---

# [fit] Organization &
# [fit] **Componentization**

---

# [fit] discrete
# [fit] **self-contained**
# [fit] *reusable*

^ no longer building using the page model, but building discrete,
reusable components that are combined to build up different pieces of UI

---

![inline](images/wireframe.png)

---

![inline](images/wireframe-components.png)

---

![inline](images/variables-example.png)

---

![inline](images/typography-example.png)

---

![inline](images/layout-example.png)

---


![inline](images/components-step1.png)


---

![inline](images/components-step2.png)

---

![inline](images/text-components.png)

---

![inline](images/components-step3.png)

---

![inline](images/entry-components.png)

^ talk about BEM a little bit

---

![inline](images/components-step4.png)

---

![inline](images/entry-components-scss.png)

^ call out nesting - increases specificity

---

![inline](images/components-step5.png)

---

![inline](images/real-life.gif)

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

# [fit] Organization **&**
# [fit] Componentization

---

# *Aly Fluckey*
## ![inline]() @**wtfluckey**
![right 100%](images/tablexi-logo.png)
