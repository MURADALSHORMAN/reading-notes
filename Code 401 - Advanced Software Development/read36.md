# Review, Research, and Discussion
## What are the advantages of storing tokens in “Cookies” vs “Local Storage”

Cookies are automatically saved, sent and removed by the browser. When doing browser level navigation, only cookies are sent. Sharing the same session across subdomains can easily be done with cookies. Cookies have a special flag called httpOnly, which means that malicious JS code cannot send the access token to the attacker.

## Explain 3rd party cookies.

Third party cookies are cookies that are stored under a different domain than you are currently visiting. They are mostly used to track users between websites and display more relevant ads between websites. Another good example is a support chat functionality provided by a 3rd party service.

## How do pixel tags work?

Tracking pixel or pixel tag (also called 1x1 pixel) is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. The website operator or sender of an email adds the tracking pixel using a code in the website’s HTML code or email. This code contains an external link to the pixel server. If a user visits the destination website, the HTML code is processed by the client – usually the user’s browser. The browser follows the link and opens the (invisible) graphic. This is registered and noted in the server’s log files. In addition, various information about the user is also transmitted using this method. To some extent, combination with JavaScript is necessary in order to collect information about the operating system or browser type. The following data can be acquired and analyzed with a tracking pixel: operating system used, type of website or email used (mobile or desktop), type of client used (browser or mail program), client’s screen resolution, time the email was read or website was visited, activites on the website during the session (when using multiple tracking pixels), IP address.

## Preparation Materials
Fundamentals of Redux Course from Dan Abramov

Redux provides a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse.

The principles of Redux aren’t new, but they are packaged and presented for you in an easy to use a library that not only elevates your applications but also improves your general understanding of building JavaScript UIs.

In this course, Dan Abramov will show you the fundamentals of Redux, so that you can start using it to simplify your applications.

This is a comprehensive (but simplified) guide for absolute Redux beginners, or any who wants to re-evaluate their understanding of the fundamental Redux concepts.













