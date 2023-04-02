+++
authors = ["Marco Catapano"]
title = "Let's automate my resume generation"
date = "2023-03-27"
description = "Let's use this repo as a PDF templating engine!"
tags = ["pdf","github","html","css","go"]
categories = ["walkthrough"]
toc = true
+++

# The need
Before automating my resume, I had a google document in which I used to maintain a fresh copy of my resume to update and fix.
Every time I want change an info about something in my resume (aka Curriculum Vitae) I needed to:
1. Go to the GDocs link
2. Change the info (could also be just a typo)
3. Export as PDF
4. Store it somewhere in the cloud
5. Give the most recent copy to recruiters, when prompted to do so

Since I am tinkering with templating and GH Actions, it's like having a hammer and starting to see everything as a nail.
So... the idea is to leverage such tech in order to keep everything versioned.

# The plan
Starting from that GDocs link, the plan is to:
1. Export the GDoc as an HTML
2. Find a templating CLI tool
3. Find an HTML to PDF renderer
4. Create a file with all my data
5. Derive a template from the GDoc HTML
6. Feed the templating tool with the aforementioned data
7. Feed the HTML2PDF renderer with the given HTML
8. Automate 6 and 7 in a GH Action

# The execution
The plan itself somewhat worked, but given the "complexity" of the solution for such a trivial task I suspect that there
was an easier way to achieve the same. The YAML+template -> HTML -> PDF pipeline seems a bit inflated. There has to be a
way to avoid the HTML -> PDF conversion, but I've yet to find a better solution.

... not that I tried that much, I just wanted to have something up, automated, and running.

## Exporting Google Doc as HTML

No tech knowledge is needed for this step. So I won't say more than just "I clicked to `File > Download > As web page`".

## Finding a templating CLI tool

I just googled a bit and, since I was already in the "let's get some Go CLI tool", I picked [`gomplate`](https://docs.gomplate.ca/).

## Find an HTML to PDF renderer

Again, quick googling and I've found [`wkhtmltopdf`](https://wkhtmltopdf.org/). From what I tried locally, it seems that
rendering HTMLs into PDFs is not a piece of cake considering that I needed to reiterate a bit on the HTML template I was
able to come up with.

## Create a file with all my data

I just went through all my resume in GDoc and I saw how to structure my data in order to prepare a template.
I won't delve too much into how I come up with some structure: there was no particular methodology behind it, you can
just see my [file](https://github.com/MrSchyzo/about-me/blob/c88c95bbe3911ab70f763426450aefed52de1969/cv/data.yaml).

## Derive a template from 
