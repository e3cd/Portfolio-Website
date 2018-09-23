> _This website was created by **Allan Gao** for the Coder Academy portfolio project_

### [Website Link](https://e3cd.github.io/Portfolio-Website/)

### [Github Repository](https://github.com/e3cd/Portfolio-Website)

## Portfolio Website

### Purpose

In creating this portfolio website, I get a chance to practice my abilities with popular front-end technology stacks.

### Functionality/Features

The website's main feature is an interactive menu button which brings forth the menu overlay, where users will be able to direct themselves to the respective pages. There is a contact form which as of now is not functional, but will be implemented with back-end features in the near future.

The website is responsive and can be viewed by a variety of devices effectively.

### Sitemap

![sitemap](https://github.com/e3cd/Portfolio-Website/blob/master/documentation/sitemap.png)

### Technology Stack

This website was created using Html5, Css3, Bootstrap, Sass and Javascript.

### Intended Audience

The intended audience for my portfolio website would be other developers and employers.

## Planning Process

![planning](https://github.com/e3cd/Portfolio-Website/blob/master/documentation/Project_timeline.png)

## Design

### Design Process

The process of designing the website involved searching through the web for potential layouts. Searching through awwwards.com, one of the websites that I came across had a menu overlay that was simple but could bring an appealing transition effect to other linked pages. I realised that this effect could be recreated mostly with css and decided to implement this as the main feature of my website. I would then build my website around this feature.

![menu](https://github.com/e3cd/Portfolio-Website/blob/master/documentation/menu1.png)
[Link to website](https://www.awwwards.com/inspiration/585275a8e13823346d0d3893)

The menu overlay would feature an image of myself to the left and the menu navigation bar on the right. I allowed it to be fixed on every page for seamless navigation when scrolling.

#### Website Content

With simplicity in mind, I decided to use four pages.

- Home page - Containing links to my linkedin, medium and github pages.
- About me page - A short introduction to myself, listing of my previous education and current technology stack experience.
- Projects page - A page showcasing three of my previous projects.
- Contact page - A page containing a contact form and a mailto: link to my email account. The contact form will purely be UI only until further back-end implementation.

#### Wireframes

With a rough layout, I created wireframes using balsamiq to visualize what I had in mind for the website.

Link to [wireframes](https://github.com/e3cd/Portfolio-Website/tree/master/documentation/wireframes)

#### Fonts/Color Scheme

To maintain a professional look, I decided to go with a two colour scheme of grey and bright yellow. The grey was used to set an background image opacity effect, whilst the contrasting bright yellow font colour would stand out. I used two google fonts- "Montserrat" and "Oxygen".

Two background images were to be used, one specifically for the homepage and one for remaining pages.

#### Usability Considerations

The menu button being fixed throughout any page enhances the websites usability, as it allows for the user to access the menu easily without having to scroll up. Hover effects on all links to internal and external pages from white to bright yellow help with visibility.

Accomodating for responsive design was an important usability consideration. Much of the responsiveness is achieved automatically via the **'viewport'** meta tag:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Media queries were also incorporated for specific singular features.

#### Agile Incorporation

A Trello board was used to help manage planned workflow and allow for adjustments to be made. This was particularly evident during the creation of the menu overlay feature.

![trello1](https://github.com/e3cd/Portfolio-Website/blob/master/documentation/Trello1.png)
![trello2](https://github.com/e3cd/Portfolio-Website/blob/master/documentation/Trello2.png)

## Encountered Difficulties

Although simple in effect, creating the menu button with it's functionality presented some difficulties.

- The menu button comprises of three individual button lines. While using pseudoclasses in sass/css to try and create a hover effect and change the colour of the menu button, it would only result in the individual hovered button line to change effect instead of all three. Thus for all menu buttons to change colour, a js script was used in the html files to create this effect.

```
  <script type="text/javascript">
        var elms = document.getElementsByClassName("btn-line");
        var n = elms.length;
        function changeColor(color) {
            for (var i = 0; i < n; i++) {
                elms[i].style.backgroundColor = color;
            }
        }
        for (var i = 0; i < n; i++) {
            elms[i].onmouseover = function () {
                changeColor("rgb(218, 218, 0)");
            };
            elms[i].onmouseout = function () {
                changeColor("white");
            };
        }
    </script>
```

- As I did not find a sass/css solution to create the effect of the overlay, javascript was used to change the respective element class using the method;

```
<document.querySelector>
```

Subsequent sass/css was applied to the new classes generated to produce the sliding effect.

It was also difficult to find a way to make the photo of myself in the menu not transparent as it is a background image of a class. The background can still be seen when viewing the image, and thus somewhat hinders user accessibility.

## Short Answers

> Describe key events in the development of the internet from the 1980s to today (max. 150 words)

From the 1980’s and onwards the internet has developed rapidly.

- The packet-switching technology that makes the internet possible and it’s standard network protocols (TCP/IP) were established in 1982.
- Dr. Jon Postel introduces domains such as .com which were to be recognised as administrative entities on the internet.
- Recognised as the father of the web, Tim Berners-Lee laid forth the foundations of the development of the internet with WorldWideWeb: Proposal for the HyperText Project in 1990.
- During the 90’s, mainstream media attention exponentially increases the awareness and usage of the web. Development of web browsers helped further the commercial use of the internet such as e-commerce.
- Web 2.0 era is ushered in during the 21st century, allowing users to interact and collaborate with each other in a social media dialogue as creators of user-generated content in a virtual community,

> Define and describe the relationship between fundamental aspects of the internet such as: domains, web servers, DNS, and web browsers

The Internet is an interconnection of computers through large networks that communicate via the Internet Protocol.

A web server is a program on a server computer that delivers web pages to web browsers, whilst a web browser can be considered as a tool in which a user uses to access web services and documents from the server.

Domains are simply the address of a website which then points to its corresponding IP address. Domain Name Servers (DNS) are the Internet's equivalent of a phone book. They maintain a directory of domain names and translate them to Internet Protocol (IP) addresses.

> Reflect on one aspect of the development of internet technologies and how it has contributed to the world today

The ushering in of the so-called Web 2.0 in the early 21st century has made a dramatic impact on our society today. Along with it came the rise of social media and other interactive communication tools.

Unlike the 1990’s users of the internet today are not satisfied with just information exchange. The internet has grown to a sophisticated multidisciplinary, enabling individuals to create content, communicate with one another and even escape reality

The internet and in particular social media has allowed global issues to be instantly placed under a microscope with the way information and data can be communicated seamlessly. As long as there is a connection anyone can have their opinions output across multiple platforms from anywhere at any time. Events such as the Arab Spring and #metoo movement would not have happened without the development of the internet.
