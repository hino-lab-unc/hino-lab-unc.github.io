```{=html}
<div class="quarto-listing-ul list">
<ul>
<% for (const item of items) { %>
  <li><a href="<%= item.path %>"> <%= item.title %></a></li>
<% } %>
</ul>
```