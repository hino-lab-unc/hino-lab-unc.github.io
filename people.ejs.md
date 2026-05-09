```{=html}
<div class="quarto-listing-people list">
<% for (const item of items) { %>
  <div class="quarto-post image-left">
    <div class="thumbnail">
      <img loading="lazy" src="<%= item.image %>" class="thumbnail-image" style="height: 400px;">
    </div>
    <div class="body">
      <h3 class="listing-title"><%= item.title %></h3>
    
      <div class="listing-subtitle">
        <%= item.subtitle %>
      </div>

      <div class="listing-description">
        <%= item.description %>
      </div>
    </div>
    <div class="metadata">
      <div class="body">
        <h3 class="listing-title">&nbsp;</h3>
        <div class="listing-subtitle">&nbsp;</div>
        <div class="listing-description">
          <ul>
            <% if(item.website) { %> <li><i class="bi bi-file-person"></i> <a href="<%= item.website %>">Website</a></li> <% } %>
            <% if(item.scholar) { %> <li><i class="ai ai-google-scholar"></i> <a href="<%= item.scholar %>">Scholar</a></li> <% } %>
            <% if(item.linkedin) { %> <li><i class="bi bi-linkedin"></i> <a href="<%= item.linkedin %>">LinkedIn</a></li> <% } %>
            <% if(item.bluesky) { %> <li><i class="bi bi-bluesky"></i> <a href="<%= item.bluesky %>">Bluesky</a></li> <% } %>
            <% if(item.github) { %> <li><i class="bi bi-github"></i> <a href="<%= item.github %>">GitHub</a></li> <% } %>
            <% if(item.orcid) { %> <li><i class="ai ai-orcid"></i> <a href="<%= item.orcid %>">ORCID</a></li> <% } %>
          </ul>
        </div>
      </div>
    </div>
  </div>
<% } %>
</div>
```