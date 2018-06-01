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
