<img  src="code-diff-logo.png" alt="Code Differently Logo" style="height:100px; width:300px; text-align:center;">

# Form Basics

## **Form Structure**

- **`<form>`** **element**

    Form controls are contained by the `<form>` element. The `action` attribute should always be added to the **`<form>`** element, along with the `method` attribute.

<br>

- **`action`** attribute

    All `<form>` elements require an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.

<br>

- **`method`** attribute

    The **method** attribute is the **HTTP** method that the browsers use to submit forms. Forms can be sent using one of the two methods: **GET** or **POST**.

    * **GET**
        * The values from the form are added to the end of the URL specified in the **action** attribute. This method is most ideal for short forms, like search boxes, and when just retrieving data from the web server.

    * **POST**
        * With the **POST** method, the values are sent in as `HTTP` headers. **POST** methods should be used if your form:
            * allows users to upload a file
            * is very long
            * contains sensitive data such as passwords
            * adds or deletes information from a database



## Inputs

The most important form element is the **`<input>`** element. This element is used to create several different form controls. the `<type>` attribute's value determines what kind of input is created. The `<input>` element does not have a closing tag. It is a void element.


<br>

### **Text Input**

```html
<form action="http://www.example.com/login.php"> 
    <p>Username:
        <input type="text" name="username" maxlength="10">
    </p> 
</form>
```

<!-- The text box can be typed in to demonstrate only 10 characters can fit -->
**When displayed in the browser:**

<form action="http://www.example.com/login.php"> 
    <p>Username:
        <input type="text" name="username" maxlength="30">
    </p> 
</form>

<br>

* **`type="text"`**

    * When the `type` attribute has a value of `"text"`, it creates a singe-line of input.

* **`name`** attribute

    * Each form control requires a `name` attribute and the value identifies the form control which is then sent along with the information they enter to the server. 

* **`maxlength`** attribute

    * The `maxlength` attribute can be used to limit the number of characters a user may enter into the text field. For example, if you required the user to enter a year, the `maxlength` would have a value of `4`.

```html
<form action="http://www.example.com/login.php"> 
    <p>Year:
        <input type="text" name="year" maxlength="4">
    </p> 
</form>
```

<!-- The text box can be typed in to demonstrate only 4 characters can fit -->
**When displayed in the browser:**

<form action="http://www.example.com/login.php"> 
    <p>Year:
        <input type="text" name="year" maxlength="4">
    </p> 
</form>

---

<br>

### **Password Input**

```html
<form action="http://www.example.com/login.php"> 
    <p>Username:
        <input type="text" name="username"  maxlength="10">
    </p> 
    <p>Password:
        <input type="password" name="password"  maxlength="10">
    </p> 
</form>
```

<!-- The text box can be typed in to demonstrate only 10 characters can fit -->
**When displayed in the browser:**

<form action="http://www.example.com/login.php"> 
    <p>Username:
        <input type="text" name="username"  maxlength="10">
    </p> 
    <p>Password:
        <input type="password" name="password"  maxlength="10">
    </p> 
</form>

<br>

* **`type="password"`**

    * When the type attribute has a value of `"password"`, it creates a text box that acts just like a single-line input, only difference is the characters are hidden from view. 

* **`name`** attribute

    * This attribute indicates the name of the password input, which is sent to the server with the password the user enters. 

* **`maxlength`** attribute

    * Similar to text input, you can control the number of characters a user enters. Although the password is hidden, this does not send the password securely to the server. This should never be used for sending sensitive data, such as social security numbers.

---

<br>


### **Text Area**

```html
<form action="http://www.example.com/comments.php"> 
    <p>What did you think of this gig?</p>
    <textarea name="comments" cols="20" rows="4">Enter your comments...</textarea> 
</form>
```

**When displayed in a browser:**

<form action="http://www.example.com/comments.php"> 
    <p>What did you think of this gig?</p>
    <textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
     
</form>

<br>

* **`<textarea>`** element

    * This element is used to create multi-line text input. The `<textarea>` element has opening and closing tags. Any content wrapped by the tags will appear in the text box when the page loads.



### **Submit Button**

```html
<form action="http://www.example.com/subscribe.php"> 
    <p>Subscribe to our email list:</p>
        <input type="text" name="email">
        <button type="submit">Subscribe</button> 
</form>
```
<!-- type in the boxes -->

**When displayed in the browser:**

<form action="http://www.example.com/subscribe.php"> 
    <p>Subscribe to our email list:</p>
        <input type="text" name="email">
        <button type="submit">Subscribe</button>
</form>

<br>

- The **`<button>`** element on a form may use one of the three `type` attribute values:

* **`type="submit"`**

    * The submit button is used to send a form to the server.

* **`type="reset"`**

    - This will automatically clear the form of all data.

* **`type="button"`**

    - Does not have a default behavior and mostly intended to be used with JavaScript.


Let's create a form together following the steps below. Add a new HTML file to you *Resources* repo. `Forms-demo.html`

<!--
1. Establish global document structure

2. Add a heading and small caption about the form

3. Add the form element

4. Add input elements to for username password

5. Add a submit button

5. Create another form

6. Add input elements for multiple lines of text
-->