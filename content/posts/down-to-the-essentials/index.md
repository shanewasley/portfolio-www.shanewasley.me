---
title: "Down to the essentials"
date: 2018-09-18T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["project-brief","2018"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
comments: false
description: "Redesigning a feature in a SASS analytics app to simplify construction site inspection."
canonicalURL: "https://www.shanewasley.me/posts/down-to-the-essentials"
disableHLJS: true # to disable highlightjs
disableShare: true
hideSummary: true
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: true

---

## Highlights
|                      |                                                              |
|----------------------|--------------------------------------------------------------|
| **Format**          | Project Brief                                                    |
| **Company**          | SKUR Inc.                                                    |
| **Product**          | Web app, SAAS analytics                                      |
| **Users**            | Engineers and operations managers working at large-scale engineering, fabrication, and construction companies |
| **Role**             | UI/UX Designer                                               |
| **Team**             | Three developers, product manager, customer success manager  |
| **Timeline**         | Two months, while working on parallel projects               |
| **Skills & Methods** | Sketching, wireframing, user flows, prototyping, user interviews, user testing, design system |
| **Tools**            | Sketch, Zeppelin, Framer Studio, Screenflow, Sketchfab, JIRA, Github |
| **Deliverables**     | User research artifacts, sketches, prototypes, UI specifications |

## Overview
SKUR Inc. created a web app for variance analysis of construction sites. By showing how high-definition laser surveys of buildings differed from a 3D CAD model, SKUR’s app helped customers identify problems that could increase project delays and costs if they went unaddressed. For more about SKUR’s technology, primary users, and the team I worked with, [see the related case study](/posts/lets-get-aligned/).

{{< webp image="/images/skur-vv/overview-variance-map.png" caption="Comparing a CAD model to an HDS laser survey (aka a point cloud) can identify the differences between a design and the built structure. SKUR’s Variance Map classified differences with a red, yellow, and green color system (most to least, respectively)." >}}

The SKUR team suspected they could deliver better value with the product after seeing lower than expected engagement with the features they built for variance analysis. As the UI/UX designer working with a five-person team, my task was to redesign the variance interface based on the customer needs we could uncover with research over two months.

The redesign process hinged on revisiting our assumptions about what users needed to do and see in the app. We assumed that customers would require an extensive view of data while performing a large portion of their workflow in SKUR’s app. We learned from user research that the customer needed to use our app to see a limited set of high-priority data to complete the rest of their job outside of our app— with tools they were already using to get the job done. Improving the user experience meant shifting the app's defaults from a state of “do everything, show everything” to “show only what’s needed to do the most important thing.”

| **Defaults before**                         | **Defaults after**                       |
|---------------------------------------------|------------------------------------------|
| Support 4 tasks                             | Support 1 task                           |
| Display all variances                       | Display only high priority variances     |
| 12 column, 1000+ row table of variance data | Variance data displayed object-by-object |

Through iterative prototyping, we stripped down the interface to the critical views and controls that would help our customers precisely get what they needed from the app to perform their jobs. By offering less, we provided more, and we transformed the experience of the variance interface to be more efficient and on-task for our customers.

{{< webp image="/images/skur-vv/overview-before-after-UI.png" caption="When I started, SKUR’s Variance Viewer had a busy interface (left). All of the viewing layers were on by default, and a user would sift through a data table to navigate building objects for inspection. The final prototype I delivered (right), was a redesigned interface that prioritized object-by-object inspection of the critical variance problems at the site."  >}}

## Key contributions
My most valuable contributions were conducting user research, training team members to perform user research when I was unavailable, creating product prototypes to test with customers, and delivering design specifications to the development team.

## Design process
### Where we started
When I started on the project, the variance analysis feature of SKUR’s app offered extensive information to customers by default. When a customer sought an answer to the question, “What parts of the construction site vary from the CAD design we started with?”, SKUR’s app answered like a peacock showing all of its feathers. A user would see a viewing screen full of brightly colored objects, fine grain dot fields, a table with thousands of rows, and a 30-plus page PDF report slicing up data in every possible combination.

{{< webp image="/images/skur-vv/starting-viewer-and-report.png" caption="By default, SKUR’s app would provide many data for users to parse through during variance analysis. A central assumption was that we discouraged engagement by delivering so much data to users with the app's default behavior."  >}}

It was clear to me that the amount of data we were presenting to users was overwhelming. We needed to simplify the interface to improve the experience and increase engagement. We did not develop most of the features present at the start of this project from SKUR’s users' researched needs, so we did not know what to prioritize or simplify.

{{< video src="where-we-started-app@450-10" autoplay="true" muted="true" loop="true" playsinline="true" caption="A screen recording from a user test with a first-time user of SKUR’s app. The user noted that they were confused about where to start and that scrolling through such a large table to get information was a tedious experience." >}}

### Revisiting assumptions about our customer’s tools
Early in the project, I had the opportunity to interview several of SKUR’s customers about their workflow. My goal was to understand how they used SKUR’s app, whom they were working with, and what other tools they used to get their job done.

I went into the customer interviews assuming that SKUR’s app was the one tool that supported the customer’s task flow from end to end. Our product team had designed the experience to help our primary user, Carson, complete the critical tasks of identifying variance problems at the construction site and initiating a resolution to those problems with his team (for more on Carson, [see the related case study](/posts/lets-get-aligned/#carson-vdc-engineer)). Accordingly, we included all of the data in SKUR’s Variance Report and Variance Viewer to support Carson in this way.

{{< webp image="/images/skur-vv/task-flow-tools-before.png" caption="We designed SKUR’s Variance Report and Variance Viewer to support our users’ task flow from end to end. At every step, whether it was reviewing the site or delegating actions to the team, we assumed our user would complete their work all within the app."  >}}

However, as Carson walked me through his process at his desk, I learned that he only needed SKUR’s app for *one* of the many tasks he undertook to get his job done. Rather than reviewing the report, he jumped right into inspecting the highest variances in the Viewer (objects we colored red). After that, he left SKUR’s app to complete his workflow using other tools: Autodesk applications to confirm his variance assessment and email or calendar apps to take the next steps with his team.

{{< webp image="/images/skur-vv/task-flow-tools-after.png" caption="After watching our users complete their work in the office, we learned that they did not use our app for as many tasks as we assumed. Instead, they only need SKUR’s app for one of their tasks: inspecting the highest variances that our app detected. They continued to use the same tools they already used with their team for the rest of their tasks."  >}}

Each interview with our primary user showed a similar pattern of tool use. The bottom line was that Carson only needed the Variance Viewer in SKUR’s app for the one crucial task that none of his other tools could do: inspecting the highest variance objects at his construction site.

### Prioritizing inspection of high variances
SKUR’s Variance Viewer was displaying data and input controls to support multiple tasks. Yet from user interviews, we learned that supporting one task— inspection— would deliver the most value for our customers. We knew we needed to transition from a high-level summary of the whole construction site to a detailed view of each high variance object within the structure. What we did not know was what specific data and controls we should display along with each object.

To answer this question, I created mockups using Sketch app to review with our customers. These mockups were zoomed-in snapshots of construction objects, with all of the data we collected about the objects displayed upfront. I then used the mockups for additional remote user walkthroughs.

{{< webp image="/images/skur-vv/inspection-mockups-details.png" caption="Samples from the object inspection mockups we reviewed with customers. Before prototyping, I wanted to understand what our users needed to see and what they didn’t."  >}}

From these walkthroughs, I learned that our users only needed a few data points from the entire buffet:
1. the variance values of the object
2. a confidence value (% of the object scanned)
3. the object identifiers (Category and ID)

The variance and confidence values helped our users establish whether the object should be flagged for follow-up with their team. The object identifiers allowed our users to reference the part numbers of the objects in the external tools they used with their team (Autocad, Navisworks, Revit). Aside from these data, all of the other data points in the mockups were nice but unnecessary.

Our research revealed what we should prioritize for the Variance Viewer redesign. We mapped what should stay prominent in the UI and what to shelf into secondary elements. My next step was to create a prototype from our findings to test with our users.

{{< webp image="/images/skur-vv/user-priorities-in-variance-viewer.png" caption="After reviewing object inspection mockups with customers, we identified elements of the current design to prioritize visually and which elements to deprioritize. My goal was to redesign a more effective display of the high-priority filters and data while minimizing the lower priority elements."  >}}

### Prototype part 1: variance filters
For the rest of the project, I iterated on prototypes while checking in with my PM along the way. The first feature I redesigned was the list of variance filters. Filters let our users see their variance map in 10 different levels of detail. From our research, I knew that we were offering too many options for filtering— we could cut the number of filters in half to 5 and provide everything our users needed.

I sketched out ideas for a redesigned filter element that treated the point cloud as a single global toggle and reduced the amount of text in the component by using colors for categories. Then I created a digital mockup using Sketch app and the Bootstrap design components we used on the team.

{{< webp image="/images/skur-vv/sketches-variance-filters.jpg" caption="Before creating a digital mockup, I sketched options for the filter list to show what was needed based on our research."  >}}

#### Setting new defaults
We also learned from our interviews th at the filters we made active by default were unnecessary for our users. When the Viewer loaded, everything was flipped on, and this wasn’t helping our user complete their inspection task. For example, keeping the point cloud on by default would fill the Viewer with a field of dots that could obscure the view of high variance objects.

{{< video src="toggle-point-cloud@384-10" autoplay="true" muted="true" loop="true" playsinline="true" caption="When the point cloud is toggled on in the Variance Viewer, it can create considerable visual noise during object inspection. In the example above, because the point cloud contains all of the furniture and equipment from an office, the structural objects are obscured until you toggle the point cloud off." >}}

Moreover, showing all objects at all measured variance levels (colored red, yellow, and green) created more visual noise for our users when they only needed to inspect the highest variance objects (red).

{{< webp image="/images/skur-vv/defaults-rgy-to-red-only.png" caption="How a structure looks as you start to filter out low (green) and medium (yellow) variance objects. Keeping only the high variance objects (red) toggled on by default meant that the essential visual data our users sought stood out clearly."  >}}

{{< blockquote author="— a SKUR customer" >}}
  "Just show me the red."
{{< /blockquote >}}

To improve the user experience, we needed to help Carson complete his inspection as efficiently as possible. As one customer said in an interview, “Just show me the red.” Accordingly, I redesigned the filter element to cut down the filter choices and keep only one filter on by default.

{{< webp image="/images/skur-vv/variance-filter-iterations-defaults.png" caption="Where we started (left), the redesign with toggles at their previous defaults (middle), and the redesign toggled to new defaults (right). By adjusting the defaults to show only the red, high variance objects, we could simplify the inspection process for our users."  >}}

### Prototype part 2: variance details
The next feature I designed for the prototype was the detailed data we would display for each object our user was inspecting. We offered a massive table to sort through even though our research showed us that our users only needed to see three data points as they viewed each object one by one (variance values, confidence, and object identifiers).

I interpreted the UI design task as two constituent pieces: (1) making the data visible and clear and (2) providing an obvious affordance for moving from one object to the next (the CTA). Rather than a table, a card element that let the user page through each object came to mind as the best way to show this data. I started my redesign process by sketching out different options for card-style data displays.

As I moved from sketches into digital mockups, I created a card element that transcribed the table data onto a card as a list, almost like an array dump of key-value pairs. Yet when I squint-tested the design, I realized that nothing in the data stood out.

{{< webp image="/images/skur-vv/sketches-variance-detail-v1.jpg" caption="Samples of sketches and an initial mockup of the variance detail card."  >}}

From our research, I knew that most of our user's work during inspection would occur outside SKUR’s app, using external tools. Our user needed to reference the object ID from SKUR’s app to find the same object in their external tool to get this work done. Accordingly, the ID of the object needed to stand out the most. Yet if my design was like a “Hello my name is” sticker, I was writing my name way too small.

{{< webp image="/images/skur-vv/hello-my-name-too-small.png" caption="Wait, isn't seeing my name the whole point of this card? I was doing something similar with my design."  >}}

Instead of what I had, I needed the design to support our users by visually prioritizing the object’s identifying information above the other data. I sketched out options that made the identifiers big and obvious.

{{< webp image="/images/skur-vv/sketches-variance-detail-v2.jpg" caption="Samples of sketches of the variance detail card. I tried to make the object identifier more prominent."  >}}

After sketching options, I started iterating on digital designs using Sketch app. With each iteration, I tried to make the object identifier stand out further from the other data.

{{< webp image="/images/skur-vv/variance-detail-card-progression.png" caption="Digital iterations of the variance detail card. With each change, I was aiming for a visual hierarchy that I assumed matched the needs of our users."  >}}

I also color-coded each card to each object's variance threshold to provide consistency across the UI. The user would see the same red-yellow-green scale in the viewing filters, the objects in view, and the data detail of that object.

{{< webp image="/images/skur-vv/variance-detail-parts-compare.png" caption="To create visual consistency across the Variance Viewer UI, I matched colors between the filter list, the object under inspection, and the object variance card."  >}}

To help visualize how everything from the redesign came together, I created a click-through prototype showing the filters, variance detail, and a minimized variance list. I used Framer Studio to overlay the UI onto screenshots of models from Navisworks.

{{< video src="proto-v1-colors@576-12" autoplay="true" muted="true" loop="true" playsinline="true" caption="A click-through prototype showing the redesigned interface with all variance filters toggled on (our previous colorful default)." >}}

{{< video src="proto-v1-red@576-12" autoplay="true" muted="true" loop="true" playsinline="true" caption="A click-through prototype showing the redesigned interface with only the highest variance objects (red) toggled on (the new default)." >}}

{{< blockquote author="— a SKUR customer" >}}
  “I’m only seeing red, and I like it.”
{{< /blockquote >}}


I had the opportunity to perform a user walkthrough of the prototype with two of our customers. They both expressed how much simpler and quicker the process of inspection appeared to be then before. One customer noted they were so busy that they only had a few minutes to review the variance analysis, noting, “I’m only seeing red, and I like it.”

### Iterations on the prototype
While the prototype I designed seemed to check all the boxes from our users' *expressed* needs during interviews, I wanted to take the redesign further. After reviewing screen recordings that I captured during previous sessions with customers, I noticed three opportunities to improve the visual experience for our users:
1. changing our Viewer’s background-color
2. introducing transparency into the object rendering
3. Using motion to orient users in space while inspecting object variance

#### Dark background
Our recordings showed that our primary users exclusively used dark backgrounds in their external CAD tools. Every CAD modeling and point cloud tool I could demo had dark backgrounds as defaults, except for SKUR’s app and Sketchup. Should we make the change to a darker view?

After comparing the red-green-yellow-grey palette that SKUR’s app used to render objects against light and dark backgrounds, dark backgrounds provided greater contrast. I assumed that greater contrast would improve the user experience, so I switched to a dark background in the next iteration of the prototype.

{{< webp image="/images/skur-vv/dark-vs-light-background.jpg" caption="Variance Maps cast against a dark background provided better contrast than a light background."  >}}

#### Utilizing transparency
From the same on-site recordings, I noted that customers would use their external tools (Autocad, Navisworks) for detailed inspection because they could hide/show objects in the building model. Since their external tools allowed model editing, when customers wanted to inspect an object visually obstructed by surrounding objects, they could hide the surrounding objects. Accordingly, if we could hide objects in SKUR’s app, we could improve the inspection experience for our users.

However, model editing was a feature far outside the scope of SKUR’s app. Instead, I assumed we could improve the inspection experience in SKUR’s app by introducing transparency. Rather than hide objects that obstructed a user’s view, we could let the user see through them.

{{< webp image="/images/skur-vv/transparency-vs-opaque.jpg" caption="If one of our uses wanted to inspect the wall-facing side of a high-variance pipe, they would be out of luck with an opaque 3D model— they would only see a gray wall (left). Introducing transparency could let our users see through obstructions and view high variance objects from all sides (right)."  >}}

#### Motion for orientation
The last enhancement I made to the prototype was motion between objects. So far, I had designed an inspection experience that took a user from object to object, like a slide deck. If this experience were happening in the real world, it would be like teleporting a user through the space of their construction site instantly.

However, when our users visited their sites to complete an inspection, they walked instead of teleporting. As they walked through the floors and rooms, they established a sense of orientation and relationship of the objects that a carousel of images on a screen couldn’t capture. To help align SKUR’s experience to our customer’s reality, I thought, why not let them move through the site inside our app?

I needed a 3D animation app to help me prototype this next idea. By good luck, I discovered the app Sketchfab which saved me from the hell of 3DS Max. Sketchfab offered (1) a straightforward process to create motion between annotated objects in a 3D model and (2) an API to embed models inside the Framer design app. With this method, I created multiple annotated examples to use within my prototype.

{{< video src="motion-demo-sketchfab@360-12" autoplay="true" muted="true" loop="true" playsinline="true" caption="A building model uploaded to Sketchfab. The Sketchfab platform makes it very easy to create annotated tours of construction models that simulate traveling through the site." >}}

### Final deliverable
For the final deliverable to the team, I brought everything together for a click-through prototype in Framer Studio: the redesigned filter element, the variance detail card, a minimized variance list, dark background, transparency, and motion.

{{< video src="proto-v2-handoff@576-10" autoplay="true" muted="true" loop="true" playsinline="true" caption="A handoff prototype that demonstrated all the features I assumed would improve the inspection experience for our customers." >}}

I also provided static mockups to demonstrate state changes for the filter list and the variance detail card— depending on what variance threshold users were examining their site with.

{{< webp image="/images/skur-vv/static-screens-handoff.png" caption="Screen mockups to demonstrate object inspection at different variance thresholds. In SKUR’s app, a mesh is overlaid on the selected object."  >}}

## Outcomes and Lessons
### Received well, not user-tested, released in pieces
The prototype was a success for the team. The PM and developers pointed out that the redesign provided a cleaner, clearer experience using the Variance Viewer. The CEO noted that the prototype was an exciting change to the visual presentation of the app, and he looked forward to showing the redesigned app to new customers and investors.

When we would be able to release the redesign was unclear, however. Many other projects were already scheduled months out, and the prototype would require most of the resources on the product team to build and ship it. For this reason, I did not perform any user walk-throughs or tests with customers because the team was concerned that we would set expectations too high for functionality they didn’t know when they could deliver.

Instead of releasing it as a complete redesign, the team shipped in pieces— part of the design was developed for the following release cycles while the rest was backlogged for a later, undefined date. I would eventually leave SKUR for other opportunities before I saw many of the design features get implemented.

{{< video src="outcomes-dev-partial-release" autoplay="true" muted="true" loop="true" playsinline="true" caption="A pre-release version showing some of the updates from the redesign— filters and viewing defaults." >}}

I was attached to my work, and it wasn't very reassuring to hear that it may not ship fully for a long time. I learned that my mistake was not bringing the developers along as I iterated on the prototype. I had buy-in from the PM and the CEO, but they weren’t the ones who needed to build the product. Since I did not stop to check about the technical feasibility of my design or how crowded the release schedule was, I inadvertently siloed my process and shot too far out into “what could be” rather than “what can be.”

### Failure to persuade team toward feature specialization
Aside from the mockups and prototypes, a major outcome of the design effort was the key learning from user research. From the interviews and walkthroughs, it was apparent that we did one thing really well: variance inspection. No other tool did this job well, and we could do an even better job for our customers if we focused on this feature.

While inspection was a critical capability, the team was committed to a grander vision of creating a comprehensive collaboration tool beyond just inspection. The release schedule was packed with new features like file versioning, project management, and in-app messaging. I was concerned that diversifying the feature set would place the app in competition with all of the tools that our customers already used for collaboration, rather than differentiating with a feature that had no substitute. Despite the research findings and my attempts at persuasion, I failed to get the product team on board with the idea of a single feature specialization.

### Individuated versus relational personas
Before the project started, our persona model depicted the primary user, Carson, working alone with SKUR’s tools to complete his job. Yet our research revealed that Carson was working with his team using multiple tools, including SKUR’s app. We had centered our research artifacts— namely our personas and experience maps— around an individual rather than the individual's relationships with his peers.

When we zoomed out and looked at the ecosystem of Carson’s relationships— VDC engineers, BIM specialists, architects, and superintendents— we could see how many tools other than SKUR’s app were used to complete the job successfully. Moving from an individual to a relational view revealed how many of the features we had included in the Variance Viewer were redundant for Carson. Hence, the redesign described in this brief was an exercise in reducing or minimizing previously developed features to improve the user experience.

The lesson for me as a designer was that individual-focused personas create blind spots. Developing a product centered around one person, performing one workflow, using one tool, could lead a team to make many features that already had solutions. In the future, I assumed that user research artifacts, including persona models, that I developed with a product team would need to consider a user’s relationships just as much as their individual needs and goals.

### Research as a bridge for customer rapport
One of the positive and enduring outcomes from the research efforts on this project was the customer rapport we built. The time and availability we provided customers and the in-depth research we conducted went far beyond customer expectations. For some customers, it was the first time that anyone from any software company had come to them to learn about the tools they used for their job. The rapport we established with this hands-on approach set the groundwork for a deeper view of our customer needs and gave us the potential to build a product that could help them excel at their jobs.

