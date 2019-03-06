# angular_notes
How to plan your architecture

# App Overview
What is the application for? What are the goals? How is the client going to use it?

# App Features
For sure that this depends if you’re using a waterfall or agile approach, but you should know some of the features.

# Domain Security
What is the domain security? Are you using rules on the server side? How are those going to be communicated down to your Angular app? How your app will communicate with your APIs?

# Domain Rules
What rules do you have? These rules going to run client side or again on the server? Or both? Normally we do this at the both sides, but you should plan those type of things.

# Services/Communication
How is the app going to talk to the server? Most of the time you will use HTTP concepts. However, in some scenarios you maybe need to use WebSockets. Well that’s good to know up front because that’s going to change some of the architecture on how data is exchanged between not only the back end and the front end, but even between services and components in your Angular app.

# Data Models
What’s the data from the API? What are we passing to components? Are we getting what we want from the API? Sometimes not. So, we need to think in what’s the most efficient way to get data passed around throughout the app.

# Feature Components
How are our features and how are we structure our components? Imagine if two features can be alive at the same time in the app and they need to communicate, how are they going to do that in a loosely coupled way?

# Shared Functionality
What shared functionality do we have? Are we using third-party components, such as Angular Material or Ng Bootstrap? Are the shared functionality just sharable in this one app or could it be reusable?

# Unit Testing
Are we using the built-in CLI tools? We can use the Karma test runner, things like that.

# End-to-end testing
What are we doing for this? Are we using Protractor or the newest Cypress? 
This might actually influence how you design your code as well, because your end-to-end testers (if do you have a team for that) they may prefer to have IDs on some of your tags to make them easier to find for the test.
