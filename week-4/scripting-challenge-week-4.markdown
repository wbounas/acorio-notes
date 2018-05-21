# Scripting Challenge Week #4 (Andrew E. & Andrew W.)
/Goals of the Week/:
- Be very comfortable with GlideAJAX
- Know when to use GA, G\_scratchpad, getReference(), or simple dot walk a field and the difference between the 4 (and client-side GR)

When do we use GA?
- When we have to pull _any_ data from the server, to the client
  - Only data that you need _immediatly_
    - If it's not very important, you can use a normal *Business Rule*
    - ^^^ things that can be done on submit

When to use the `G_scratchpad` in combination with an onDisplay Business Rule
- When to stash away data or values that you receive from the server side to then use on the client side

Any time you do a GlideAJAX, you are moving to the server and then back to the client

onDisplay BR = goes to server
- Grab data and move it to the g\_scratchpad, and then use on the client side
  - This prevents having to go back and forth from the server
- *ONLY TIME* this will work if you click into the form
  - The data on the form has to be _static_
  - You must use GlideAJAX if you need to _*pull data depending on the change*_

Another way to interact with the Server-Side is gr.getReference [https://www.servicenowguru.com/scripting/client-scripts-scripting/gform-getreference-callback/]
*NOTE*: Always use a callback with getReference(), as it saves _a lot_ of performance
- Does not require a script include, could potentially be faster
- Not as efficient as GlideAJAX, which is generally better in most use-cases

When dot-walking to a field on a form, that field is actually editing the data on the field that was dot-walked to
- This can be *scary* because without knowing it, you could be changing the value on one field and changing that value throughout the entire system
  - Most of the time, when you use `dot-walked fields` on a form, you make them `Read Only` specifically for that reason, so that an end-user can't make a non-sensical change thinking it would only apply on the form


GlideAJAX vs. getReference
- You can always use them interchange-able when pulling back data that does NOT require processing
*NOTE*: When you have to use a lot of information from a record (basically the entire record), that's when you'd like to use getReference more-so
