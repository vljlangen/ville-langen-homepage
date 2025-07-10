---
title: 'Projekteja'
date: 2023-10-24
type: landing

# design:
#   spacing: '5rem'


# cascade:
#   - _target:
#       kind: page
#     params:
#       show_breadcrumb: true


# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: collection
    id: projects
    content:
      #title: E-books and guides
      count: 300
      filters:
        folders:
          - projects
        #featured_only: 
    design:
      view: article-grid
      columns: 3
      #view: showcase



  # - block: collection
  #   content:
  #     #count: 10
  #     title: Other Published Works
  #     #text: I enjoy making things. Here are a selection of projects that I have worked on over the years.
  #     filters:
  #       folders:
  #         - other-publications
  #   design:
  #     view: citation
  #   # design:
  #   #   view: no-date-article-grid
  #   #   fill_image: true
  #   #   columns: 2
---
