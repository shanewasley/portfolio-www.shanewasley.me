---
title: "Let's get aligned"
date: 2018-09-16T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["case-study","2018"]
author:
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
comments: false
description: "Designing a new feature in a SAAS analytics app that aligned site surveys with CAD models."
canonicalURL: "/posts/lets-get-aligned"
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
| **Format**          | Case Study                                                    |
| **Company**          | SKUR Inc.                                      |
| **Product**          | Web app, SAAS analytics                                            |
| **Users**            | Engineers and operations managers working at large-scale engineering, fabrication, and construction companies                        |
| **Role**             | UI/UX Designer                                                  |
| **Team**             | Three developers, product manager, customer success manager                     |
| **Timeline**         | Two months, while working on parallel projects              |
| **Skills & Methods** | Sketching, wireframing, user flows, prototyping, user interviews, user testing, design system |
| **Tools**            | Sketch, Framer Classic, Invision, Zeppelin, Screenflow, HTML/CSS, JIRA, Github                     |
| **Deliverables**     | User research artifacts, sketches, prototypes, UI specifications |


## Introduction

SKUR Inc. created a SAAS analytics app for variance analysis of construction sites. By showing how laser surface scans of buildings differed from their 3D design specifications, SKUR’s app helped customers identify problems that could increase project delays and costs if they went unaddressed. As SKUR's UI/UX designer, I helped design new product features and improve the user experience for customers. This case study will highlight the team effort to transform a service into a new product feature that would save customers time.

## Background

SKUR created a software solution at the intersection of two other technologies: 3D modeling (CAD) and high definition laser surveying (HDS). SKUR’s customers used the design models from CAD software to plan and construct their buildings. As they built the structure from the CAD plan, SKUR’s customers would use HDS technology to survey the site and create a snapshot of the current state. This snapshot, also known as a “reality capture,” was a 3D rendering of the site made up of millions of points, called a point cloud.

{{< webp image="/images/skur-aa/background-CAD-vs-pointCloud.jpg" caption="On the left, a CAD model of piping in a trench. On the right, a laser-based, high-definition survey (HDS) of the same trench during construction. Millions of points create the HDS image, called a point cloud." >}}

By comparing the CAD model to the point cloud, SKUR’s app created a visual map of variance between the planned structure and the structure in reality. With this map in hand, SKUR’s customers had an accurate, objective tool to investigate construction site discrepancies and take action.

{{< webp image="/images/skur-aa/background-varianceMap-process.jpg" caption="Comparing a CAD model to a point cloud can identify the differences between design and built structure. With SKUR’s Variance Map, the differences are classified with a red, yellow, and green color system (most to least, respectively)." >}}

Even minor variances identified by SKUR’s app can reveal costly implications for a construction site. A chemical pipe installed one inch higher than planned could be misaligned to the pipe it will connect to later in the project. Adjusting for such a discrepancy quickly— such as ordering new parts before crews arrive to continue construction— can prevent increases in costs and delays on a project. The Variance Map was meant to identify these problems sooner before they became much more expensive repairs later.

{{< webp image="/images/skur-aa/background-variance-misalign.jpg" caption="The utility of the Variance Map comes from what it can predict. A pipe installed outside of design tolerances may be a problem for the pipe it should connect to at a later stage of the project." >}}

### Faster and easier than competitors

SKUR’s competitors’ problem was that displaying an accurate variance between a CAD model and a point cloud required a tedious series of steps and hacks using specialized software on high-end desktop computers. It was a job you could hand to someone like McGuyver, but it was too much to add to the existing workday for everyone else.

SKUR developed a web-based application that simplified or automated the steps to produce a Variance Map to address this issue. Furthermore, the Variance Map could be accessed on any laptop or mobile device. The value SKUR provided was time and simplicity: they could produce a Variance Map quicker than competing tools without the need for specialized hardware, training, or McGuyvers.

## Problem

The product team was performing a concierge service behind the scene: the precision alignment of customer’s 3D CAD models and HDS point clouds. This alignment step was critical for producing an accurate Variance Map. Yet having a team member aligning files for each customer was too time-consuming to scale.

Our goal was to remove the alignment-as-a-service bottleneck by making it a feature that customers could use on their own schedule. Once the product team developed the technology to perform alignment within the app— which we called “Assisted Alignment”— my role was to design the interface that customers would use. If we were successful in our design, the new feature would let customers obtain Variance Maps quicker and free up time on our team to support other customer needs.

## Users

Before joining the team, SKUR had created several provisional personas of VDC and BIM engineers working at large-scale construction companies. We named the primary user Carson. I limited the scope of this case study only to cover Carson.

### Carson, VDC Engineer

Carson, a virtual design and construction (VDC) engineer, worked for a construction company that built enormous structures— like skyscrapers, hospitals, and sports stadiums. Carson had a background in construction planning, visualization, modeling and HDS reality capture. He worked with a team of site surveyors, architects, superintendents, and project managers assigned to a specific construction site. Carson and his team used the Autodesk suite of applications— primarily Revit, Navisworks, and Autocad— to get their day-to-day work done.

Every site Carson was assigned to experienced inaccuracies. As the holder of all the building model information, Carson could assess whether those inaccuracies were within tolerances as acceptable mistakes or urgent problems to fix.

The most significant pain point in his role was obtaining timely and accurate data about the site that he could compare to his models. None of his current tools could show what area of an HDS corresponded to the parts in his model at the level of precision he needed. The lack of precision in his inputs meant extra work for Carson to confirm site accuracy and extra risk to the project the longer it took to identify errors. If SKUR’s app could increase Carson’s efficiency in assessing site-to-model variance, we would help him save time, reduce risk, and excel at his job.

## Roles and Responsibilities

I worked locally at SKUR’s offices in Oakland, CA, with a team of five others:

- A front-end developer
- Two back-end developers
- A customer success manager
- A product manager

As the UI/UX Designer, I took the lead on creating and maintaining user research artifacts, user flows, wireframes, and interactive prototypes. I worked with the customer success manager to perform on-site user research, such as interviews, walkthroughs, and usability tests. I created customer use cases and transformed product requirements into design specifications with the product manager. Handoff of mockups and prototypes was done in collaboration with the development team.

## Scope and Constraints

### Scope

The work in this case study took place over two months during a period when the team was busy with many other feature updates and fixes in parallel. I decided to stitch together all the related sprints as one narrative about releasing a new feature for this case study.

### Constraints

The most significant limitation for this work was direct, in-person access to users to test the prototypes. We had many complex interactions to design for, but the Carson users were rarely able to meet in person to test prototypes. Limited testing meant we had to make more assumptions for each release and probably created more work for ourselves by fixing incorrect assumptions in subsequent updates.

Another limitation was time. We were working on multiple product areas for each release, and the Assisted Alignment feature we were building was just one of many JIRA issues on our respective plates.

The other major constraint was limited technology to design prototypes in 3D. During my time with SKUR, I designed interface elements meant to change the orientation, position, rotation, and surface appearance of 3D objects in the product. Yet, none of the UI design applications available to me could interact with 3D CAD files or point clouds. Therefore prototyping took some extra effort and collaboration with the developers to be useful.

## Design Process

### Understanding Alignment

To see how much taller your tallest books are from the rest of your books, you could put them all on a bookshelf and compare them. With the books upright and aligned along their bottom edge, you could see precisely how far your tallest books stood out. Alignment reveals the variance.

{{< webp image="/images/skur-aa/process-variance-books.jpg" caption="Aligning objects along a standard reference helps identify how they vary in dimensions. Picture by Annie Spratt @ Unsplash">}}

For SKUR’s customers, alignment was a necessary step before reviewing variance. In their case, alignment took place in three dimensions: the corners, edges, and surfaces of a CAD model had to line up with an HDS capture of a built structure. In the industry, this lining-up process is called registration, aka alignment.

When Carson used SKUR’s app, he would encounter the new alignment feature we were building as an intermediate step of the user flow: after he uploaded his model and point cloud files, and before the app provided him a variance map.

{{< webp image="/images/skur-aa/process-alignment-within-overall-flow.png" caption="This case study covers a new feature, Assisted Alignment, which is in the middle of the user flow for SKUR's app.">}}

### Scope and requirements

To kick this project off, I met with the PM and developers to understand the scope and requirements of the new feature called “Assisted Alignment.” My goal was to understand what we needed to build and gather enough information to create a working prototype as soon as possible.

After reviewing various alignment methods, we determined that matching surfaces on the CAD model to surfaces on the point cloud would be the easiest method. We assumed that other approaches, such as point-matching, would be more difficult for Carson to perform and lead to more user error.

We needed Carson to match three non-coplanar pairs between the model and point cloud for alignment to succeed. In other words, we needed the user to pick a surface on the X, Y, and Z-axis planes of the model and pick the corresponding surfaces on the X, Y, and Z-axis of the point cloud.

{{< webp image="/images/skur-aa/process-coplanar.png" caption="Surfaces in 3D space that share the same plane are coplanar. Surfaces that do not share the same plane are non-coplanar. SKUR’s Assisted Alignment required three pairs of non-coplanar planes to align two objects." >}}

#### Tasks

We determined that the initial prototype needed to let Carson accomplish the following tasks, at a minimum:

1. Picking three surfaces on the model
2. Picking three surfaces on the scan
3. Undoing a pick on either the model or scan, if the user made an incorrect pick
4. Executing the alignment, once all surfaces were picked

#### Views and controls

To accomplish these tasks, the prototype needed to show Carson, at a minimum:

1. Views of:
   - the model and scan, side by side, with all surfaces visible
   - feedback showing the user when a surface was picked
   - the model and scan aligned with each other
2. Controls for:
   - rotating, panning, and zooming to identify surfaces
   - undoing an incorrect surface pick
   - executing the alignment

### Designing a prototype

I began my design process by focusing on the surface picking feature before moving to the broader user flow, navigation, and supporting screens. I started by sketching ways that the system could provide visual feedback after a surface pick. The three methods I compared were (a) coloring the surface, (b) labeling the surface with a number, or (c) both.

{{< webp image="/images/skur-aa/process-protoV1-sketch-color-boxes.jpg" caption="I sketched various combinations of colors and numbers as a system for showing surface picks." >}}

Using simple blocks as examples, both numbering and coloring (c) provided the most feedback. The colors showed which surfaces were picked, and numbers indicated the sequence— a proxy for showing progress. However, when I compared both methods with real-world examples, the numbering method (b) would sometimes block my view of a surface on the model I wanted to pick. An occluded surface might be frustrating for a user trying to access it. Moreover, after checking with the developers, I learned that rendering a floating label would take longer to code than changing the color of surfaces. Considering all these factors, going with colored surfaces only (a), was the best choice.

I assumed it was best to choose three colors for this new AA feature— corresponding to the three pairs of surfaces to align. But which colors? In the construction industry, colors are used ubiquitously and for high-stakes tasks (e.g., work instructions, machinery controls, electrical wiring). Hence systems with high-contrast and color-blind-friendly combinations are used to help people avoid mistakes and accidents.

Keeping our customer’s context in mind, my criteria for choosing the three colors for the new AA feature were:

1. Not reusing Variance Map colors (red, yellow, green)
2. Color-blind-friendly
3. High contrast with:
   - colors in the UI navigation and controls
   - the greyscale rendering of models and point clouds
   - the light background of the viewing screen

{{< webp image="/images/skur-aa/process-protoV1-color-tiles.png" caption="I narrowed the color choices for the new feature by laying out the colors already used in SKUR’s app." >}}

While researching color combinations, I came across [Colorbrewer](https://colorbrewer2.org), a tool that provides color-blind-friendly color schemes for data sets. To help constrain my choices, I viewed the output of Colorbrewer while using [Color Oracle](http://colororacle.org)— a tool that lets you wear colorblind glasses. Lastly, I ranked choices based on their [WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/) contrast rating. I narrowed down the options to two sets and then picked the set that seemed like the best compromise: green, orange, and purple.

{{< webp image="/images/skur-aa/process-color-blind.jpg" caption="Color-blind-friendly design tools also helped narrow the new feature’s color palette." >}}

Then I created a click-through prototype to show two paths that Carson could take using the feature:

1. the default or “happy path” picking surfaces and executing alignment,
2. an error path for undoing an incorrect pick.

{{< webp image="/images/skur-aa/process-user-flow.png" caption="Visualizing the user flow for the task of Assisted Alignment— a loop of plane-picking." >}}

I started with sketching to visualize the simplest way to demonstrate the plane-picking interaction and undoing the action.

{{< webp image="/images/skur-aa/process-protoV1-sketch-screens.jpg" caption="Sketching the process of plane picking, screen-by screen, helped me create a digital prototype to review with the team." >}}

Using the app SketchUp, I created simple 3D examples to represent a CAD model of a house and an in-progress HDS capture of the house.

{{< webp image="/images/skur-aa/process-sketchup-models.png" caption="I chose a simple house model for the prototype because it could show the consequences of choosing incorrect surface pairs more clearly than cubes." >}}

Then I imported the vector drawings into wireframes I made in Sketch, and then inserted the frames into a click-through prototype in Invision.

{{< video src="process-protoV1-animation" autoplay="true" muted="true" loop="true" playsinline="true" caption="An early prototype showing a successful plane-picking and alignment task.">}}

I repeated my process for the undo path, using different frames and created a second click-through prototype for the team.

{{< video src="process-protoV1-animation-undo@540" autoplay="true" muted="true" loop="true" playsinline="true" caption="Alignment will fail if a user picks non-matching pairs of planes. This prototype demostrates how a mismatch can happen and how it can be undone.">}}

After reviewing the prototype with the team, we agreed on the assumption that the system needed to provide more visual feedback on Carson’s progress to help him succeed with the task. We then considered what else the customer would need based on real-world use cases with much larger models. After the discussion concluded, we reached an agreement on new elements to add to the design that would further help Carson complete the alignment task:

1. A progress indicator for surface picks
2. Instructions displayed at each step and or an option for help
3. Controls for standard isometric views (top, down, left, right, front, back)

### Adding features to the design

I started my process by sketching various UI patterns I was familiar with for progress indicators, viewing angles, and help screens. I also looked through common UI pattern examples on the internet for inspiration. Since the team was using Bootstrap v3 for their app, when it came to choosing options, I also considered what could be reused from existing components.

I started with progress indicators and viewing angles. Then I sketched options for help patterns. Finally, I wrapped up by sketching options for layouts within the constraints of the viewing window of the SKUR app.

{{< webp image="/images/skur-aa/process-protoV1-sketches-progress-view.jpg" caption="Sketches of various UI patterns for task progress and isometric viewing angles." >}}

{{< webp image="/images/skur-aa/process-protoV1-sketches-help.jpg" caption="Sketches of various UI patterns help features." >}}

{{< webp image="/images/skur-aa/process-protoV1-sketches-controls.jpg" caption="Sketches of layouts for the controls in our next iteration." >}}

After comparing options, I decided on a collapsable sidebar containing the view controls, progress, and CTA (“align”) that I could assemble from Bootstrap components. Considering the limited window we had for our release cycle, I decided on the bare minimum for a help pattern: a dismissible notification describing steps and a link to an off-page support Wiki. The customer success team was already managing a help Wiki, so I assumed this would be a consistent (albeit not ideal) choice for Carson to get us over the finish line for our first release.

Next, I created a basic wireframe of the features and layout to share during a review meeting with the PM. Then, with the go-ahead on my design, I moved to a higher-fidelity design process to prepare for handoff to the developers.

{{< webp image="/images/skur-aa/process-protoV1-wf.png" caption="This wireframe was meant to show just enough of the layout to understand where the requested features could be found in the UI." >}}

### Digital designs and handoff

Using Sketch and components from the Bootstrap v3 design system I assembled for SKUR, I produced mockups and handed off my work to the developers. These mockups contained each screen at every step of the user flow, with all the corresponding component states. In order to make the process quick and consistent with the rest of the SKUR app, I used default settings for colors and components.

{{< webp image="/images/skur-aa/process-protoV1-handoff.png" caption="An example screen from the design I handed off to developers for testing." >}}

### Designing the input forms

While the developers built the new feature, I met again with the PM to understand product requirements for the input forms that Carson would interact with before starting the surface-picking task. In addition to offering our new feature (Assisted Alignment), we would offer an option to use a numerical shortcut called an XYZ transform. We also wanted to allow Carson an undo path to re-align a model and point cloud if a mistake was made.

{{< webp image="/images/skur-aa/process-user-flow-forms.png" caption="The flow for interacting with the input forms a user would encounter before seeing the Assisted Alignment interface." >}}

#### Tasks

1. Choose a model and point cloud to align
2. Choose Assisted Alignment or an XYZ transform as the method
3. Request re-alignment, using steps 1 & 2 above, if a mistake was made

#### Views and controls

1. Input field for the model
2. Input field for the point cloud
3. Either or option for Assisted Alignment or Transform
4. A control to start alignment
5. A control to start re-alignment

After outlining the design problem with the PM, we decided that the quickest option would be appending a sub-modal form to an existing modal form that Carson already interacts within the app within their user flow. Before handing off to developers, I created mockups of this appended form using Sketch and Bootstrap system components.

{{< webp image="/images/skur-aa/process-input-forms-01.png" caption="Mockups of the input forms for the new Assisted Alignment feature. We kept it simple by adding a field with inline validation to an existing form (highlighted yellow)." >}}

I created a separate mockup of the re-alignment form (undo path) because Carson could mistakenly undo his work. We wanted the user to explicitly confirm the removal of their previous work, to prevent an upsetting amount of data loss, so we decided to create an input form that reflected that. To further prevent redundant work for Carson, we included in-line validation on the form to check whether the selected files were already aligned.

{{< webp image="/images/skur-aa/process-input-forms-02.png" caption="Mockups of the modal confirmation forms a user would see if they wanted to remove their previous alignment work and start over." >}}

### Learning from internal testing

When the team pushed a working version of Assisted Alignment to the development server, we tested the feature internally with real-world examples, and regrouped to discuss our observations.

{{< video src="process-protoV1-dev-demo@360" autoplay="true" muted="true" loop="true" playsinline="true" caption="Screen recording of an early development version of the Assisted Alignment feature— before colors and component styling were completed. The model and point cloud are based on a section of SKUR's offices in Oakland.">}}

During our discussion, the number one problem was disorientation while trying to rotate, pan, or zoom around the viewing area to select surfaces. Several team members demonstrated frustration if they zoomed or panned the model out of view while trying to find surfaces. Choosing a standard isometric view from the controls could help reestablish orientation, but it also meant restarting the surface searching task— like being kicked to the back of the line. In other words, using the standard views as an escape didn’t save time or reduce effort.

While the input from the team certainly illuminated potential problems with the design, I wanted to validate some of our assumptions with actual users. My next step was to test the new feature with a small group of SKUR’s customers.

### Learning from customers

The PM and success manager had arranged product walkthroughs of the AA feature with three customers (all Carson personas). After a demonstration by the team, I observed users completing the alignment task themselves, noting any errors or points of confusion.

Every user was able to complete the alignment task, despite some difficulty finding and picking surfaces. Just as we saw from internal testing, our customers could accidentally pan or zoom the model out of the viewing area and would have to use a control to re-center their view.

We also learned what parts of the UI were not used. Out of all the controls we offered in the design, the users almost exclusively used the “reset” button instead of the top-down-left-right controls that were also available. Also, users were not referencing the instruction text. Instead, if they had questions about the process, they would ask us instead.

{{< webp image="/images/skur-aa/process-protoV1-markup.png" caption="A visual summary of what we learned after limited internal and user-based testing of the new feature. We certainly had an opportunity to improve the design." >}}

These observations showed us that we had over-designed the UI and made the experience more difficult than expected. We had chosen a rotational axis for the viewer that provided more options for navigation, but it was unwieldy and disorienting. We offered numerous controls to help establish standard views, but only one was used. We provided help instructions within the viewer, but they weren’t read. And finally, I had not designed an obvious CTA because users weren’t finding it quickly.

### Redesigning the viewer experience

Research observations showed us that we needed to iterate on the UI controls I had designed and an area outside of those controls: the viewer. I suspected that finding surfaces was complex because the rotational axis changed position to wherever the mouse was placed in the viewer. Even when we explained to the users that rotation occurred around the point they set their mouse cursor, we still observed user error trying to find surfaces. The difficulty, I suspected, was in the inconsistency we built in to the interaction.

However, this was an area of technology that I had little experience with, and I needed to lean on the development team to determine what we could do differently. After whiteboarding options, we assumed that limiting the system to one origin point for the rotational axis would provide the missing consistency. With more consistent feedback to the user, we assumed they would have an easier time searching for surfaces.

{{< video src="rotation-axis-change@532" autoplay="true" muted="true" loop="true" playsinline="true" caption="A demonstration of how we created consistency for the user by changing how the cursor controlled rotation.">}}

After the team pushed the update to the development server, we reviewed the experience again. While the fixed axis made navigation around objects feel easier, the fixed axis didn’t help the problem of easily panning objects out of view.

Then one of the developers proposed a compelling solution: splitting the screen. Rather than have the axis centered between the objects, give each object its own viewing space with a centered rotation. In this way, searching for a surface on the model— whether you were panning, zooming, or rotating— would not affect your view of the point cloud (and vice versa).

{{< webp image="/images/skur-aa/process-protoV2-split-screen.png" caption="We created more consistency and increased ease-of-use by splitting the screen between the model and point cloud." >}}

Once the team pushed a working version of the new rotational system to the development server, improvement to the viewing experience was evident. With the model and scan in their own viewing space, they rotated in place and required little or no panning to navigate around their shape. This split-screen change had made the process of finding surfaces quicker and easier. Split-screen was here to stay.

### Minimal UI redesign

Considering the new split-screen format and my notes about the user experience from research, I started iterating on the UI. My goal was to include only the critical elements for accomplishing the task — keep it simple and obvious. Another guiding principle was maximizing the viewing space to help the user find surfaces— take out as much UI chrome as possible.

I took an inventory of what we could cut and what we needed to keep in the UI. The list of what to include in the next iteration was shorter:

1. Align the model and point cloud (CTA)
2. Save your work (secondary CTA)
3. Close the viewer
4. Undo an mistaken pick
5. Reset the viewer to the default
6. An indicator of progress

#### Navigation controls

To simplify and maximize space for viewing, I sketched out options that constrained all the controls to the navigation bar.

{{< webp image="/images/skur-aa/process-protoV2-sketches-nav.jpg" caption="Considering responsive state changes helped narrow the nav bar options." >}}

I considered whether spacing out controls from each other might prevent errors (e.g., “Undo” placed farther from “Align”). I also compared how putting controls centrally or duplicated on the right and left (e.g., “Undo”) would allow shorter cursor travel and less user effort. Yet when I took responsive design into account, the best option seemed to be placing all of the controls on the right side of the navigation bar. I ordered the buttons from left to right, in the order that we assumed the user would need them, as they completed the task.

#### Progress Indicator

With the new split-screen format, I assumed that displaying progress in the model and point cloud’s respective viewing spaces (rather than a group, as before) would lead to a better user experience. Keeping progress displayed in the same visual area where the user would be searching for surfaces to pick could make progress easier to find and understand.

{{< webp image="/images/skur-aa/process-protoV2-sketches-progress.jpg" caption="Sketching out options helped narrow the choices for a progress pattern. I chose based on simplicity, reusing existing code, and minimizing eye movement." >}}

After sketching out options, I chose a pair of vertical checkboxes, centered in the viewing space, for progress. I assumed this pattern would keep the progress indicator in view with the least amount of eye movement to find it. This pattern also worked well for responsive screen changes and would be easiest to implement because developers had already built checkboxes in the earlier iteration.

#### Removing Help

The last decision was to remove help. The release date was looming, and I did not think we had enough time to design, build and test a successful help feature — especially when we couldn’t schedule additional user testing to validate our ideas. Instead, the PM and customer success manager agreed to distribute a screen recording demo to customers during the update announcement. We reasoned that we could build a help page on the Wiki site or revisit an in-app help feature in a future release.

### Final Deliverables

For my final deliverables, I used Sketch and components from our Bootstrap design system to produce a second round of mockups for my handoff to the developers. These mockups contained each screen at every user flow step, with all the corresponding component states. I also created a click-through prototype to demonstrate the state changes.

{{< webp image="/images/skur-aa/process-protoV2-responsive.png" caption="Sample screens from the design specifications showing responsive state changes for the nav bar and progress indicators." >}}

{{< webp image="/images/skur-aa/process-protoV2-mockup.png" caption="A sample screen from the final deliverables to the development team." >}}

{{< video src="process-protoV2-demo@540" autoplay="true" muted="true" loop="true" playsinline="true" caption="A click-through prototype demonstrating the default path to complete alignment.">}}


## Outcomes and Lessons

### Launch of a new feature

We successfully launched the new feature, Assisted Alignment, within the release cycle we allocated for it. While we did perform updates and bugs fixes to this feature during subsequent cycles, I was proud that what we released was based on a user-informed iteration. As the user experience advocate, it felt like a win. Moreover, the time the team got back by not having to perform alignment-as-a-service let them put more effort into supporting other customer needs.

{{< video src="process-protoV2-dev-demo@480-15" autoplay="true" muted="true" loop="true" playsinline="true" caption="Screen recording from dev server testing of the new feature before it was released.">}}

### Challenges with 3D prototyping

One of the challenges with prototyping a UI for an app that manipulated 3D objects is that no prototyping tools could manipulate 3D objects. I would only truly see how the UI prototypes worked after they were pushed to a development server. This delay slowed my process down and revealed mistakes I could have corrected on my own, but the upside was that the dependency helped build rapport with the development team. Otherwise, I might have been more siloed in my work efforts.

### New approach to prototyping

I worked around some of the limitations of 3D prototyping by using videos and video production software in my design process. After this project, I learned to insert footage from screen recordings of the live app into my design tools— such as autoplay videos on-page changes. Emulating product usage with screen recordings helped reveal the blindspots with static screenshots. Video production software helped highlight areas I wanted my audience to focus on in prototype demos. The process helped expand my view on what tools were available to communicate a product idea.

### Attachment to pixels

Before this project, I was used to minor differences in the deployed product’s UI and the mockups I used for handoffs. The effort I put into precise spacing, rounded borders, and other minutiae would not always show up in the launched product, and I would point it out and try to get changes made. Yet as the work and tech debt piled up and the developers had less time for my one-offs, I had to find another way to preserve the design work. This project, in particular, helped kick start this search.

I assumed that I could help retain the fidelity of my design into production by providing handoffs in front-end code. So I learned just enough HTML and Bootstrap CSS to create mockups of UI designs. The problem with my assumption was that I thought the developers would just copy-paste my kindergarten code into the product and done, but no. So the search for a new process that this project kickstarted ended up back at me. If the team kept moving big continental plates while I stayed attached to pixel-level details, I’d be left behind. “It was time to move on,” became a recurrent mantra. We were, after all, a startup, and moving fast with good enough was the more important lesson.
