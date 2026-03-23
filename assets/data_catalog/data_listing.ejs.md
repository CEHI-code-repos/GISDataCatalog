```{=html}
<div class="list grid quarto-listing-cols-1">
```

<% for (const item of items) { %>

```{=html}
<div class="g-col-1" <%= metadataAttrs(item) %>>
<a href="<%- item.path %>" class="quarto-grid-link">
<div class="quarto-grid-item card h-100">
<div class="card-body post-contents">
```

<h5 class="no-anchor card-title listing-title"><%= item.title %></h5>

<% if (item.categories) { %>

```{=html}
<div class="listing-categories">
<% for (const category of item.categories) { %>
<div class="listing-category" onclick="window.quartoListingCategory('<%= utils.b64encode(category ) %>'); return false;"><%= category %></div>
<% } %>
</div>
```

<% } %>

```{=html}
<table class="card-other-values">
  <tbody>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Description:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_description %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Time Frame:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_time_frame %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Spatial Scale:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_spatial_scale %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Format:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_format %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Source:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_source %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Original Repository:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_orig_repo %></td>

```{=html}
    </tr>
    <tr>
      <td style="width: 30%; font-weight: bold; vertical-align: top;">Living Atlas:</td>
```

<td style="width: 70%; vertical-align: top;"><%= item.data_living_atlas %></td>

```{=html}
    </tr>
  </tbody>
</table>
```

```{=html}
<div class="card-text listing-description delink">
```

<%= item.data_details %>

```{=html}
</div>
</div>
</div></a>
</div>
```

<% } %>

```{=html}
</div>
```

