# Debugging in ServiceNow (Kathy Blackburn)

**When we talk about debugging, typically we think tools, Google, etc.**
- We do work in an awesome community at Acorio
  - #help-dev (searching, creating new posts)
  - Sometimes the best way to get a bug out of your code is getting
    another person on the call

## Best Practices in ServiceNow
![Which is Best Practice to debug?](https://cl.ly/3i172k2G2K2i/Image%202018-06-08%20at%2012.09.51%20PM.png)

- Using an alert message pops up on the screen of ANY user that uses that thing you're developing
  - It is better to use the `dev tools` in your environment so it's specific to you, and you're not
    disrupting other testers or developers on the platform

## Service Portal Widget Logging
You can log the widget in your browser
https://cl.ly/1W1I342M1l31/Image%202018-06-08%20at%2012.11.35%20PM.png

**JSON.stringify();** - will help you log `Service Portal Service Script`

### Session Debug
- Kathy has used this the most in her SN career (also most commonly known)
  - Displays messages in the user interface for the current user session
- If you have a specific issue with security, or a biz rule not running when it was supposed to,
  you can use these to help debug
**Most Commonly Used:**
