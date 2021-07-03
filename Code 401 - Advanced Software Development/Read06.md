# Router Middleware


Middleware functions are functions that have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

Middleware functions can perform the following tasks:

- Execute any code.
- Make changes to the request and the response objects.
- End the request-response cycle.
- Call the next middleware in the stack.
- If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function. Otherwise, the request will be left hanging.
- 
The following figure shows the elements of a middleware function call:
![](https://github.com/MURADALSHORMAN/reading-notes/blob/main/Code%20401%20-%20Advanced%20Software%20Development/Capturexx.JPG)



```
var express = require('express')
var app = express()

app.get('/', function (req, res) {
  res.send('Hello World!')
})

app.listen(3000)
```
# Dynamic loading

Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. It is one of the 3 mechanisms by which a computer program can use some other software; the other two are static linking and dynamic linking. Unlike static linking and dynamic linking, dynamic loading allows a computer program to start up in the absence of these libraries, to discover available libraries, and to potentially gain additional functionality

# Singleton Pattern
In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.
 
 ![](https://www.tutorialspoint.com/design_pattern/images/singleton_pattern_uml_diagram.jpg)



# Authentication

Authentication is the act of proving an assertion, such as the identity of a computer system user. In contrast with identification, the act of indicating a person or thing's identity, authentication is the process of verifying that identity. It might involve validating personal identity documents, verifying the authenticity of a website with a digital certificate, determining the age of an artifact by carbon dating, or ensuring that a product or document is not counterfeit.



Authentication is relevant to multiple fields. In art, antiques and anthropology, a common problem is verifying that a given artifact was produced by a certain person or in a certain place or period of history. In computer science, verifying a user's identity is often required to allow access to confidential data or systems.
![](https://res.cloudinary.com/practicaldev/image/fetch/s--i3PAUmjc--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://i1.wp.com/blog.mallow-tech.com/wp-content/uploads/2016/12/user-authentication.jpg%3Fresize%3D820%252C400)
Authentication can be considered to be of three types:

- The first type of authentication is accepting proof of identity given by a credible person who has first-hand evidence that the identity is genuine. When authentication is required of art or physical objects, this proof could be a friend, family member or colleague attesting to the item's provenance, perhaps by having witnessed the item in its creator's possession. With autographed sports memorabilia, this could involve someone attesting that they witnessed the object being signed. A vendor selling branded items implies authenticity, while he or she may not have evidence that every step in the supply chain was authenticated. Centralized authority-based trust relationships back most secure internet communication through known public certificate authorities; decentralized peer-based trust, also known as a web of trust, is used for personal services such as email or files (Pretty Good Privacy, GNU Privacy Guard) and trust is established by known individuals signing each other's cryptographic key at Key signing parties, for instance.

- The second type of authentication is comparing the attributes of the object itself to what is known about objects of that origin. For example, an art expert might look for similarities in the style of painting, check the location and form of a signature, or compare the object to an old photograph. An archaeologist, on the other hand, might use carbon dating to verify the age of an artifact, do a chemical and spectroscopic analysis of the materials used, or compare the style of construction or decoration to other artifacts of similar origin. The physics of sound and light, and comparison with a known physical environment, can be used to examine the authenticity of audio recordings, photographs, or videos. Documents can be verified as being created on ink or paper readily available at the time of the item's implied creation.






