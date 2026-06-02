```{=html}
<div class="quarto-listing-ul list">
<ul>
<% for (const item of items) { %>
  <li><a href="people.qmd#<%= item.title.toLowerCase().replace(/\s+/g, '-') %>"> <%= item.title %></a></li>
<% } %>
</ul>
```