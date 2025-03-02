/*
Given an integer array Array, calculate the sum of elements within each specified interval.

Input Description
The first line contains an integer n, representing the length of the array Array.
The next n lines each contain one integer, representing the elements of the array.
Following this, each subsequent line contains two integers a and b (b ≥ a), specifying the indices of the interval.
The input continues until the end of the file.

Output Description
For each specified interval, output the sum of elements within that range.

Input Example
5
1
2
3
4
5
0 1
1 3

Output Example
3
9

Constraints:
0 < n <= 100000
*/

/*
Solution 1
*/

#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[])
{
    int num;
    scanf("%d", &num);

    int *a = (int *)malloc((num + 1) * sizeof(int));

    // Initialize the prefix and the first element of the array to 0
    a[0] = 0;

    // Read array elements and compute prefix sums
    for (int i = 1; i <= num; i++)
    {
        int mm;
        scanf("%d", &mm);
        // Accumulate prefix sums
        a[i] = a[i - 1] + mm;
    }

    int m, n;
    // Loop through the intervals and calculate the sum of the intervals 
    // until the end of the input.
    // scanf() returns the number of successful matches and assignments, 
    // or EOF if it reaches the end of the file.
    while (scanf("%d%d", &m, &n) == 2)
    {
        // Output the interval sum, noting that the interval is left-closed and right-open, 
        // so a[n+1] is the prefix sum of the elements containing n
        printf("%d\n", a[n+1] - a[m]);
    }

    free(a);
    return 0;
}
