# Exam-Memo
COP4331 - For 10 points of extra credit, implement your solution in code and provide a link to your personal github site with the source.

## About the Project

### Stakeholders
..- Professor: Dr. Christopher D. Hollander
..- Student: Gustavo Monaco

### Requirements
1. As a note taker, I want to be able to write a memo and this memo to be saved for later reading.
2. As a note taker, I want to be able to read a previously saved memo
3. As a note taker, I want to be able to modify a previously saved memo. 
4. As a note taker, I want to be able to discard/clear my writing in case I am not happy with it.
5. As a note taker, I want to be able to delete my previously saved memo. 

### Non-functional requirements
1. Memo application should load in less than 5 seconds
2. Memo application should be accessible from any modern browser.
3. Memo application should take less than 5 minutes to learn
4. Memo application should take less than 100MB of space in the hard drive (not including the memos)

### Application Architecture
For the Memo Application, we are looking for a very simple approach, taking advantage of the localStorage feature in HTML5 for our memo database. 

Web Browser: Platform
HTML5: for design
CSS: for styles
JavaScript: for logic
localStorage: for data storage
Hosting: Deployment
Will contain all the files needed. 
Once downloaded on the client's web browser, no communication is needed with the server. 






This architecture will allow the note taker:

To write a memo and this memo to be saved for later reading (while the browser is open)
To read a previously saved memo (while the browser is open)
To modify a previously saved memo (while the browser is open) 
To discard/clear my writing in case I am not happy with it.
To delete my previously saved memo (until the browser is closed, then all is deleted). 
This architecture should make the application

Load in less than 5 seconds
Accessible from any modern browser.
Take less than 5 minutes to learn
Take less than 100MB of space in the hard drive (not including the memos)


### User interface
Minimalistic UI includes:

Text area: Where the memos will be written and modified
Delete Button: when clicked it removes the Memo instance from the MemoList. 
Cancel Button: when clicked it sets the text area to an empty string
Save Button: when clicked it checks if this is a modification, if it is, then it removes the existing instance of the Memo, then continues and saves a new memo.
Memo List: Shows the list of memos in the localStorage




Explained: 



User story mapping:

The text_area will allow to write a memo and this memo to be saved using the save_button.
By selecting the memo from the memo_list, the whole memo will be loaded in the text_area, allowing the user to read a previously saved memo
By opening, modifying and then clicking on the save_button, the user will be able to modify a previously saved memo. 
By clicking the cancel_button, the user will be able to discard/clear any writing from text_area.
By selecting the memo from the memo_list, the will be able to delete my previously saved memo, by clicking delete_button. 


### Class diagram
As a note taker, I want to be able to write a memo and this memo to be saved for later reading.
MemoList.add(new Memo(content))
As a note taker, I want to be able to read a previously saved memo
text_area = MemoList.items[selected_index]
As a note taker, I want to be able to modify a previously saved memo. 
if selected_index != null, then MemoList.remove(selected_index) and MemoList.add(new Memo(content))
As a note taker, I want to be able to discard/clear my writing in case I am not happy with it.
N/A
As a note taker, I want to be able to delete my previously saved memo. 
MemoList.remove(selected_index)

## Test
User Story	Test	Results
As a note taker, I want to be able to write a memo and this memo to be saved for later reading.

Open the application
Type a memo
Click save
Confirm is in the list to the right
PASSED
As a note taker, I want to be able to read a previously saved memo

Open the application
Select a memo from the list to the right
Confirm is it showing the memo content in the text area
PASSED
As a note taker, I want to be able to modify a previously saved memo.

Open the application
Select a memo from the list to the right
Make a modification to it in the text area.
Click Save
Confirm is in the list to the right
Then select the memo from the list to the right
Confirm is it showing the modifications to the memo content in the text area
PASSED
As a note taker, I want to be able to discard/clear my writing in case I am not happy with it

Open the application
Type a memo
Click Cancel
Confirm text area is blank
PASSED
As a note taker, I want to be able to delete my previously saved memo. 

Open the application
Select a memo from the list to the right
Click Delete
Confirm is not in the list to the right
PASSED
