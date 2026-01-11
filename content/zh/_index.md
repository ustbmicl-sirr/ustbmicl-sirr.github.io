---
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        SIRR
        面向机器人的群智能研究
      image:
        filename: welcome.jpg
      text: |
        <br>

        **SIRR (Swarm Intelligence for Robotics Research)** 专注于将群智能理论与算法应用于机器人领域。我们的研究涵盖多机器人协同、自主导航、协同SLAM，并扩展至物联网、边缘计算、智能交通等相关应用领域。

  - block: collection
    content:
      title: 研究项目
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
      title: 最新论文
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
        {{% cta cta_link="./project/" cta_text="查看所有项目 →" %}}
    design:
      columns: '1'
---
