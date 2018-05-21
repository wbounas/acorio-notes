# ServiceNow Recap with Sean Duhaime
GlideRecord creates a JavaScript Object

When you reference a glide record, and dotwalk to a field name (property), it returns a *Glide Element*

`Glide Element` is a pointer to the actual object itself, but it is a JS Object
- You COULD `.toString()` everything, and not worry about it

.getDisplayValue() is important with *reference fields*, as they will display a sys_id by default
- Reference fields will always  a sys_id
- If there is no display value, it might default to the value

cmd+shift+j = *JavaScript Executor*
- You have full-access to the GlideForm API through

GlideAJAX
If you make AJAX calls, you want the `answer` attribute inside of an XML payload
- If someone asks you if you want XML or JSON back, really you're _always_ getting `XML` back, just looking for that particular attribute `answer` and pulling its value


