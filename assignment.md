Angular Messaging Format:

Angular Messaging format is a module that allows you to easily scale your messaging for your web application. What this means is you use Angular Messaging format to conditionally display messages to the end user based on gender, pluralism and possibly locale. A sample code snippet provided on the Angular documentation site illustrates the use case for this module:

<div ng-controller="AppController">
  Select Recipient:<br>
     <select ng-model="recipient" ng-options="person as person.name for person in recipients">
     </select>
     <p>{{recipient.gender, select,
               male {{{recipient.name}} unwrapped his gift. }
               female {{{recipient.name}} unwrapped her gift. }
               other {{{recipient.name}} unwrapped their gift. }
     }}</p>
</div>

As you can see from the code snippet above, a different message will be displayed based on the gender of the recipient. This could be extremely powerful and allow you to make your user experience customized.

To install this using npm issue the following statement:

npm install --save angular-message-format@X.Y.Z

You must then include the angular-message-format.js in your HTML like so:

<script src="path/to/angular.js"></script>
<script src="path/to/angular-message-format.js"></script>

And after that is complete load the module in your application by adding it as a dependent module:

angular.module('app', ['ngMessageFormat']);

Reference:

https://docs.angularjs.org/api/ngMessageFormat
