# Sending Form Data
**An HTML form is gathers user input and this input is most often sent to a server for processing**

## Refresher: How to create a Form
* The HTML `<form>` element is used to create an HTML form.
* The HTML `<input>` element is the most used form element.
* Some other examples include:
```
<input type="text">	Displays a single-line text input field
<input type="radio">	Displays a radio button (for selecting one of many choices)
<input type="checkbox">	Displays a checkbox (for selecting zero or more of many choices)
<input type="submit">	Displays a submit button (for submitting the form)
<input type="button">	Displays a clickable button
```
**Once the form data has been validated on the client-side, it is okay to submit the form.**

## What happens when a user submits a form?
1. A client (usually a web browser) sends a request to a server using the HTTP protocol. 
2. The server answers the request using the same protocol.
3. An HTML form on a web page is a user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.
4. The `<form> element` defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. 
5. The two most important attributes are **action and method.**

## The action attribute
1. The action attribute defines where the data gets sent. 
2. Its value must be a valid relative or absolute URL. 
3. If a URL is NOT provided the data will be sent to the URL of the page containing the form — the current page.
4. The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation

## The method attribute
* The method attribute defines how data is sent.
* HTML form data can be transmitted via a number of different methods, the most common being the **GET** method and the **POST** method

To understand the difference between those two methods, let's step back and examine how HTTP works. Click [here](https://www.lifewire.com/hypertext-transfer-protocol-817944) to learn how HTTP works.

**An HTTP request consists of two parts: a header that contains a set of global metadata about the browser's capabilities, and a body that can contain information necessary for the server to process the specific request.**

## The GET method
1. The GET method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource." 
2. In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.
3. The data is appended to the URL as a series of name/value pairs

# The Post Method
1. The POST method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request.
2. The POST method says, "Hey server, take a look at this data and send me back an appropriate result." 
3. If a form is sent using this method, the data is appended to the body of the HTTP request.
4. When the form is submitted using the POST method, data is NOT appended to the URL and the HTTP request includes the data included in the request body instead.

**Please click below to learn more about sending form data as well as HTTP requests. The articles below were used to provide the information above:**

* [MDN Web Docs: Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)
* [W3schools.com : The `<input>` element](https://www.w3schools.com/html/html_forms.asp)
* [Lifewire.com : How HTTP works](https://www.lifewire.com/hypertext-transfer-protocol-817944)




