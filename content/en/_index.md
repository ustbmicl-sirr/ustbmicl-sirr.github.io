---
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        SIRR
        Swarm Intelligence for Robotics Research
      image:
        filename: welcome.jpg
      text: |
        <br>

        **SIRR (Swarm Intelligence for Robotics Research)** explores swarm intelligence theories and their applications across diverse collaborative scenarios. Our research spans multi-robot systems, UAV swarms, intelligent transportation, distributed sensor networks, and human-robot collaboration, aiming to enable intelligent collective behavior in complex real-world environments.

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
