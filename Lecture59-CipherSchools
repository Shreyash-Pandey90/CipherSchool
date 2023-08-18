

class Solution {
    // Function to return Breadth First Traversal of given graph.
    public ArrayList<Integer> bfsOfGraph(int V, ArrayList<ArrayList<Integer>> adj) 
    {
       ArrayList<Integer>a=new ArrayList<>();
       Queue<Integer> q=new LinkedList<Integer>();
       Boolean status[]=new Boolean[V];
       Arrays.fill(status,false);
       
       q.add(0);
       
       
       while(!q.isEmpty())
       {
           int u=q.peek();
           for(int i=0;i<adj.get(u).size();i++)
           {
               if(status[adj.get(u).get(i)]==false)
               q.add(adj.get(u).get(i));
           }
           int b=q.remove();
           if(status[b]==false)
           {
               a.add(b);
               status[b]=true;
           }
       }
       
       return a;
    }
}
