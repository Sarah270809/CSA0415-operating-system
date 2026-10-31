#include <stdio.h>
#include <string.h>

int main()
{
    FILE *fp;
    char buffer[100];

    fp = tmpfile();

    if (fp == NULL)
    {
        printf("File creation failed.\n");
        return 1;
    }

    printf("File created successfully.\n");

    fprintf(fp, "Operating System File Management");

    printf("Data written successfully.\n");

    rewind(fp);

    fgets(buffer, sizeof(buffer), fp);

    printf("File contents: %s\n", buffer);

    fseek(fp, 0, SEEK_END);

    fprintf(fp, " - C Programming");

    printf("Data appended successfully.\n");

    rewind(fp);

    fgets(buffer, sizeof(buffer), fp);

    printf("Updated contents: %s\n", buffer);

    fclose(fp);

    printf("File closed successfully.\n");

    return 0;
}
