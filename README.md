# BREADTH FIRST SEARCH

<a href="https://github.com/learn-co-curriculum/bfs/">review of Learn readme and lab</a>

# POP QUIZ

## which of these is a graph?

A) Linked list<br>
B) Tree<br>
C) Pairwise connections between items<br>
D) Subway map<br>
E) A collection of points where one item is connected to another item.<br>

<br>


A graph is made up of vertices and edges:



## Vertices (points):
[
	 {name: '34th&6th', distance: null, predecessor: null},
	 {name: '23rd&6th', distance: null, predecessor: null},
	 {name: '28th&Bwy', distance: null, predecessor: null},
	 {name: '14th&6th', distance: null, predecessor: null},
	 {name: '23rd&Bwy', distance: null, predecessor: null},
	 {name: '14th&Lex', distance: null, predecessor: null},
	 {name: '23rd&Lex', distance: null, predecessor: null}
]

## Edges (lines between points):

[
	['14th&6th', '23rd&6th'],
	['23rd&6th', '34th&6th'],
	['34th&6th', '28th&Bwy'],
	['28th&Bwy', '23rd&Bwy'],
	['23rd&Bwy', '14th&Lex'],
	['14th&Lex', '23rd&Lex']
]

<br>

<a href="https://docs.google.com/a/flatironschool.com/drawings/d/1t_ZeW7pAWtMtcPd8hu-HOttN2Plbk7mulnAzGeAVilE/edit?usp=sharing">Visual example</a>


<br>


component: subset of connected vertices. 



<br>


breadth first search is a way of exploring the connectivity of a graph.


<br>


## What do we want a BFS function to do?


	1. Starting with a vertex, we first find all adjacent vertices.
	2. A vertex is ‘visited’ if we have encountered it in our search. Each time we visit a vertex, we place it in a queue.
	3. We use ‘first in first out’ approach to decide with vertex to make our next starting point. For each vertex, we want to track its predecessor and distance from the root node.
	4. A vertex is ‘explored’ if we have visited all of its adjacent vertices.
	5. Once we have explored all vertices, we return an array of all discovered vertices.





## pseudocode BFS: 

	function bfs(rootnode, edges, vertices){
	

	}





## pseudocode:
	rootNode = vertices[0]
	queue = []
	addVertexToQueue(rootNode)
	while(queue.length !== 0) {
		let firstNode = queue.shift()
	adjacentVertices = findAdjacent(firstNode)
		for vertex in adjacentVertices {
			markDistanceAndPredecessor(vertex)
			addToQueue(vertex)
		}
	}
  
  <a href="https://repl.it/I73Y/3">my solution</a> 

