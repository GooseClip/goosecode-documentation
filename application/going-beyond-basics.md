---
icon: flask
---

# Going Beyond Basics

## Your Codebase Minimap&#x20;

{% hint style="info" %}
To use this walkthrough please make sure you're familiar with your IDE setup [ide-integration-alpha.md](ide-integration-alpha.md "mention")
{% endhint %}

After generating code in canvas, you can "rewalk" you dataflows by using `minimap mode` .

#### Prerequisites

* [ ] You've set up your IDE connection
* [ ] You've generated some swimlane code
* [ ] Your connection is still running

{% stepper %}
{% step %}
### Open GooseCode
{% endstep %}

{% step %}
### Turn on Minimap Mode

1. Click the overflow menu in the [#floating-toolbar](canvas.md#floating-toolbar "mention")
2. Select `minimap`&#x20;

{% hint style="info" %}
You will notice a numer of changes

1. Your window got smaller.
2. Your window now floats above other windows.
3. All your HUD is gone except a little `X` at the bottom (exit minimap mode).
4. You cannot click on much.
{% endhint %}
{% endstep %}

{% step %}
### Resize GooseCode to your preferred size

When you exit minimap mode your window will be restored to its original size.
{% endstep %}

{% step %}
### Return to your IDE

Your minimap should follow you. Adjust it to a location on your screen which isn't in the way.
{% endstep %}

{% step %}
### Rewalk code

Click on code in the GooseCode minimap and your IDE should immediately switch to the relevant code section.
{% endstep %}

{% step %}
### Exit Minimap Mode

Click the small floating `X` in GooseCode to return to the default mode.
{% endstep %}
{% endstepper %}

### What should I use it for?

#### Flowstate

When coding, we often lose key structural information about dataflows due to the necessity to swap tabs and scroll. With minimap, we can always see our stucture in a visually easy to understand representation, and we can skip to relevant sections without breaking our flowstate.

#### Bookmarking

Ever tried using IDE bookmarks? As humans we're visual creatures, geometric shapes and colors are what we've evolved to recognise, not text on a screen.

#### Code reviews

Highlight key areas of concern and review them with the submitter.

#### Communicate with the team

Prepare your question and reasoning ahead of time so you can confidently communicate about your ideas without losing yourself in the code.

#### Codebase Documentation

Prepare flows which effectively communicate how the codebase works.

{% hint style="warning" %}
Collaboration and sharing is not yet available
{% endhint %}

***

## Reduce Context-Switching with Ovelay

The purpose of overlay is to keep you focused on what you're doing and not window swapping constantly.

{% stepper %}
{% step %}
### Open GooseCode


{% endstep %}

{% step %}
### Turn on Overlay Mode

1. Click the overflow menu in the [#floating-toolbar](canvas.md#floating-toolbar "mention")
2. Select `overlay`&#x20;

{% hint style="info" %}
You will notice a few changes

1. Your window floats above other windows.
2. Your window follows you as you move between spaces (MacOS).
{% endhint %}
{% endstep %}

{% step %}
### Exit Overlay Mode

Click the small floating `X` in GooseCode to return to the default mode.
{% endstep %}
{% endstepper %}

### What should I use it for?

#### Toolbox

Use the [toolbox.md](toolbox.md "mention") while keeping focus on your work.&#x20;

Examples:

* Pick colors while working on UI code.
* Debug hex strings while reading from the terminal.
* Decode base64 log payloads.
* Debug a JWT claim.
* Generate a new UUID for a database entry.

#### IDE Generate&#x20;

View your generated code as you walk through your codebase. Quickly swap into minimap when you want to revisit part of your code from earlier in the flow. Undo or delete generated code after making a mistake.

#### AI

AI's work surpisingly well with images. You can screenshot a drawing of some wireframing and paste it into your AI agent and ask it to generate some UI, or copy code snippets from the canvas and use it in your prompt.

#### Document

Write documentation about your codebase as you click through.

#### Tasks

Create TODO lists as you come across important things that need to be addressed. Enrich the TODOs with snippets or screenshots.

#### Learning

Keep notes and code side by side as you watch a YouTube tutorial or read some documentation. Add links to the canvas for later.&#x20;

#### Architecting

Diagram in GooseCode as you step through the codebase.

#### Decompose complex codebases

Combine all of the above to create a mental model of a new or complex codebase which you're trying to understand.





