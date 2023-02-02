# CMPUT404-Lab-4-Django
Follows this https://uofa-cmput404.github.io/lab-4-django.html and parts 1-4 of https://docs.djangoproject.com/en/3.1/#first-steps

**Question 1: What is the link to your github repository for this lab?**
- https://github.com/Sean-Meyers/CMPUT404-Lab-4-Django

**Question 2: After starting a brand new Django application and running the runserver command, what does the browser show you?**
- It shows me a page with a fancy rocket that says "The install worked successfully! Congratulations! You are seeing this page because DEBUG=True is in your settings file and you have not configured any URLs." It has links to Django documentation, tutorial, and community, and release notes.

**Question 3: After creating the first view within polls, what does the browser show you when navigating to / and to /polls respectively?**
- / gives me a 404 page, /polls gives me the hello world text we wrote.

**Question 4: What is a Django migration and why do we need them?**
- Migrations allow changes made to our models to be reflected in the database.

**Question 5: What do you see after you log into the Django adminstration site? From a high levle, how do you get custom models to appear in the Django admin page?**
- I see an authentication table and a table for the polls app. In the polls app table, the custom models are displayed. There are buttons beside them to allow me to make changes and add entries. To get the models to appear in the admin page, I need to register them in the admin.py file.

**Question 6: What do you see when you go to /polls/38/ in your browser? What about /polls/38/results and /polls/38/vote? What happens when you don’t put a number, and instead use a string? How would you modify the urls.py file to allow arbitrary alphabetic characters?**
- It displays the views we made, which is currently comprised of text that specifies what the page is (eg results, vote, nothing), and what the question number is. with an arbritrary string, I get a 404. To not get the 404, I would need to specify a str instead of int in the path string in the urlpatterns array item.

**Question 7: Why is it a bad idea to hardcode urls into the templates?**
- It's hard to change urls on projects with many templates if they are hardcoded into the templates.

**Question 8: What are the benefits of using Django's generic views over writing views 'the hard way'? When should you use a generic view and when shouldn't you use a generic view?**
- Using generic views can allow us to avoid reinventing the wheel for commonly used layouts, which will save time and keep our code shorter. There's also the maintainability advantage that comes with the shorter code and the fact that these views are standardized django. We probably don't want to use generic views if we would have to modify them significantly in order to get what we want. Generally, we also should not use them if the project is already using non-generic views, as refactoring everything would be more work than it's worth potentially.
