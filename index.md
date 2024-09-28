---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

permalink: /
title: Home
layout: all
---

![RR banner](assets/img/banner.png)

#### Details
- When: 13:30-17:30 ([MDT](https://www.worldtimeserver.com/current_time_in_CA-AB.aspx?city=Edmonton), UTC-6) \| Tuesday, September 24, 2024
- Where: Room **Salon 5** \| Edmonton Convention Center \| Edmonton, Canada
- 👉 Participants should **bring laptops with [installed required software]({% link requirements.md %})** to participate in hands-on sessions. 

#### Overview
This tutorial is dedicated to **reproducible research (RR) in transportation**. As transportation researchers, it has been our experience that research in transportation is hard to reproduce. Needless to say, this holds back the scientific progress of the field; every time a student needs to re-implement another paper or collect a similar dataset, that is time that could have been spent on new research. Fortunately, tools and best practices supporting RR are maturing, so it is the perfect time for the ITS community to engage with RR. We hope that this tutorial will help to move the needle on reproducibility in transportation, so that our research collectively achieves greater impact.

This is the first of hopefully many tutorials on RR in transportation; as such, we want your feedback on your RR needs and interests! Please do not hesitate to get in touch.

#### Background

Reproducibility is a cornerstone of scientific research, providing the foundation for validating results and advancing knowledge. In research fields where computation-based scientific publication is pervasive, a credibility crisis has been warned. RR is gaining extensive attention in various fields, such as remote sensing, medicine, and data science, to ensure the validity and reliability of scientific findings.

In the field of traffic and transportation, Intelligent Transportation Systems (ITS) represent the most computationally intensive, fast-growing area of research with significant implications of outcomes for the general population. In ITS, the rapid evolution of technologies and methodologies has emphasized the need for RR practices. Reproducibility can refer to computational reproducibility (the focus of this tutorial), ensuring that the same data and analysis steps produce consistent results. However, when it is infeasible to replicate an entire scientific study, achieving reproducibility sets a minimum standard of scientific rigor by allowing others to validate and build upon the findings. With ITS being inherently interdisciplinary and data-driven, reproducibility forms the backbone for credible, reliable research outputs.

#### The objectives of the tutorial
- An introduction to the fundamental concepts and importance of RR to the domain of ITS 
- Provide hands-on training in the use of tools and software that facilitate reproducibility
- Guide researchers on how to properly document and organize data and project outcomes to foster open science
- Encourage collaboration among tutorial participants and the broader ITS community to foster a community that values and practices reproducible research

#### Topics we will cover

- **Foundations of reproducible research (RR)**: What does it mean for research to be reproducible? Why is it important? Why is it worthwhile to engage in RR? What makes reproducibility hard? Even when provided the exact dataset and code of another research paper?!
- **RR challenges in ITS**: What are challenges of RR in the field of ITS? Are they general across many fields or specific to this one? What are examples of (non-)reproducibility in ITS research?
- **The state of RR in ITS**: Through a live participant survey, we will get a taste of the RR attitudes and needs of the ITS community.
- **Documenting code and data for RR**: What kinds of missing metadata can be responsible for reproducibility failures? How can version control tools like git and github be used for RR? How can project files be organized for readability?
- **Hands-on activities**: Through two hands-on activities, participants will attempt to create small reproducible projects. Another participant will then try to reproduce it. Will they succeed? The first activity will focus on a simple report. The second activity will use a small project with code and data.

#### Participant requirements
Participants should **bring laptops with [installed required software]({% link requirements.md %})** to participate in hands-on sessions.

### Tentative Schedule

<table>
<thead>
  <tr>
    <th>Time (<a href="https://www.worldtimeserver.com/current_time_in_CA-AB.aspx?city=Edmonton">MDT</a>, UTC-6)</th>
    <th>Event</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>13:30 pm - 13:40 pm</td>
    <td>Introductory Remarks</td>
  </tr>
  <tr>
    <td></td>
    <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSdUXa7uf4D9zW8D6UEkNYb8ue0GayxvcXmuTSTpqiZypv5eGQ/viewform">Pre-tutorial survey</a></td>
  </tr>
  <tr>
    <td>13:40 pm - 14:55 pm</td>
    <td><b>Session 1: Introduction to Reproducible Research</b> <br/>Speakers/Contributors: Bidisha Ghosh, Zuduo Zheng</td>
  </tr>
  <tr>
    <td></td>
    <td><a href="https://docs.google.com/presentation/d/1ocI17qjLhJwA-6DWOF61kSNBBiUvSgbz5cCmImSLe70/edit">Lecture 1: Introduction to reproducible research</a></td>
  </tr>
  <tr>
    <td></td>
    <td>Hands-on activity 1: Is your research reproducible? <br/><br/>
    👉 Please download the following two csv files for this activity:
    <ul>
      <li><a href="session_files/session1/data_TCS183.csv">data_TCS183.csv</a></li>
      <li><a href="session_files/session1/data_TrafficData.csv">data_TrafficData.csv</a></li>
    </ul>
    </td>
  </tr>
  <tr>
    <td>14:55 pm - 15:30 pm</td>
    <td><b>Session 2: Documentation of Data and Code for Reproducibility</b> <br/>Speaker: Cathy Wu, TA: Junyi Ji</td>
  </tr>
  <tr>
    <td></td>
    <td><a href="https://docs.google.com/presentation/d/11I0fnvDBUvcsiQ0mezRysiLBvfzGHPz92kT_R9PXey8/edit">Lecture 2: How to badly document a research project</a>
      <br/> <br/>
      <em>Learning objectives:</em>
      <ul>
        <li>Fundamentals of organizing projects, code, & data</li>
        <li>Working knowledge of Github</li>
        <li><em>(Advanced skills)</em> Automatically extract the computing environment for reproducibility</li>
        <li><em>(Advanced skills)</em> VS Code and powerful extensions (tools for Jupyter, Markdown, csv, lint)</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>Hands-on activity 2: Can you reproduce my simulation results in 5 minutes?
      <br/> <br/>
      👉 <b>Please make sure to go through the <A href="{% link requirements.md %}#requirements-section2">participant requirements</A> prior to this session.</b> <br/> <br/>
      <em>Learning objectives:</em>
      <ul>
        <li>Main goal: Create an ITS project that someone can reproduce in less than 5 minutes.</li>
        <li>Stretch goal: Organize the project and make it understandable.</li>
      </ul>
      👉 Please download the following messy code files for this activity:
      <ul>
        <li><a href="session_files/session2/itsc24-rr-tutorial-example-messy-v1.1.zip">itsc24-rr-tutorial-example-messy-v1.1.zip</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>15:30 pm - 16:00 pm</td>
    <td>Coffee Break and Office Hours</td>
  </tr>
  <tr>
    <td>16:00 pm - 17:25 pm</td>
    <td><b>Session 2: Documentation of Data and Code for Reproducibility (cont...)</b></td>
  </tr>
  <tr>
    <td>17:25 pm - 17:30 pm</td>
    <td>Concluding Remarks</td>
  </tr>
  <tr>
    <td></td>
    <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSePwCggee6GQAV1P6AedYjQvx_zGigVMnIJpB7u7T16GD-3OQ/viewform">Post-tutorial survey</a> (and optionally, sign up to stay in touch or get involved)</td>
  </tr>
</tbody>
</table>

### Citing the tutorial

If you use this tutorial in your work, you are encouraged to cite us:

C. Wu, B. Ghosh, Z. Zheng, and I. Martínez, “Reproducibility in transportation research: a hands-on tutorial.” IEEE International Conference on Intelligent Transportation Systems (ITSC), 2024. [Online]. Available: https://rrintransportation.github.io/itsc24-rr-tutorial/

```
@misc{wu2024reproducibility,
  title = {Reproducibility in Transportation Research: A Hands-on Tutorial},
  author = {Wu, Cathy and Ghosh, Bidisha and Zheng, Zuduo and Mart{\'i}nez, Irene},
  year = {2024},
  publisher = {IEEE International Conference on Intelligent Transportation Systems (ITSC)},
  url = {https://rrintransportation.github.io/itsc24-rr-tutorial/}
}
```

### Acknowledgements
We are grateful to the [REROUTE](https://reroute-project.eu/) project funded by Horizon Europe Marie Skłodowska-Curie Actions (MSCA) for financial support. We thank our early testers of the material: Cathy Wu’s research group, Xiaoyi Wu, Junyi Ji, Kate Sanborn, and Bidisha Ghosh's research group. Thank you to Vindula Jayawardana and Jung-Hoon Cho for feedback and contributing materials, to Nicholas Saunier for brainstorming, the [RERITE working group](https://rrintransportation.github.io/) for moral support, the [ITSS Educational Activities Committee](https://ieee-itss.org/educational-activities/) for dissemination, and, last but not least, to [ITSC 2024](https://ieee-itsc.org/2024/) for giving us a platform and a deadline. :)


### Potential future topics and activities
We simply did not have enough time to cover many important topics in the area! If you have suggestions for what you need to succeed in your research, we are all ears. Here are a few potential future topics and activities:
- **A Special Issue on Reproducible Research in Transportation**: We are doing this! See our [call for papers](https://www.springeropen.com/collections/RRT24) for European Transport Research Review (ETRR).
- **A Special Issue on Datasets and Benchmarks**: Explicitly reward creation of datasets and benchmarks that enable comparable and reproducible research in transportation.
- **Focus groups** to identify unique reproducibility barriers for subareas within transportation (e.g., travel demand, traffic flow theory, etc.).
- **A reproducibility checklist for transportation research**, such as for [NeurIPS](https://neurips.cc/public/guides/PaperChecklist) and [AAAI](https://aaai.org/conference/aaai/aaai-25/aaai-25-reproducibility-checklist/).
- **Data sharing and management for RR**: What are best practices for storing data? How to choose a data format, and does it matter? How to participate in RR inspite of data with sensitive information?
- **Reproducible Analysis**: Our analysis pipeline are getting more and more sophisticated. What are best practices for leveraging Jupyter or Google Colab notebooks to perform and share interactive analysis?
- **Reproducible Reporting**: What are dynamic documents? Reproducible reports? How does someone create one?
- **Best Practices for Peer Review and Publication**: What role do reviewers and publication policies play in reproducible research? How can we move the needle forward? What are open science checklists? How well are they working?
- **Reproducibility in Machine Learning and AI**: How can we standardize and manage ML experiments for reproducibility? 
- **Addressing non-technical barriers to reproducible research**: The elephant in the room is the pressure to 'publish or perish'; researchers simply respond to the incentive structure. What or who can make a difference in RR?
- **Case Studies in ITS**: Do we understand the extent of the RR issue in the field of ITS? How can we find out? What are the success stories of RR in ITS? What are the horror stories?
- **Hands-on RR workshop**: Participants bring a research project and work on making it reproducible (lectures, work sessions, collaborative sessions, discussion).