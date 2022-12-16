# **Refactoring-site**

## Technology Used

| Technology Used         | Resource URL                                        |


| HTML                    | [https://developer.mozilla.org/en-US/docs/Web/HTML] |

| CSS                     | [https://developer.mozilla.org/en-US/docs/Web/CSS]  |   

| Git                     | [https://git-scm.com/]                              |    

## Description

This is a challenge to html and CSS refactoring for week 1. Students are instructed to refactor codes in html and CSS without any changes to the appearance of the website page.

My strategy is to try to use least lines of code for this challenge by using class selectors and ids. Many elements in the challenge are having the same CSS properties and values, thus I could group them into a single class to simplify the code and more clear to the viewer.

## Instruction

The URL below is for accessing the final result for this project.
> Deployed Link https://byxzesc.github.io/refactor-site/

## Code Refactor Example

```html
<div id="search-engine-optimization" class="search-engine-optimization">
    <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
    <!-- add content title class to h2 -->
    <h2 class="content-title">Search Engine Optimization</h2>
    <p>
        The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
    </p>
</div>
<div id="online-reputation-management" class="online-reputation-management">
    <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
    <h2 class="content-title">Online Reputation Management</h2>
    <p>
        The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
    </p>
</div>
<div id="social-media-marketing" class="social-media-marketing">
    <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
    <h2 class="content-title">Social Media Marketing</h2>
    <p>
        Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
    </p>
</div>
```

Grouping the above non-semantic div elements with the class name of 'content-items' for easier targeting when applying CSS properties to them.

```html
<div id="search-engine-optimization" class="content-items">
    <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
    <!-- add content title class to h2 -->
    <h2 class="content-title">Search Engine Optimization</h2>
    <p>
        The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
    </p>
</div>
<div id="online-reputation-management" class="content-items">
    <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
    <h2 class="content-title">Online Reputation Management</h2>
    <p>
        The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
    </p>
</div>
<div id="social-media-marketing" class="content-items">
    <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
    <h2 class="content-title">Social Media Marketing</h2>
    <p>
        Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
    </p>
</div>

```

This change factoring out repetitive CSS code to similar contents:

```css
.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
    color: #ffffff;
}

.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
    color: #ffffff;
}

.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
    color: #ffffff;
}
```

No longer targeting each element on the page with their own class but instead the css selector targeting the 'content-items' element that they all share.

```css
.content-items {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
    color: #ffffff;
}

```

## Credits

Brian Zhao [GitHub] https://github.com/byxzESC


---

© 2022 https://github.com/byxzESC. All Rights Reserved.
