

class Solution {
    // Function to return a list containing the DFS traversal of the graph.
    public ArrayList<Integer> dfsOfGraph(int V, ArrayList<ArrayList<Integer>> adj) 
    {
        ArrayList<Integer>z=new ArrayList<Integer>();
        Boolean status[]=new Boolean[V];
        Stack<Integer> s=new Stack<>();
        
        Arrays.fill(status,false);
        s.add(0);
        
        while(!s.isEmpty())
        {
            // int a=s.peek();
            if(status[s.peek()]==false)
            {
            z.add(s.peek());
            status[s.peek()]=true;
            }
            int a=s.pop();
            for(int i=adj.get(a).size()-1;i>=0;i--)
            {
                if(status[adj.get(a).get(i)]==false)
                {
                    s.add(adj.get(a).get(i));
                }
            }
        }
        return z;
    }
}
