<div align="center">
  <img width="200" height="200" alt="Fullsterkur.ai logo" src="https://github.com/user-attachments/assets/5cc5737e-2b27-4554-a98e-d19ebabedd88" />

  # J26-SE-342 | Fullsterkur.ai
  *Full strength, with modern technology*

  AI-driven strength training for modern athletes

</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#system-and-architecture-design">System and Architecture Design</a>
      <ul>
        <li><a href="#components">Components</a></li>
      </ul>
    </li>
    <li><a href="#development">Development</a></li>
    <li><a href="#team">Team</a></li>
  </ol>
</details>

---

## Introduction

Fullsterkur.ai is a research project from **J26-SE-342**, a research team of SLIIT (Sri Lanka Institute of Information Technology). It explores how AI and modern technology can aid strength athletes and coaches with training, program planning, recovery, nutrition and hydration.

Coaches do a great job with program planning. Years of trial and error have taught them what works, and they are good at watching athletes and giving the right cues. However, they cannot match a computer's precision on minor details, and those details matter a lot to some athletes. Fullsterkur.ai tries to provide those details as suggestions, so coaches and athletes can both benefit from them.

Athletes also cannot always rely on a coach. Many cannot afford one, and many train alone. This project is meant to help those athletes as well. It aims to answer the everyday questions that come up in training:

- How should I train this week?
- Is my technique ok?
- When should I push, and when should I hold back?
- Is my body holding up, or do I need more recovery? If so, what kind?
- What should I eat and drink, given the weather, my mood, my sleep, and how I feel?

This repository is the entry point to the project. It links to every component repository and explains how the pieces fit together.

## System and Architecture Design

The overall solution will be delivered a **mobile app**, where users can conveniently use them in any setting they are in; whether that be from home, work or from the gym.
However, the solution also comes as a **web application** for in detailed planning where a small screen would not help much.

Fullsterkur.ai uses a **microservices** architecture, where each component is its own service. This lets each team member focus on one part at a time, using the methods they are comfortable with, and it isolates failures so that a problem in one service does not take down the whole system.

<img width="1003" height="446" alt="image" src="https://github.com/user-attachments/assets/247600b5-428d-49d7-ba5b-6499e5be0c19" />


### Components

Each part of the system lives in its own repository.

#### Services

- [Mobile](https://github.com/fullsterkur-ai/mobile): Mobile application for Fullsterkur.ai
- [BFF](https://github.com/fullsterkur-ai/bff): Backend for Frontend. Connects the services together
- [Program Planner](https://github.com/fullsterkur-ai/program-planner): Periodized program planner and recommendation generator
- [Lift Analyzer Service](https://github.com/fullsterkur-ai/lift-analyzer-service): Analyzes lifts
- [Rehabilitation Service](https://github.com/fullsterkur-ai/rehabilitation-service): Fatigue management and rehabilitation
- [Environment Nutrition Service](https://github.com/fullsterkur-ai/environment-nutrition-service): Nutrition and hydration coach

#### Tools and Experiments

- [Lift Analyzer Tool](https://github.com/fullsterkur-ai/lift-analyzer-tool): Python desktop application to analyze lifts on the go
- [Periodization tool](https://github.com/fullsterkur-ai/periodization-tool): Experimenting periodization engine implementation
- [Playground](https://github.com/fullsterkur-ai/playground): Free-form testing space for experimenting before building anything big


## Development

For coding conventions, branching and merging strategy, please refer to [DEVELOPMENT.md](DEVELOPOMENT.md)

## Team

**J26-SE-342**

| <img src="https://github.com/RivinmaWethmini.png" width="100" /> | <img src="https://github.com/SanjithaRa.png" width="100" /> | <img src="https://github.com/Seniru.png" width="100" /> | <img src="https://github.com/smthilakaratne.png" width="100" /> |
|:---:|:---:|:---:|:---:|
| D.M. R. W. Dissanayake (IT23166660)<br>RivinmaWethmini | S. Ratnayake (IT23156838)<br>SanjithaRa | Indira D. H. S. P. (IT23284852)<br>Seniru | Thilakaratne A. A. S. M. (IT23205956)<br>smthilakaratne |
| Environmental Quality & Nutrition Timing Optimizer | Recovery & Fatigue Management Suite | Lift Analysis | Periodization Program Planning Tool |


**Supervisor:** [Ms. Aparna Jayawardena](https://www.sliit.lk/academic/academic-staff/aparna.j), Lecturer, Department of Software Engineering, Faculty of Computing, SLIIT

**Co-Supervisor:** [Ms. Kaushalya Rajapakse](https://www.sliit.lk/academic/academic-staff/kaushalya.r), Assistant Lecturer, Department of Software Engineering, Faculty of Computing, SLIIT


<p align="right">(<a href="#top">back to top</a>)</p>
