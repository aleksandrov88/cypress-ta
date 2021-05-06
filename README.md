##The approach

The project is organized:

specs - In this folder are located tesing scenarios. 

We have two sets of tests, which cover positive and negative scenarios.

I order to run the tests, you need to start Cypress, running the command “npx cypress open” with in elevated terminal.

Test cases:
###Positive scenarios 

1. Add new todo in the list

Steps:

Navigate to https://todomvc.com/examples/angular2/
Click on "What needs to be done" text box
Enter the value of your ToDo
Press Enter key
Expected result

The newly entered ToDo will be added to the list

2. Remove a todo in the list

Create new Todo
Click on the delete button
Expected result

Verify that the todo is not in the list
Verify that the list is empty

3. Edit a todo

Create new Todo
Double click on the todo from the list
Edit the text
Press Enter key
Expected result

Verify that the todo will be edited successfully

4. Mark to do completed

Create new Todo
Click on the checkbox in order to mark the todo completed
Expected result

The todo will be marked as completed

###Negative scenarios 

1. Add new todo when title is missing

Steps:

Navigate to https://todomvc.com/examples/angular2/
Click on "What needs to be done" text box
Enter a empty string
Press Enter key
Expected result

Verify that the todo will not be created
Verify that the list will be empty

2. Delete todo from an empty list

Preconditions:

Have an empty list of todos
Steps:

Verify that there is no delete button present and that user can not delete non existing todo
Expected result

The user will not be able to delete todo from an empty list

3. Verify that todo can not be edited with single click

Create new Todo
Single click on the todo from the list
Verify that the todo will not go in edit mode
Expected result

The todo will not be in edit mode

4. Clear complete clears not completed todos

Create a couple of todos 
Check the first todo in the list
Click the Clear completed button
Verify that only the todos that are completed will be removed from the list
Expected result

Only the todos that are completed will be removed from the list
The todos that are still not completed will still be present in the list