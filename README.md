# Specification
This project provides an implementation using Java of a Recipe book program that can be used and added to by Users.
Users of the program have the following access and capabilities when using the recipe book.
* Manually adding a new *Dish* to the *Recipe Book* from within the program. For example, adding 'Pepperoni Pizza' to the *Recipe Book* during runtime.
* View *Dishes* inside the recipe book with search functionality
* Reading *Dish* information from a specifically formatted file and adding to the *Recipe Book*
* Searching for a *Dish* or Dishes in the *Recipe Book* by name, favourites, cook time, user preferences, certain attributes (Vegetarian, Non-Vegetarian, Vegan)
 and whether it contains certain *Ingredient*(s) (eg: Searching for dishes that contain *Potato*)
* Create favourites and preferences for the *User* within the program which can then be used with search functionality to sort through recipes
* Serialize the recipe book via a database

Each *Dish* in the *Recipe Book* must store information such as name, *Ingredient*(s), cook time, attributes (Veg, Non-Veg, etc.) and
cooking instructions.
These can either be input manually during runtime by the user or uploaded through a file. The structure splits each dish by the @ symbol in the file.

Each *User* will be able to add dishes to the communal *Recipe Book* (If allowed access) and have their own implementation of *favourites* and *Preferences*
When a new *User* is created, the program will ask for and store *Preferences* but these can be edited at anytime in the program
These can be saved as well as the current status of the dishes and ingredients known to the recipe book.\
*IMPORTANT*: Since the program will be tested without our assistance, we have decided to allow the User to give themselves editorial access, since otherwise the TA would have to email us in order to gain access to the functionality

Commands:
* "end" terminates the program
* "create" creates a new user
* Entering a username that exist prompts a password entry
* UserConsole Commands:
  * "favourites" lists out the names of the dish the user has added to their favourites
  * "preferences" lists out the user's preferences
  * "add to preferences" adds a preference to the user's preferences
  * "remove from preferences" removes a preference from the user's preferences
* BookConsole Commands:
  * Typing in a name of a dish or ingredient will show its description. If there's a dish and an ingredient sharing
    * the same name, the dish is displayed. The user can use "view ingredient" to view the ingredient
  * "search" starts a search function with difference search filters
    * -n dishname : returns a list of dishes containing dishname in their names
    * -p : returns a list of dishes matching the user's preferences
    * -t time : returns a list of dishes with cook time less than or equal to time
    * -i ing1/ing2/... : returns a list of dishes with ing1, ing2, ... as their ingredients
    * -a att1/att2/... : returns a list of dishes with att1, att2, ... as their attributes
    * EXAMPLE: search -n burger -t 15 -i lettuce/pickles -a vegan
      * this will return a list of dishes that has "burger" in its name, cook time no more than 15 minutes,
      * lettuce, pickles as ingredients, and the vegan attribute.
  * "view dishes" lists out the dishes in the dish manager
  * "view ingredients" lists out the ingredients in the ingredient manager
  * "view ingredient" allows user to input the ingredient name to view attributes of the ingredient
  * "favourites" lists out the favourite dishes of the user
  * "add to favourites" adds a specified dish to the user's favourites list
  * "remove from favourites" removes a specified dish from the user's favourites list
  * "preferences" shows the dishes matching the users preferences
  * "create dish" starts the dish creator
  * "create ingredient" starts the ingredient creator
