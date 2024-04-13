

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; ![Drawing-23 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/b9c51f86-275e-4059-8940-e3f7291cea01) ![Drawing-24 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/1c595d6d-1800-40c3-872a-4e6b1e2427d4)


# &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; User Manual 

This is the manual to help with first time users to our web applications. For instructions on setting up our environment please check out the external code repository.

## Account Setup & User Login 

The user will need to create an account for the web application, using a email, username, and password.

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-26 sketchpad](https://github.com/Deegee13244/Senior-Design/assets/75388877/7a652092-ce18-4f32-8256-8b725f3f4ee5)

This email and password will then be used to login in to the application through the sign in page. 


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-26 sketchpad (1)](https://github.com/Deegee13244/Senior-Design/assets/75388877/35b549f9-0e6c-4d2e-bb78-13d904803775)


## Site Navigation: The Navbar

Once logged into the application, you will be directed to the home page. From there you will see a navbar to the left with the following options: Home, Tasks, Add Task, Social, and Profile. This navbar will be the users tool for conviently switching from page-to-page at ease. Below is a screenshot of the homepage and the navbar with labels. 

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Desktop &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Mobile

![Drawing-26 sketchpad (3)](https://github.com/Deegee13244/Senior-Design/assets/75388877/bbe46dac-3371-45d8-867b-5dce1af9630e) ![Drawing-26 sketchpad (4)](https://github.com/Deegee13244/Senior-Design/assets/75388877/cb72d932-73f4-4122-8bc3-4877b9b2e464)

### Home Page

The homepage allows the user to see their current tasks, which is sorted primarily by urgency (the difference between the current date and the due date) and secondarily by priority (a self assigned priority level: low, medium, or high). In the top left corner of the page, the users badge and score are displayed. At the right side, the users streak is displayed. This streak represents how many tasks in a row the user has completed ON TIME. At the far right side is the user and villains health bars. The users health bar represents their current weekly progress (the number of tasks completed out of the number of tasks due by sunday). The villains health represents the opposite (1 - the current weekly progress), the villain can be thought of as the numeric value to your procrastination!

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (1)](https://github.com/Deegee13244/Senior-Design/assets/75388877/b7d9b453-7125-42f6-bf5c-f140e255111f)

When a user clicks on the complete task button (the check mark on the right side of each task) a few things can happen. The first thing is that the users score can either increase or decrease depending on the time they completed the task. To determine this increase or decrease, we get the quotient of the current date minus the task creation date and the due date minus the task creation date. Lets call this "p". "p" is then used to determine the multiplier for the added score, if p id greater than 1000, the multiplier is one plus the first digit of the quotient of tasks priority level (low is 1, medium is 2, high is 3) and p. If less than 1000 and greather than 0, the multiplier is just 1. If greater than -1000 and less than 0 the multiplier is -1. If less than -1000 the multiplier is the first digit of the quotient of tasks priority level (low is 1, medium is 2, high is 3) and p, minus 1. As you can see below, the user gained +12 points. 

The user also gains back some of their progress, which depends on whether or not the task is due before the upcoming Sunday. If so, users weekly progress is increased by one, meaning the health increases by 1 over total number of tasks due by Sunday. The villains decreases by this much. If the user is able to get all the tasks done by Sunday and the villains health is at 0%, then they defeat the villain and it is unlocked as an achievement (similar to the one on the screen) and placed in their achievements table (on the profile page). The user then has to go against a new weekly villain, however, if they dont defeat the villain they have to compete the same villain for another week (or until they defeat them!). 

When a task is completed on time, the completion streak is incremented. However, if the user does not complete a task on time the streak will go back to 0. The user will also gain achievements along the way, such as the one below titled "First Blood" for completing their first task. These achievements will be stored on their profile page. The users badge will also change as they complete more tasks, in fact, every 50 tasks they will be upgraded to a new badge that indicates their experience level. 

After this is done, the tasks update. Showing the newly sorted lists of tasks. 

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (2)](https://github.com/Deegee13244/Senior-Design/assets/75388877/dd8a2760-59ba-4743-8ced-57bb20daaa4d)

Below is a representation of an advanced user. They have a large completion streak, a level four badge, obtained a high score, and are competing against the second villain. As you can see, the icon on the completion streak has changed. This is because it changes every ten streaks to indicate a hotter flame (red is hotter than orange, blue is hotter than red, green is hotter than blue). 

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Drawing-27 sketchpad (3)](https://github.com/Deegee13244/Senior-Design/assets/75388877/ec8d8898-c4d1-44b0-ac6b-5cbfb805875b)


### Task Page

### Add-Task Component 

### Social Page 

### User Profile 

The user is able to enter a settings screen to edit personalization settings and security settings. 

1. Personalization settings:
1. Color theme (radio buttons)
2. Avatar (select from preset avatar images)
2. Security settings:
1. Account privacy (toggle between private/public)
2. Data sharing (allow data to be shared to developers)

### Website Navigation

The application has several different pages with unique functionality's to help the user complete their daily tasks. Here is a quick rundown of these different pages and how to navigate them:

