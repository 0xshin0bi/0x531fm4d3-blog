---
title: Effective notes with Obsidian
draft: false
tags:
  - Obsidian
  - AtomicNotes
  - EffectiveStudy
---
# What to expect in here?

In this blog, I will talk about my note-taking experience with Notion and the various cons I encountered while using it. I will then highlight the Obsidian features that significantly improved both my note-taking process, effectively making my notes much more usable and **effective to remember**. After briefly explaining how I structured my Vault, I will present my setup, including templates (with some JavaScript snippets), folder organization, and the plugins I use. For everyone who wants to give it a try, I also provide a link to a ready-to-download Vault hosted on my GitHub.
**Spoiler alert** - No AI whatsoever in this vault :), while I often use llm for finding good resources or summarizing them for understanding, I find my learning much more effective when I write notes in my own words.

# The struggles — my note-taking experience before Obsidian

For a long time, I struggled making my learning notes effective, to the point they will be re-usable on a daily basis. I bounced between Notion and Evernote, trying to summarize what I was learning, but the fact I was never going back to the notes clearly stated I'm doing something wrong. A few things made it especially frustrating while using Notion:

## Folder hierarchies were a mess

Notion uses the traditional folder-based organization. *hence*, i tried grouping related notes under the same parent directory. While it seemed like a good idea at first, eventually everything turned into a  mess of nested folders, and it wasn’t scalable. To try and make things more manageable, I began creating a separate note for each book or course I went through. That led to giant, bloated notes packed with highlighted text of information I liked: green for useful tools, blue for smart code snippets, and so on. Honestly, it was hard to find these "gems" in the monstrous notes, so I'd rarely went back and actually looked at those notes again.

## Search was bad

Whenever I needed to dig up a specific idea/research technique, I encountered a big problem; The built-in search in those apps just wasn’t good enough. looking for the specific information was actually quicker to just look online. moreover, even if i had an idea where it should be, the big "one-per-book notes" made it really hard to find exactly what I wanted.

## The lags...

Notion in particular really struggled with my "note-per-book" approach as pages took forever to load. Trying to quickly jump between notes or update something mid-thought was frustrating enough to make me want to stop writing entirely.

# Then came Obsidian

Things changed when my friend Yuval Nativ introduced me to Obsidian — a markdown-based, local-first note-taking app. It has a great free version too, which is what I am currently using.

There are already tons of great tutorials out there (I'll link some on the bottom) on how to set it up, so instead, I want to focus on why I personally think it is the ultimate note-taking solution:


# Finding my way in Obsidian

Obsidian does have a learning curve. It’s so flexible that the hardest part is figuring out how you want to use it, and assembling the initial structure (mostly plugins and their configurations, templates, folders, note naming conventions, hotkeys).
I gave myself a few weeks to get familiar with different plugins and configurations. During that time, I came across the **Zettelkasten** method—an approach based on atomic notes and linking ideas together. While I connected with the approach behind it, I needed to do some adjustments to ZettelKasten  Vault setups I encountered due to the technical nature of the subjects I like digging into.

# Why Obsidian?

## It’s fast

Obsidian runs locally, which means everything is super fast. Open the app, your vault loads, and you’re off. 

## Linked notes will make your own personal Wikipedia

 Notes can be linked together using simple syntax, and backlinks are generated automatically. This made it easy for me to connect related concepts—like tools, techniques, or terms—while keeping each note focused and atomic. Whenever a topic felt even slightly outside the scope of the current note (but still related to it), I could just create a new one and link them together.

## Small notes, big value

A by product of the previous point: I stopped writing massive, monolithic summaries and started breaking things down into bite-sized notes. This made each note easier to maintain, and I could build on them over time. As my vault grew, individual notes became richer, more connected, and far more useful. 

## Second brain

Obsidian is essentially my second brain that never forgets. complicated topics that take time to digest and understand are written in my own words and saved in it forever, so I can pull them out whenever I need them.

## Templates for structure

Obsidian lets you create templates for different types of notes. Each one can have pre-filled sections, metadata, and prompts; This keeps note-taking process consistent, because it forces me to think about what kind of information is worth keeping, essentially making note-taking process more intentional.

## Plugins ftw

There’s a plugin for nearly everything—syntax highlighting, diagrams, whiteboards, visualizations and even Python integration.
Since plugins are just JavaScript under the hood, you can (and should honestly) audit the ones you install (and yes, there’s a plugin to help you manage plugins too ;)).

## Metadata with YAML

Every note can have a YAML metadata block at the note's top (called **frontmatter** in Obsidian)  where you can store key-value pairs for different purposes. With a little help from community plugins like Templater, I even set things up so I get prompted to fill in certain metadata fields when I create a new note. This way, I don’t forget to capture the important stuff. I personally use them for additional note categorization and sub-categorization, linking the notes to the resource where I initially read about them, and easen the search by adding aliases to the notes.

# Some explanations before the vault setup

## What is a Vault?

A vault is simply the folder on our local file system where obsidian stores your notes and the configurations of your vault as well (plugins, themes, etc.)

## Why does frontmatter matter? 

As mentioned before, frontmatter is the yaml structure located on the note's top. it could be queried using Dataview into lists and tables, which can provide a high-level overview of whatever's in your vault. keep in mind that at this time, **there's no native way to query other information from within the note itself other than frontmatter** (though possible through python scripts with Python Scripter).l

## What are tags in Obsidian?

Tags are keywords that help you find what you're looking for. They can be used in two main ways:
1. You can search for a tag directly to see all notes that include it.
2. You can use tags in Dataview queries to act as powerful filters.

# ./My vault --verbose

**Heads up - this part is long.**
if you're building your own Vault or want to try mine, then please bare with me because it will all make sense in the end.

## Plugins

below are the community plugins installed on the Vault. each has its own short description and how I use it in the Vault. I added some screenshots of how it looks like inside 

### Templater

[Templater](https://github.com/SilentVoid13/Templater) is a powerful template engine for Obsidian that automates note creation using JavaScript-based logic. It enables dynamic content generation, user input prompts, and advanced workflows within templates. I use JavaScript snippets in the templates' frontmatter to quickly insert data when creating a new note, and by doing so ensure that important metadata related to each note is properly documented. Some examples in the screenshot below:

![[Pasted image 20250428161711.png]]
_how the snippets look like in the templates' frontmatter_

![[Pasted image 20250428154018.png]]
_an example of how the JS takes affect when creating a new note_

### QuickAdd

[QuickAdd](https://github.com/chhoumann/quickadd) goes hand in hand with Templater. The plugin is ideal for building fast, repeatable workflows with emphasis on user-defined actions, templates, and macros. I use it to quickly create different types of notes through a keyboard shortcut and a few mouse clicks.

![[Pasted image 20250428154212.png]]
_an example of quickadd used to create notes with a certain prefix, in a specific folder (couldn't capture in the SS all the options possible_

### Omnisearch

[Omnisearch](https://github.com/scambier/obsidian-omnisearch) provides an advanced search experience in Obsidian, allowing you to query your entire vault by content, tags, links, and other metadata. It also offers the option to index PDFs and images through OCR, which I find particularly useful. The search algorithm is well-designed, making it easy to quickly find exactly what you are looking for.

![[Pasted image 20250428154334.png]]
_showing Omnisearch's awesome capabilities_

### Dataview

[Dataview](https://github.com/blacksmithgu/obsidian-dataview) is essential for building dashboards, summaries, and structured views across your vault based on your notes frontmatter values and tags. it has basic query options, but also support more advance queries based on JS. I use it for grouping my vault's tasks, and creating a per-resource table of terms i encountered in them.

![[Pasted image 20250428154803.png]]
_using dataview to show all tasks open in the vault in one place_

### Excalidraw

[Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin) is an integration of the Excalidraw visual whiteboard tool directly within Obsidian. It allows for the creation of sketches, diagrams, and mind maps, all saved as markdown-linked files. The plugin is useful for visual thinking and planning workflows alongside traditional notes. I use it to create visualization of more complex stuff I encounter.

### Plugin Update Tracker

[Plugin Update Tracker](https://github.com/swar8080/obsidian-plugin-update-tracker) monitors your installed plugins and records when they are updated. It provides a changelog view directly inside Obsidian for easier tracking of new features and fixes. The plugin helps maintain awareness of changes that could affect your workflows, or potentially malicious code that found its way into the plugin god forbid :).

![[Pasted image 20250428160148.png]]
_plugin update tracker summary pulled from github; also a direct link to the diff from last version_

### Settings Search

[Settings Search](https://github.com/javalent/settings-search) enhances Obsidian’s settings interface by adding a search bar to it. It saves alot of time looking for what you're looking for.

![[Pasted image 20250428160330.png]]


### Colored Text

[Colored Text](https://github.com/erincayaz/obsidian-colored-text) provides a quick and comfortable way to highlight sentences and words with colors inside your notes; instead of writing your own color html element, this plugin does it for you. It has some predefined color names and also supports custom color hex codes.

### Code Styler

[Code Styler](https://github.com/mayurankv/Obsidian-Code-Styler) customizes the appearance of code blocks in Obsidian by allowing fine-grained control over fonts, backgrounds, padding, and more. It works with both light and dark themes. it just looks alot nicer than the native Obsidian code blocks 

![[Pasted image 20250428161919.png]]
_supporting syntax highlighting of many coding languages and different text types_

### Recent Files

[Recent Files](https://github.com/tgrosinger/recent-files-obsidian) creates a dynamic list of your most recently opened or edited notes in Obsidian. It adds a panel or command for quick access to recently used documents. it makes it very easy editing multiple notes at once without wasting time looking for the last few notes you were in.

![[Pasted image 20250428162043.png]]
_how Recent Files look like_

### Tasks

[Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) turns standard markdown checkboxes into powerful task management elements, with support for due dates, priorities, recurring tasks, and queries. It enables you to track and organize tasks directly within your notes. I use it mainly when there are aspects that I haven't covered yet in certain notes and do not want to forget. I especially like using Dataview to present current open tasks across the Vault in a single location.

### Update Time on Edit

[Update Time on Edit](https://github.com/beaussan/update-time-on-edit-obsidian) helps maintain accurate metadata by automatically recording when a note was last modified (in the frontmatter. I use it to easily keep track of the last time i made changes to my notes.

## Tags

I use tags in my "term" and "technical explanation" notes for categorization. Since a single note can relate to multiple categories, tags have proven to be the most convenient method for this purpose.

## Templates

in this section I will list and provide details for both each template's frontmatter key pairs and note's headlines. for each template type, I'll give a simple example of what might I capture in each (styled in _italic_). explanations for each frontmatter key-pair or headline is in the frontmatter/note prototype after each line. I'll skip key-pairs/headlines already explained previously.

### Origin

This note is intended for each resource I am currently studying (book, course, research, etc...).

_Say I'm diving into a book dealing with windows internals. The "origin" note in this case is the book itself, where I'll save useful information._

#### Origin frontmatter

```yaml
created: 2024-12-22T08:34
updated: 2025-04-21T15:54 // updated automatic by Update Time on Edit. 
origin_value: <% tp.file.title %> // grabs the title as is 
type: origin // useful key-pair to query notes from specific types.
started: <%tp.system.suggester(["yes","no"],[true,false],throw_on_cancel=false, placeholder="started writing?")%> // have I started going over the resource?
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %> // captures the origin name without the prefix I configured through QuickAdd. this way, linking this current note on another note will appear cleaner.
```
#### Origin headlines

```text
# Origin Link // link to the local pdf/URL

# Currently At // contains a yaml with the following key-pairs:
'' 
Page/Minute: // which page/minute am I at on the book/video
Headline: "" // for books, under what headline is the point i stopped at.
Text: "" // specific line where i stopped at.
Current term editing: // which term related to the origin i'm currently at (incase I stopped middle writing)
''
# Summary // if it's a short resource, a small summary of what's it's about

# Concepts Learned // self explanatory

# Related Origins // self explanatory

# Relavant links // links to related internal notes or external resources
```
### System

this note type is intended for each new system I encounter and wish to understand better.

_while going through the Windows internals book, I encountered Windbg. I'll open this template for it._

#### System frontmatter

```yaml
created: 2024-12-22T08:34
updated: 2025-04-21T15:54
origin_value: <% tp.file.title %>
type: system
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
cssclasses:
  - dv-equal-columns
```
#### System headlines
```text

# Overview // general background on the system

# Use cases // when do i use this system. either general cases or links to technical explanation notes. 

# Common Commands/Functions // self explanatory

# Customizations // incase the system requires some preperations or additional installations to make it work properly.

# Relevant Links
```

### Technical explanation

 this note type is intended for hands-on step by step explanation of using certain system to perform wanted action.
 
 _in the book they discussed how to look at the PEB structure in Windbg. This is where i'll capture it._


#### Technical explanation frontmatter 

```yaml
created: 2024-12-22T08:34
updated: 2025-04-22T13:00
term_value: <% tp.file.title %>
type: technical_explanation
origin_value: <%* const files = app.vault.getFiles().filter(f => f.path.startsWith('01 - Origins/') || f.path.startsWith('04 - Systems/')).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %> //the origin from which i got to this technical explanation part. JS prompts a dropdown of existing origin files located in the origin folder.
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
cssclasses:
  - dv-equal-columns
status: in progress 
maturity: baby  // helps me understand if it is a note i need to work on more. here I insert baby/child/adult
```

#### Technical explanation headlines


```text
# Categories // storing tags of note's related categories

# Objective // what does this note's instruction achieve

# Tooling // what tools are needed for it

# Steps // the main part where I document step-by-step

# Notes // important things I should remember in the future (bugs, mistakes i've previously made, etc)

# Relevant Links
```

### Term

**term** - this note is intended to describe more theoretical knowledge.
_I first encounter what is  a PEB. this is where i'll capture the details._


#### Term frontmatter

```yaml
created: 2024-12-22T08:34
updated: 2025-05-06T08:39
term_value: <% tp.file.title %>
type: term
origin_value: <%* const files = app.vault.getFiles().filter(f => ['01 - Origins', '04 - Systems'].some(folder => f.path.startsWith(folder + '/'))).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %>
cssclasses:
  - dv-equal-columns
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
status: in progress
maturity: baby
```

#### Term headlines

```text
# Categories

# Summary // self explantory

# Detailed Description // the main headline where i breakdown the term.

# Structure // here i store screenshots, function prototypes, strucutures, charts; anything that helps me understand the term visually.

# Contextual Use // When/how this term becomes relevant.

# Related Links  
```

## Vault's folders

While Obsidian doesn’t require folders to function, I still prefer to keep things visually organized that way. Below is a screenshot of my folder structure, along with explanations for the ones that aren’t immediately obvious:

![[Pasted image 20250510130827.png]]

## Home note

This is a special note where I store data that gives me more control over the vault. Currently, it contains my tasks table, various Dataview queries, and a list of topics I've stumbled upon that I want to add to the vault.


# Great Obsidian guidance links

Shoutout for these content creators that helped me formulate my ideal note-taking vault :)

https://www.youtube.com/@FromSergio

https://www.youtube.com/@nicolevdh

https://www.youtube.com/@BenCodeZen
