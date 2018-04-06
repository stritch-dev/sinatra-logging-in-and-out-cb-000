# Sinatra Sessions Lab - User Logins


DONE Users class has a username, password, and balance (a decimal storing their bank account balance). 
 
DONE `rake db:migrate` and
DONE `rake db:seed` once your User migration and model are in place.

DONE  login form on the index page that accepts 
    DONE username
    DONE password 
  DONE sends  `POST` 
  DONE action of `/login`.

DONE * In the controller action that processes the `POST` request, find the user in the database based on their username.

DONE * If there is a match, set the session to the user's ID, 
    redirect them to the `/account` route (using `redirect to`), 
    and use ERB to display the user's data on the page.

DONE * If there is no match, render the error page.

DONE * On the `/account` page, set up a link called 'Log Out' that clears the
  session.

* In `app/helpers/helpers.rb`, you'll notice a predefined `Helpers` class. In
  this class, you'll want to define two **class** methods, `current_user` and
  `is_logged_in?`.

* `current_user` should accept the session hash as an argument. This method
  should use the `user_id` from the session hash to find the user in the
  database and return that user.

* `is_logged_in?` should also accept the session hash as an argument. This
  method should return true if the `user_id` is in the session hash and false
  if not. The Ruby `!!` operator will come in handy here.

* In `account.erb`, you'll want to use the `is_logged_in?` helper method to
  only display the username and account balance if the user is logged in.
  Otherwise, it should contain a link to the home page. You'll also want to use
  `current_user` to display the username and balance.

