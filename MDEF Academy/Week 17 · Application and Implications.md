---
tags: [🌐Website]
publish: true
---


---

## Schedule
_[[Week 16 · Wildcard Week|Last week]] - [[Week 18 · Invention, Intellectual Property, and Income|Next week]]_

_From [[MDEF Academy 2]]_

| Day                         | Description                  |
|:--------------------------- |:---------------------------- |
| [[2022-05-18\|18/05]] · Wed | Application and Implications | 

## Links
- [Local reference: Application and implications](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/material/week10/)
- [Global reference: Application and implications](http://academy.cba.mit.edu/classes/applications_implications/index.html)
- [Global recording: Application and implications](https://vimeo.com/711370621)

---

## Assignment
> [Week 17 · Application and Implications](https://fablabbcn-projects.gitlab.io/learning/fabacademy-local-docs/course_info/mdef/weeklytasks/#week17-application-and-implications)
> - The main objective of this week is to begin focusing on your final projects and interventions, defining the scope and developing a project plan for the rest of the course **Some of the questions you should reflect on it and answer in your website:**
> 	- What will it do?
> 	- Who’s done what beforehand?
> 	- What will you design?
> 	- What materials and components will be used?
> 	- Where will it come from?
> 	- How much will they cost?
> 	- What parts and systems will be made?
> 	- What processes will be used?
> 	- What questions need to be answered?
> 	- How will it be evaluated?

I answered the questions below.

#### What will it do?

It will be a tool for thought that will help me process information, create new ideas, store knowledge, manage projects, write papers, collaborate with others, and other stuff too. It will present a user interface to a graph database of thoughts.

It will be an experimental prototype tool for mapping highly networked thoughts and wrangling them into a single sequence for dissemination. It is intended to be used for sensemaking, knowledge synthesis and management, source reference management, and as a tool to facilitate writing. 

#### Who’s done what beforehand?

I've looked through over a hundred programs and projects in the knowledge management space, and these are the closest ones. 
- Xanadu
- ZigZag, Fenfire
- The semantic web
- Heptabase
- Kosmik
- Subconscious
Each of these have components of what I want, but none of them have implementations that are what I am looking for. 

Tim Berners-Lee and Ted Nelson have proposed solutions for this long ago; what I am trying to do is not new, but yet, was never implemented. Gordon Brander is making progress on his own implementation, and he has a very solid theoretical foundation, but I suspect his implementation may differ from mine.

#### What will you design?

Software, and open policy around it. My [[subatomic notes design space.pdf|design space is here]].

#### What materials and components will be used?

Targeting the web, will probably end up being a progressive web app. Likely to use rust, webassembly, and webgpu.

Structure/features/workflow components:

- Thoughts and connections: Each thought - a short sentence or phrase - is represented visually as a node in a graph, and can be semantically linked to other thoughts with visual connections. Thoughts can be arbitrarily connected, enabling both diverging and converging thought patterns.

- Groups: Thoughts can be grouped together, enabling a layer of abstraction. Groups behave similarly to thoughts in that they can be linked to other thoughts or other groups.

- Chains: Each group may be represented by a special sequence of thoughts within it, called a chain. Chains define a narrative path through a web of thoughts. They have a single thought at the beginning and a single thought at the end.

- Markdown files: A chain can be used to generate the contents of a markdown file. Editing that markdown file will also update the contents of the chain.

#### Where will it come from?

You can get it from [this GitHub repository](https://github.com/jeremyparadie/Subatomic-Notes).

#### How much will they cost?

It will be free and open source.

#### What parts and systems will be made?

Features to develop:
- Thought nodes
- Decentralized graph database
- Real-time multi-user collaboration
- Typeless links
- Typed links
- Groups
- Node version control
- Chains
- Chain-driven markdown generation
- Markdown GUI with visual connections
- Markdown edits propagate to chain
- Primary source file import
- Source reference tracking
- User accounts and persistent data

#### What processes will be used?

Web development processes will be used, including git for version control, and GitHub Pages for deployment, for now. I'll use Visual Studio Code as my IDE.

#### What questions need to be answered?

When will I have time and resources to spend on completing the project?

#### How will it be evaluated?

If it facilitates me writing, thinking, and managing my life without the frictions characterized by other tools, it will be a success. If not, it was a worthwhile experiment. 