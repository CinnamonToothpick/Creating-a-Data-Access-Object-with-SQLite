# Creating-a-Data-Access-Object-with-SQLite

There are two inner classes: ExpenseItem, which defines constants used in mapping the Expense data to the database, and Helper. You should see that the Expense class is a simple POJO with properties of amount, description, and expenseDate.

A DAO is an excellent and widely-used design pattern where the code to access a data source is encapsulated within a single class.

   1. Open edu.csuglobal.expenses.data.DAO.java.
   2. Inside the DAO constructor near line 35, add the code to initialize an instance of the database helper class at the location marked TODO.
   3. Locate the queryExpenses() method and complete the steps marked TODO.
   4. Expand app | java |edu.csug.expenses(androidTest) | data.
   5. Right-click DAOTest and select Run 'DAOTest'. If you are offered a choice of two DAOTest options, take the first one, which has the Android symbol next to it. When prompted to choose a device, select the Galaxy-Nexus AVD and click OK.
   6. Click the "4:Run" button at the bottom of the Android Studio window to show the test results.
   7. Open edu.csug.expenses.ExpensesListActivity.java. In the following steps, you may see class names marked as errors due to the required imports not being in the code. The simple solution is to click the class name. When prompted, press AltEnter. Android Studio will add the required import.
   8. Locate the onCreate() method and complete the steps marked TODO.
   9. If it is not already running, start the Galaxy-Nexus AVD. Make sure the app is selected next to the Run button, then run the application by clicking the green run arrow as normal. You should see the list of sample expenses.
   10. At the end of the onCreate() method in ExpensesListActivity, add a call to registerForContextMenu(). Use "mList" as the reference for the View; this should display the context menu.
   11.  Override onCreateContextMenu() and inflate the menu with an id of R.menu.context_menu. Right-clicking on the file and selecting Generate | Override Methods... is the easy way to create the new method.
    12. Save and execute the application.
    13. Click and hold on one of the expenses in the list. Your context menu should appear. Of course, there is no associated functionality yet.
    14. Add a new method public int deleteExpensesById(int id) to the DAO.
    15. Create a where clause, get an instance of a writable database, then call the delete method.
    16. Uncomment the onContextItemSelected() code at the bottom of ExpensesListActivity. Organize imports as needed.
    17. Test your work.
