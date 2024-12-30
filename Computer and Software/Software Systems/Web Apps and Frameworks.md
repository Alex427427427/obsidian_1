Category: [[Software]]
___
## Background: Web Applications
The most basic components of a web app involve:
1. a process - often called a "service", really just a computer program - running on some computer - called a "host" - at some IP address. It will also have a specific port on the computer for communication addressing. (Because different programs requiring communication on the same computer need different ports, so that the OS can differentiate between messages that need to be delivered to each program)
2. a browser - which is a program specialised in establishing contact and communicating back and forth with the above service, and displaying what that remote process serves, to the end user. 
So the service has some internet address of the form IP:port. And the browser needs to talk to that address IP:port. 
## The Modern Web App Architecture
Today, we have standardised the kinds of ways browsers can interact with services. Browsers send requests to the address of the service, and the service sends back an HTML, CSS, and Javascript. HTML ([[Hyper Text Markup Language (HTML)]]) is a language that a browser can use to generate the structure of a web page, CSS if additional aesthetics settings, and Javascript is code that a browser can use to define the logic of the webpage. 
## Frameworks
It's quite tedious to code in HTML, CSS and Javascript directly. What if you can write code in your own favourite language, like python, and have it automatically generate the corresponding HTML, CSS and Javascript? Add on top of that common structures that everyone would want to put in a webpage, abstracted into simple commands. Put it into a library for your favourite language. That is what frameworks are. 

