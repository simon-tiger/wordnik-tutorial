# wordnik-tutorial

<span id="home"></span>
**Home** | [**Wordnik Basics**](#wordnik-basics) | [**Types of queries**]()

This tutorial is a walkthrough wordnik.
Wordnik is an API that knows a lot about words in the English language.

Questions:

1. What is an API?<br>
   Answer: API stands for Application Programming Interface. This means the following:
   You're writing an application, somebody else wrote an application, you want these two applications to talk to eachother.

2. Why do you need an API?<br>
   Answer: If you need data, you most likely don't want to type the data yourself. Instead, you want to get the data from somewhere. But where? The answer to this is an API. Just search for the API you're looking for, and use it!

3. What is a query?<br>
   Answer: **Querying** an API is a term for Asking an API for something. This term exists because normally with an api, you cannot just say "Give me all of your data"! Normally, you've got to be more specific.
   For example, we're going to use the wordnik api. You can't just say to wordnik "Give me all of your data"! Right? you've got to be more specific. For example "Give me **a single word related to the word apple**.".
</div>

<span id="wordnik-basics"></span>
[**Home**](#home) | **Wordnik Basics** | [**Types of queries**]()

Go to the url: `developer.wordnik.com`, and click on `Docs`.

Now, what's the qusetion? Let's add it to our list.

4. There already is a documentation, why are you reading this documentation?<br>
   Answer: The docs in wordnik documentation is an interface. This documentation is actually a tutorial!

## Syntax

The actual syntax is using **AJAX**! What's the question now?

5. What is AJAX?<br>
   Answer: **AJAX** stands for Asynchronous JavaScript and XML.
   Asynchronous just means "in the background", so things are happening while other things are happening.
   XML is an older version of JSON, that looks like HTML. Wordnik is going to output JSON, but AJAX can send or receive data of **any** type.

Here's what the syntax looks like:

```javascript
var request = new XMLHttpRequest();
request.onreadystatechange = function() {
  if (this.readyState === 4 && this.status === 400) {
    // code to be executed if the data is finished loading
    // the data itself is in request.responseText
  }
}
request.open("GET", "your-request-url", true);
request.send();
```

Another syntax you can use is using a library called swagger.js. This is a bit out of scope of this particular tutorial, so there is a link to a tutorial about that [here](https://github.com/swagger-api/swagger-js).

Finally, [p5.js](https://github.com/processing/p5.js) syntax can also be used. This is the syntax for you if you're a beginner.
Let's show that syntax within the tutorial:

```javascript
function setup() {
  loadJSON("your-request-url", gotData);
}

function gotData(data) {
  // code to be executed if the data is finished loading
  // the data itself is in data
}
```
