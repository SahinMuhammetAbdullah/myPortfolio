---
id: urldet 

order: 1

title: "URLDet | Malicious URL Analysis"

short_description: "An application featuring a browser extension and a web-based query screen for malicious URL analysis, developed using Machine Learning and Reinforcement Learning."

tags: ["Python", "Machine Learning", "Reinforcement Learning", "JavaScript", "React JS"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fa-solid fa-blog"

cover_image: "/assets/images/projects/urldet-img.png"
live_url: "https://urldet.masahin.dev"

layout: default
description: "An application featuring a browser extension and a web-based query screen for malicious URL analysis, developed using Machine Learning and Reinforcement Learning."
image: /assets/images/projects/urldet-img.png
lang: en
---

## Working Principle

A system with over 97% accuracy has been developed as a result of tests and training conducted on more than 1 million URL data points.

### The system has a two-stage structure:

1. Maliciousness Detection (Binary Classification):
In the first stage, it is determined whether the entered URL is malicious or benign. In this stage, classical machine learning algorithms such as Random Forest, SVM, and Naive Bayes were compared, and the model with the highest accuracy rate was selected.

2. Malicious Type Determination (Multi-class Classification):
URLs identified as malicious are further analyzed in the second stage using the **Reinforcement Learning** method and classified into categories such as phishing, malware, or defacement. In this process, the model constantly improves itself through a reward-penalty mechanism and adapts to new threat types.

Additionally, the blacklist module within the system reduces processing load by preventing URLs that have already been detected as malicious from being analyzed again.

The browser extension developed within the scope of the project evaluates the security of the links users intend to visit in real-time and shows the URL's status with icons in the search results. Furthermore, through the web-based interface, users can manually query any URL and access a detailed analysis report.

In this way, URLDet offers a powerful, scalable, and continuously self-improving cybersecurity solution for both end-users and security analysts.