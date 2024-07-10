---
---
date: <% tp.date.now("DD-MM-YYYY") %>

# edar
<%* tp.file.title %>

// File creation date <% tp.file.creation_date() %> // File creation date with format <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm") %>


<% await tp.file.move("/mouse guard/locations/" + tp.file.title)%>
