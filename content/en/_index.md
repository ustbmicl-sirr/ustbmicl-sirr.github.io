---
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Swarm Intelligence
        Research Lab
      image:
        filename: welcome.jpg
      text: |
        <br>

        **Swarm Intelligence Research Lab (SIRL)** focuses on cutting-edge research in swarm intelligence, multi-robot systems, and distributed cooperative control. We are dedicated to exploring the applications and innovations of collective intelligence in robot collaboration, multi-agent systems, and SLAM.

  - block: collection
    content:
      title: Research Projects
      subtitle: ''
      text: ""
      count: 6
      filters:
        folders:
          - project
    design:
      view: card
      columns: '2'

  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image:
          filename: coders.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen

  - block: collection
    content:
      title: Recent Publications
      subtitle: ''
      text: ""
      count: 5
      filters:
        folders:
          - publication
    design:
      view: citation
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./project/" cta_text="View All Projects →" %}}
    design:
      columns: '1'
---
