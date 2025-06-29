---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV (PDF)
        url: uploads/resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: background.jpg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  # - block: markdown
  #   content:
  #     title: '🏥 My Research & Clinical Work'
  #     subtitle: ''
  #     text: |-
  #       I am a medical professional specializing in cardiology, internal medicine, and geriatrics. My research focuses on hypertension, cardiovascular health, and geriatric medicine, with a particular interest in data science applications in healthcare.

  #       I combine clinical practice with active research, having completed my PhD in Internal Medicine and published extensively in peer-reviewed journals. My work bridges traditional medicine with modern data analysis techniques.
        
  #       Please reach out to collaborate on medical research or educational projects 🩺
  #   design:
  #     columns: '1'
  # - block: collection
  #   id: papers
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publication
  #       featured_only: true
  #   design:
  #     view: article-grid
  #     columns: 2
  # - block: collection
  #   content:
  #     title: Peer-Reviewed International Articles
  #     text: |-
  #       {{% callout note %}}
  #       Quickly discover relevant content by [filtering publications](./publication/).
  #       {{% /callout %}}
  #     filters:
  #       folders:
  #         - publication
  #       exclude_featured: true
  #   design:
  #     view: citation
  # - block: collection
  #   content:
  #     title: Peer-Reviewed Finnish Publications
  #     text: |-
  #       {{% callout note %}}
  #       Quickly discover relevant content by [filtering publications](./peer-reviewed-finnish-publications/).
  #       {{% /callout %}}
  #     filters:
  #       folders:
  #         - peer-reviewed-finnish-publications
  #       exclude_featured: true
  #   design:
  #     view: citation      
  # - block: collection
  #   content:
  #     title: Other Publications
  #     text: |-
  #       {{% callout note %}}
  #       Quickly discover relevant content by [filtering publications](./other-publications/).
  #       {{% /callout %}}
  #     filters:
  #       folders:
  #         - other-publications
  #       exclude_featured: true
  #   design:
  #     view: citation
  # - block: collection
  #   id: projects
  #   content:
  #     title: E-books and guides
  #     filters:
  #       folders:
  #         - project
  #     # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  #     default_button_index: 0
  #     # Filter toolbar (optional).
  #     # Add or remove as many filters (`filter_button` instances) as you like.
  #     # To show all items, set `tag` to "*".
  #     # To filter by a specific tag, set `tag` to an existing tag name.
  #     # To remove the toolbar, delete the entire `filter_button` block.
  #     buttons:
  #       - name: All
  #         tag: '*'
  #       - name: Science
  #         tag: Science
  #       - name: Other
  #         tag: Other
  #   design:
  #     # Choose how many columns the section has. Valid values: '1' or '2'.
  #     columns: '2'
  #     view: article-grid

  # - block: collection
  #   id: news
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: date-title-summary
  #     # Reduce spacing
  #     spacing:
  #       padding: [0, 0, 0, 0]
  # - block: markdown
  #   id: contact
  #   content:
  #     title: Contact me
  #     subtitle: ''
  #     text: |-
  #       **Address:**  
  #       University of Turku  
  #       20014 Turku, Finland
  #       
  #       **Email:** [Contact me via social media links above](#about)
  #       
  #       The University of Turku is where I conduct my research activities. Feel free to reach out through any of the social media platforms linked in my profile.
  #   design:
  #     columns: '2'
---
