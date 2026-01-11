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

        **SIRR (Swarm Intelligence for Robotics Research)** 探索群智能理论及其在多样化协作场景中的应用。我们的研究涵盖多机器人系统、无人机集群、智能交通、分布式传感器网络、人机协作等领域，旨在复杂真实环境中实现智能集体行为。

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
