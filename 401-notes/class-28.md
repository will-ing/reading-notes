# Django Forms

* Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models)
* The view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed).
* What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.
* The declaration syntax for a Form is very similar to that for declaring a Model,

* `required`: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.
* `label`: The label to use when rendering the field in HTML. If a label is not specified, Django will create one from the field name by capitalizing the first letter and replacing underscores with spaces (e.g. Renewal date).
* `label_suffix`: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other character(s).
initial: The initial value for the field when the form is displayed.
* `widget`: The display widget to use.
* `help_text` (as seen in the example above): Additional text that can be displayed in forms to explain how to use the field.
* `error_messages`: A list of error messages for the field. You can override these with your own messages if needed.
* `validators`: A list of functions that will be called on the field when it is validated.
* `localize`: Enables the localization of form data input (see link for more information).
* `disabled`: The field is displayed but its value cannot be edited if this is True. The default is False.


[Main Page](https://will-ing.github.io/reading-notes)