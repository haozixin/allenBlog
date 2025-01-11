---
layout: post
title: "Monash Winter Research"
date:   2023-09-01
tags: [Research Assistant, Software Engineering] 
comments: true
author: allen
---


**Title:** Optimizing Healthcare Workflow with ChatGPT-Enabled Patient Information 
Collection


Github Link: https://github.com/haozixin/medicalGPT

## Details

### Background

The background of this project is that hospitals spend a significant amount of time collecting patient information by filling out forms, which wastes doctors’ and nurses’ time and affects their work efficiency. Therefore, I decided to use ChatGPT to help hospitals optimize this process, enabling doctors and nurses to collect patient information more quickly and improve their efficiency.

At the time, ChatGPT was just emerging, so we considered leveraging it to help optimize the process. We started by collecting some data from the hospital and then used ChatGPT to streamline the workflow.

However, with the evolution of ChatGPT, the application we developed might now be outdated or replaced by simpler alternatives. Nonetheless, the significance of this project remains critical—the need still exists, and the design approach may still hold value as a reference.

Our application was developed based on the hospital’s requirements, and we made improvements according to their feedback.

### Main ideas

1. Requirements & Functions：

    Our application automatically interacts with patients to collect their information and fills it into forms (while also generating a summary and highlighting key details). The questions asked are guided by instructions provided by doctors, ensuring comprehensive coverage of all necessary information and deeper follow-up inquiries. To enhance the user experience, we also implemented an answer suggestion feature, which predicts possible answers in advance, allowing users to simply click on the appropriate response.

2. Design & Implementation:
    
    We used four ChatGPT instances working collaboratively: one was responsible for asking questions, another for generating answer suggestions, a third for creating summaries, and the last one for guiding the question-asking ChatGPT to ensure we gathered sufficient information in both depth and breadth.

    We integrated these four ChatGPT instances using backend logic and developed the chatbot’s frontend.



### What I did

- Participate in the design of back-end logic development. Design promptions for 4 components.
- Completed a simple version with same logic as final product (backend - Python, frontend - Gradio), serving as a testing and tuning platform for preliminary testing and exploration.
- Conducted prompt engineering, reviewed 10 papers about designing an evaluation matrix to assess quality of robot.


### Challenges

During the development process, we received feedback from the client that the chatbot’s questions lacked breadth (i.e., certain areas were not being covered). However, for ChatGPT at the time, breadth and depth were inherently opposed—no matter how the prompts were designed, improving one would come at the expense of the other.

To address this, we optimized by adjusting ChatGPT’s divergence to a relatively broader setting (to ensure depth-related needs were met) and then compensated for the lack of depth with backend logic. For instance, after ChatGPT asked 10 questions about Area A, it would automatically switch prompts to inquire about another area.

Through this optimization approach, we improved the chatbot’s performance and successfully met the client’s requirements.





