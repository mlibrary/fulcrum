---
layout: post
title:  "Building a Hosted Platform for Managing Monographic Source Materials: Interim Report – Year 1"
date:   2016-04-10 16:46:30 -0400
author: Melissa Baker-Young
categories: blog
---
## 1. Summary of the Project

In March 2015, University of Michigan Press received $899,000 from the Andrew W. Mellon Foundation for a project entitled “Building a Hosted Platform for Managing Monographic Source Materials.” The proposal was for a suite of activities to be conducted over a period of three years (April 1, 2015 to March 31, 2018) with the end deliverable being a publishing platform built on the Hydra/Fedora framework, to be made available open source reuse as well as in the form of a hosted for-fee solution. While in the short term the primary application of the platform is to address the “companion website” problem (an increasing demand from authors for a way of presenting research data alongside their books), in the longer term it will also provide the infrastructure to enable long form presentations of digital scholarship (the monographs of the future?) to be published. The Hydra/Fedora framework has become popular among large research libraries building data repositories and other content management solutions, and the proposal leverages the developing relationship between libraries and university presses to further their joint goal of better serving the digital scholarship needs of faculty. To provide a proof of concept and keep platform development grounded in real-world needs, five case studies will be published on the platform during the project from Indiana University Press, University of Michigan Press, University of Minnesota Press, Northwestern University Press, and Penn State University Press. Charles Watkinson, Director of University of Michigan Press, and Jeremy Morse, Director of Publishing Technology, are co-PIs on the grant and Melissa Baker-Young is the project manager.

## 2. Accomplishments

### 2.1 Undertaking a collaborative but controlled approach to design

Under the co-leadership of Melissa Baker-Young and a User Experience specialist (50% of Michigan Publishing’s front-end developer, Jon McGlone), the first nine months of the project were focused on gathering user requirements from colleagues at University of Michigan Press and the editors and sometimes authors of the four case studies. Key personas were identified and user stories constructed, leading to a series of wireframes iteratively developed with case study partners. This strong emphasis on planning before software development started enabled the team to clearly communicate with Data Curation Experts when they started programming work in February 2016.

### 2.2 Leveraging library strengths in metadata organization

Nicole Scholtz, a data librarian, is dedicating 5% of her effort to the grant over all three years of the grant. She has been an active participant in the needs assessment calls with partners, focusing on the development of a metadata template distributed to the partner presses to prepare materials for ingest to the platform. This Google Spreadsheet allows the project team to capture descriptive, structural, and rights metadata in a consistent, low-barrier way; provides the authors and editors with a consistent format for organizing their materials; and will drive a batch-upload process for content ingest. By comparing metadata templates from partner presses, the team will be able to clearly communicate the development needs for the Hydra ingest system.

### 2.3 Leveraging library strengths to understand IP issues

Melissa Levine, lead copyright officer at the Library, is dedicating 5% of her effort to the grant for the first two years. She has coordinated with copyright experts at the partner universities to lead “deep dive” conversations into the particular intellectual property challenges faced by the five case study projects. The conversations focused on both specific issues and broader challenges that the specific issues suggested. The general discussions have informed the development of a new proposal (Emory University with University of Michigan) to the Foundation to develop a “Model Contract for Digital Scholarship” which will include a sample permissions letter to third-party rights-holders which was funded in late February 2016.

## 3. Setbacks and Challenges

### 3.1 Hiring programmers

The initial proposal included funds to hire two junior Ruby on Rails programmers to work internally at University of Michigan. Due to challenges finding the right talent within the grant timeline, we instead decided to use the first year’s worth of programming grant money to purchase 14 weeks worth of work from Data Curation Experts — a leading Hydra/Fedora development company. This was not only a pragmatic decision so that we could begin development, but also offered an opportunity to co-develop with DCE and get existing Library developers supporting the grant to become more familiar with the Hydra/Fedora codebase. The participants of various Hydra projects currently under development at Michigan will continue to look for areas of overlap and common needs, which will reduce redundancy in effort but also afford opportunities to leverage DCE development for other Library needs. A new recruitment effort is currently underway with the aim of hiring staff to continue development work for years 2 and 3 of the grant, although DCE will remain a backup option.

### 3.2 Publishing Gabii

While the four partner case studies clearly differentiate the “narrative” (published as monographs outside the platform) from the “data” (published on the platform), the University of Michigan Press case study is deliberately more ambitious. A Mid-Republican House from Gabii presents an archaeological report that is primarily accessed from an interactive 3D model that exists alongside a “narrative” and “data” view. This is long-form digital scholarship that cannot be adequately represented in print and poses a number of challenges:

* The research team uses a MySQL database (ARK), with a PHP front-end, to gather hard data from the dig site, including hi-res still images of the artifacts. We will take a snapshot of the data relevant to the specific building (House B) and treat it as an image database with associated metadata. This strategy allows us to host the database on our current DLXS imageclass platform at present, and places it in the planned migration work of all imageclass content and functionality into Hydra.

* The 3D model that represents the Gabii site is generated in and exported from the popular Unity 3D game engine. While Unity 5.3 can export to the open WebGL format, browser compatibility is still an issue. We are weighing the benefits of using the WebGL version now vs. starting with the proprietary Unity format (which requires a browser plugin) and waiting for WebGL support to improve. Throughout the 3D content, anchor points will contain additional textual information and links to the relevant records in the ARK database.

* The text manuscript contains links to the anchor points in the 3D game. The texts need to be expanded for accessibility purposes to ensure that any readers unable to access the 3D content will find its most salient information conveyed in the text. The links will also be encoded in such a way that those users unable to access the 3D content will be able to bypass the 3D and link directly to the ARK database.

In order to accommodate the Fall 2016 publication date for Gabii, we will be posting the narrative and the 3D model on our existing DLXS platform in beta form. This title will then serve as a pilot for the large-scale migration of content from DLXS to Hydra as the new platform matures.

### 3.3 Branding the platform

While we believed that we could come up with a name for the platform and a visual identity internally, it became apparent that we had underestimated this aspect of product design and needed professional help not only to develop the identity that might encourage client interest as we built toward a sustainability model, but to ensure that the multiple internal stakeholders bought into the project. We decided to hire a professional branding agency (Berman Creative) with non-grant funds to lead us through a discovery process, create a “strategic brand platform,” and develop both a textual and visual identity. This was a helpful process in defining some of the unique selling points of our platform and built upon the insights developed by our business consultant Brian O’ Leary of Magellan Media, who interviewed a number of stakeholders in late 2015 in preparing a strawman business plan.
