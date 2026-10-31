#include <stdio.h>
#include <string.h>

int main()
{
    char filename[50] = "sample.txt";
    char data[100] = "UNIX File Management System Calls";
    char buffer[100];

    FILE *fp;

    printf("File Management Demonstration\n");

    fp = tmpfile();

    if (fp == NULL)
    {
        printf("File creation failed.\n");
        return 1;
    }

    printf("File created successfully.\n");

    if (fwrite(data, 1, strlen(data), fp) != strlen(data))
    {
        printf("Write failed.\n");
        fclose(fp);
        return 1;
    }

    printf("Data written successfully.\n");

    rewind(fp);

    if (fread(buffer, 1, sizeof(buffer) - 1, fp) == 0)
    {
        printf("Read failed.\n");
        fclose(fp);
        return 1;
    }

    buffer[strlen(data)] = '\0';

    printf("File contents: %s\n", buffer);

    fclose(fp);

    printf("File closed successfully.\n");

    return 0;
}
