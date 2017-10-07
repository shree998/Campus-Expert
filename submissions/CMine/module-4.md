# Geo-Spatial Data Clustering Workshop Outline

Purpose: Walk through how to reduce the size of a spatial data set: Latitude & Longitude Coordinates for the infamous Sidney Atanas's vehicles.

Audience: Agents (i.e. participants in the CS adventure game) who are seeking additional assistance in:
* determining what algorithm to use to reduce the data set
* creating a visualization from the data for the debriefing
* watching a coding example

### Background Knowledge
What is clustering? 
* [Clustering Wiki] (https://en.wikipedia.org/wiki/Cluster_analysis)
* "Cluster analysis groups data objects based only on information found in the data that describes the objects and their relationships. The goal is that the objects within a group be similar (or related) to one another and different from (or unrelated to) the objects in other groups. The greater the similarity (or homogeneity) within a group and the greater the difference between groups, the better or more distinct the clustering." ~ Cluster Analysis: Basic Concepts and Algorithms (Chapter 8)

### Learning Goals
At the end of the workshops agents should walk away feeling they have a firm understanding of:
* what clustering algorithm they should employ to complete the mission
* why some clustering methods work better than others for this mission
* how to use simple information from a data set to tell a larger picture through visualizations
* how to indepedently foster a sense of community by connecting with (via FB Messenger, text, etc) other participants who the agents may want to working with on future coding assginments
  * not only will this help the agent complete the game but it also ensures that they know more people in the RPI community on a more personal level

## Workshop Outline

### Demonstrate A Complete Debriefing 
The first five to ten minutes will be spent informing the agents about what a strong debriefing might look like. The debriefing will most likely be a detailed README detailing the implementation steps taken to achieve the end goal: extracting the warehouse locations from nothing more than the latitude and longitude coordinates of various vehicles. Given that the debriefing should be a creative outlet, I will encourage the agents to put their own spin on the report but offer what I have as a stepping stone to something greater.

* Once I complete the assignment myself, I will link to the debriefing report I made.

### Re-Introduction To The Mission
1. "Agent for your first assignment we need you to preform cluster analysis on the car log data to divide the data into groups (clusters) that are meaningful and useful in the search for the locations of the warehouses which the agency believes are being used to house illegal goods."

2. Ask the agents if there are any questions about what it is we are trying to accomplish in the assignment. If there are none, move to the next step.

3. Invite agents to download the data set if they have not already done so
	* Explain that we are asking ourselves: How we can reduce the size of the data set down to smaller set of spatially representative points?
	* Why do we want to do this? This makes the data set more manageable in that we have provided some contextual meaning to only the data points that actually matter given their ability to cover a large amount of variance in the data.
	* Show plot of the full data set a scale where only a couple dozen of the data points can be see anyway 

4. Invite agents to open the editor of their choice (the workshop itself will be in either Python or R)

### Let's Figure Out How To Cluster!
1. Briefly talk about the most popular clustering algorithm: k-means

2. Highlight why k-means doesn't work very well in this situations
	* k-means specializes in minimizing variance, but what we need to minimize is geodetic distance
	* k-means also requires that we know how many clusters we desire the algorithm to create before hand (we don't have this information because we are trying to figure out how many warehouses Atanas even has.)
	* k-means will result in over-representation because the initial random selection used to seed the algorithm would select overlaps in the data set (which as the car staying in one place for a long time) multiple times

3. So what works well for clustering arbitrary distances: DBSCAN
	* DBSCAN clusters spatial data based on density and it only needs two parameters: a max distance between points and a minimum clustering size.
	* In regards the max distance - if two places are 30 miles apart then we know they are not the same place so we pass in this "common sense" so the algorithm can mathematically represent that
	* Talk about the steps in DBSCAN in detail (there are 8) | [DBSCAN Wiki](https://en.wikipedia.org/wiki/DBSCAN#Algorithm)
4. Questions - If not then move on to the next section

### Break time

### Let's Get Clustering!!!!
A pre-made repo will already exist for this workshop, so the following will be broken into the different branches available on the repo

Branch 1:

	* Import the required Python / R modules && Load the full data set in
	* Convert the parts of the data set we need (latitude and longitude) into arrays (Python) and tiny tables (R)

Branch 2:

	* Select appropriate epsilon values for our data set (DISCUSS IN PAIRS WHAT VALUES WOULD BE BEST)
	* Compute DBSCAN (pre-existing implementations exist for both)
	* Show the number of clusters DBSCAN found
	* Ask agents what they think each of these clusters represents? (SHOULD BE REVIEW FROM ASSIGNMENT RE-INTRODUCTION)
	* Yaayyyy! We have already done most of the assignment in that we understand the algorithms and can tell the agency exactly how many warehouses there are within this data set

BREAK TIME

Branch 3:

	* Begin working on the visualization of the data
		** Take the point right in the center of the cluster (understanding clusters can be irregularly shaped)
		** Plot the reduced set of data points. For the labels we will reverse geocode so that we have the city and country showing for each cluster
		** Plot a bar graph and shared gradient map of each of the clusters per city and/or state so we can see which warehouses were visited the most
		** Ask for what other types of visualizations might be an interesting way to showcase these findings

### The Workshop Is Over...Now What?
In an ideal world this workshop will be open to the entire RPI community and not just those who are already agents participating in the adventure. Thus said there would be a small call to action inviting those interested to join our little community (and other RPI CS communities). Finally, I would encourage agents to keep in contact with other agents should they have more questions moving forward. Oh...and the screen recording of the workshop would be main available should anyone need it.
