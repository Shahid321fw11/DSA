The Celebrity Problem
In this question, we are given a list of [n] people, and each person is either a celebrity or not a celebrity.
Matrix will be the question.

My approach is to first eliminate the number of people who are not celebrities.
Then, we can find the celebrity by checking if the celebrity is the only person who is present in the matrix.

// { Driver Code Starts
//Initial Template for Java

import java.io._;
import java.util._;

class GFG{
public static void main(String args[]) throws IOException {
Scanner sc = new Scanner(System.in);
int t = sc.nextInt();
while(t>0)
{
int N = sc.nextInt();
int M[][] = new int[N][n];
for(int i=0; i<N; i++)
{
for(int j=0; j<N; j++)
{
M[i][j] = sc.nextInt();
}
}
System.out.println(new Solution().celebrity(M,N));
t--;
}
}
} // } Driver Code Ends

//User function Template for Java

class Solution
{
//Function to find if there is a celebrity in the party or not.
int celebrity(int m[][], int n)
{
// code here
Stack<Integer> myStack = new Stack<Integer>();
for(int i=0;i<n;i++){
myStack.push(i);
}
while(myStack.size()>=2){
int i = myStack.pop();
int j = myStack.pop();
if(m[i][j]==1) myStack.push(j);
else myStack.push(i);
}
int pot = myStack.pop();
for(int i=0;i<n;i++){
if(i!=pot){
if(m[i][pot]==0 || m[pot][i]==1) return -1;
}
}
return pot;
}
}
