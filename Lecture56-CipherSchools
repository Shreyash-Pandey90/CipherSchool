//-------------------------------------DELETION IN HEAP------------------------------------------

class Heap{
    final int capacity=20;
    static int arr[]=new int[20];
    static int no=0;


    public static void add(int x)
    {
            arr[no++]=x;
            Minheapify();
        
    }

    public static void Minheapify()
    {
        int i=no-1;
        while(i>0 && arr[i]<arr[(i-1)/2])
        {
            int temp=arr[(i-1)/2];
            arr[(i-1)/2]=arr[i];
            arr[i]= temp; 
            i=(i-1)/2; 
        }
    }

    static boolean isEmpty()
    {
        return no==0;
    }

    static int peek()
    {
        if(!isEmpty())
        return arr[0];
        else return -1;
    }


    public static void printL()
    {

        for(int i=0;i<no;i++)
        {
            System.out.print(arr[i]+" ");
            
        }
        System.out.println();
    }

//-----------------------METHOD TO DELETE THE ITEMS FROM THE HEAP-------------------------
    static int poll()
    {
        int del=arr[0];
        arr[0]=arr[no-1];
        no--;
        heapifyDown();
        return del;
    }


    static void heapifyDown()
    {
        int i=0;
        while(2*i+1<=no)
        {
            int min=2*i+1;
            if(2*i+2<=no && arr[2*i+2]<arr[min])min=2*i+2;
            if(arr[min]<arr[i])
            {
                int temp=arr[i];
                arr[i]=arr[min];
                arr[min]=temp;
                i=min;
            }
            else break;
            
        }
    }
}

public class Lecture56
{
    public static void main(String args[])
    {
        Heap a=new Heap();
        System.out.println(a.isEmpty());
        a.add(60);
        a.add(40);
        a.add(70);
        a.add(10);
        a.add(50);
        a.add(40);
        a.add(20);
        a.add(30);
        a.add(60);
        System.out.println(a.isEmpty());
        System.out.println(a.peek());
        a.printL();
        a.add(8);
        System.out.println(a.peek());
        a.printL();
        System.out.println(a.poll());
        a.printL();
        System.out.println(a.poll());
        a.printL();
    }
}
