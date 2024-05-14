Checking If Two Strings are Anagram or Not
In this article we will learn how to code a C program to check if two strings are anagram or not. Two strings are said to be anagram if they contains same characters, only the order of characters is different. Therefore, in both strings, the frequency of each letter must be the same. For example, strings ‘listen’ and ‘silent’ are anagrams. We will count the frequencies of both the string and if the frequencies matches then strings entered are anagram.

Checking if two strings are anagram or not in C
Algorithm:
Initialize the variables.
Accept the inputs.
Calculate frequencies of both the strings.
If frequencies does not match set flag =1.
If flag= 0, string are anagram else they are not.
Print result.
C programming code to check if two strings are anagram or not
#include<stdio.h> 
int main()
{
    //Initializing variables.
    char str1[100]="prep",str2[100]="perp";
    int first[26]={0}, second[26]={0}, c=0, flag=0;
    
    //Calculating frequencies of characters in first string.
    while(str1[c] != '\0')
    {
        first[str1[c]-'a']++;
        c++;
    }
     
    c=0;
    //Calculating frequencies of characters in second string. 
    while(str2[c] != '\0')
    {
        second[str2[c]-'a']++;
        c++;
    }
    //Checking if frequencies of both the strings are same or not.
    for(c=0;c<26;c++)
    {
        if(first[c] != second[c])
            flag=1;
    }
    //Priting result.
    if(flag == 0)
    {
        printf("\n%s and %s are Anagram Strings.",str1,str2);
    }
    else
    {
        printf("\n%s and %s are not Anagram Strings.",str1,str2);
    }
    return 0;
  
}
Output
prep and perp are Anagram Strings.
