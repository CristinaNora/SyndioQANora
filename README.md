# SyndioQANora

TEST CASES

1. Drop down 
    1. Drop down responds to click
    2. Drop down values: 
        1. Group by Function
        2. Group by Role
    3. Upon changing the value, the display in the drop-down changes as well
 
 	
     
2. Tabs: 
    1. Group by Function: Ability to toggle between Gender and Race
    2. Group by Role: Ability to toggle between Gender and Race



3. Gender tab contains what’s in the json file as in tabs + content 
 	1. Pay Equity Gap 
		1. Title = tab label
		2. Content = {minority:label} earn {minority:label  for every {majority:value} earned by comparable {majority:label}  
	2. Employees in Comparison: 
		1. Title = tab label
		2. Content = {label} make up {value} of employees
	3. Budget: 
		1. Title = tab label
		2. Content = {value} minimum recommended budget to reduce pay equity gap



4. UI elements
    1. General look and feel should match the mockups for:
        1. Drop down
        2. Tabs
        3. Text/font
        4. Positioning in the page, etc
    2. Graphic elements specs match what’s in the mockups 


5. Responsiveness - without going in details (that I don’t actual spec anyway) the page is responsive in relationship to:
	1. Windows resizing
	2. Screen size (aka mobile, desktop)
	3. Zoom in/out


6. Accessibility - logical tab order, keyboard (enter/space/arrows), focus, readable elements (bigger test bucket here, can develop later)


7. Errors:
	1. Check for network errors or any other errors on the page
	2. Verify the GET request goes through


========================

BUGS

Bug 1: Drop-down Group by Function grayed out
1. Click on the Group by Function drop down 

*** Group By Function option greyed out and, if I get this right, we want to have access to that option as well, especially since the json is provided and the drop-down value is stuck on that


Bug 2: Drop-down is not changing values
1. Group by Function drop-down 
2. Choose Group by Role

*** The display is left to Group by Function and should change to Group by Role


Bug 3: Drop-down Change Group - undefined and confusing to the user
1. Group by Function drop-down 
2. Look for the drop down options
*** Change Group - has no logical meaning to be there, unless in itself creates another grouping, but that is inactive and I see no references to it


Bug 4: Drop-down - won’t close unless clicked on
1. Click on the Group by Function drop-down
2. Click anywhere else on the screen

*** The drop-down should close without any action. Instead, it stays open and you have to explicitly close it


Bug 5: Misspell in the Budget tab
1. Take a look at the Budge tab

*** budget should be spelled “budget”, not “buget”


Bug 6: Active tab height doesn’t match mockups
1. Inspect the active tab

*** Height is 41px and according to the mockups it’s supposed to be 40


Bug 7: Active tab - background color is not matching mockups
1. Inspect the active tab

*** Body background color is F8F8F8 and according to the mockups it’s supposed to be D8D8D8


Bug 9: Inactive tab - background color
1. Inspect the inactive tab

*** The background is transparent. In theory this is a bug, in practice it doesn’t matter as the background color is #F2F2F2 as mentioned in the mockups


Bug 10: Tabs - capitalization doesn’t match the mockups 
1. Take a look at the tabs

*** in the mockups the tabs are capitalized, while in the app they are not


Bug 11: Accessibility not implemented
Several bugs here, as the only thing that seems to work is space on the drop-down
Also, the tabs are not particularly visible on a bad vision or older monitor

========

NOTES

I would have to understand the context of this dashboard, so I made a lot of presumptions and the test cases are based on those presumptions. There are also more test cases, just did what I could with what I have available

For matching with mockups I used the Chrome inspect feature.

For checking the mobile I used the Chrome emulator. I also resizes and check the responsiveness of the page for various displays using the emulator.

========

QUESTIONS

Json identical between Roles and Function, just different values. Is that supposed to happen?

========

ENVIRONMENT

Chrome 93.0.4577.63 (Official Build) (x86_64)
Mac OS Catalina 10.15.17
