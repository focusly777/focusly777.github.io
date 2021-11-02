---
title: "Splash Page2"
layout: splash
permalink: /splash-page2/
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/unsplash-image-1.jpg
  actions:
    - label: "Read more"
      url: "https://focusly777.github.io/categories/"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "ART + TECH + HEART, <br>
고대그리스시절<sup>(플라톤, 피타고라스 등)</sup>부터 중세 르네상스시절<sup>(레오나르도 다빈치,미켈란젤로)</sup>까지 아름다움을 연구하는 예술가와 기술을연구하는 과학기술자와 철학<sup>(사랑과 자유에 대한 연구를 하는)</sup>자는 지금처럼 분리되어있지 않았습니다. "
intro: 
  - excerpt: 어떤사람은 아름다움만 연구하고 어떤사람은 과학기술만 연구하고 어떤사람은 철학만연구한다면, 본질을 잊게 되버리죠.  '따로따로 떨어졌기떼분에 원형적이고 본질적인것과 우리는 점점 멀어졌고, 현대인은 자신안에서 빛나는 내면의 밝은 빛의 길을 읽어버렸습니다. 더이상 영감에 넘치지도 않으며, 분노조차도 낼 힘이 없어졌습니다.  내면의 공허함속에서 우리는 열망해야합니다. 저는 오랜시간 열망해왔습니다. '
feature_row:
  - image_path: assets/images/unsplash-gallery-image-1-th.jpg
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 1"
    title: "Placeholder 1"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Placeholder 2"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/unsplash-gallery-image-3-th.jpg
    title: "Placeholder 3"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
feature_row2:
  - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Left Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Left aligned with `type="left"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Right Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row4:
  - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Center Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Centered with `type="center"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}