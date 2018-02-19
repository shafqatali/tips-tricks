# Form validation using basic Javascript for all type of input fields
You can use this library to validate all types on input using basic Javacsript. This library is flexible and allow developers to set custom messages during initlization. This library doesn't require jQuery or anyother Javascript library to validate input fields.

## Features
  - Allow custom messages using data attribue in input field tag
  - Allow pattern base validation to use for input field
  - Allow custom messages during initlization
  ```HTML
  <input type="text" class="form-control" id="exampleName" placeholder="Name" pattern="[a-z]{1,15}" data-require-error="Name is required" data-pattern-error="Username should be lower case upto 15 characters" required>
  ```

### How to Initilize library
 ```HTML
 <form id="validateForm">
    <div class="form-group">
    <label class="control-label" for="text1">Sample Text</label>
    <input type="text" class="form-control" name="sample text" id="text1"
 placeholder="Enter Text" required>
    </div>
</form>
 <script>
    document.getElementById('validateForm').validateForm({
        invalidEmail: "Please enter a valid email address",
        invalidNumber: "Please enter a number between 1 to 100",
        invalidPhone: "Please enter a valid phone number.",
        invalidOption: "Please select at least one option",
        invalidCheckbox: "Please check the checkbox",
        invalidRange: "You have entered a number that is not valid",
        successClass: "has-success",
        errorClass: "has-error",
        closestTagSelector: ".form-group",
        messageWrapperTag: "<span class='help-block'></span>"
    });
</script>
 ```
 For detail information please see this [file](https://github.com/shafqatali/tips-tricks/blob/master/form-validation/js/form-validation.js)

It's not necessary to pass all the properties, each property has its default value defined in Javascript library. If you pass the value during initilization then it will override the default value otherwise the default value will be used.

##Customize Styling for errors and success state
By default "has-error" and "has-success" classes are being used in styling. If you want to change classes to style you can do this by setting the class names to these properties
 - successClass
 - errorClass
 You can also change the default selector hook being used in library by setting this property during initlization
 - closestTagSelector
You can also customize the HTML markup for error messages by setting this property 
 - messageWrapperTag: Please ensure a valid HTML markupm cannot be nested i.e <div><span></span></div>
 - 
 
Feel free to send your feedback/suggesstion/enhancements for this library.
