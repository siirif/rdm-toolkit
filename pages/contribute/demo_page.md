---
title: Demo page
keywords: [ Demo page, showreel, markdown, Kramdown, Jekyll ]
sidebar: contribute
permalink: demo_page.html
folder: contribute
summary: This is a demo page to showcase what is possible
contributors: [bedroesb]
search: false
---

## Possible metadata attributes of a page

Minimum of metadata in a page:
```
---
title: Demo page
permalink: demo_page.html
---
```
* `title`: Specify here the title of the page. This wil be the H1 title (replacing the top level title using the # in markdown )

* `permalink`: This is the url where the page will be rendered to. For example *demo_page.html* will render the Demo page towards the link https://elixir-europe.github.io/rdm-toolkit/demo_page.html

This can be extended with following attributes (each with an example):

```
---
title: Demo page
keywords: [ Demo page, showreel, markdown, Kramdown, Jekyll ]
sidebar: contribute
permalink: demo_page.html
folder: contribute
summary: This is a demo page to showcase what is possible
contributors: [bedroesb]
search: false
datatable: true
toc: false
custom-editme: _data/tool_and_resource_list.xlsx
tags: [research_it] 
---
```

* `folder`: When your page is located in a subfolder within the pages directory, please specify this folder here.

* `summary`: Using this attribute it is possible to specify a summary which will be displayed under the title of the page. This summary will also be used as description of your page when the page is tagged.

* `contributors`: list here all the contributors that helped in establishing the page. Make sure that the person ID that is listed can be found in the CONTRIBUTORS.yaml file in the _data directory.

* `search`: by setting this field to false, the page will not end up in the search results of the searchbar. By default this is true.

* `hide_sidebar`: When true, the sidebar will be hided. Default: false

* `custom-editme`: This attribute can be used to specify an alternative file/link when clicked on the edit-me button

* `keywords`: List here all the keywords that can be used to find the page using the searchbox in the right upper corner of the page.

* `sidebar`: Specify here an alternative sidebar. Default: main

* `toc`: When set to false, the table of contents in the beginning of the page will not be generated.

* `tags`: If you want to tag this page list the tag using this attribute

* `datatable`: use this attribute to activate the pagination + sorting + searching in tables

## Titles

Using:
```
## Title
```

### Sub titles

Using:
```
### Sub titles
```

#### Sub sub titles

Using:
```
#### Sub sub titles
```

## Bold text

**Bold** text

Using:
```
**Bold** text
```

Make sure there are no spaces between the asterisks and the text you want to put in bold.

## Italic text

*Italic* text

Using:
```
*Italic* text
```

Make sure there are no spaces between the asterisks and the text you want to put in italic.

## File names/ Files / software names

`Text` can be highlighted using:

```md
`Text`
```

## Tables

You can use Multimarkdown syntax for tables. The following shows a sample:

```md
| Priority apples | Second priority | Third priority |
|-------|--------|---------|
| ambrosia | gala | red delicious |
| pink lady | jazz | macintosh |
| honeycrisp | granny smith | fuji |
```

**Result:**

| Priority apples | Second priority | Third priority |
|-------|--------|---------|
| ambrosia | gala | red delicious |
| pink lady | jazz | macintosh |
| honeycrisp | granny smith | fuji |

## Message boxes

Change the content attribute in the code snippet to change the text in the message box

{% include note.html content="This is my note." %}

{% include tip.html content="This is my tip." %}

{% include warning.html content="This is my warning." %}

{% include important.html content="This is my important info." %}


This is done by using this snippet:
{% raw %}
```
{% include note.html content="This is my note." %}
```
{% endraw %}
note.html can be replaced with tip.html, warning.html, important.html, depending on the type of message you want. 

## Images

{% include image.html file="exampleImage.png" caption="Figure 1. Say something about this pic." alt="Servers" %}

This image is inserted in the markdown using following snippet:

{% raw %}
```
{% include image.html file="exampleImage.png" caption="Figure 1. Say something about this pic." alt="Servers" %}
```
{% endraw %}

Make sure that you add the image to the `images` directory and give it an understanding filename. Adapt the snippet so it points towards you image. In the case of the example, the image exampleImage.png is loaded. The alt attribute describes the image and  used for blind people.

## Icons

Go to the [Font Awesome library](https://fontawesome.com/v4.7.0/icons/) to see the available icons.

The Font Awesome icons allow you to adjust their size by simply adding `fa-2x`, `fa-3x` and so forth as a class to the icon to adjust their size to two times or three times the original size. As vector icons, they scale crisply at any size.

Here's an example of how to scale up a camera icon:

```html
<i class="fa fa-camera-retro"></i> normal size (1x)
<i class="fa fa-camera-retro fa-lg"></i> fa-lg
<i class="fa fa-camera-retro fa-2x"></i> fa-2x
<i class="fa fa-camera-retro fa-3x"></i> fa-3x
<i class="fa fa-camera-retro fa-4x"></i> fa-4x
<i class="fa fa-camera-retro fa-5x"></i> fa-5x
```

Here's what they render to:

<i class="fa fa-camera-retro"></i> 1x
<i class="fa fa-camera-retro fa-lg"></i> fa-lg
<i class="fa fa-camera-retro fa-2x"></i> fa-2x
<i class="fa fa-camera-retro fa-3x"></i> fa-3x
<i class="fa fa-camera-retro fa-4x"></i> fa-4x
<i class="fa fa-camera-retro fa-5x"></i> fa-5x

## Links

### Create an external link

When linking to an external site, use:

```md
[Google](http://google.com)
```


### Linking to internal pages

When linking to internal pages, you can manually link to the pages like this:

```md
[Planning](planning)
```
Will link to the planning page.

If you change the file name, you'll have to update all of your links.

## Emoji's

Use Github emoticons! Look [here](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md) to find a cheat sheet for all the emoticons.
:+1: is made with `:+1:`

## Code snippets

For syntax highlighting, use fenced code blocks optionally followed by the language syntax you want:

<pre>
```java
import java.util.Scanner;

public class ScannerAndKeyboard
{

	public static void main(String[] args)
	{	Scanner s = new Scanner(System.in);
		System.out.print( "Enter your name: "  );
		String name = s.nextLine();
		System.out.println( "Hello " + name + "!" );
	}
}
```
</pre>

This looks as follows:

```java
import java.util.Scanner;

public class ScannerAndKeyboard
{

	public static void main(String[] args)
	{	Scanner s = new Scanner(System.in);
		System.out.print( "Enter your name: "  );
		String name = s.nextLine();
		System.out.println( "Hello " + name + "!" );
	}
}
```


## List and sub-list 

* List line 1
* List line 2
    * Sublist line 1

Comes from:

```md
* List line 1
* List line 2
    * Sublist line 1
```

## A collapsible piece of text

<details>
  <summary>Click to expand!</summary>
<ol>
Text
</ol>
</details>
<br>
Is made with this code snippet:

```html
<details>
  <summary>Click to expand!</summary>
<ol>
Text
</ol>
</details>
```

## Tagging pages and listing those pages

Tagging pages is done by the `tags:` property in the metadata of the markdown page.
Add the tag(s) to a list (square brackets). Make sure your tag corresponds to an existing page. 

This metadata example shows how we tag the "Storage" page with the **research_it** tag:
```md
---
title: Storage
keywords:
permalink: storage.html
tags: [research_it] 
---
```

If you than want to list all the pages containing the tag **research_it** you can us the code snippet:

{% raw %}
```
{% include pagelist.html tag='research_it'%}
```
{% endraw %}

Giving:

{% include pagelist.html tag='research_it'%}

This is preferably done on the 'research_it' page. In this way the tag visible on the tagged pages will link to the 'research_it', interlinking everything. To only allow a curated list of tags, make sure you find the tag in the `tags.yaml` file in the `_data` repository. 

## Adding a filtered tool and resource-list to your page

Here we list all the tools with the tag **monitoring**  by using the code snippet:

{% raw %}
```
{% include toollist.html tag="monitoring" %}
```
{% endraw %}

Giving:

{% include toollist.html tag="monitoring" %}

Make sure the tag exists in the `tool_and_resource_list.yml` file + in the `tags.yml`.

Tools and resources can be added by manipulating the tool_and_resource_list.xlsx file in the `_data` repository.

## Enforce space between two lines

To have space between two lines of text, simply leave one empty line in between the line in the markdown. If more is needed, you can force this with:


```md
<br>
```

## Enforce no space between two lines

When you want to have a line of text.\\
And another line underneath it without space, use:

```md
When you want to have a line of text.\\
And another line underneath it without space, use:
```

Without these backslashes

```
When you want to have a line of text.
And another line underneath it without space, use:
```

looks like this:

When you want to have a line of text.
And another line underneath it without space, use: