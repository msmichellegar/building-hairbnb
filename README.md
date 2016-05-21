# Building Hairbnb

Workshop notes for building an Airbnb front page clone with HTML/CSS.

## The Challenge

The task is to recreate the front page of Airbnb using just HTML and CSS. The page does not need to be functional in the way of the real Airbnb website. It just needs to look the part.

The Airbnb website has simple, modular design that is good practice to  recreate. But since the actual Airbnb front page has a lot of content, I have created a simplified version, which you can find [here](http://msmichellegar.github.io/hairbnb). This is what you will be working to.

## Design Resources

You won't be making any actual design decisions as I've prepared all the assets, fonts and colours for you. This leaves you to focus solely on the CSS (the best part).

#### Images

We're using different images to the real Airbnb site. I have created a series of assets ready for you to insert into the site, which you can find [here](https://www.dropbox.com/sh/8snzlcegjn58fsx/AAABuEyeJt7piv8UPil9jsPQa?dl=0).

###### Image Links

Logo: https://dl.dropboxusercontent.com/u/297682547/Hairbnb/logo.png
Header background: https://dl.dropboxusercontent.com/u/297682547/Hairbnb/header/nyc.jpg

#### Colours

We're going to use the same colours as the Airbnb website, which are as follows:

* Body background colour: #EDEFED
* Body text colour: #565A5C
* Header text colour: #FFFFFF (aka white)

#### Fonts

Airbnb uses its own beautiful fonts. Rather than mess around with a custom font, we're just going to use classic Helvetica, which is already built-in to browsers.

## How To Do It

#### Step 0: File Setup

Create two documents in the same folder: one called `index.html` and one called `main.css`.

Set up the `index.html` with the basic HTML document structure. If you've forgotten how, here's [how to do that](http://www.w3schools.com/html/html_intro.asp).

You'll need to link to your CSS from the HTML document. In the `<head>` section, insert the following:

```html
<link rel="stylesheet" href="main.css">
```

Set some basic CSS properties for the website.

```css
body {
    margin: 0; /* gets rid of the defauult border around the page */
    background-color: #EDEFED; /* sets background colour for site */
    color: white; /* sets text color for site */
    font-family: Helvetica; /* sets font for page */
}

```

Now you're good to go.

#### Step 1: Header

Break up the page into different sections (or "divs"), and style each section individually. You'll be nesting elements within different containers to style and format them more easily. In every case, create the full HTML structure for a section first before styling it.

Start with the header. This refers to the top section with the large background image. You can use [the semantic HTML5 tag](http://www.w3schools.com/tags/tag_header.asp) and call it "header":

```html
<header>
</header>
```

Within the header section, you will need to create the following elements:
* An image element holding [the logo](https://dl.dropboxusercontent.com/u/297682547/Hairbnb/logo.png). Here's [how to create an image tag](http://www.w3schools.com/tags/tag_img.asp).
* The navigation. A good strategy for creating the navigation is to create the headings as a bullet pointed list (`<ul> </ul>`). Don't worry, we'll remove the bullet points and style it with CSS. Here's [how to create an unordered list](http://www.w3schools.com/tags/tag_ul.asp).
* The main tag line "LIVE THERE". Create it as a heading1 (`<h1> </h1>`) as it is the biggest bit of text on the page.
* The second tag line underneath. Create is as a heading4 (`<h4> </h4>`).

Now you need to style. Remember here's how you select an ID (`#id`) and here's how you select a class (`.class`), and anything else is just like this (`p`). Here are the properties you will need. If any of them are confusing, you can look them up [here](http://www.w3schools.com/css/default.asp).

```css
.selector {
    background: url("[link to image]"); /* sets background image for a div */
    background-size: cover; /* sets width of background to cover page */
    border: [number]px solid [colour]; /* creates a border */
    border-radius: [number]px; /* rounds to corners of a square border */
    color: [colour]; /* sets text colour */
    display: inline-block; /* makes block elements sit in a line */
    float: left; /* makes something stick to the left of the page */
    float: right; /* makes something stick to the right of the page */
    font-size: [number]px; /* sets font size */
    font-weight: [number: 100, 200, 300, 400, 500, 600, 700, 800]; /* sets how bold the text is */
    height: [number]px; /* sets height of an element */
    list-style: none; /* removes bullet points or styling from a list */
    margin: [number]px; /* puts space around an element (from outside) */
    padding: [number]px; /* puts space around an element (from inside) */
    text-align: center; /* centers an element and elements within it */
}
```

#### Step 2: Inspiration Sections

Below the header, you can see there are two mini-sections of content. As they have exactly the same structure, we are going to create them as two separate sections, but give them the same class. Let's work on one to start with. Create a [div](http://www.w3schools.com/tags/tag_div.asp) and give it a class.

```html
<div class="inspiration">
</div>
```

You will need to create the following elements inside the inspiration div:

* A heading. Make it an `<h2>`.
* Text underneath the heading. Just use basic paragraph text `<p>`.
* Three image elements, linking to [different images](https://www.dropbox.com/sh/p65qv0cjewuu4ja/AABfabSwMj4v3ZAchlork8_5a?dl=0).
* A button. Create it as simple paragraph text and we will style it to look like a button.

Remember divs are used to group content together. As the three images are a section of their own within this larger section, put them in their own inner div and give that div a class.

Now to style it. There are no new properties for this section, so refer to the list you used above to find the properties required. One useful trick for this section is to center an element using `margin: 0 auto`.

Once you have successfully styled the "weekend" section, clone the HTML and insert the "world travel" content. Check the styling works. You might have to add some spacing between the sections.

#### Step 3: Footer

The final bit of content is the footer. I have provided you with a background image for the section [here](https://dl.dropboxusercontent.com/u/297682547/Hairbnb/footer.png). Use a semantic HTML5 tag to set up the section.

```html
<footer>
</footer>
```

Create the following elements:

* Three [unordered lists](http://www.w3schools.com/tags/tag_ul.asp)), preceded by an `<h5>` tag containing the list heading.
* A horizontal rule to insert a line across the footer. Read about `<hr>` tags [here](http://www.w3schools.com/tags/tag_hr.asp).
* A line of paragraph text listing the copyright for Hairbnb. The text `&copy;` should insert a copyright symbol that looks like this: &copy;.

The three lists and their corresponding headings will need to each be grouped as a block. Put a div around each list and give it a class to use for styling.

Additional properties you will need for styling are:

```css
.selector {
    width: [number]px or [number]%; /* sets width of an element */
    vertical-align: top; /* aligns elements to the top as opposed to bottom of a line */
    line-height: [number]; /* sets height of line */
}
```

#### Step 4: Mobile View

Congratulations! You made the front page. But it's not over yet. If you look at this on mobile, it won't display quite as planned. You want it to look good on every device.

Thankfully in CSS there are things called "media queries". These allow you to set different styling properties at different screen widths. So you can set a heading to be 100px big on desktop, but only 50px on mobile.

A media query looks like this:

```css
@media (max-width: 700px) {
    h1 {
        font-size: 50px;
    }
}
```

That sets the font size of an h1 to be only 50px when the screen is less than 700px wide. You just pop that in anywhere in your CSS document.

Here is a set of media queries that will make your Hairbnb site mobile-responsive. They include some new properties that you haven't seen, such as setting elements not to display `display: none;` and using a special selector to only grab the first element of a type `:first-of-type`. Add these media queries to the end of your CSS file.

```css
@media (max-width: 700px) {

    header ul {
        display: none;
    }

    footer {
        height: 250px;
    }

    .footer-block {
        display: none;
    }

    .footer-block:first-of-type {
        display: block;
        text-align: center;
        margin-top: 50px;
    }

    .footer-block h5 {
        display: none;
    }

    .footer-block li {
        margin: 0 5px;
        display: inline-block;
    }

}
```

#### Step 5: Deploy!

Now we're making it live. You are going to be deploying the site with [GitHub pages](https://pages.github.com/), which basically means GitHub will host the website for us.

On GitHub, create a new public repository called "hairbnb" (or a short, memorable name you'd like to call it). Instructions for creating a repo are [here](https://help.github.com/articles/create-a-repo/).

Now navigate to this repository on your account. Create a "branch" called "gh-pages" (it's important that you type this exactly). Instructions for doing that are [here](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/).

Now upload your `index.html` and `main.css` files into the repository by clicking "Upload Files" and dragging them onto the screen. Instructions for that are [here](https://github.com/blog/2105-upload-files-to-your-repositories).

In a minute, your site should be live! Visit the url [yourgithubname].github.io/[repositoryname] to see it in action.

Good work :)
