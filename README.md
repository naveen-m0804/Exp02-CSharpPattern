# Exp02-CSharpPattern

## Aim:
To write a C# program for a pascal's triangle. 
## Algorithm:

### Step1:
Begin by prompting the user to enter the number of rows for the pattern.

### Step2:
Read the input from the user and store it in a variable row. Initialize loop variables i and j to iterate over rows and columns respectively. Also, initialize variable c to hold the value of each element in the pattern.

### Step3:
Start a loop to iterate over each row (`i`), and within this loop, start another loop to print spaces before each element in the row. Inside the inner loop, print spaces based on the row number (`row - i`). Then, start another loop (`j`) to calculate and print the elements of the pattern for the current row.


### Step4:
Within the innermost loop, calculate the value of each element using the binomial coefficient formula (n choose k), where `n` is the row number and `k` is the column number. For each element, if `j` is 0 or equal to `i`, set `c` to 1, otherwise, update `c` by multiplying it with `(i - j + 1) / j`.

### Step5:
Inside the innermost loop, after calculating the value of `c`, print it followed by a space.

## Program:
```
using System;
public class Pattern
{
    public static void Main()
    {
        int row;
        row=Convert.ToInt32(Console.ReadLine("Enter the number of rows: "));
        for (int i=0;i<row;i++)
        {
            for (int s=0;s<row-i;s++)
                Console.Write(" ");
                for (int j=0;j<=i;j++)
                {
                    if (i==0 || j==0)
                        c=1;
                    else
                        c=c*(i-j+1)/j;
                        Console.WriteLine(c+" ");
                }
        }
    }
}
```
## Output:
![Screenshot 2024-02-24 104229](https://github.com/naveen-m0804/Exp02-CSharpPattern/assets/117974950/8bdfba05-7abb-43d9-a1e7-a98bd06ccfea)


## Result:
Thus the above C# program for pascal's triangle is successfully executed
