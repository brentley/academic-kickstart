---
title: Encrypting and Managing Secrets in EKS
summary: Secure EKS Secrets using KMS
tags:
- Encryption
- Security
- EKS
date: "2020-05-17T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

# Containers University

# Video 0
{{< vimeo 420245095 >}}

## Intro to Amazon EKS Secrets Encryption

- etcd store for base64 encoded secrets
- Difference between encoding and encryption
- Demonstrate the difference using code

# Video 1
## Creating a KMS CMK in AWS KMS and Key Origins

- Create a new KMS CMK
- Explain CMK Key Origins and the benefits of each


# Video 2
## Creating a cluster with Secrets Encryption using `eksctl`

- Open yaml cluster config
- Add KMS Key created in previous video
- Create cluster
- Describe cluster

# Video 3
## Create a secret within cluster

- Create secret
- Describe secret
- Show logs
- Show etcdctl view


# Video 4
## Conclusion and Recap

- What we learnt
- How this is useful
