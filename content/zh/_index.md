---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        群智研究实验室
        Swarm Intelligence Lab
      image:
        filename: welcome.jpg
      text: |
        <br>

        **群智研究实验室 (Swarm Intelligence Research Lab)** 专注于群智能、多机器人系统、分布式协同控制等前沿研究领域。我们致力于探索群体智能在机器人协同、多智能体系统、SLAM等方向的应用与创新。

  - block: collection
    content:
      title: 研究项目
      subtitle: Research Projects
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
      subtitle: Recent Publications
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
