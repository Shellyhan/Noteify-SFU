# SFU Noteify

**Contributor:** Lily Doo - Melissa Wang - Wei Wang - Xue (Shelly) Han

Noteify is a web application for Simon Fraser University students of all faculties where we can easily share course notes online. This is beneficial in situations where students want to help their classmates whom have difficulty taking good notes, cannot attend classes for various reasons such as medical conditions and emergencies, or just want to supplement their own study materials.

NOTE: This is a course based project. Website is only deployed locally. For info, please refer to project poster. For demo, please contact shellshell456@gmail.com. Thank you!

---
---

## 1. SETUP

1. `vagrant plugin install vagrant-librarian-chef-nochef`
2. `vagrant up`
3. http://localhost:8080  

You can register your own account and/or sign in with existing accounts using our SFU IDs at the top of this README (e.g. ldoo@sfu.ca). You can also sign in to an admin account with **admin@sfu.ca**. The password for all the accounts is **password1**.

---

## 2. FEATURES

- Register an account and sign in
- Upload PDFs to create, view, edit, and delete notes
- Annotate notes
- Rate notes from 1 to 5 stars
- Comment on notes and vote on comments with a thumbs up or thumbs down
- Flag notes for inappropriate content for the admin to look at
- Search, filter, and sort through a list of public and private notes
- View and edit your profile page
- Add friends to share private notes
- Receive friend request notifications

### 2.1. Administrator Accounts

In addition to the features above, administrator accounts can access a management page via the navigation bar's dropdown menu that includes the following features:
- Edit and delete users
- Create, edit, activate/deactivate, and delete departments, courses, and professors
- Edit notes and delete inpropriate content based on user reports

---

## 3. IMPLEMENTATION

We chose Ruby on Rails as our full-stack framework to implement Noteify because it is great for rapid prototyping, supports good web development practices such as the Model-View-Controller (MVC) framework and RESTful resources, and supports a wide variety of third-party Ruby libraries known as gems.

### 3.1. Gems

- **actioncable:** Framework for real-time communication over WebSockets. It is used in Noteify to manage friend request notifications.
- **bootstrap-sass:** A front-end framework for developing responsive websites used in conjunction with Sass, a CSS extension that simplifies writing CSS.
- **cancancan:** Authorization library that restricts what resources a given user is allowed to access such as editing notes. All permissions are centralized in the [Ability class](/app/models/ability.rb) to keep the code DRY (Don’t Repeat Yourself).
- **coffee-rails:** JavaScript-enhanced language used with Rails to compress CSS and JavaScript assets. It is used in Noteify to manage note page navigation, annotations, note ratings, and dropdown menus.
- **devise:** Authentication library that provides several modules such as registration and login validation that are used in Noteify.
- **filterrific:** Querying library that makes it easy to search, filter, and sort Noteify notes (ActiveRecord^1 objects) by relying on ActiveRecord scopes for building database queries.
- **jquery-rails:** JavaScript library that Bootstrap uses to add functionality to its components.
- **jquery-ui-rails:** User interface library with UI interactions, effects, widgets, and themes built on top of jQuery. It is used in Noteify for dragging and resizing note annotations.
- **paperclip:** File attachment management library that manages file uploading and processing. It is used in conjunction with ImageMagick, an image manipulation tool that Noteify uses to convert notes from PDF to JPEG. Paperclip is used in Noteify for creating user avatar and note thumbnails.

^1 *ActiveRecord* is a Ruby library for working with relational SQL databases.

---

## 4. REFERENCES

### 4.1. Fonts
- **Blue Fires:** DaFont [[link](http://www.dafont.com/blue-fires.font)]
- **DINPro Regular:** FreakFonts [[link](http://freakfonts.com/free/dinproregular2320.html)]

### 4.2. Images
- [**divider.png**](/app/assets/images/divider.png): SFU CourSys [[link](https://cas.sfu.ca/cas/login)]
- [**session-banner.jpg**](/app/assets/images/session-banner.jpg): Pexels (free stock photos) [[link](https://static.pexels.com/photos/7096/people-woman-coffee-meeting.jpg)]
- [**sfu-logo.png**](/app/assets/images/sfu-logo.png): SFU CourSys [[link](https://cas.sfu.ca/cas/login)]
- [**textured-bg-tile.png**](/app/assets/images/textured-bg-tile.png): SFU CourSys [[link](https://cas.sfu.ca/cas/login)]

### 4.3. Source Code
- [**Gems**](Gemfile): RubyGems [[link](https://rubygems.org/)]
- **jQuery Raty:**  GitHub (star rating plugin) [[link](https://github.com/wbotelhos/raty)]
- **Loading Wheel:** W3Schools [[link](https://www.w3schools.com/howto/howto_css_loader.asp)]
- **Responsive Bootstrap Tabs:** Stackoverflow [[link](https://stackoverflow.com/questions/25855428/make-bootstrap-3-tabs-responsive)]
