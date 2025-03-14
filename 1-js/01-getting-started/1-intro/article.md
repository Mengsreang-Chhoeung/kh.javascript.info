# សេចក្តីចាប់ផ្តើមនៃភាសា JavaScript

តោះទៅមើលអ្វីដែលពិសេសអំពីភាសា JavaScript អ្វីដែលយើងអាចសម្រេចបានជាមួយវា និងបច្ចេកវិទ្យាផ្សេងទៀតដែលដំណើរការល្អជាមួយវា។

## អ្វីទៅជា JavaScript?

_JavaScript_ ត្រូវបានបង្កើតដំបូងដើម្បីធ្វើឲ្យទំព័រនៃគេហទំព័រមានភាពរស់រវើក។

កម្មវិធីនៅក្នុងភាសានេះត្រូវបានគេហៅថា _scripts_ ។ ពួកវាអាចសរសេរបានត្រឹមត្រូវនៅក្នុង HTML របស់គេហទំព័រ ហើយដំណើរការដោយស្វ័យប្រវត្តិនៅពេលទំព័រត្រូវបានបង្ហាញ។

Scripts ត្រូវបានផ្តល់ និងប្រតិបត្តិជាអត្ថបទធម្មតា។ ពួកគេមិនត្រូវការការរៀបចំជាពិសេស ឬការចងក្រងដើម្បីដំណើរការទេ។

នៅក្នុងទិដ្ឋភាពនេះ JavaScript គឺខុសគ្នាយ៉ាងខ្លាំងពីភាសាផ្សេងទៀតហៅថា [Java](<https://en.wikipedia.org/wiki/Java_(programming_language)>).

```smart header="ហេតុអ្វីបានជាវាត្រូវបានហៅថា <u>Java</u>Script?"
នៅពេលដែល JavaScript ត្រូវបានបង្កើត ដំបូងមានឈ្មោះផ្សេងទៀត: "LiveScript" ។ ប៉ុន្តែ Java មានប្រជាប្រិយភាពខ្លាំងនៅពេលនោះ ដូច្នេះវាត្រូវបានគេសម្រេចចិត្តថាដាក់ឈ្មោះភាសាថ្មីជា "ប្អូនប្រុស" របស់ Java។

ប៉ុន្តែនៅពេលដែលវាវិវឌ្ឍ ភាសា JavaScript បានក្លាយជាភាសាឯករាជ្យពេញលេញជាមួយនឹងលក្ខណៈជាក់លាក់របស់វាហៅថា [ECMAScript](http://en.wikipedia.org/wiki/ECMAScript), ហើយ​ឥឡូវ​នេះ​វា​មិន​មាន​ទំនាក់​ទំនង​ជាមួយនឹងភាសា Java ទាល់​តែ​សោះ។
```

សព្វ​ថ្ងៃ JavaScript អាច​ប្រតិបត្តិ​មិន​ត្រឹម​តែ​នៅ​ក្នុង​ browser ប៉ុណ្ណោះ​ទេ ប៉ុន្តែ​ក៏​នៅ​លើ server ឬ​​ទៅ​លើ​ឧបករណ៍​ណា​មួយ​ដែល​មាន​កម្មវិធី​ពិសេស​ដែល​គេ​ហៅ​ថា [the JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine).

Browser មាននូវម៉ាស៊ីនបង្កប់(embedded engine) ដែលជួនកាលអាចហៅថា "JavaScript virtual machine"។

ម៉ាស៊ីនផ្សេងគ្នាមាន "កូដឈ្មោះ" ផ្សេងគ្នា។ ឧទាហរណ៍:

- [V8](<https://en.wikipedia.org/wiki/V8_(JavaScript_engine)>) -- នៅក្នុង Chrome, Opera and Edge.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- នៅក្នុង Firefox.
- ...មានកូដឈ្មោះផ្សេងទៀតដូចជា "Chakra" សម្រាប់ IE, "JavaScriptCore", "Nitro" និង "SquirrelFish" សម្រាប់ Safari ។ល។

ពាក្យខាងលើគឺល្អក្នុងការចងចាំ ព្រោះវាត្រូវបានប្រើនៅក្នុងអត្ថបទអ្នកអភិវឌ្ឍន៍នៅលើអ៊ីនធឺណិត។ យើងនឹងប្រើពួកវាផងដែរ។ ឧទាហរណ៍ ប្រសិនបើ "មុខងារ X ត្រូវបានគាំទ្រដោយ V8" នោះវាប្រហែលជាដំណើរការនៅក្នុង Chrome, Opera និង Edge ។

```smart header="How do engines work?"

Engines are complicated. But the basics are easy.

1. The engine (embedded if it's a browser) reads ("parses") the script.
2. Then it converts ("compiles") the script to the machine language.
3. And then the machine code runs, pretty fast.

The engine applies optimizations at each step of the process. It even watches the compiled script as it runs, analyzes the data that flows through it, and further optimizes the machine code based on that knowledge.
```

## What can in-browser JavaScript do?

Modern JavaScript is a "safe" programming language. It does not provide low-level access to memory or CPU, because it was initially created for browsers which do not require it.

JavaScript's capabilities greatly depend on the environment it's running in. For instance, [Node.js](https://wikipedia.org/wiki/Node.js) supports functions that allow JavaScript to read/write arbitrary files, perform network requests, etc.

In-browser JavaScript can do everything related to webpage manipulation, interaction with the user, and the webserver.

For instance, in-browser JavaScript is able to:

- Add new HTML to the page, change the existing content, modify styles.
- React to user actions, run on mouse clicks, pointer movements, key presses.
- Send requests over the network to remote servers, download and upload files (so-called [AJAX](<https://en.wikipedia.org/wiki/Ajax_(programming)>) and [COMET](<https://en.wikipedia.org/wiki/Comet_(programming)>) technologies).
- Get and set cookies, ask questions to the visitor, show messages.
- Remember the data on the client-side ("local storage").

## What CAN'T in-browser JavaScript do?

JavaScript's abilities in the browser are limited for the sake of a user's safety. The aim is to prevent an evil webpage from accessing private information or harming the user's data.

Examples of such restrictions include:

- JavaScript on a webpage may not read/write arbitrary files on the hard disk, copy them or execute programs. It has no direct access to OS functions.

  Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions, like "dropping" a file into a browser window or selecting it via an `<input>` tag.

  There are ways to interact with camera/microphone and other devices, but they require a user's explicit permission. So a JavaScript-enabled page may not sneakily enable a web-camera, observe the surroundings and send the information to the [NSA](https://en.wikipedia.org/wiki/National_Security_Agency).

- Different tabs/windows generally do not know about each other. Sometimes they do, for example when one window uses JavaScript to open the other one. But even in this case, JavaScript from one page may not access the other if they come from different sites (from a different domain, protocol or port).

  This is called the "Same Origin Policy". To work around that, _both pages_ must agree for data exchange and contain a special JavaScript code that handles it. We'll cover that in the tutorial.

  This limitation is, again, for the user's safety. A page from `http://anysite.com` which a user has opened must not be able to access another browser tab with the URL `http://gmail.com` and steal information from there.

- JavaScript can easily communicate over the net to the server where the current page came from. But its ability to receive data from other sites/domains is crippled. Though possible, it requires explicit agreement (expressed in HTTP headers) from the remote side. Once again, that's a safety limitation.

![](limitations.svg)

Such limits do not exist if JavaScript is used outside of the browser, for example on a server. Modern browsers also allow plugin/extensions which may ask for extended permissions.

## What makes JavaScript unique?

There are at least _three_ great things about JavaScript:

```compare
+ Full integration with HTML/CSS.
+ Simple things are done simply.
+ Supported by all major browsers and enabled by default.
```

JavaScript is the only browser technology that combines these three things.

That's what makes JavaScript unique. That's why it's the most widespread tool for creating browser interfaces.

That said, JavaScript also allows to create servers, mobile applications, etc.

## Languages "over" JavaScript

The syntax of JavaScript does not suit everyone's needs. Different people want different features.

That's to be expected, because projects and requirements are different for everyone.

So recently a plethora of new languages appeared, which are _transpiled_ (converted) to JavaScript before they run in the browser.

Modern tools make the transpilation very fast and transparent, actually allowing developers to code in another language and auto-converting it "under the hood".

Examples of such languages:

- [CoffeeScript](https://coffeescript.org/) is a "syntactic sugar" for JavaScript. It introduces shorter syntax, allowing us to write clearer and more precise code. Usually, Ruby devs like it.
- [TypeScript](https://www.typescriptlang.org/) is concentrated on adding "strict data typing" to simplify the development and support of complex systems. It is developed by Microsoft.
- [Flow](https://flow.org/) also adds data typing, but in a different way. Developed by Facebook.
- [Dart](https://www.dartlang.org/) is a standalone language that has its own engine that runs in non-browser environments (like mobile apps), but also can be transpiled to JavaScript. Developed by Google.
- [Brython](https://brython.info/) is a Python transpiler to JavaScript that enables the writing of applications in pure Python without JavaScript.
- [Kotlin](https://kotlinlang.org/docs/reference/js-overview.html) is a modern, concise and safe programming language that can target the browser or Node.

There are more. Of course, even if we use one of transpiled languages, we should also know JavaScript to really understand what we're doing.

## Summary

- JavaScript was initially created as a browser-only language, but it is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language, fully integrated with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.
