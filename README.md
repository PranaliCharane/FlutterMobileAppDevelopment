# Step 1
Clone the repository using the given link

# Step 2
Install all the dependencies using 
`flutter pub get`

# Step 3
use `flutter run` to start the project

# Video for this project
`https://drive.google.com/file/d/1KfOv2ytKCa8__46dnwKd5ViH1y7QBNaQ/view?usp=sharing`

# expense_app
A complete expense app that tracks expenses based on categories and displays the pie chart of categories.
also displays the line chart for weekly transactions.

now let's start from scratch.
delete all the default code from main.dart.

# first_screen
create a dashboard.
add it to our 'main.dart'.

now let's create some models and constants.
we need to generate the icons.
to do that let's define some initial properties.
now let's create another model that will define a expense.

now let's create a database.
import sqflite and the path package.
now we can fetch the categories from the database.
since we are using a native feature(storage and database) of android.
we need to reinstall our app.

now let's setup our 'category_screen' to fetch the categories.
for passing data and managing state we are going to use provider package.
let's make our 'database_provider' a provider class.
with that we can see our category list.
let's separate some widgets to organize our code.

now let's work on adding some expenses to categories.
now let's create a form for adding expenses.
so we can add expenses now.
let's see if they persist.
as you can see the data is still there.
a problem is still there.
ok let's modify the logic.
let's see.
now it works.

now let's work on our second screen.
expense screen  where we can see our expenses.

there was an issue where the totalAMount being 0 at the start of our app.
it happened because we didn't fetch the expenses on starting of our app so our in-app
'_expenses' was empty. that's why the totalAmount was not working.

let's reinstall the app and add some entries/expenses.


# second_screen
let's create our second screen.
to reach the second screen we need an action from somewhere.

we passed an argument because we will fetch the expenses based on the category.
let's fetch the expenses.

now that we can see the expenses.
let's format the date and the currency.
we will use the intl package.

with that it looks good.

now let's start working on charts.
for that we will use fl_chart
with that our total_chart is working.

now let's start working on our expense chart inside the expense screen.
in this chart we will show the last week's expenses.
let's calculate last week's expenses.
let's add some more expenses of different date.
it's showing it in reverse.
that looks good.
let's start on titles.
with that our expense chart looks good.

now let's add another screen to show all the transactions.
let's add some actions to access the all expenses screen

now let's create a search function for this screen.
let's implement the search method.
let's take a look at method.
with that it works.

# delete_logic
now that I see it, we don't have a method for deleting the expenses.
let's fix that.
we should make it dynamic but for now let's keep it.
it's working.

now our app is working fine but there is still an issue when it loads for first time.
let me show what that is.

when the app starts, there is no pie chart, 'NaN' everywhere.
let's fix that.

now one more thing.
when we delete an entry, it get's deleted without warning.
let's fix that.

that takes care of it.
