# DFS
# geeks for geeks dfs implementation
class Solution:
    
    #Function to return a list containing the DFS traversal of the graph.
    def dfsOfGraph(self, V, adj):
        l=adj
        n=len(l)
        # visited array to maintain visited nodes to don't visit again
        vis=[0]*n
        #first node always be visited
        vis[0]=1
        l=[0]
        def dfs(i):
            for j in l[i]:
                if not vis[j]:
                #only visit if it is not visited
                    vis[j]=1
                    o.append(j)
                    dfs(j)
        # dfs call from first node            
        dfs(0)
        return o

