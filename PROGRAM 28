#include <stdio.h>
#include <string.h>

int main()
{
    char text[200];
    char pattern[50];

    printf("Enter a line of text:\n");
    fgets(text, sizeof(text), stdin);

    printf("Enter the word to search: ");
    scanf("%49s", pattern);

    if (strstr(text, pattern) != NULL)
    {
        printf("\nPattern found!\n");
        printf("Matching line: %s", text);
    }
    else
    {
        printf("\nPattern not found.\n");
    }

    return 0;
}
