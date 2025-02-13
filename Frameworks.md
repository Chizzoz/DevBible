# Frameworks
![Frameworks](https://github.com/gabru-md/DevBible/blob/master/assets/frameworks.png?raw=true)


While writing everything from scratch is amazing, practical development work involves quick learning of Frameworks and their best practices to reduce development time and re-use highly maintained code as a dependency to your project.

We can't possibly teach every framework, hence we first propose an approach for learning frameworks followed by nice resources for the same.

## Approach

* We believe that in today's world learning any framework requires hands-on experience and good quality tutorials. Books make sense for sure, but who has time for them ?
* Follow API docs of the Framework, it should suffice in most cases.
* Websites like YouTube, [egghead](http://egghead.io) etc are great for learning new things.
* Once you have basic idea, create something, something that involves most of the concepts. For UI related APIs create a TodoList App for example.
* Do have a look at [awesome](https://github.com/sindresorhus/awesome) repo of the same on Github. For example [awesome-swift](https://github.com/matteocrippa/awesome-swift) has some nice sources for learning Swift.

Now we look at popular libraries and frameworks.

### [React](https://facebook.github.io/react)
![React](https://github.com/gabru-md/DevBible/blob/master/assets/reactOS.png?raw=true)

React isn't really a framework, it's a library, however it isn't used as is in practical world.

React technically is a library for "View" part of your MVC, i.e. its responsibility is to create interactive views based on your data.
You can say View is a function of data and events. React is the function that implements it.

  ```
View = React(data, events)
  ```

  It allows you to create composable Components that can talk to each other, and can maintain state of their own. Based on several functional programming concepts, React has created an ecosystem which is redefining the way we look at UI. Same approach is extended to desktop and mobile applications today ([React Native](https://facebook.github.io/react-native))


#### Tools

  React and ES2015+ is infamous for requiring a lot of tools. However,
  we recommend using online bins like [webpackbin](http://webpackbin.com) or [esnextbin](http://esnextb.in) for
  writing code directly without setting up tools like Webpack, Babel etc.

#### Videos

  * [Intro Video](https://egghead.io/lessons/react-core-concepts-of-react-components-props-and-state) - Quick video to get basic idea

  * [Intro Series](https://www.youtube.com/watch?v=walnw4n8vSY&list=PLs0HJRuXPAqtG4P-YBUPYWpH1M6j5J60-) - Quick video series to understand basic idea *deeply*.

  * [Crash Course](https://www.youtube.com/watch?v=DfRibIkjhew) - Covers hell lot: Webpack/Babel/React/Router/Redux/React-Redux

  * [React Router](https://egghead.io/series/getting-started-with-react-router) - A nice brief playlist to get you started with React-Router

  * [React + Redux](https://www.youtube.com/playlist?list=PLQDnxXqV213JJFtDaG0aE9vqvp6Wm7nBg) - Watch this one for practical usage of redux, skip react part as by now you would be cool with it

  * [Redux](https://egghead.io/series/getting-started-with-redux) - For deep understanding of Redux from the author himself.

### [Meteor](https://github.com/meteor/meteor)
![Meteor](https://guide.meteor.com/images/logo-coralspace-left.svg)

Meteor is a Node-based full-stack framework which allows to create reactive webapps, that could easily be ported to Android and iOS platforms.
Reactive webapp implies real-time behaviour: There is a continuous connection between the client and server side, and so, a change made in application by any means(direct entry in database, from server, or even by a client) is reflected on every instance of the application without any page reload.

Meteor is based on Websockets(sockJs). In Meteor, the client talks to server over DDP(Distributed Data Protocol), which is like "REST" for websockets. For websockets.

Meteor has its own package manager(Atmosphere) that seperates it from the rest of Node universe. However, NPM packages could be easily wrapped as a Meteor package.

It allows to create simple apps really fast since, most of the configuration comes packed. This makes it ideal for hackathons :P
It doesnot follow any strict development model (like MVC) and the files can be placed as we would like.

Meteor by default uses Blaze templating system that resembles Handlebars, and is really simple to build upon. It now supports Angular and React templating systems as well.

#### Tutorials and References
  * https://www.meteor.com/tutorials/blaze/creating-an-app
  * https://github.com/ericdouglas/Meteor-Learning

#### Essential Packages
  * https://github.com/aldeed/meteor-collection2
  * https://github.com/iron-meteor/iron-router
  * https://github.com/meteorhacks/npm
  * https://github.com/alanning/meteor-roles
  * https://github.com/arunoda/meteor-up/tree/mupx

### [Django](https://www.djangoproject.com/)
![Django Framework](https://github.com/gabru-md/DevBible/blob/master/assets/_django.png?raw=true)

Django is a full featured web applications framework for Python that allows for rapid development. It achieves
this by including a vast number of features that prevent developers from reinventing the wheel. This helps enforce a
don't repeat yourself (DRY) principle where components can be reused and pluggable, which allow developers
the option to share components and enhance their apps functionality. Arguably, Django is the most
popular web framework for Python and is adopted by many well-known sites such as Pintrest, Mozilla and Disqus.

At its core Django follows a Model View Template (MVT) pattern. The model provides the way the data is structured within
the database. Represented as a Python class, the model is the single definitive source of information about the data and handles
the creation of the database table. In order to interface with the database, Django provides an object relational mapper (ORM).
This allows database queries to be constructed by interfacing with a Python object rather than communicating directly with
the database by constructing SQL queries.

The view handles all the logic required to process requests and return the proper response. This includes the ability to
define URL endpoints, handle file uploads and serialize the data returned in the response. In general, data is
retrieved by constructing a ORM query through a model object. The result is passed to the response in the form of a
context. Typically, the code will load a template which uses the context as a dictionary that maps template variable
names to Python objects.

The template defines the overall presentation of the data. This defines how the front end will look when a user receives
the response from the view. Templates are powerful, because they reduce the need to repeat code on the front end.
Templates have their own syntax that introduces logic and variables within the typical HTML markup. This makes it possible
to access the content of the context. For instance, one can loop through all the data of a query while applying the
correct styling. Lastly, templates can import from a base template, which allow common elements, such as a navbar, to be
written once and plugged where needed.

Django also includes more advance features such as an administrative interface, user authentication and a caching
framework. Additionally, Django's features can be extended further through third party apps. Some popular choices
include the Django Rest Framework (DRF), Channels, Elasticsearch and Celery.


#### Tutorials and References
  * http://www.tangowithdjango.com
  * https://tutorial.djangogirls.org
  * https://docs.djangoproject.com/en/1.10/intro/tutorial01

#### Essential Packages
  * http://www.django-rest-framework.org
  * https://github.com/django/channels
  * https://django-endless-pagination.readthedocs.io/en/latest
  * http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html
  * https://github.com/liberation/django-elasticsearch

### [Express](https://www.expressjs.com/)

Express is a minimalist web applications framework for Node. It is a great solution for single page applications, web sites, hybrids, or
public HTTP APIs. It is the most popular web framework for Node and is used by companies like Uber, Paypal and Paytm.

Express can be used to follow the Model View Controller (MVC) pattern but is not a MVC framework by itself. 
The contoller is used to process the requests and return appropriate response. It helps to define URL endpoints, send the response in appropriate format, interacting with databases and authentication.

The model provides the way the data is structured within the database. **Express does not come with an ORM or an ODM** but you can use 
various packages to connect with a database by writing either raw SQL queries or in the form of JavaScript classes and functions. 

The views defines the overall presentation of the data as rendered by the browser. This defines how the front end will look 
if a user receives an HTML response from the controller. They help in populating templates with the relevant data (like user name, profile
picture) without having to write one for each. Templates have their own syntax that introduces logic and variables within the typical HTML
markup. Express gives a choice of using one of 24 templating languages depending on your needs. Templates can import from a base template, 
which allow common elements, such as a navbar, to be written once and plugged where needed.

Express aims to give the bare essentials so that users have the choice to create what they want. For features like user authentication, 
caching, csrf protection etc you have to include other packages.

#### Tutorials and References
  * https://expressjs.com/en/4x/api.html
  * https://www.codeschool.com/courses/building-blocks-of-express-js
  * https://www.freecodecamp.com/challenges/build-web-apps-with-expressjs
  * https://github.com/azat-co/expressworks

#### Essential Packages
  * http://expressjs.com/en/resources/middleware.html
  * http://mongoosejs.com/
  * http://knexjs.org/
  * http://passportjs.org/
  * https://www.npmjs.com/package/nodemon
  * https://nodemailer.com/


### [Flask](http://flask.pocoo.org/)
![Flask](https://github.com/gabru-md/DevBible/blob/master/assets/flask.png?raw=true)

Flask is a micro web framework written in Python and based on the Werkzeug toolkit and Jinja2 template engine.

Flask is a really cool Web Development framework for Python designed by POCCO. It is easy to learn and master!


"It came out of an April Fool's joke but proved popular enough to make into a serious application in its own right." - as quoted by
Armin Ronacher of Pocoo, who created FLASK.
In mid 2016 Flask was the most popular Python Web Development framework on GitHub.

Flask is called a micro framework because it does not require particular tools or libraries. It has no database abstraction layer, form
validation, or any other components where pre-existing third-party libraries provide common functions. However, Flask supports
extensions that can add application features as if they were implemented in Flask itself. Extensions exist for object-relational 
mappers, form validation, upload handling, various open authentication technologies and several common framework related tools. 
Extensions are updated far more regularly than the core Flask program.

### Features

  * Contains development server and debugger
  * Integrated support for unit testing
  * RESTful request dispatching
  * Uses Jinja2 templating
  * Support for secure cookies (client side sessions)
  * 100% WSGI 1.0 compliant
  * Unicode-based
  * Extensive documentation
  * Google App Engine compatibility
  * Extensions available to enhance features desired
  
### Tutorials
  * https://goo.gl/agwmmq - Tutorials by sentdex!
  * http://flask.pocoo.org/
  * https://www.tutorialspoint.com/flask/
  * http://flask.pocoo.org/docs/latest/tutorial/
  * https://www.fullstackpython.com/flask.html
  * https://pythonspot.com/en/flask-web-app-with-python/
  * https://hackr.io/tutorials/learn-flask
  


### [OpenCV](http://opencv.org/)
![OpenCV](https://github.com/gabru-md/DevBible/blob/master/assets/opencv.png?raw=true)

OpenCV (Open Source Computer Vision) is a library of programming functions mainly aimed at real-time computer vision. Originally 
developed by Intel, it was later supported by Willow Garage and is now maintained by Itseez. The library is cross-platform and free 
for use under the open-source BSD license.

It is particularly difficult to say whether OpenCV is a framework or a tool.
But what is important is to learn it and try to master it.

It has C++, C, Python and Java interfaces and supports Windows, Linux, Mac OS, iOS and Android. OpenCV was designed for computational 
efficiency and with a strong focus on real-time applications. Written in optimized C/C++, the library can take advantage of multi-core 
processing. Enabled with OpenCL, it can take advantage of the hardware acceleration of the underlying heterogeneous compute platform.

Cool! isn't it?

### Features

#### Applications

  * 2D and 3D feature toolkits
  * Egomotion estimation
  * Facial recognition system
  * Gesture recognition
  * Human–computer interaction (HCI)
  * Mobile robotics
  * Motion understanding
  * Object identification
  * Segmentation and recognition
  * Stereopsis stereo vision: depth perception from 2 cameras
  * Structure from motion (SFM)
  * Motion tracking
  * Augmented reality

#### Machine Learning Features

  * Boosting
  * Decision tree learning
  * Gradient boosting trees
  * Expectation-maximization algorithm
  * k-nearest neighbor algorithm
  * Naive Bayes classifier
  * Artificial neural networks
  * Random forest
  * Support vector machine (SVM)


### Tutorials

  * http://docs.opencv.org/master/d9/df8/tutorial_root.html
  * www.tutorialspoint.com/opencv/
  * https://goo.gl/cYqM5Y
  
  These are some Machine Learning Tutorials to start with
  
  * https://goo.gl/w7aObb
  * https://goo.gl/EzqOPN


### [Laravel](https://laravel.com/)
![Laravel](./assets/laravel_6.png)

Laravel is a free, open-source PHP web framework, created by Taylor Otwell and intended for the development of web applications following the model–view–controller (MVC) architectural pattern. Some of the features of Laravel are a modular packaging system with a dedicated dependency manager, different ways for accessing relational databases, utilities that aid in application deployment and maintenance, and its orientation toward syntactic sugar.

As of March 2015, Laravel is regarded as one of the most popular PHP frameworks, together with Symfony, CodeIgniter, Yii2 and others.

The source code of Laravel is hosted on GitHub and licensed under the terms of MIT License.

### Features
  * Expressive, beautiful syntax.
  * Modern toolkit. Pinch of magic.
  * Amazing ORM
  * Routing
  * Queue library
  * Simple authentication

#### Tutorials and References
  * https://laravel.com/docs/master/installation
  * https://laracasts.com/series/laravel-5-fundamentals
  * https://www.youtube.com/watch?v=oltgtexDbdo&list=PLnBvgoOXZNCP2LEKmvu2W-eUkO-DYn0TL

  #### Essential Packages
  * https://github.com/spatie/laravel-backup
  * https://github.com/spatie/laravel-activitylog
