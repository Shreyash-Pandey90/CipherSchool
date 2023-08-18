//          ------------DJKSTHRA ALGORITHM----------


import java.util.*;

public class Lecture61 
{
    public static void main(String args[])
    {
    Scanner sc=new Scanner(System.in);
    System.out.println("Enter the number of vertices");
    int v=sc.nextInt();
    int arr[][]=new int[v][v];
    System.out.println("Enter the no of edges");
    int e=sc.nextInt();
    for(int i=0;i<e;i++)
    {
        int a=sc.nextInt();
        int b=sc.nextInt();
        int c=sc.nextInt();

        arr[a][b]=c;
        arr[b][a]=c;
    }

    // for(int i=0;i<v;i++)
    // {
    // for(int j=0;j<v;j++)
    // {

    //     System.out.print(arr[i][j]+" ");
    // }
    // System.out.println();
    // }

    Dijkstra(arr,0);
    }


    static void Dijkstra(int arr[][],int source)
    {
        int v=arr.length;
        boolean visited[]=new boolean[v];
        Arrays.fill(visited,false);
        int path[]=new int[v];
        Arrays.fill(path,Integer.MAX_VALUE);
        path[source]=0;
        for(int i=0;i<v-1;i++)
        {
                int minvertex=min(path,visited);
                visited[minvertex]=true;
                for(int j=0;j<v;j++)
                {
                    if(arr[minvertex][j]!=0 && visited[j]==false)
                    {
                        int newpath=path[minvertex]+arr[minvertex][j];
                        if(newpath<path[j])
                        path[j]=newpath;
                    }
                }
        }

        System.out.println("Shortest paths are: ");
        for(int i=0;i<path.length;i++)
        {
            System.out.print(path[i]+" ");
        }
    }


    //this minvertex is to select the minimum net nearest node for visit as we know it is greedy algorithm
    static int min(int path[],boolean visited[])
    {
        int minindex=-1;
        for(int i=0;i<path.length;i++)
        {
            if(visited[i]!=true &&( minindex==-1 || path[minindex]>path[i]))
            {
                minindex=i;
            }
        }
        return minindex;
    }
}

/*
 * Dijkstra's algorithm provide us the 
 * single-source-shortest path
 * means from node a(source)  to evry other node
 */
