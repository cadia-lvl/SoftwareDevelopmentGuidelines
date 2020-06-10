Testing (Þorsteinn)
Split testing cases based on deliverable.
WEB = test browser support (required), User testing (required?)
APP = Test if works on different platforms
MOD = Test API
All projects should attempt to do as much unittesting as possible

Unit tests (App/Mod)

[Add motivation]
[Add examples]

Aim for 100% coverage

Python
[Unittest, PyTest] in each module
Coverage
C/C++
…
Java

Web
Test on all major browsers (Chrome, Firefox, Safari & Edge)
Keep in mind your user base (mobile/desktop) and the browsers market share.
    If it doesn’t work on that browser then add errors messages or hints to switch
Helpful for Javascript development: https://caniuse.com/
Keeping a beta instance running openly but not in active use is preferable to test deployment of new features and updates.
 
Add links for automated test [not required]
MonkeySomething [Find]

User testing

User testing is difficult to do well. When doing user tests keep these points in mind:
User tests should only be used if you have planned time to make adjustments
User testing should focus on specific features
Up to 4 people for tests [...]
Testing prototypes often gives no useful information (users will most likely point out things that you know are missing and are less likely to give additional feedback)
