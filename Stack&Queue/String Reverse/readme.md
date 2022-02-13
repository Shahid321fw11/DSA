Reverse a string using Stack
We are putting the characters of the string in a stack. Then we are popping the characters from the stack and printing them, as simple as that.

We can do the same with the help of inbuilt method of java or using an arraylist of character.

Question:
You are given a string S, the task is to reverse the string using stack.

Example 1:

Input: S="GeeksforGeeks"
Output: skeeGrofskeeG

Your Task:
You don't need to read input or print anything. Your task is to complete the function reverse() which takes the string S as an input parameter and returns the reversed string.

class Solution {

    public String reverse(String S){
        //code here
        String input = S;
        String str = "";
        Stack <Character> myStack = new Stack<Character>();
        for(int i=0;i<input.length();i++){
            char ele = input.charAt(i);
            myStack.push(ele);
        }
        while(myStack.size()>0){
            str+=myStack.pop();
        }
        return str;
    }

}
