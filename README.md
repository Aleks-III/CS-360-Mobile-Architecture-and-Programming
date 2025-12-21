# CS-360 Mobile Architecture & Programming

## Project Reflection
<br>
<br>

<ins>**Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?**</ins>

The mobile app I designed is a weight-tracker that allows users to create an account, set a goal weight, log their daily weight, and track their progress over time. The primary goal of the app is to provide a simple way for individuals to monitor weight changes and stay motivated to do so by striving to reach a goal. Users can opt in to SMS notifications to present them with an exciting message when they reach or surpass their goal. 

The user needs for accountability, progress-tracking, and clarity are all addressed by minimizing unnecessary steps and keeping the core actions of logging weight and viewing history easy to access.
<hr>

<ins>**What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?**</ins>

To support user needs, the app includes a login and account creation screen, a goal weight setup screen, a daily weight entry screen, a weight history screen, and an SMS permission screen. Each screen was designed with a clear, singular purpose to reduce cognitive load. 
- User flows were carefully structured so new users are guided through goal setup before entering daily data, while returning users are immediately navigated to the daily entry screen to log their weight. 
- After adding weight data, users are presented with their weight history where they can view and edit previous entries, or navigate back to the weight entry screen to add a new record. 
- If users would like to change their goal, they can access the goal setup screen again from the weight entry screen, before adding a new weight. 
- The goal setup screen also contains a toggle for SMS notifications which, when enabled, prompts the user with the option to allow the permissions if they would like to take advantage of the feature.
  - I chose a toggle to initiate the SMS permission screen rather than an automatic pop-up to avoid an obtrusive experience, while still promoting user-choice with a simple way to enable/disable the feature.

The UI design prioritizes readability, consistency, and accessibility. Inputs are clearly labeled, primary actions are visually emphasized, and secondary actions (logout and notification preferences) are present but unobtrusive. Careful attention was paid to color contrast and text sizing, as well as optimization for light/dark themes and portrait/landscape orientations to appeal to all users. These design choices align visual hierarchy with user intent and reduce friction when performing common tasks.
<hr>

<ins>**How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?**</ins>

The app was developed using a structured, modular approach. Database logic was centralized in a helper class, UI logic was separated by activity, and reusable components (adapters and model classes) were used to keep the codebase organized. Defensive programming techniques such as null checks, input validation, and conditional logic were used throughout to prevent crashes and unexpected behavior.

These strategies can be applied to future projects by improving maintainability and scalability, particularly for apps with growing feature sets or more complex backend logic. This approach would be especially valuable when developing larger applications or games that require persistent data and state management.
<hr>

<ins>**How did you test to ensure your code was functional? Why is this process important, and what did it reveal?**</ins>

Testing was performed through iterative manual testing using the Android emulator, Logcat debugging, and edge-case validation. Each feature was tested individually and then in sequence to ensure proper data flow between screens. This process was ideal for identifying issues like database schema mismatches, incorrect intent handling, and logic errors related to goal detection and notifications.

Testing revealed how small oversights such as uninitialized views or incorrect query assumptions can lead to crashes or unintended behavior. Addressing these issues improved both app stability and the overall user experience.
<hr>

<ins>**Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?**</ins>

One significant challenge involved implementing goal-based SMS notifications in a way that worked for both weight gain and weight loss goals, while also allowing users to change their goal over time. This required rethinking the logic to detect when a user crossed their goal threshold rather than simply matching an exact value. The solution involved comparing previous and current weight entries dynamically, which ensured accurate notifications regardless of direction.

Another challenge was managing feature scope while maintaining deadlines. Balancing UI polish with backend development required prioritization and refinement of features to ensure core functionality was completed reliably.
<hr>

<ins>**In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?**</ins>

The database design and weight-tracking logic best demonstrate my skills and understanding. Implementing user-specific data storage, editable entries, and goal-aware notification logic required integrating SQL queries, Android lifecycle management, and conditional business logic. This component reflects a strong grasp of data-driven mobile development and highlights my ability to design systems that are both functional and adaptable to changing user requirements.
