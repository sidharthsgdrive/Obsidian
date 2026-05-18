# Bubble Sort

```C
#include <stdio.h>
int main(void)
{
    int n = 5, temp, arr[5] = {4,1,7,6,2};
    for (int i = 0; i < n-1; i++)
    {
        for (int j = 0; j < n-i-1; j++)
        {
            if (arr[j] > arr[j+1])
            {
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
    printf("Sorted array: ");
    for (int k = 0; k < n; k++)
    {
        printf("%d ", arr[k]);
    }
    printf("\n");
}
```
*******
# `Strings`
* When declaring character arrays, we must allow one extra element space for the null terminator \0.
* type conversion from str to int: `x = character - '0';`  
*******
# String formatting
* `scanf("%ws", arrname);` => reads characters till maximum field width w is reached
* `printf("%10.4s", samplestr);` => prints first 4 characters in a field width of 10
* `printf("%-10.4s", samplestr);` => prints above, but left-justified
******
# String functions
* `gets(line);` or `scanf("%[^\n]", line);` => reads multiple words
* `puts(line);` => prints string
* `strcat(string1, string2);` => concatenates string2 to string1, leaving string2 unchanged (basically removes the null character from the end of string1 and places string2 there)
*  `strncat(string1, string2, n);` => concatenates first n characters of string2 to string1
* `strcmp(string1, string2);` => if strings equal, returns 0; else returns numeric difference between first nonmatching chars (ASCII(string1) - ASCII(string2))
* `strncmp(string1, string2, n);` => compares first n chars of string1 and string2
* `strcpy(destination, source);` => assigns contents of string2 to string1
* `strstr(string, substring);` => if string2 in string1, returns position of first occurrence; otherwise returns NULL pointer 
* `strchr(string1, 'm')`; => returns first occurrence of 'm' in string1
* `strrchr(string1, 'm');` => returns last occurrence of 'm' in string1
