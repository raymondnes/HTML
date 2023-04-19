Anchor Elements

To create a link in HTML, we use the anchor element. An anchor element is defined by wrapping the text or another HTML element we want to be a link with an <a> tag.

Add the following to the body of the index.html page we created and open it in the browser:

<a>click me</a>

An HTML attribute gives additional information to an HTML element and always goes in the element’s opening tag. An attribute is usually made up of two parts: a name, and a value; however, not all attributes require a value. In our case, we need to add a href (hyperlink reference) attribute to the opening anchor tag. The value of the href attribute is the destination we want our link to go to.

<a href="https://www.theodinproject.com/about">click me</a>

Absolute Links
Links to pages on other websites on the internet are called absolute links. A typical absolute link will be made up of the following parts: protocol://domain/path. An absolute link will always contain the protocol and domain of the destination.

We’ve already seen an absolute link in action. The link we created to The Odin Project’s About page earlier was an absolute link as it contains the protocol and domain.

https://www.theodinproject.com/about

Relative Links
Links to other pages within our own website are called relative links. Relative links do not include the domain name, since it is another page on the same site, it assumes the domain name will be the same as the page we created the link on.

Relative links only include the file path to the other page, relative to the page you are creating the link on. This is quite abstract, let’s see this in action using an example.

Within the odin-links-and-images directory, create another HTML file named about.html and paste the following code into it:

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Odin Links and Images</title>
  </head>

  <body>
    <h1>About Page</h1>
  </body>
</html>
Back in the index page, add the following anchor element to create a link to the about page:

<body>
  <h1>Homepage</h1>
	<a href="https://www.theodinproject.com/about">click me</a>

	<a href="about.html">About</a>
</body>

A Metaphor
Absolute and relative links are a tricky concept to build a good mental model of, a metaphor may help:

Think of your domain name (town.com) as a town, the directory in which your website is located (/museum) as a museum, and each page on your website as a room in the museum (/museum/movie_room.html and /museum/shops/coffee_shop.html). Relative links like ./shops/coffee_shop.html are directions from the current room (the museum movie room /museum/movie_room.html) to another room (the museum shop). Absolute links, on the other hand, are full directions including the protocol (https), domain name (town.com) and the path from that domain name (/museum/shops/coffee_shop.html): https://town.com/museum/shops/coffee_shop.html.

Images
Websites would be fairly boring if they could only display text. Luckily HTML provides a wide variety of elements for displaying all sorts of different media. The most widely used of these is the image element.

To display an image in HTML we use the <img> element. Unlike the other elements we have encountered, the <img> element is self-closing. Empty, self-closing HTML elements do not need a closing tag.

Instead of wrapping content with an opening and closing tag, it embeds an image into the page using a src attribute which tells the browser where the image file is located. The src attribute works much like the href attribute for anchor tags. It can embed an image using both absolute and relative paths.

For example, using an absolute path we can display an image located on The Odin Project site:

 <img src="https://www.theodinproject.com/mstile-310x310.png">
