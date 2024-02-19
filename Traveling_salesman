from sys import maxsize 
from itertools import permutations
V = 4 #Represents the number of vertices (cities) in the graph 
def travellingSalesmanProblem(graph, s): 
# Function takes graph as a 2D matrix and a starting vertex (s)
#The function returns the minimum cost to travel the whole graph from the starting vertex to the starting vertex 
    vertex = []
    for i in range(V): 
        if i != s: 
            vertex.append(i)  #stores all vertex except the starting vertex 
    min_path = maxsize 
    next_permutation=permutations(vertex) #calculates all permutations of that vertex 
    for i in next_permutation: 
        current_pathweight = 0
        k = s 
        for j in i: 
            current_pathweight += graph[k][j] 
            k = j 
        current_pathweight += graph[k][s] 
        min_path = min(min_path, current_pathweight) #updates the mimimum cost when it finds a smaller cost
         
    return min_path #reurns the mimimum path needed to do the whole loop from starting vertex
 
if __name__ == "__main__": 
 
    # matrix representation of graph 
    graph = [[0, 10, 15, 20], [10, 0, 35, 25], 
            [15, 35, 0, 30], [20, 25, 30, 0]] 
    s = 0
    print(travellingSalesmanProblem(graph, s))
