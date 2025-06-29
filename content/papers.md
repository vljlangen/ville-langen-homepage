---
title: 'Papers'
date: 2023-10-24
type: landing

design:
  spacing: '5rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - peer
        featured_only: true
    design:
      view: article-grid
      columns: 1
  - block: collection
    content:
      title: Publications in International Peer-Reviewed Journals
      text: ""
      filters:
        folders:
          - peer
        exclude_featured: false
    design:
      view: citation
  - block: collection
    content:
      title: Peer-reviewed Finnish publications
      text: ""
      filters:
        folders:
          - peer-reviewed-finnish-publications
        exclude_featured: false
    design:
      view: citation
  - block: collection
    content:
      #count: 10
      title: Other Published Works
      #text: I enjoy making things. Here are a selection of projects that I have worked on over the years.
      filters:
        folders:
          - other-publications
    design:
      view: citation
    # design:
    #   view: no-date-article-grid
    #   fill_image: true
    #   columns: 2
---
