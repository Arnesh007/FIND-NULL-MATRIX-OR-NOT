# FIND-NULL-MATRIX-OR-NOT
Write a program to find whether the given matrix is null or not with using functions.

A NULL matrix is a matrix in which all its elements are zero, NOT NULL otherwise.

Function specifications for the function details:

The first argument corresponds to the number of elements in the array.

The second argument corresponds to the pointer to an array.

The function returns a value of 1 if it is a null matrix and 0 otherwise.

Input and Output Format:

Assume that the maximum number of rows and columns in the matrix is 10.

Refer sample input and output for formatting specifications.
Sample Input

3

3

2 5 0

0 0 0


0 0 7

Sample Output


The matrix is
2 5 0 
0 0 0 
0 0 7 
The matrix is NOT NULL


ANSWER:

#include<iostream>
using namespace std;
int nul(int r, int c)
{
    int i,j,val;
    
    int a[r][c];
    for(i=0;i<r;i++)
    {
        for(j=0;j<c;j++)
        {
            cin>>a[i][j];
        
        }
    }
    cout<<"The matrix is"<<endl;
     for(i=0;i<r;i++)
    {
        for(j=0;j<c;j++)
        {
            cout<<a[i][j]<<" ";
        
        }cout<<endl;
    }
    for(i=0;i<r;i++)
    {
        for(j=0;j<c;j++)
        {
             val=1;
            if(a[i][j]==0)
            {
                val=0;
            }
        }
    }
    
    if(val==0)
     {
         cout<<"The matrix is NULL";
     }
    else
     {
         cout<<"The matrix is NOT NULL";
     }
    
    // return 0;  
}


int main()
{
    int i,j,r,c;
    cin>>r>>c;
    int a[r][c];
    nul(r,c);
    return 0;
}
   
