= Introduction to IoT
Clément Levallois <clementlevallois@gmail.com>
2017-01-20

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: gephi-logo-2010-transparent.png[width="450" align="center"]

image::gephi-logo-2010-transparent.png[width="450" align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


== Description of the project

//ST: Description of the project
//ST: !


This project is for complete beginners to Gephi.
It supposes you have Gephi installed and running on your computer. That is all.

When finishing this tutorial, you should be able to:

- be familiar with the vocabulary to discuss networks
- download a network file for this exercise
- description of the file / the network

//ST: !

- open a network file
- read the report after opening a file
- show the labels of the nodes
- layout the network

//ST: !

- visualize attributes of the network
- prettify the network for enhanced readability
- compute the centrality of the nodes in the network
- visualize attributes created by Gephi
- export a visualization as a picture or pdf


== be familiar with the terminology to discuss networks
//ST: terminology to discuss networks
//ST: !

image::terminology-for-networks.png[align="center",title="terminology for networks"]
{nbsp} +


== download a network file
//ST: download a network file
//ST: !

link:../resources/miserables_result.zip[download this zip file] and unzip it on your computer.

You should find the file `miserables.gexf` in it.

Save it in a folder you will remember (or create a folder specially for this small project).

== description of the file / the network

//ST: description of the file / the network
//ST: !

This file contains a network representing "who appears next to whom" in the 19th century novel _Les Misérables_ by Victor Hugofootnote:[D. E. Knuth, The Stanford GraphBase: A Platform for Combinatorial Computing, Addison-Wesley, Reading, MA (1993)].

A link between characters A and B means they appeared on the same page or paragraph in the novel.

The file name ends with ".gexf", which just means this is a text file where the network information is stored (name of the characters, their relations, etc.), following some conventions.


== open the network in Gephi
//open the network in Gephi
//ST: !
- open Gephi. On the Welcome screen that appears,  click on `Open Graph File`
- find `miserables.gexf` on your computer and open it

image::en/gephi-welcome-screen-open-graph-en.png[align="center", title="welcome screen"]
{nbsp} +

== read the report after opening a file

//ST: !
A report window will open, giving you basic info on the network you opened:

image::en/opening-file-report-en.png[align="center", title="report window"]
{nbsp} +

//ST: !
This tells you that the network comprises 74 characters, connected by 248 links.

Links are undirected, meaning that if A is connected to B, then it is the same as B connected to A.

The report also tells us the graph is not dynamic: it means there is no evolution or chronology, it won't "move in time".

Click on `OK` to see the graph in Gephi.

== initial view

//ST: !

image::en/project-initial-view.png[align="center", title="initial view when opening a graph"]
{nbsp} +

This is how the network appears in Gephi. Not very useful! Let's examine what we have here.

== basic view of Gephi's interface

//ST: !

image::the-3-main-screens-in-Gephi.png[align="center", title="the 3 main screens in Gephi"]
{nbsp} +

//ST: !
Gephi has 3 main screens:

1. Overview: where we can explore the graph visually
2. Data Laboratory: provides an "Excel" table view of the data in network
3. Preview: where we polish the visualization before exporting it as a pictue or pdf

What we see here is the Overview.

//ST: !

image::Filters-and-statistics-panels-in-Gephi.png[align="center", title="Filters and statistics panels in Gephi"]
{nbsp} +

//ST: !

In the Overview, the graph is shown at the center. Around it, several panels help us fine tune the visualization.

[options="compact"]
[start=4]
4. "Filters", where we can hide different parts of the network under a variety of conditions
5. "Statistics", where we can compute metrics on the network

//ST: !
image::Appearance-and-layout-panels-in-Gephi.png[align="center", title="Appearance and layout panels in Gephi"]
{nbsp} +


//ST: !

[options="compact"]
[start=6]
6. "Appearance", where we can change colors and sizes in interesting ways
7. "Layouts", where we can apply automated procedures to change the position of the network

//ST: !
image::3-groups-of-icons.png[align="center", title="3 groups of icons"]
{nbsp} +

//ST: !

[options="compact"]
[start=8]
8. A series of icons to add / colorize nodes and links manually, by clicking on them
9. Options and sliders to change the size of all nodes, links, or labels
10. More options become visible if we click on this *little arrow head pointing up*


== showing labels of the nodes

//ST: showing labels of the nodes

//ST: !

image::showing-node-labels.png[align="center", title="showing node labels"]
{nbsp} +


== layout ("spatialize") the network

//ST: layout ("spatialize") the network

//ST: !

image::selecting-the-force-atlas-2-layout.png[align="center", title="selecting the force atlas 2 layout"]
{nbsp} +

//ST: !

[[force-atlas-2-parameters]]
image::changing-a-few-parameters-and-launching-the-layout.png[align="center", title="changing a few parameters and launching the layout"]
{nbsp} +


//ST: !

image::result-of-Force-Atlas-2-layout.png[align="center", title="result of Force Atlas 2 layout"]
{nbsp} +

== visualize the properties of the nodes

//ST: visualize the properties of the nodes

//ST: !

A network consists in entities and their relations.
This is what we just visualized.
Yet, the properties of these entities remain invisible.

For instance: the characters in the novel "Les Misérables" are male or female. Are males more likely to be connected to males, or females? Just looking at the network in Gephi, we can't tell.

Now, we will see how to make this property ("Gender") visible.

//ST: !

image::Switching-the-view-to-the-data-laboratory.png[align="center",title="Switching the view to the data laboratory"]
{nbsp} +

//ST: !

image::We-see-there-is-a-Gender-attribute-for-each-character..png[align="center",title="We see there is a Gender attribute for each character."]
{nbsp} +

//ST: !

We will color the nodes based on their gender. To do that, we select `Gender` in the `Appearance` panel:

image::Coloring-nodes-according-to-their-gender.png[align="center",title="Coloring nodes according to their gender"]
{nbsp} +

//ST: !

The result:

image::appearance-miserables-result.png[align="center",title="After coloring characters according to their gender"]
{nbsp} +

== prettify the network for enhanced readability

//ST: prettify the network for enhanced readability
//ST: !

There are a number of issues with the result we get:

1. the network is too big or too small, it is hard to read
2. the labels of the characters overlap
3. the size of the labels might be too big / small
4. the links are sometimes too large

Let's fix these issues.

//ST: !
==== 1. Enlarge or shrink the network

- either we use the "scaling" parameter of the layout, as we have seen <<force-atlas-2-parameters,here>>.
- or the scale is fine, it is just that we need to zoom it or out. Use the scrolling wheel of your mouse, and right click to move the network.

//ST: !
==== 2. Prevent the Labels from overlapping

In the layout panel, choose "Label Adjust" or "Noverlap": these layouts will move the nodes just so that the Labels stop overlapping:

image::en/choosing-a-label-adjust-algo-en.png[align="center",title="Noverlap or Label Adjust will help you"]
{nbsp} +

Don't forget to click on "Run" to apply these layouts.

//ST: !
==== 3. Changing the size of the labels
Open the bottom panel of Gephi by clicking on tiny arrow head (1). Then select "nodes" (2), then move the slider (3).

//ST: !
image::Adjusting-label-size.png[align="center",title="Adjusting label size"]
{nbsp} +

//ST: !
==== 4. Adjusting the thickness of the links

image::Adjusting-edge-thickness.png[align="center",title="Adjusting edge thickness"]
{nbsp} +

== computing the centrality of the nodes

//ST: Computing the centrality of the nodes
//ST: !
==== 1. Definitions of centrality

"Centrality" is a very good metrics to first get an idea of a network.
What does centrality mean? Intuitively, we understand that a "central" node will probably sit in the middle of the network.
But how to measure that "scientifically", so that we have an objective confirmation of our visual impression?

There are several ways, all equally interesting.

//ST: !
We can measure `degree centrality`. "Degree" is the technical term for "number of connections that a node has".

So, `degree centrality` just means that the most central node is the node which has the most connections. Simple!

//ST: !
Another measure is `betweenness centrality`. This one is more tricky.

- First, you have to imagine what is a `shortest path`.
   - A `path` from node A to node B is a chain of nodes, the road if you will, that you have to traverse to go from A to B.
   - The `shortest path` from A to B is the quickest road from A to B: the path that has the smallest number of nodes between A and B.

- A node which is on many shortest paths is "between" many nodes. And when you realize it, it is a very intuitive sense of what it means to "be central". These nodes have a high `betweenness centrality`.

//ST: !
==== 2. Computing betweenness centrality with Gephi

Gephi computes it for you. Find "Network diameter" in the statistics panel and click "run":

image::Computing-betweenness-centrality.png[align="center",title="Computing betweenness centrality"]
{nbsp} +

//ST: !
This will open a window with parameters (explained in a more advanced tutorials). Click "OK":

image::Parameters-for-the-computation-of-betweenness-centrality.png[align="center",title="Parameters for the computation of betweenness centrality"]
{nbsp} +


//ST: !
A report window opens (also explained in a other tutorials). Close it.

image::Report-after-the-computation-of-betweenness-centrality.png[align="center",title="Report after the computation of betweenness centrality"]
{nbsp} +

Now we can visualize this information.

== visualize attributes created by Gephi

//ST: visualize attributes created by Gephi
Gephi has computed for us the betweenness centrality of all nodes. This remains invisible on the network, however.

It would be interesting to, say, resize the nodes according to their centrality: the more central a node, the bigger.
This would allow for a very quick visual appreciation of which nodes are the most central.

//ST: !
First, let's switch to the data laboratory to see how Gephi stored the "betweenness centrality" of each node:

image::Switching-the-view-to-the-data-laboratory.png[align="center",title="Switching the view to the data laboratory"]
{nbsp} +

//ST: !

When we ran "Network Diameter" in the statistics panel, Gephi has actually computed many kinds of centralities (not just "betweenness centrality"):

image::Different-centrality-measures-visible-in-the-data-laboratory.png[align="center",title="Different centrality measures visible in the data laboratory"]
{nbsp} +

//ST: !
To resize the nodes according to the value of their betweenness centrality, we use the `Appearance` panel:

CAUTION: make sure you select the correct options

image::Ranking-node-sizes-by-centrality.png[align="center",title="Ranking node sizes by centrality"]
{nbsp} +

//ST: !

image::Selecting-the-minimum-and-maximum-sizes-of-nodes.png[align="center",title="Selecting the minimum and maximum sizes of nodes"]
{nbsp} +

//ST: !

image::ranking-centrality-miserables-3--en.png[align="center",title="Result of the ranking"]
{nbsp} +

//ST: !

image::Resizing-labels-to-reflect-their-node's-size.png[align="center",title="Resizing labels to reflect their node's size"]
{nbsp} +

//ST: !
image::result-label-resizing-en.png[align="center",title="Result of the label resizing"]
{nbsp} +

== exporting a network as a picture

//ST: exporting a network as a picture

//ST: 1. exporting a screenshot from the Overview (a png image)

//ST: !

image::Open-the-configuration-panel-for-screenshots.png[align="center",title="Open the configuration panel for screenshots"]
{nbsp} +

//ST: !

Select the maximum value for anti-aliasing, and multiply values for width and height for higher resolution. For example, resolution x 3 is width = 3072 and height = 2304

image::en/configuration-screenshot-en.png[align="center",title="The configuration panel for screenshots"]
{nbsp} +

//ST: 2. exporting a pdf or svg picture

//ST: !
Let's switch to the preview panel:

image::Switching-to-the-preview-panel.png[align="center",title="Switching to the preview panel"]
{nbsp} +

//ST: !
The preview panel is dedicated to the preparation of the picture to be exported as a pdf or svg, which are "scalable": in pdf or sv, the resolution of the graph will remain perfect, even with a strong zoom.
But as you see, it means the network is now looking different than in the Overview.

//ST: !
CAUTION: contrary to the Overview panel, here you need to hit the "refresh" button after each parameter change.

image::Updating-the-parameters.png[align="center",title="Updating the parameters"]
{nbsp} +

//ST: !
Here I change just 2 parameters: `Show Labels` and  `Font` (which I reduce to size "5"), to get:

image::Result-of-preview.png[align="center",title="Result of preview"]
{nbsp} +

//ST: !
Export: just click on the button and select the file format you prefer

image::Export-button.png[align="center",title="Export button"]
{nbsp} +

//ST: donwload the result file

link:../resources/miserables_result.zip[download this zip file] if you need to see the network in its final form.

== the end

//ST: The end!
Visit https://www.facebook.com/groups/gephi/[the Gephi group on Facebook] to get help,

or visit https://seinecle.github.io/gephi-tutorials/[the website for more tutorials]


== questions and exercises

//ST: questions and exercises

//ST: !
1. Open the file `miserables.gexf` with a text editor (here is how to do it on a http://www.dummies.com/computers/macs/how-to-open-and-edit-a-text-file-on-a-mac/[Mac], and on https://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/app_notepad.mspx?mfr=true[Windows]). See how the nodes and the links are written in the file. Can you find the character Javert?

//ST: !
[start=2]
2. Our network of Les Miserables characters was undirected. Can you think of networks which are directed?

Imagine how undirected and directed networks differ when computing centrality, for example.

//ST: !
[start=3]
3. Force Atlas 2 is a layout which brings together connected nodes, and spreads out unconnected nodes. We might have nodes with no relation at all with other nodes (called "isolated nodes").

How will these isolated nodes move on screen?

//ST: !
[start=4]
4. When applying the Force Atlas 2 layout, the network moves quickly, then stabilizes, and then keeps moving a bit.

Can you guess why this is happening?

//ST: !
[start=5]
5. In the list of layouts, Force Atlas 2 is just one of many options you can choose.
Try "Fruchterman Reingold" and "Yfan Hu".

These are layouts which follow the same logic as Force Atlas 2, but with slight variations. Explore how these algorithms result in similar, yet specific layouts.

//ST: !
[start=6]
6. In this tutorial, we defined degree centrality.
Can you imagine a situation when a node with the largest degree centrality will actually be in the periphery of the network? You can draw a toy network to help you figure.
rk of Les Miserables characters was undirected. Can you think of networks which are directed?

Imagine how undirected and directed networks differ when computing centrality, for example.

//ST: !
[start=3]
3. Force Atlas 2 is a layout which brings together connected nodes, and spreads out unconnected nodes. We might have nodes with no relation at all with other nodes (called "isolated nodes").

How will these isolated nodes move on screen?

//ST: !
[start=4]
4. When applying the Force Atlas 2 layout, the network moves quickly, then stabilizes, and then keeps moving a bit.

Can you guess why this is happening?

//ST: !
[start=5]
5. In the list of layouts, Force Atlas 2 is just one of many options you can choose.
Try "Fruchterman Reingold" and "Yfan Hu".

These are layouts which follow the same logic as Force Atlas 2, but with slight variations. Explore how these algorithms result in similar, yet specific layouts.

//ST: !
[start=6]
6. In this tutorial, we defined degree centrality.
Can you imagine a situation when a node with the largest degree centrality will actually be in the periphery of the network? You can draw a toy network to help you figure.
