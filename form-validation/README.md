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
