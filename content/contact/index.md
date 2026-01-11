---
title: 联系我们
date: 2022-10-24

type: landing

sections:
  - block: contact
    content:
      title: 联系我们
      text: |-
        欢迎对群智能研究感兴趣的同学和老师与我们联系。我们长期招收对群智能、多机器人系统、SLAM等方向感兴趣的本科生、硕士生和博士生。
      email: contact@example.org
      phone:
      address:
        street:
        city: 北京
        region:
        postcode: '100000'
        country: China
        country_code: CN
      coordinates:
        latitude: '39.9042'
        longitude: '116.4074'
      directions:
      office_hours:
        - '周一至周五 9:00-17:00'
      appointment_url: ''
      #contact_links:
      #  - icon: comments
      #    icon_pack: fas
      #    name: Discuss on Forum
      #    link: 'https://discourse.gohugo.io'
    
      # Automatically link email and phone or display as text?
      autolink: true
    
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: contact.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen
---
