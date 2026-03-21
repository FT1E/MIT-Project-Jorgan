## Usability Testing

### Testing Plan

Before performing the tests, users are informed briefly of what our project is, then they perform the tests, and afterward a short interview is performed. During the tests the group members act as observers and take notes of anything notable.

Also, the usability tests will be performed on the UI of services which are run on the server. Like Immich for services related to image, and VS code website emulator for services related to programming.

**Starting point**

For tests 1 and 2, starting point is the [Immich website](https://immich.stackrack.org/photos). <br>
For test 3 and 4, starting point is the [VS code website](https://visualstudiocode.stackrack.org/?folder=/projects) which opens the folder *Projects* on the server using VS code web emulator with an SSH connection.



**Test 1** <br>
Goal - Successfully upload and download image. Check if there are changes in the file before and after. <br> 
Task - Upload the provided image "*test_image.png*", then download it. See if the file size is different.


**Test 2** <br>
Goal - Organization of images into albums <br>
Task - Create an album, give it some name and upload images from a given folder.


**Test 3** <br>
Goal - Check if there are noticable differences in the VS Code web interface, compared to the one run locally <br> 
Task - Open a terminal, navigate to the folder "*graphTheory/frontEnd*" then start hosting a website using the given command (with copy/paste), then visit the website (link given)

**Test 4** <br>
Goal - Same as test 3, checking for terminal responsiveness in the VS Code web interface <br> 
Task - Navigate to SecretFolder, see the contents of the file inside using the command "cat", and check when the file was created using "ls -l" 


### Test Findings

**Does anything need to be fixed?** <br>
- U1: Immich - should have right click functionality to open alt menu of the app instead of browser alt menu.
- U2: Immich - could have an easier way to access download button. 
<br>
VS Code - tab auto-complete is case sensitive. Example 'frontEnd' isn't auto completed with tab when user types 'Fro'
- U3: 

**Did users face any problems?** <br>
- U1: Immich - right click functionality not present. User expected an alt menu when right clicking, which was not implemented. And instead got the browser alt menu. <br>
 Could have an extra button for a quicker way to create an album. Not only in the albums section of the app.
- U2: Immich - download button shouldn't be in the extra options (3 dots menu). Also needed time to find where to create an album.
- U3: Immich - download button as well.<br>
Also took a bit to find create album.

<br>

**Time spent on each task** 

Note that the times are rounded to whole integers.
- U1: 24s - 32s - 27s - 20s
- U2: 22s - 27s - 22s - 13s
- U3: 20s - 28s - 21s - 15s

<br>

**Which task was the most intuitive?** <br>
- U1: Task 2, after finding the album section
- U2: Task 3 as it's just cd and copy/paste command. 
- U3: Task 3

<br>

**Extra notes** <br>
- Noted by the users, some things should be easier and quicker to access in the Immich UI
- VS Code familiarity - as users have operated VS Code themselves they felt comfortable with it
- Users felt it was a bit weird working on VS code in the browser, but got used to it quickly during test 3.