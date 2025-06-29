---
title: 'About'
date: 2023-10-24
type: landing

design:
  spacing: '5rem'

sections:

  - block: skills
    content:
      title: Skills
      text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
      username: admin
    design:
      columns: '1'



#   - block: resume-skills
#     content:
#       title: Skills
#       text: ''
#       # Choose a user profile to display skills from (a folder name within `content/authors/`)
#       username: admin
#     design:
#       columns: '1'
#       background:
#         color: ''
#         text_color_light: false
#       spacing:
#         padding: ['20px', '0', '20px', '0']
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Note: company_logo is currently non-functional in Hugo Blox but kept for future compatibility
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Clinician (MD)
          company: Several hospitals/health centers
          company_url: ''
          company_logo: custom/caduceus2
          location: Finland and Sweden
          date_start: '2002-06-12'
          date_end: ''
          description: |2-
              Responsibilities include:

              * Outpatient clinic
              * Patient rounds
              * Mentoring and teaching young doctors and medical students
        - title: Researcher
          company: University of Turku
          company_url: https://www.utu.fi/en
          company_logo: custom/turun_yliopisto
          location: Turku, Finland
          date_start: '2013-11-29'
          date_end: ''
          description: |2-
              Significant contributions:

              * PhD completed in 2018
              * Post-graduate research with no passive years in publishing
              * Mentorship of three PhD students
        - title: Research physician
          company: Clinical Research Services Turku (CRST)
          company_url: https://www.crst.fi/
          company_logo: custom/crst
          location: Turku, Finland
          date_start: '2006-05-02'
          date_end: '2006-05-31'
          description: |2-
              Worked in a multidisciplinary team to implement clinical trials for pharmaceutical and food products, ensuring compliance with Good Clinical Practice (GCP) guidelines throughout the research process
    design:
      columns: '2'
  - block: resume-awards
    content:
      title: Awards
      username: admin
--- 