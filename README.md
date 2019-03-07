# Notes for Angular Architecture
<img src="https://github.com/latreta/angular_notes/blob/master/1_22skrCDLM6C3oRTuIecIng.png">

# App Overview
- What is the application for?
- What are the goals? 
- How is the client going to use it?

# App Features
- For sure that this depends if you’re using a waterfall or agile approach, but you should know some of the features.

# Domain Security
- What is the domain security?
- Are you using rules on the server side?
- How are those going to be communicated down to your Angular app?
- How your app will communicate with your APIs?

# Domain Rules
- What rules do you have?
- These rules going to run client side or again on the server? Or both?

# Services/Communication
- How is the app going to talk to the server? Most of the time you will use HTTP concepts. However, in some scenarios you maybe need to use WebSockets.
- Well that’s good to know how data is exchanged between not only the back end and the front end, but even between services and components in your Angular app.

# Data Models
- What’s the data from the API?
- What are we passing to components?
- Are we getting what we want from the API? So, we need to think in what’s the most efficient way to get data passed around throughout the app.

# Feature Components
- How are our features and how are we structure our components? Imagine if two features can be alive at the same time in the app and they need to communicate, how are they going to do that in a loosely coupled way?

# Shared Functionality
- What shared functionality do we have?
- Are we using third-party components, such as Angular Material or Ng Bootstrap?
- Are the shared functionality just sharable in this one app or could it be reusable?

# Unit Testing
- Are we using the built-in CLI tools? Karma test runner.

# End-to-end testing
- What are we doing for this?
- Are we using Protractor or the newest Cypress? 
- This might actually influence how you design your code as well, because your end-to-end testers (if do you have a team for that) they may prefer to have IDs on some of your tags to make them easier to find for the test.

# The core module(Recommended by the Angular Style Guide)
- Core really is designed for your singleton type of services, anything that would be shared throughout the app and obviously any singleton would be good for that. 
- Services that are specific to a feature can go in the feature folder. Make a subfolder, call it services, put that in the feature folder and then that particular service would just be imported or provided directly into the feature module. This only make sense if this service will not be reused elsewhere.

# The shared module(reusable components, pipes, directives and so on)
- An important distinguishing factor of this is will the component, pipe or directive be only used in this app or could it be used across apps?
- Is it so generic that you could reuse it over and over?
- If that’s the case, don’t put it in shared. That’s when we want to talk about creating an Angular library.
- So, shared modules would normally be imported potentially multiple times. Core modules on the other hand, should only be imported once and that should only happen into the root.
