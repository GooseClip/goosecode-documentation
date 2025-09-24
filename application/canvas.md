---
description: Designers and product managers get a canvas, so why don't we?
icon: pen-paintbrush
---

# Canvas

{% hint style="info" %}
The GooseCode canvas is designed to feel familiar to common tools such as Figma, and Miro.&#x20;
{% endhint %}

## HUD

### Floating Toolbar

The `floating toolbar` is where you can open and close panes, and activate / deactivate tools.

Buttons

1. Explorer pane \[expand | collapse]
2. Overflow
3. Search
4. Drawing
5. Vector
6. Toolbox
7. Shapes
8. Undo
9. Redo
10. Properties & Search pane \[enable | disable]

### Project Toolbar

On the top right you'll see a floating toolbar which allows you to return to the home screen.

### Bottom Toolbar

You may see a toolbar open at the bottom of the screen.

#### Vectors

Here you'll fine the available vectors when you enable the vector tool.

#### IDE integration /  Minimap / Overlay

See [#modes](canvas.md#modes "mention")

### Explorer Pane

When you first enter the canvas you will see the `explorer pane` on your left with 3 tabs.

{% hint style="info" %}
Collapse and expand this pane using the button at the very top of the [#floating-toolbar](canvas.md#floating-toolbar "mention")
{% endhint %}

#### IDE

The IDE tab allows you to connect to Visual Studio or Cursor using the GooseCode extension.

{% hint style="info" %}
See [ide-integration-alpha.md](ide-integration-alpha.md "mention") for more information
{% endhint %}

#### GitHub

The GitHub tab allows you to view and add code from your connected GitHub accounts.

* Code - view or add code to the canvas from your repos
* Commits
* Pull Requests
* Issues&#x20;

{% hint style="info" %}
See [github-integration.md](github-integration.md "mention") for more information.
{% endhint %}

#### Explore

The Expore tab allows you to see all the objects in your canvas. Use it to locate, label, and organize objects in the canvas.

### Properties & Search Pane

On the right side of the canvas you may see the `properties & search pane` open when you click search, or select an object in the canvas.&#x20;

#### Properties

Change the properties of canvas objects using the provided options.

{% hint style="info" %}
It can be distracting to have this open and close constantly so the default behaviour is `disabled`
{% endhint %}

#### Search

Find information in your canvas using the search pane - activate it using the [#floating-toolbar](canvas.md#floating-toolbar "mention")&#x20;

{% hint style="info" %}
Enable and disable this pane using the button at the very bottom of the [#floating-toolbar](canvas.md#floating-toolbar "mention")
{% endhint %}

***

## Canvas Objects

### Collections&#x20;

<details>

<summary>Sections</summary>

Sections are collapsible window panes.

Key features:

* Collapse content without hiding

</details>

<details>

<summary>Frames</summary>

Frames help you organizing your canvas.

Key features:

* Create column
* Create rows
* Control alignmet
* Autosize to content &#x20;
* Label and style related content

</details>

<details>

<summary>Groups</summary>

Groups help with selection of related canvas objects.

</details>

<details>

<summary>Folders</summary>

Folders are purely organizational to clean up the explorer pane.

</details>

### Code

Render code in the canvas with syntax highlighting.

### Text Editor

Create documentation or TODO lists directly in the canvas.

### Shapes

Basic shapes to use to write notes, prototype UIs and create visual boundaries. &#x20;

### Drawing

Draw freehand using your mouse or stylus (iPad).&#x20;

{% hint style="info" %}
This feature is designed for iPad as we all know drawing with a mouse is cumbersome.
{% endhint %}

### Vectors

We've included vector icon packs from Google Cloud, AWS and Azure so that you can enrich your projects with architectural information without needing to switch to more complex tooling.

***

## Modes

If you click the overflow in the [#floating-toolbar](canvas.md#floating-toolbar "mention")you may discover a few tools whose purpose is not immediately obvious. These modes relate to views which will appear in [#bottom-toolbar](canvas.md#bottom-toolbar "mention").

#### Overlay Mode

{% hint style="warning" %}
Overlay mode is available in desktop platforms only.
{% endhint %}

In this mode, GooseCode will try and stay above other windows open in your computer. This can be useful when you don't want to lose context of some notes, code, or maybe even the toolbox while you're working in another program.

{% hint style="danger" %}
Currently in MacOS this does not work over windows which are in fullscreen.
{% endhint %}

#### Minimap Mode

Minimap mode allows you to navigate your codebase using GooseCode like a minimap in a game.

{% hint style="info" %}
Requires IDE integrations and an active connection.
{% endhint %}

{% hint style="success" %}
You can use your iPad as a minimap while you work on your desktop.
{% endhint %}

#### IDE Generator Session Mode

When generating canvas objects from your IDE, you'll see an active session icon appear in the [#bottom-toolbar](canvas.md#bottom-toolbar "mention"). This allows you to stop a session (e.g. if you want to generate in a new [#sections](canvas.md#sections "mention")), and also provides visual feedback when you resume a session by double clicking a generated `section`.
