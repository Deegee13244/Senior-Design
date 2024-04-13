

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; ![Drawing-23 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/b9c51f86-275e-4059-8940-e3f7291cea01) ![Drawing-24 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/1c595d6d-1800-40c3-872a-4e6b1e2427d4)
<br>
<br>

<br>

# &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp; User Manual 

This is the manual to help with first time users to our web applications. For instructions on setting up our environment please check out the [external code repository](https://github.com/duncan222/TASKHEROAPI).

## Account Setup & User Login 

The user will need to create an account for the web application, using a email, username, and password.

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-26 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/7a652092-ce18-4f32-8256-8b725f3f4ee5)

This email and password will then be used to login in to the application through the sign in page. 


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-26 sketchpad (1)](https://github.com/Deegee13244/Senior-Design/assets/75388877/35b549f9-0e6c-4d2e-bb78-13d904803775)
<br>


## Site Navigation: The Navbar

Once logged into the application, you will be directed to the home page. From there you will see a navbar to the left with the following options: Home, Tasks, Add Task, Social, and Profile. This navbar will be the users tool for conviently switching from page-to-page at ease. Below is a screenshot of the homepage and the navbar with labels. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Desktop &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Mobile
<br>

![Drawing-26 sketchpad (3)](https://github.com/Deegee13244/Senior-Design/assets/75388877/bbe46dac-3371-45d8-867b-5dce1af9630e) ![Drawing-26 sketchpad (4)](https://github.com/Deegee13244/Senior-Design/assets/75388877/cb72d932-73f4-4122-8bc3-4877b9b2e464)
<br>

### Home Page

The homepage allows the user to see their current tasks, which is sorted primarily by urgency (the difference between the current date and the due date) and secondarily by priority (a self assigned priority level: low, medium, or high). In the top left corner of the page, the users badge and score are displayed. At the right side, the users streak is displayed. This streak represents how many tasks in a row the user has completed ON TIME. At the far right side is the user and villains health bars. The users health bar represents their current weekly progress (the number of tasks completed out of the number of tasks due by sunday). The villains health represents the opposite (1 - the current weekly progress), the villain can be thought of as the numeric value to your procrastination!
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (1)](https://github.com/Deegee13244/Senior-Design/assets/75388877/b7d9b453-7125-42f6-bf5c-f140e255111f)
<br>

When a user clicks on the complete task button (the check mark on the right side of each task) a few things can happen. The first thing is that the users score can either increase or decrease depending on the time they completed the task. To determine this increase or decrease, we get the quotient of the current date minus the task creation date and the due date minus the task creation date. Lets call this "p". "p" is then used to determine the multiplier for the added score, if p id greater than 1000, the multiplier is one plus the first digit of the quotient of tasks priority level (low is 1, medium is 2, high is 3) and p. If less than 1000 and greather than 0, the multiplier is just 1. If greater than -1000 and less than 0 the multiplier is -1. If less than -1000 the multiplier is the first digit of the quotient of tasks priority level (low is 1, medium is 2, high is 3) and p, minus 1. As you can see below, the user gained +12 points. 

The user also gains back some of their progress, which depends on whether or not the task is due before the upcoming Sunday. If so, users weekly progress is increased by one, meaning the health increases by 1 over total number of tasks due by Sunday. The villains decreases by this much. If the user is able to get all the tasks done by Sunday and the villains health is at 0%, then they defeat the villain and it is unlocked as an achievement (similar to the one on the screen) and placed in their achievements table (on the profile page). The user then has to go against a new weekly villain, however, if they dont defeat the villain they have to compete the same villain for another week (or until they defeat them!). 

When a task is completed on time, the completion streak is incremented. However, if the user does not complete a task on time the streak will go back to 0. The user will also gain achievements along the way, such as the one below titled "First Blood" for completing their first task. These achievements will be stored on their profile page. The users badge will also change as they complete more tasks, in fact, every 50 tasks they will be upgraded to a new badge that indicates their experience level. 

After this is done, the tasks update. Showing the newly sorted lists of tasks. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (2)](https://github.com/Deegee13244/Senior-Design/assets/75388877/dd8a2760-59ba-4743-8ced-57bb20daaa4d)
<br>

Below is a representation of an advanced user. They have a large completion streak, a level four badge, obtained a high score, and are competing against the second villain. As you can see, the icon on the completion streak has changed. This is because it changes every ten streaks to indicate a hotter flame (red is hotter than orange, blue is hotter than red, green is hotter than blue). 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (3)](https://github.com/Deegee13244/Senior-Design/assets/75388877/ec8d8898-c4d1-44b0-ac6b-5cbfb805875b)


### Task Page
The next option on the navbar is the Task Page. This page allows the user to add, edit, mark-off, and delete tasks. Using the form below, users enter the tasks title, a description, the date, and the priority level (low, medium or high). After this is entered, the user will add the task using the large plus sign button. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (4)](https://github.com/Deegee13244/Senior-Design/assets/75388877/61658c50-6493-4649-8069-07a43b0e11f1)
<br>

When tasks are added, they appear in the tasks list below. Here the items are sorted by closest due date (by default) but the user can also filter the items based on the priority as well. Each task has their own color border representing the priority level. Green is low priority, Yellow is medium priority, and Red is high priority. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (5)](https://github.com/Deegee13244/Senior-Design/assets/75388877/f9e744c5-2254-4cb9-a608-b05d47ad851e)
<br>

When the user is finished with a task, they can mark the task as complete by clicking the check mark and then confirming their decision in the popup shown below. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (7)](https://github.com/Deegee13244/Senior-Design/assets/75388877/48bd4443-e1f4-489a-9597-812389173a51)
<br>

If a user decides they want to edit their task in any way, they can select the edit button below and edit the desired feild belonging to the task. Once they submit their changes they will be present. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (6)](https://github.com/Deegee13244/Senior-Design/assets/75388877/cacae614-eb95-4713-bb12-1177adb6385c)
<br>

If the user decides they want to delete a task without affecting their score, they can delete the task through the trash can button depicted below and confirm their decision through the pop-up.
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (8)](https://github.com/Deegee13244/Senior-Design/assets/75388877/01019a10-c8fd-4914-8b24-e9bf0880bf88)
<br>


### Add-Task Component 
The add task component is accessible from any page and it is located in the middle of the navbar. Similar to the option to add a task on the task page, it allows the user to enter a title, description, due date, and priority level. Once they select the green plus sign button, their task will be added. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (9)](https://github.com/Deegee13244/Senior-Design/assets/75388877/e17b6a09-1ea9-41a3-8cf6-7ab4dc4ff979)
<br>

### Social Page 
The social page allows you to connect with other users that use task hero. Encouraging motivation and competition through global and local leaderboards, visable scores and badges, as well as comparing achievements earned by others and yourself. 
<br>

Below is the display of the following page, which shows all the users that you are currently following and sorts them based on their total score. This would be considered the local leaderboard. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (12)](https://github.com/Deegee13244/Senior-Design/assets/75388877/61b37d20-4c79-4d76-97ce-bd8ea1fa2960)
<br>

Below is the display of the global page, which shows all the users that are on task hero and sorts them based on their total score. This would be considered the global leaderboard. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (10)](https://github.com/Deegee13244/Senior-Design/assets/75388877/842e8c06-299c-42d9-9f36-c0aa0d52001a)
<br>

Below is the search tool, which allows the user to search for another user by their username. Allowing you to instantly connnect with friends. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (11)](https://github.com/Deegee13244/Senior-Design/assets/75388877/f101e4ec-c1b3-4474-991d-56130443e97d)
<br>

When you click on a username displayed in either the global, local, or search page you will be redirected to that users profile. This is where you have the option to follow/unfollow a user, see their score and badge, view their achievements and their account stats. 
<br>

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (13)](https://github.com/Deegee13244/Senior-Design/assets/75388877/f6b664d3-f16b-4f16-bffe-e819e5ef1daf)
<br>
### User Profile 
The last option in the navbar is the user profile. This page displays all of your achievements/villains, your current score, and the number of people following you (if you click on the number is displays the users as a list). It also offers you the ability to change your username and password through the edit profile button or sign out of your account all together. 
<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (14)](https://github.com/Deegee13244/Senior-Design/assets/75388877/0fdbf203-4f51-4752-81c6-786fa324398a)
<br>
If you press the edit avatar button on the right hand side of the profile picture, you will be redirected to the page below where you are given the option to change your avatar. Some of the avatars are only available to users with a certain number of points to their name, otherwise they will be locked until your score has surppased that amount. Encouraging you to do better and get tasks done on time!
<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (15)](https://github.com/Deegee13244/Senior-Design/assets/75388877/e7a51a42-77d6-47e1-86ff-16b65ec59277)

## FAQ: 


