<!-- the link of the question  -->

https://practice.geeksforgeeks.org/problems/implement-two-stacks-in-an-array/1

In this question,
Your task is to implement 2 stacks in one array efficiently.
In this example we will implement two stack using one array.

Your Task:
You don't need to read input or print anything. You are required to complete the 4 methods push1, push2 which takes one argument an integer 'x' to be pushed into stack one and two and pop1, pop2 which returns the integer poped out from stack one and two. If no integer is present in the array return -1.
Expected Time Complexity: O(1) for all the four methods.
Expected Auxiliary Space: O(1) for all the four methods

<!-- Explanation -->

<!-- Ans  -->

/\* Structure of the class is
class TwoStack
{

    int size;
    int top1,top2;
    int arr[] = new int[100];

    TwoStack()
    {
    	size = 100;
    	top1 = -1;
    	top2 = size;
    }

}\*/

class Stacks
{
//Function to push an integer into the stack1.
void push1(int x, TwoStack sq)
{
if(sq.top1+1<sq.top2){
sq.top1++;
sq.arr[sq.top1] = x;
}

    }

    //Function to push an integer into the stack2.
    void push2(int x, TwoStack sq)
    {
        if(sq.top2-1>sq.top1){
            sq.top2--;
            sq.arr[sq.top2] = x;
        }

    }

    //Function to remove an element from top of the stack1.
    int pop1(TwoStack sq)
    {
        if(sq.top1>=0){
            int x = sq.arr[sq.top1];
            sq.top1--;
            return x;
        }
        return -1;

    }

    //Function to remove an element from top of the stack2.
    int pop2(TwoStack sq)
    {
        if(sq.top2<sq.size){
            int x = sq.arr[sq.top2];
            sq.top2++;
            return x;
        }
        return -1;
    }

}
