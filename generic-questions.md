# UI interview questions

#### _What does a doctype do?_ ####

``<!DOCTYPE html>``: The doctype. In the mists of time, when HTML was young (about 1991/2), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. They used to look something like this:
``<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">``

However, these days no one really cares about them, and they are really just a historical artifact that needs to be included for everything to work right. <!DOCTYPE html> is the shortest string of characters that counts as a valid doctype; that's all you really need to know.

Source: https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started

Notes: should be there for a valid html and without it the browser enters "quirks" mode and you can face crazy things.
https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode


#### _How do you serve a page with content in multiple languages?_ ####

https://www.youtube.com/watch?v=u5i_dnqj43w 

#### _What kind of things must you be wary of when design or developing for multilingual sites?_ ####

https://www.quora.com/What-kind-of-things-one-should-be-wary-of-when-designing-or-developing-for-multilingual-sites

#### _What are data- attributes good for?_ ####
https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes
https://codepen.io/gyurrcibacsi/pen/VdLNWQ

#### _Describe the difference between a cookie, sessionStorage and localStorage_ ####

https://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies

#### _Describe the difference between <script>, <script async> and <script defer>._ ####
https://www.quora.com/What-is-the-difference-between-DEFER-and-ASYNC-attributes-on-a-resource-in-html
https://javascript.tutorialhorizon.com/2015/08/11/script-async-defer-attribute/
 ###### Normal execution <script> ######
This is the default behavior of the <script> element. Parsing of the HTML code pauses while the script is executing. For slow servers and heavy scripts this means that displaying the webpage will be delayed.
###### Deferred execution <script defer> ######
Simply put: delaying script execution until the HTML parser has finished. A positive effect of this attribute is that the DOM will be available for your script. However, since not every browser supports defer yet, don’t rely on it!
###### Asynchronous execution <script async> ######
Don’t care when the script will be available? Asynchronous is the best of both worlds: HTML parsing may continue and the script will be executed as soon as it’s ready. I’d recommend this for scripts such as Google Analytics.
  
 #### _Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions?_ ####

You usually put the ``<link>`` tags in between the <head> to prevent Flash of Unstyled Content which gives the user something to look at while the rest of the page is being parsed.

Since Javascript blocks rendering by default, and the DOM and CSSOM construction can be also be delayed, it is usually best to keep scripts at the bottom of the page.

Exceptions are if you grab the scripts asynchronously, or at least defer them to the end of the page.

#### _What is progressive rendering?_ ####
With HTML progressive rendering is chunking the HTML into separate bits and loading each block as it's finished. Usually, the backend code loads the HTML at once, but if you flush after finishing one part of the structure, it can be rendered immediately to the page.

This can be done asynchronously with different components being loaded as they finish. There's new features which can be used with [Web Components](https://www.html5rocks.com/en/tutorials/webcomponents/imports/) making it more standard. Another interesting article on this is from eBay with [Async Fragments](https://www.ebayinc.com/stories/blogs/tech/async-fragments-rediscovering-progressive-html-rendering-with-marko/).

#### _Why you would use a ``srcset`` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute._ ####
#### _Have you used different HTML templating languages before?_ ####
#### _How prototypical inhertitance working? What is the differences between ``_.prototype, .__proto__`` and ``[[Prototype]]``?_ ####
http://www.javascripttutorial.net/javascript-prototype/
https://hackernoon.com/understand-nodejs-javascript-object-inheritance-proto-prototype-class-9bd951700b29

#### _What is an event loop in JS?_ ####
[Event loop explained well](https://www.youtube.com/watch?v=8aGhZQkoFbQ&t=2s)

#### _Delegation vs assignment_ ####

Delegation is a common practice in contract law. Delegation occurs when a party to the contract transfers the responsibility and authority for performing a particular contractual duty to another party. Delegation doesn't involve the transfer of contractual rights.

Let's say that you hire me to remodel your kitchen. I'm planning to do all of the work myself, but I'm not a painter. Paint fumes give me a headache. I'm planning to delegate the painting to my friend, Pam. I'm still responsible for the kitchen remodel, and you'll pay me when I'm finished. The contract is between you and me. Pam is only responsible for the painting.

###### Differences in Delegation and Assignment ######
An assignment occurs when an original party to the contract transfers the rights and duties of the contract to another party. A party can assign the entire contract, meaning that the party assigns both the rights and the obligations of the contract. Alternatively, the party can assign only the rights, or benefits, due under the contract. The party making the assignment is called the assignor. The party receiving the assignment is the assignee. It's helpful to remember that the assignee steps into the shoes of the assignor.

Delegation, on the other hand, involves only a portion of the contract. With delegation, a particular contractual task or activity is transferred. Delegation means that an obligation is transferred, but no rights are transferred. The party making the delegation is called the delegator. The party receiving the delegation is the delegatee. The delegatee doesn't assume responsibility for the entire contract or receive the benefits of the contract. Therefore, the delegatee doesn't step into the shoes of the delegator. In our scenario, I am the delegator and Pam is the delegatee.

In both assignment and delegation, there is an obligor. The obligor is the other original party to the contract and is obligated to do something under the terms of the contract. In our scenario, you are the obligor. You're obligated to pay me once I finish your kitchen.


