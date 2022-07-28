# video_manager_readme

Problem Description
-------------------
You are currently working as a software developer for a media production company.
Within this company your are part of a small team that is instructed to implement a new
custom video editing software. One major component of the framework design is a
video manager class that is able to store multiple video clips and should have functions
for adding and deleting such video clips. The key requirements for the video manager
class is that there is only one instance of this class and that this instance is easy to access
from other components of the software framework that your team designs.

Task
----
Your team’s task is to design and implement a video manager class using an object
oriented language. Your implementation of the video manager should store multiple
video clips and should have functions for adding and deleting such video clips. The
key requirements for the video manager class is that there is only one instance of this
class and that this instance is easy to access from other components of the software
framework that you design. You don’t need to take care of the implementation of the
video clips, this will be the task of a different team, but you should use an empty proxy
implementation for this class. In order to success with this task your manager rec-
ommends a recap on design patterns (e.g. D. Nesteruk, Design Patterns in Modern
C++, https://doi.org/10.1007/978-1-4842-3603-1_5, available as ebook in
the library) . What are challenges with your software design?


Instructions to Run
-------------------
- import the videomanager library
  - using import videomanager.core.VideoManager;
  - import videomanager.core.VideoClip;
- Create the single instance of the Video Manager by using:
  - VideoManager test2 = VideoManager.getInstance();
  - VideoManager test2 = new VideoManager() WILL NOT WORK! As the constructor is private!
- Add or delete clips using the functions .addClip .deleteClip and .receiveClip
- There is already a test file attached which I have used to test both the implementation of
  the hash map and the singleton using .hashcode
- So run and edit the test file if you would like to do more testing on the class.

Included in this project are
----------------------------
- Test.java
  - The test file with correct syntax for editing and using the Video Manager and Video Clip classes
- VideoManager.java
- VideoClip.java
  - A quick proxy class for future teams to improve and implement

Singleton Discussion
---------------------
The way I have designed this class to be a singleton instance is by keeping the
constructor private so it isnt able to be called. The only way to get *the* instance of the class is by 
calling the getInstance method. The challenges that we faced when creating this
was the static methods and creating a very controlled class that is user safe.
The main challenge is making sure that the user cannot in any way accidentally or purposely
create a new instance of the class.
The purpose of the singleton is if hundreds upon
hundreds of video clips are added to the hashmap, there is one global instance that
hosts all of these video clips. Therefore if this was used in an organisation, the video
clips are all in one place and can't go missing.
