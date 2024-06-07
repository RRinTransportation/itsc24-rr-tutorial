---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

permalink: /
title: Home
layout: all
---

![RR banner](/assets/img/banner.png)

This workshop will investigate the role of learning within Task and Motion Planning (TAMP). TAMP has shown remarkable capabilities in scaling to long action sequences, many objects and a variety of tasks. However, TAMP often relies on simplified models, assumes perfect world knowledge, and requires long computation time, which limits the real world applicability. To address these limitations, there has been significant recent interest in integrating learning methods into TAMP [
<span class="secret1"><a href="https://proceedings.mlr.press/v164/ortiz-haro22a.html" target="_blank">1</a></span><span class="reveal1">Structured deep generative models for sampling on constraint manifolds in sequential manipulation. <br>Joaquim Ortiz-Haro, Jung-Su Ha, Danny Driess, Marc Toussaint. <br>CoRL 2022.</span>,
<span class="secret2"><a href="https://arxiv.org/abs/2210.12250" target="_blank">2</a></span><span class="reveal2">TAPS: Task-Agnostic Policy Sequencing. <br>Christopher Agia, Toki Migimatsu, Jiajun Wu, Jeannette Bohg. <br>arXiv 2022.</span>,
<span class="secret3"><a href="https://arxiv.org/abs/2210.12631" target="_blank">3</a></span><span class="reveal3">Guided skill learning and abstraction for long-horizon manipulation. <br>Shuo Cheng, Danfei Xu. <br>CoRL Workshop on Learning, Perception, and Abstraction for Long-Horizon Planning 2022.</span>,
<span class="secret4"><a href="https://arxiv.org/abs/2103.00589" target="_blank">4</a></span><span class="reveal4">Learning symbolic operators for task and motion planning. <br>Tom Silver, Rohan Chitnis, Joshua Tenenbaum, Leslie Pack Kaelbling, Tomás Lozano-Pérez. <br>IROS 2021.</span>,
<span class="secret5"><a href="https://arxiv.org/abs/2211.01576" target="_blank">5</a></span><span class="reveal5">Sequence-based plan feasibility prediction for efficient task and motion planning. <br>Zhutian Yang, Caelan Reed Garrett, Leslie Pack Kaelbling, Tomás Lozano-Pérez, and Dieter Fox. <br>RSS 2023.</span>
]. Despite this progress, there remain many open questions that must be addressed before learning-based TAMP can be applied in real-world settings and in full generality.

The goal of this workshop is to bring together a diverse set of researchers from TAMP, learning for TAMP, computer vision, classical AI planning, and NLP to discuss not only the current state of learning for TAMP, but also the broader state of learning for planning in robotics. Subtopics include: benchmarks, language, perception, skill learning, manipulation, closed-loop TAMP, and policy learning. All of these discussions will take place against the backdrop of recent progress in foundation models.


#### Discussion Topics

- **Benchmarks**: What benchmark environments will help the community better measure the progress of TAMP and integrate learning with TAMP?
- **Large Language Models for Task Planning**: LLM has shown promise in generalizable task planning. What are the potentials and challenges in integrating LLM with TAMP?
- **Perception**: Perception in TAMP and the latest developments in this area, including 3D computer vision, open-world recognition, and sensor fusion.
- **Error Recovery / Closed-Loop TAMP**: Techniques and principles that allow TAMP to be more robust and recover from errors and interventions.
- **Skill Learning / Manipulation**: Skill learning and manipulation for TAMP, including but not limited to deep reinforcement learning and imitation learning. How do we make the learned skills generalizable and composable?
- **Model Learning**: Techniques and principles for learning discrete or continuous transition models from interaction data.


### Schedule

The workshop happened on July 10 in hybrid mode. The in-person location is in Daegu, Republic of Korea. 

The [recording of the workshop](https://youtu.be/5VN7T0HujnQ) can be accessed on YouTube.

<table>
<thead>
  <tr>
    <th>Time (<a href="https://www.worldtimeserver.com/current_time_in_KR.aspx?city=Daegu">KST</a>, GMT+9)</th>
    <th>Event</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>9:00 am - 9:10 am</td>
    <td>Introductory Remarks</td>
  </tr>
  <tr>
    <td>9:10 am - 9:25 am</td>
    <td>Invited Talks 1: Siddharth Srivastava</td>
  </tr>
  <tr>
    <td>9:25 am - 9:40 am</td>
    <td>Invited Talks 2: Pratyusha Sharma</td>
  </tr>
  <tr>
    <td>9:40 am - 9:55 am</td>
    <td>Invited Talks 3: Dieter Fox (Remote)</td>
  </tr>
  <tr>
    <td>9:55 am - 10:30 am</td>
    <td>Panel 1: Dieter Fox (Remote), Pratyusha Sharma, Siddharth Srivastava</td>
  </tr>
  <tr>
    <td>10:30 am - 11:00 am</td>
    <td>Coffee Break</td>
  </tr>
  <tr>
    <td>11:00 am - 11:15 am</td>
    <td>Spotlight Talks 1: Nishanth Kumar, Willie McClinton (Remote)</td>
  </tr>
  <tr>
    <td>11:15 am - 11:30 am</td>
    <td>Spotlight Talks 2: Robert Gieselmann</td>
  </tr>
  <tr>
    <td>11:30 am - 11:45 am</td>
    <td>Spotlight Talks 3: Nina Marie Moorman</td>
  </tr>
  <tr>
    <td>11:45 am - 12:00 pm</td>
    <td>Spotlight Talks 4: Zirui Zhao</td>
  </tr>
  <tr>
    <td>12:00 pm - 1:30 pm</td>
    <td>Lunch</td>
  </tr>
  <tr>
    <td>1:30 pm - 3:00 pm</td>
    <td>Poster session</td>
  </tr>
  <tr>
    <td>3:00 pm - 3:30 pm</td>
    <td>Coffee Break</td>
  </tr>
  <tr>
    <td>3:30 pm - 3:45 pm</td>
    <td>Invited Talks 4: Hector Geffner</td>
  </tr>
  <tr>
    <td>3:45 pm - 4:00 pm</td>
    <td>Invited Talks 5: Florian Shkurti</td>
  </tr>
  <tr>
    <td>4:00 pm - 4:15 pm</td>
    <td>Invited Talks 6: Masataro Asai (Remote)</td>
  </tr>
  <tr>
    <td>4:15 pm - 4:50 pm</td>
    <td>Panel 2: Masataro Asai (Remote), Hector Geffner, Florian Shkurti</td>
  </tr>
  <tr>
    <td>4:50 pm - 5:00 pm</td>
    <td>Conclusion Remarks / Best Paper Award</td>
  </tr>
</tbody>
</table>


Please use this [Latex paper template](https://zt-yang.github.io/rss23-l4tamp-workshop/assets/paper-template-latex.zip) and [submit](https://openreview.net/group?id=roboticsfoundation.org/RSS/2023/Workshop/LTAMP) via Open Review. Review will be single-blind so there's no need to anonymize your document.
