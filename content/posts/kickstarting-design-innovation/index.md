---
title: "Kickstarting design innovation"
date: 2017-09-14T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags:
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
comments: false
description: "Training a team to prototype inspires the launch of a corporate design innovation lab."
canonicalURL: "https://www.shanewasley.me/posts/kickstarting-design-innovation"
disableHLJS: true # to disable highlightjs
disableShare: true
hideSummary: true
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: true
---


| `Highlights`       | |                                       |
|----------------------|-|-------------------------------------------------------------|
| **Format**        | | Case Study                                                    |
| **Company**          | | Turner Construction Co.                                      |
| **Product**          | | Web app prototype                                            |
| **Users**            | | Superintendents at construction mega-sites                        |
| **Role**             | | UX Designer                                                  |
| **Team**            | | Two other designers, one product manager                     |
| **Timeline**         | | Five months in 2017, while working on parallel projects              |
| **Skills & Methods** | | Sketching, task flows, prototyping, training the team to perform user research |
| **Tools**            | | Sketch, Framer Classic, paper prototypes                     |
| **Deliverables**     | | Research synthesis reports, personas, experience maps, sketches, prototypes |
| **Outcome**   | | Formation of design innovation lab |

## Introduction

As a UX designer, I led the research and design process for an application intended to help superintendents monitor work progress at construction sites. My team's efforts lead to an organization-wide transformation towards design-driven innovation at one of the world's largest construction companies.

## Summary

Turner Construction Co. manages mega-projects: construction projects above $1 billion, such as skyscrapers and hospitals. Delays in the scheduled work on a mega-project site present a colossal source of increased costs and reduced profit—and a significant motivation to understand the causes of these delays and develop ways of preventing them or responding more quickly to mitigate them.

At Turner, I joined a design team that focused on reducing schedule delays on mega-projects. Our task included researching why Turner’s current progress-tracking tools were failing to deliver value and how our team might design a solution that could provide more user-targeted information and thus greater value for the company’s superintendents.

Our four-person team worked from Turner’s offices in Oakland, CA., for five months to create user-focused desktop and mobile solutions. Our goal was to research the needs of Turner’s superintendents, design a technology that could help them perform construction planning tasks more quickly, and then present our results and recommendations to the Turner executive team.

My most valuable direct contributions were to facilitate the design and strategy workshop, transform the findings from Turner’s internal research into a design project plan, design several interactive prototypes, and train the team to conduct user and product research in the field. The most significant outcome of my work at Turner was the organizational change towards design-driven innovation, including creating an internal innovation team.

## Problem

### Delays to the construction schedule were increasing costs

As a construction project gets underway, tradespeople enter the site, do their work, and hand-off to the next team—from pouring concrete for the foundation to completing the interior finishing and decoration. The construction schedule defines all of the hand-offs from one work team to the next.

{{< webp image="/images/turner/turner-construction-parade-trades.jpg" caption="From foundation onwards, mega-construction projects run on schedules that dictate the sequence of thousands of tradespeople and activities at the site. Photos by Scott Blake, Jose Figueroa, Ricardo Gomez Angel, Morgan Von Gunten @Unsplash." >}}

When teams fall behind schedule in their assigned work, they create delays for the teams that follow, which puts the project’s final delivery date at risk. Such delays are common in construction and pose a big problem for the industry. A McKinsey report acquired by Turner Construction showed the following:

{{< blockquote author="— McKinsey Co. report for Turner’s industry" >}}
  “Schedule delays add an average of 20 additional months and 80% additional costs to mega-projects.”
{{< /blockquote >}}

When Turner’s executive team considered the potential risk to their profit margin on upcoming mega-projects, they were eager to find solutions to help their work teams stay on schedule by being more responsive in mitigating any delays.

### Becoming more responsive to construction delays required new technology

The speed at which problems are identified and resolved is critical to the success of any operation. Think about a time you sent in a support ticket to your IT department, and they responded that they would get back to you in 24 hours. If that problem prevented you from working, then your company stood to lose a lot more money because of your inactivity than it would have lost if IT had responded to your problem in one hour or less.

Similarly, internal research conducted by Turner Construction showed that the company would lose less money due to schedule delays if the superintendents responsible for monitoring a job could respond more quickly to the problems tradespeople were having at the construction site.

An essential activity on a construction site—the site-walk performed by superintendents—significantly impacts responsiveness. During a site walk, the superintendent physically walks through the site to check the progress in each area and identify any problems. On mega-project sites like sports stadiums, this activity can take days to complete.

It is easy to see how the time starts to add up: a problem happens and takes days to identify, days to get reported, and even more days and several meetings to get resolved. Turner’s executives knew that the superintendents needed new tools to help them cut down the time lost in this process.

### Technologies Turner had selected to solve the problem were falling short

When I joined the design team at Turner, the company had already begun trials of a third-party application to help superintendents perform site assessments faster. This application overlaid photos taken at the site every day onto a floor plan that the superintendent could access and review by computer. The thinking went this way: if the superintendent could assess the site and identify problems by clicking on photos viewed on his office computer (rather than by walking the site), he would save time, and the work team involved could respond more quickly.

{{< webp image="/images/turner/turner-problem-current-tool.jpg" caption="Current tools were only providing heaps of construction site photos without the context needed to identify problems and create solutions." >}}

This application, however, was falling short in two key areas:

1. While photos were taken all over the site, only specific photos needed attention: the photos showing areas with problems that needed to be reviewed and solved. Since the tool did nothing to prioritize the areas the superintendent should direct the most attention to, the superintendent had to comb through hundreds of photos to find out where problems existed.
2. The application did not show which tradespeople were working on the building area that had been photographed. The superintendents needed to have this information included in the application to call the correct tradespeople and ask about any problems spotted in the photos.

### Summary: The Problem Statement

Our product would allow superintendents to save time by assessing construction site progress from their office computers instead of doing site walks. Our product would improve on other solutions because (1) it would visually prioritize areas for the superintendent to review, and (2) it would identify the tradespeople responsible for each area.

## Users

### Super Jack

The primary users for this project were Turner’s superintendents, whom we collectively named “Jack.” I got to know Jack through other members of my team who had interviewed Turner’s superintendents directly.

{{< webp image="/images/turner/turner-users-super-jack.png" caption="" >}}

Known as a “super” on the job, Jack has enormous shoes to fill as he manages the day-to-day operations at a mega-project construction site. He has to track the progress of hundreds of tradespeople in great detail while quickly prioritizing and resolving any problems before they affect the schedule.

{{< blockquote author="- a member of Turner’s design team" >}}
  “On the busy days, I’ve watched Jack answer requests on his phone every 8 seconds.”
{{< /blockquote >}}


The demands on Jack require that he have a rare form of focus and discipline to excel at his job. I learned that it is not uncommon for companies like Turner to recruit military commanders to fill positions like Jack’s. To understand why, consider the roles that Jack must play.

### Jack serves as a conduit between tradespeople and the Turner office

One of Jack’s most critical roles is that of arbitrator and intermediary between the tradespeople that build the project and the team based in the company office, which plans, approves, and finances all project activities.

{{< webp image="/images/turner/turner-users-super-conduit.png" caption="Jack is the conduit between the field teams who wield the tools and the office team that holds the plans and paychecks. Office photo by Campaign Creators @Unsplash" >}}

### Jack’s site walks uncover problems at the job site

One of Jack’s main tasks as the site-to-office conduit is performing walking tours of the construction site (site walks) to assess the tradespeople’s progress. Jack visits areas of the building where work is incomplete, talks to the tradespeople working there, and then documents the status of each area with paper notes and photographs.

{{< blockquote author="- a member of Turner’s design team" >}}
  “He’ll use whatever is available to him for taking notes. Sometimes he’ll grab a piece of scrap cardboard, outline a $1 million change order for the project on it, then stuff it in his belt.”
{{< /blockquote >}}

After completing the site walk, Jack uses all the source information he’s gathered to notate the status of each area on the building plans—with attention specifically on those areas that are behind schedule or need a problem resolved. Then Jack takes his notated plans to a meeting with the in-office team, where any findings that may affect the project’s schedule or budget are discussed and evaluated.

{{< webp image="/images/turner/turner-users-site-walk-meeting.jpg" caption="Jack's site-walks lead to meetings with the office team to update plans and schedules based on what problems Jack finds." >}}

### Site walks take too much of Jack’s time

Jack’s problem with site walks is that they require too much of his time to gather information. In addition, the Turner in-office team believes that Jack provides the most value for the company when he uses his expertise to assess progress and make decisions _from the data gathered_, not when he’s out walking around gathering data himself.

Therefore, to help Jack provide the most value for Turner, our design team needed to focus on a technology that would let Jack spend less time walking and collecting information and more time in the captain’s chair, making critical operational decisions for the construction areas he managed.

## Roles and Responsibilities

I worked as a contract UX designer on this project with a product designer and a visual designer. We reported to a Turner employee who was the project lead and product manager (PM). Our four-person team worked both remotely and on-site at the Turner offices in Oakland, Calif.

As the UX designer and researcher on the project, I was responsible for developing the project plan for my team’s research and design, creating research artifacts and design deliverables, and training my team members to conduct evaluative user research in the field. I spent most of my time working with the product manager—to whom I reported and provided deliverables.

The PM conducted the initial background user research, interviewed stakeholders, and conducted user testing with the prototypes I produced. The PM also organized our team’s meetings and established project milestones.

The product designer on the team had a background in construction technology applications working at Autodesk. The product designer performed competitive research and product research for the team and helped me improve my designs during critique sessions.

The visual designer created higher-fidelity mockups of the team’s designs near the end of the project. The PM used the visual designer’s work in our team’s presentations to executive stakeholders.

## Scope and Constraints

### Scope

I have limited the scope of this case study to the desktop prototype designed for a single user. Our team had five months to research, design, and present potential technology solutions to Turner’s executive team.

We also limited the prototype’s features to those that would address a single floor of a building during the phase of a construction project that occurs after the “enveloping,” or the completion of the building’s exterior walls, the point at which the interior infrastructure work begins. The work done in this phase of a construction project is sometimes referred to as “MEP” (for mechanical, electrical, plumbing).

### Constraints

The main challenge for our design team was gaining access to superintendent Jack. Superintendents spent most of their time at restricted construction sites. Only our PM and product designer had access to the sites. We risked designing outside of the superintendents’ specific needs with fewer opportunities to test and iterate our designs with input and feedback from the primary user.

I determined that the best way to address this problem was to design paper prototypes and train the team members who had site access to test those prototypes with the superintendents. In this way, our team could get the critical feedback it needed to design a user-centered prototype.

## Design Process

### Project Kickoff

When I joined this project, the initial design team at Turner had already spent months performing research and discovery. They had observed superintendents at Turner’s construction sites, interviewed numerous stakeholders, and reviewed several competitors’ technologies that did not provide the value Turner was seeking. Yet, as this team sat on a mountain of research findings, they were stuck on what to do next. What was the first problem they wanted to solve? Which roles should they focus on first?

### Design workshop

To kick off the project and get the initial team members unstuck, I conducted a week-long design workshop at Turner’s headquarters in Oakland, Calif. My goals for the workshop were these:

1. Learn about Turner’s specific needs for new technology.
2. Review the research the initial Turner design team had conducted.
3. Identify the primary user and most important problem to be solved
4. Understand why Turner’s current tools were not solving the problem.

We spent many hours at the whiteboard breaking down the hugely complex processes that underlie construction projects. I was greatly impressed by the deep expertise the initial team members brought to the meetings and excited by all the opportunities their research had revealed.

{{< webp image="/images/turner/turner-whiteboards.jpg" caption="Our design workshop became a crash coarse in how mega projects get done. TBH I don't expect you to learn much from this eye chart, I just placed it here to break up the text!" >}}

We achieved our main objectives for the workshop. We decided on the primary user of our work—Turner’s construction site superintendents—and we clarified a set of problems we would need to tackle—the superintendents’ site-planning tasks. We also established what was missing from the current planning applications that Turner was using.

At the end of the workshop, the team requested that I design an early version of the product to show the superintendents. My next steps were to transform our team’s research findings into documentation that would guide my design process.

### Capturing the provisional persona of Jack

In the weeks following the workshop, I met with the PM to refine what I had learned. We focused on the needs, problems, and activities of the superintendents. As we made progress, I wanted to capture all of the background research that the initial team had conducted as a deliverable to other stakeholders. I translated all of the gathered research about the superintendents’ behaviors, needs, goals, and problems into a provisional persona that we named “Jack.”

{{< webp image="/images/turner/turner-provisional-persona-jack.png" caption="A provisional persona of Jack, focusing on behaviors, goals and needs above all." >}}

I advocated for provisional personas in this project because I thought it would help the team stay focused on the user’s needs that we were presently designing for (Jack), amongst all the other users identified during discovery that we intended to design for next.

### Describing Jack’s journey

The next step in my process was to distill what we knew about Jack’s site assessments into a simple set of activities and supporting tasks. By describing the journey Jack would take to complete a site assessment with his current tools (walking around with pen and paper), I could start to design the user experience Jack would have as he completed those same steps on a computer screen.

Building from the provisional persona, the PM and I refined our conceptual model into an experience map that treated Jack’s activities as a series of phases with corresponding tasks. We then aligned these tasks to the features in our design that would support Jack as he completed the tasks.

{{< webp image="/images/turner/turner-experience-map-jack.png" caption="An experience map helped us visualize how Jack's goals and tasks connected to problems we could solve." >}}

I advocated for a journey map since it provided the design team a visualization for Jack’s experience as a flow of connected tasks over time, rather than a set of siloed activities that the use case model visualized.

In this case study, I will cover just two of Jack’s activities that the team focused their efforts on:

1. First, we would provide a way for Jack to review all of the uncompleted areas of the construction site being worked on each day.
2. Second, we would provide a way for Jack to see which tradespeople were working on a given area so that he could contact them and inquire about progress.

### Designing a digital prototype

After establishing an understanding of Jack’s needs and core tasks for our design team, I sketched designs for a digital prototype. I decided to create an interactive prototype for Jack because an interactive prototype is one of the best ways for a team to validate whether a design supports user needs.

The PM and I decided to limit the scope of this prototype to the first step of Jack’s activities (reviewing the site), which included the following supporting tasks:

1. Quickly identify the problem zones on a given floor of a building.
2. Determine which walls in the zone are affected by the problem identified.
3. See a photo of the wall(s) in question to verify the problem.

### Finding inspiration in Jack’s paper process

I used samples of Jack’s annotated floor plans as inspiration for my design. I could see that Jack marked-up paper floor plans by shading in areas, highlighting walls, and making annotations.

{{< webp image="/images/turner/turner-samples-super-jack.jpg" caption="Jack would annotate directly on paper floor plans of construction site to indicate progress and problems he discovered during site-walks." >}}

Jack assesses the progress of a construction site by looking at walls, zones, and floors. Tradespeople first work on walls, and walls make up a zone (e.g., a room). When all the walls of a zone are completed, the zone is completed. When all the zones are completed, the floor is completed, and so on throughout every floor in the building. Jack’s annotations over site plans reflect this order of construction.

{{< video src="turner-jack-annotate-zones-walls@540" autoplay="true" muted="true" loop="true" playsinline="true" caption="Marking a zone complete happens after all the walls are marked as complete.">}}

I assumed that if I designed a familiar view to Jack’s markup, we could create a familiar user experience in the app. For my early sketches, I focused on a single floor plan view with zones with different statuses or stages of work.

{{< webp image="/images/turner/turner-dig-protoV1-sketches-1.jpg" caption="Initial sketches of the floor plan view prototype where blue was used for in-progress, green for completed, and red for problems." >}}

{{< webp image="/images/turner/turner-dig-protoV1-sketches-2.jpg" caption="Refined sketches of the floor plan view prototype using the same blue, green, and red color scheme for progress and problems." >}}

### Creating a click-through prototype

After presenting several rounds of sketches to our team, I got a green light to continue refining with digital tools. I created low-fidelity wireframes in Sketch app and then imported my work into Framer Classic to create an interactive prototype.

{{< video src="turner-digital-prototype-animation@480" autoplay="true" muted="true" loop="true" playsinline="true" caption="An early interactive prototype in Framer Classic to view wall and zone progress, and view photos taken at problem zones.">}}

The next step would be to get this prototype in front of Jack to understand the following research questions:

- How well does this prototype help Jack identify which zone and walls need the most attention?
- Can the prototype show him what the problem is by using a photo?

### Restricted access to Jack: a complication

With a prototype and research plan, I was ready to start testing our design with Jack, and this is where we faced our biggest constraint. The only place where Jack could meet with us for user testing was at the construction site, and the only people on the team authorized to visit the site were the PM and product designer. This complication raised a concern: How would our team make progress in evaluating our design? The team members with authorized access had no experience with digital prototyping or user testing.

To set up the team for success, we would need another tool for the job. After discussing options, I recommended that we use paper prototyping. The following assumptions informed our decision:

- Jack was already using paper as a medium for his planning tasks, so the medium would be familiar and accessible if we used paper prototypes.
- The learning curve for paper prototyping and testing is much lower than for digital prototypes. Using paper, I could get our team up and running quickly, and team members with access could quickly iterate the tests and uses of our design ideas with Jack.

While this design method was not a favorite at first (going back to paper from digital seemed like going backward to our team), it proved to be quite helpful for making progress in our research and testing with Jack.

### Designing a paper prototype

To get started, I designed a paper prototype, submitted it to my team for critiques, and made updates based on team members’ feedback. The next iteration would include more ways to filter and sort zones and walls according to their status.

We also decided to add features to the design that would help Jack with the second step of his site assessment activities: contacting tradespeople to inquire about problems or delays in the zone where they were working. Accordingly, the supporting tasks expanded to include the following:

1. Quickly identify the problem zones on a given floor of a building.
2. Determine which walls in the zone are affected by the problem identified.
3. See a photo of the wall(s) in question to verify the problem.
4. See which tradespeople are working in the zone that contains the problem.
5. Provide contact information for those tradespeople and their subcontractor organizations.

I created a prototype on paper to demonstrate how to display pertinent information for Jack as he worked through these five tasks.

{{< webp image="/images/turner/turner-paper-proto-example.jpg" caption="I sketched out elements of the paper prototype to start." >}}

{{< video src="turner-process-paper-proto-hands-example" autoplay="true" muted="true" loop="true" playsinline="true" caption="After assembling the paper prototype, I demonstrated the method to the team. I re-created the demonstration in this video to show you roughly what it looked like in person.">}}

Eventually, the team members who had construction site access felt prepared to test the prototypes and do the iterations independently. They took their paper prototypes to the sites and conducted evaluative research sessions with several superintendents.

### Iterations added more features

As I checked in with team members on their progress, we started to see a pattern emerging from the design iterations that clarified Jack’s needs.

At first, the iterations I reviewed had expanded in the amount and types of information available for Jack. There were new ways to show contractor information, organization hierarchies, activity feeds, and photo streams.

{{< webp image="/images/turner/turner-paperProto-iteration-ex01.jpg" caption="As the team continued to test paper prototypes with Jack in the field, they started to add more and more features." >}}

Yet, when I reviewed notes with the team back at the office, it became clear that he did not need the additional filters, controls, or ways to manipulate the data. Instead, Jack wanted a simple visual display of information that would help him understand the status of specific walls in conjunction with the type of tradespeople working on them.

### Feature creep serving another user

The team had not seen the needs of another user creeping into our process: the project manager. For that user, a design with multiple levels of detail regarding activities and subcontractor company hierarchies helped them track performance and plan resources. Helping Jack meant putting project management features aside and focusing our iterations on the visual identification of the tradespeople working on each wall.

### Returning to Jack’s core needs

As I continued to meet with the team after their prototyping sessions with Jack, we identified two ways to identify tradespeople visually. The first way was an icon system, where each trade had a symbol that acted as a status indicator and filter. The walls would remain colored-coded based on their state of completion.

{{< webp image="/images/turner/turner-paperProto-iteration-ex02.png" caption="Subsequent prototypes tested different icon systems to indicate the tradespeople working at the wall and zone level of a site." >}}

{{< video src="turner-process-paper-proto-iteration-example" autoplay="true" muted="true" loop="true" playsinline="true" caption="A re-assembled demo of what the icon-based approach might have looked like while the team tested designs in the field.">}}

The second way was by adding color to the walls on a floor plan view according to the type of tradesperson working there. In this view, we would highlight only the completed walls in the tradesperson’s assigned color.

{{< webp image="/images/turner/turner-paperProto-color-walls-01.png" caption="Another iteration of the prototypes used a color-based system to indicate tradesperson type." >}}

This tradespeople-colored view became the favored approach with the design team after we made a connection to an in-field practice used by the tradespeople themselves: paint-striping.

### Incorporating paint-striping into the design

In the practice of paint-striping, each tradesperson uses spray paint with a unique color to mark walls and zones they complete. The design team decided that if we used the same coloring system in the prototype, it would provide Jack the most explicit connection between the prototype’s floor plan view and photos captured on site.

{{< webp image="/images/turner/turner-paperProto-color-walls-02.png" caption="The color-based system became the favored approach after the team made a connection to color-based markings used by tradespeople at the construction site, called paint-striping." >}}

After multiple iterations of the paint-stripe paper prototypes were tested, we were nearing our deadline for the executive presentation. The PM wanted more visual awe for the presentation so we decided that the best next step was to have the visual designer take on the assignment.

### Hand-off to the visual designer

The main problem to be solved was to show the status of a given subcontractor at a given stage without having the amount of information overwhelm the superintendent. The visual designer continued the team’s iterations and created several UI mockups for presentations to executive stakeholders. Note: I could not show all final assets for this case study due to NDA.

{{< webp image="/images/turner/turner-visual-designer-deliverable.png" caption="An early mock-up of the paint-stripe-inspired design that was eventually presented to executive stakeholders." >}}

## Outcomes and Lessons

### Project review and pending follow-up

We finished the project within time constraints and budget. The final deliverable was the PM’s presentation of our research, prototypes, and mockups to the executive team. The work completed on this desktop prototype was included, along with our work on a mobile prototype and a reporting dashboard for management users.

Overall, the results of our efforts were well received. Still, the executives decided to put the project into backlog as they decided whether to pursue further development in three directions:

1. Hiring more internal resources
2. Collaborate with an outside partner that would co-fund the investment
3. Or to try to persuade outside vendors to build these features into their existing products.

### The formation of Turner Labs

The findings from the project impressed Turner’s executive team with how much we accomplished in such a short time by using design-driven methods. As a result, our process was used as a model to form [Turner Labs](https://turnerlabs.org/), a new department that would seek out and support innovative projects throughout the company. I acted as a consultant to the PM to help launch the initiative and design content on the website.

{{< webp image="/images/turner/turner-outcomes-turnerLabs.jpg" caption="Screenshots of the Turner Labs website that launched after the innovation team was formed." >}}

### Lessons learned as a designer and researcher

One of the most important lessons I learned from this project is that in the future, I need to ensure that access to the primary user is available before kicking off a design or research effort. An equally important lesson was ensuring that the research question and the design iterations stay focused on the user’s most important tasks to prevent “feature bloat” from creeping in and taking over the project.

These valuable lessons will play a key role in guiding and focusing my work on future research and design projects.
