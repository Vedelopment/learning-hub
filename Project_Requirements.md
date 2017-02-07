# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Project 2 - Rails Group Project

**Read this entire document before writing a line of code.**

## Overview

For this project, you will use your knowledge of front-end and back-end web development to produce a polished Rails web application that can be used by friends, family, or the wider online community -- and that will benefit your portfolio.

**You will be working in groups of 3-4 for this project.**

## Deliverables

### Project Planning Deliverables

**You must review the following with your instructional team BEFORE you start to code.**

* **Motivation:** Who is your user? How will your app help them solve a problem or achieve a goal?
* **Scope:** What are you planning to build? What do you reasonably think you can implement in the time period?
* **User Stories:** What will users be able to do with your app? 
* **Wireframes:** Sketch out what your core pages will look like and how they will connect (site flow). Consider making a detailed *site flow diagram* or even a *paper prototype* to demonstrate and/or test key user interactions.
* **Data Models:** Draw out the models and any associations for your project in an entity relationship diagram (ERD).
* **Milestones:** Outline the milestones/sprints for your group.
* **Delegating Tasks:** How will you track and delegate tasks? How will you handle git and GitHub? Set up your project tracking in <a href="https://trello.com">Trello</a> or in some other organized, online format.

### Completed Project Deliverables

* Link to Heroku hosted project, with all core technical requirements and correct number of flexible technical requirements complete.
* Link to on each team member's personal site to the hosted project.
* A link on the GitHub repo to the hosted project. 
* A `README.md` file with the following:
  * Description: Short paragraph (2-3 sentences) "elevator pitch" describing what your project does
  * Wireframes and user stories (or a link to Trello with wireframes)
  * Link to Heroku-hosted project
  * Technologies (languages, external libraries, APIs)
  * Wish List / Future Development
  * Contributors (with links to their GitHub profiles)

## Technical Requirements

### Core Technical Requirements

**Your app should have all of the following:**

* **Rails:** Use Rails as the core framework for Ruby.
* **PostgreSQL:** Use PostgreSQL for your database in development and production.
* **Data Models** Include at least two data models with associations.
* **Data Validation:** Your application should validate incoming data before entering it into the database.
* **Error Handling:** Forms in your application should also validate data, handle incorrect inputs, and provide user feedback on the client side.
* **Views:** Use **partials** to follow DRY (Don’t Repeat Yourself) development in your views.
* **Home & About Pages:** Create a landing page (homepage) that clearly explains your app's value proposition and guides the user through the "get started" funnel. Create an about page that includes photos and brief bios of your team members.
* **User Experience:** Ensure a pleasing and logical user experience. Have at least one person from outside your team attempt to use your project, noting points of confusion.
* **Custom Styling:** Use the Asset Pipeline and your front-end skills to create custom styles with CSS or SCSS.   Use a framework like Bootstrap to enhance and ease your CSS styling.
* **Responsive Design:** Make sure your app looks great on a phone or tablet.
* **Heroku:** Deploy your app to Heroku. Ensure no app secrets are exposed. *Do not commit secret keys to GitHub!*

### Flexible Technical Requirements

**Your app should have 3 out of the 6 following options:**

* **Authentication & Authorization** Allow users to sign up, log in, log out, and access restricted portions of the site. 
* **External API** Use HTTParty or a third-party API gem to integrate third-party data into your app. Remember to hide secret keys!
* **JavaScript & jQuery:** Add dynamic behavior with event-driven functionality on the client side.
* **User-Friendly URLs:** Make "pretty" URLs that don't expose database IDs. Consider using a gem like FriendlyId.
* **Testing** Use `rspec-rails` and `shoulda-matchers` to write specs for any custom model methods and all model validations. Take it further with tests for controller actions. 
* **Additional Associations**  Incorporate more complex data with additional associated models. Carry through data valdiation and error handling for additional resource(s). 



## Further Exploration Ideas

If you want to push yourself and learn something new, optionally consider doing any of the following ideas. *Please talk to an instructor beforehand.*

* **AJAX** Use AJAX to communicate with the server without reloading the page, when appropriate.
* **Material Design:** Research the material design paradigm and apply it to ground your app's UI in the physical realm.
* **CSS Animations:** Use jQuery or animate.css to include animations on your site.
* **SASS/SCSS:** Write DRYer styles with a language that compiles into CSS, and take advantage of the asset pipeline to process them easily. 
* **Search:** Build a form that allows users to search your data, based on attributes. Consider looking into Elasticsearch to speed up queries.
* **Accessibility:** Research web accessibility (e.g. for blind users), and apply accessibility principles to your app.
* **File Uploads** Upload files with solutions like Paperclip, CarrierWave, or UploadCare.  Remember to hide secret keys!
* **Emails:** Use ActionMailer to send emails to your users.
* **Sessions:** Use sessions to store data for site visitors (who aren't necessarily logged in).
* **Charting:** Visualize your data! Possibilities include D3, Morris.js, Highcharts, Chart.js, and Google Charts.
* **Payment:** Use Stripe to allow your users to purchase from or donate to your site.
* **Job Scheduling:** Set up a job-scheduler like Delayed Job or Resque to queue actions that don't need to run immediately.
* **Text Messaging:** Use Twilio or a similar gem to send texts to your users (note: not free).
* **Whatever else you can think of!**



## Deadlines

* **Tuesday, February 7th, by 4:30pm** - [Project planning deliverables](#project-planning-deliverables) due! Get your project plan approved by end of day so you can get started coding!

* **Tuesday, Feburary 14th, 1:15pm** - [Completed project deliverables](#completed-project-deliverables) due and presentations!


<!-- 
## Presentation Guidelines

Each group will present their project on **Tuesday, Feburary 14th** starting at **1:15pm**. Please follow these guidelines:

* **Maximum 20 minutes.**
* **Minimum 5 slides.** 
* **Presentation should include:**
  * Who is the user?
  * Motivation for building this project
  * Wireframes
  * User stories
  * ERDs
  * Demo of some interesting feature, something unique or creative your group chose to do
  * Walk through the development of one feature from ideation to execution. At minimum, this should include wireframes, code samples, and the final result.
  
**Each member of your group should speak for equal parts during your presentation** and mention which parts of the project they worked on.
-->

## Project Feedback

See the [feedback doc](./project2-feedback.md) for details.
