# User Interface Specifications
## Login Page
* Task Hero Logo with “Task Hero” text
* Required Email input
  * Must be validated and match existing account in database
* Required Password input
  * Must be validated and match existing account in database
* “Log In” button
  * If email and password are valid, this routes user to home page
  * If email or password are invalid, user stays on login page and is prompted that their information is incorrect
* “Don’t have an account? Sign Up here” text
  * “Sign Up” text is highlighted and links to Sign Up page upon clicking
## Sign Up Page
* Task Hero Logo with “Task Hero” text
* Required Email input
  * Must have @ symbol and end in .com/.net/.uc.edu/etc.
* Required username input
  * No restrictions
* Required Password input
  * No restrictions
* Required Confirm Password input
  * Must match password input
* “Sign Up” button
  * If all inputs are valid, user is routed to home page
  * All account info saved to database
  * If any input is not valid, user is prompted to fix inputs before being able to sign up
* “Already have an account? Login here.”
  * “Login” text is highlighted and links to Log In page upon clicking
## Navigation Bar
* Task Hero logo
* Contains clickable icons for:
  * Home Page (house icon)
  * Tasks Page (list icon)
  * Add Task Popup (plus sign icon)
  * Social/Leaderboard Page (people icon)
  * Profile Page (single person icon)
    * Clicking any icon navigates user to that page
## Home Page
* Levels and Streaks box
  * Medal-like icon to show current user level
  * Fire icon shows how many tasks user has completed without missing any due dates
    * Text says how many tasks in streak
  * Ice icon shows if user has no streak
    * Text says user has no streak
* Task box
  * Shows sleepy super hero if no tasks exist
    * Prompts user to add more tasks
  * Shows task titles and due date in green if tasks exist
    * Green check mark button on right side of each task to mark task as completed
* Progress bars
  * One progress bar for user (hero) and one progress bar for the weekly villain
  * As tasks are added, progress bar for villain goes up and progress bar for user goes down
  * As tasks are marked as completed, progress bar for villain goes down and progress bar for user goes up  
## Tasks Page
* Add Task box
  * User can input task:
    * Title
    * Description
    * Due Date
    * Priority
  * "Plus sign" button to add task
    * Task is added to "Task List" below
* Task List box
  * Any added tasks (from tasks page or add task popup) show up here
    * Highlighted green if low priority, yellow if medium priority, red if high priority
  * Filter by:
    * Nearest Due Date
    * Newest
  * Each task is in its own box and has three buttons:
    * Edit (pencil icon)
      * A popup will appear
      * Any task details can be edited
      * Click button at bottom to save task edits  
    * Delete (trash icon)
      * User is asked "Are you sure?", select yes or no
        * If user selects "Yes", task is deleted and page refreshes
        * If user selects "No", task stays on page and nothing happens
    * Mark as Complete (check mark icon)
      * User is asked "Have you Completed?", select yes or no
        * If user selects "Yes", task is deleted, page refreshes, and user score, streaks, and progress bar increase
        * If user selects "No", task stays on page and nothing happens
## Add Task Popup
* Same concept as Add Task box on the Tasks Page
* User can input task:
    * Title
    * Description
    * Due Date
    * Priority
  * "Plus sign" button to add task
    * Task is added to "Task List" on the Tasks Page
## Social/Leaderboard Page
* Three buttons across the top, navigate to different social content:
  * Following
    * Shows leaderboard of only other users the user follows
    * User can click any user on this page to see the selected user's profile page
  * All Users
    * Shows global leaderboard and where user falls among all Task Hero users based on total score
    * Users can select any user from this page to see the profile page of selected user
  * Search User
    *  Type a username in the input box and click magnifying glass to search
    *  You can select users and follow them by clicking on any user that pops up during the search
## Profile Page 
* User Avatar/Edit Avatar
  * User has a default avatar or can change avatar by clicking the pencil icon near their avatar
    * User can select a new avatar (based on how many points the user has, more avatars may be available)
    * Save changes
    * Return to profile page
* Edit Profile button
  * Allows user to change username and/or password for the account
  * Any changed information must be saved with the "Save changes" button
* Sign out button
  * Takes user back to log in page  
* Followers, Points, Achievements
  * Keeps a count of how many followers, points, and achievements the user has
  * Can toggle over followers to view user followers
* Achievements menu
  * Shows achievement icons for all achievements the user has earned so far
