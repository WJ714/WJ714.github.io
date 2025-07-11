---
layout: single-with-sidebar
title: "Example Page with Research Sidebar"
permalink: /example-sidebar/
author_profile: true
---

## Example Page with Research Sidebar

This is an example page demonstrating how the right sidebar displays research content, plots, and useful information while filling the empty space that was previously unused.

### Features of the Research Sidebar:

1. **Research Focus** - Key areas of your work
2. **Methods** - Techniques and tools you use
3. **Quick Links** - Easy access to important pages
4. **Contact Information** - How to reach you

### How to Use:

To add the research sidebar to any page, simply change the layout in the front matter:

```yaml
---
layout: single-with-sidebar
title: "Your Page Title"
# ... other settings
---
```

To disable the sidebar on specific pages, add:

```yaml
---
layout: single-with-sidebar
show_sidebar: false
# ... other settings
---
```

### Responsive Design:

The sidebar automatically hides on smaller screens (< 1300px width) to maintain mobile-friendly design.

### Customization:

You can customize the sidebar content by editing the `_layouts/single-with-sidebar.html` file to include:
- Your own research images
- Custom plots and visualizations
- Updated contact information
- Different research focus areas
- Additional quick links

This approach makes much better use of the available screen space while providing visitors with valuable research information at a glance!