# Content: 

## CSS

>> CHAPTER 16 : 

>> * Controlling size of images in CSS
>> * Aligning images in CSS
>> * Adding background images


>> CHAPTER 19 : 

>> * Search engine optimization
>> * Using analytics to understand visitors
>> * Putting your site on the web


<br>
<br>
<hr>
<br>
<br>


### CHAPTER 16

<br>
<br>

+ **Controlling size of images in CSS**

![Image-property!](https://bitsofco.de/content/images/2016/06/repeat.png)


You can change the size of an image using **Width** & **Height** properties.

>> Why specifying the image size is important?

>>> The HTML and CSS code are often load before the images do and tell the browser how much space to leave for the image.


<br>
<br>

+ **Aligning images in CSS**


We can align images next to each other using the ``float`` attribute: 

```
align-left {
    float: left;
}

alighn-right {
    float: right;
}
```
>> Centering images using CSS : 

>>> By default, images are inline elements, in order to center an image we should turn int to be a block-level element then we apply the style on it : 

```
<p><img src=""  alt="" class="align-center></p>

<style>

img.align-center { 
    text-alight: center;
    }


img.align-center {
display: block;
margin: 0px auto;
} 

</style>

```


<br>
<br>



+ **Adding background image**

>> It allows you to place an image behind any HTML element. It could fill the entire page or be repeated to fill the page.


**1- The background-repeat property can have four values:**

* ``repeat`` -> It will repeats the image horizontally and vertically.

* ``repeat-x`` ->  It will repeats the image horizontally only.

* ``repeat-y`` -> It will repeats the image vertically only.

* ``no-repeat`` -> There will be no repeating.

* ``fixed`` -> The image will stay in its position.

* ``scroll`` -> Will be moving up and down with scroling.


**2- background-position:**

![background-position!](https://www.tutorialrepublic.com/lib/images/background-position-illustration.png)


**3- Image sprites:**

>> An image sprite is a collection of images put into a single image. <mark>[1]</mark>

<br>
<br>

### CHAPTER 19


![search-engine-optimization!](https://ciirs.com/wp-content/uploads/2021/03/seoimage.jpg)


**First of all, What do we mean by SEO?**

>> <mark>SEO</mark> stands for <mark>S</mark>earch <mark>E</mark>ngine <mark>O</mark>ptimization. 

>> It is the practice to help your site appear nearer the top of search engine results when people look for the topics that your website covers. <mark>[2]</mark>


**on-page techniques** 

>>> The main component of this is looking at keywords that people are likely to enter into a search engine if they wanted to find your site, and then including these in the text and HTML code for your site in order to help the search engines know that your site covers these topics. <mark>[3]</mark>



**off-page techniques**

>>> It is really important when other sites link to yours, Search engines help determine how to rank your site by looking at the number of other sites that link to yours.


![OFF/ON-PAGE!](https://www.mrgeek.pk/wp-content/uploads/2020/07/offpage-seo-on-off-page.png)


<br>

### ON-PAGE: 

1- Page title

2- URL/Web Address

3- Headings

4- Text

5- Link text

6- Image alt text

7- Page descriptions

<br>

**How to Identify Keywords and Phrases?**

1- Brainstorm

2- Organize

3- Research

4- Compare

5- Refine

6- Map

7- Page descriptions


<br>
<br>
<br>

>> To put your site on the web, you will need to obtain a domain name and web hosting.

>> FTP programs allow you to transfer files from your local computer to your web server.




<br>
<br>
<hr>
<br>
<br>


References :

* [<mark>[1]</mark> W3School](https://www.w3schools.com/css/css_image_sprites.asp)

* [<mark>[2]</mark> HTML and CSS by Jon Duckett](https://CSS/book)

* [<mark>[3]</mark> HTML and CSS by Jon Duckett](https://CSS/book)

