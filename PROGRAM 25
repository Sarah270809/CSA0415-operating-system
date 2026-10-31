#include <stdio.h>
#include <fcntl.h>
#include <unistd.h>
#include <sys/stat.h>
#include <dirent.h>

int main()
{
    int fd;
    struct stat st;
    DIR *dir;
    struct dirent *entry;

    printf("UNIX I/O System Calls\n");

    fd = open("/dev/null", O_RDONLY);

    if (fd == -1)
    {
        perror("File opening failed");
        return 1;
    }

    printf("File opened successfully.\n");

    int flags = fcntl(fd, F_GETFL);

    if (flags != -1)
        printf("fcntl: File flags = %d\n", flags);

    if (lseek(fd, 0, SEEK_SET) == -1)
        printf("lseek: Operation not supported.\n");
    else
        printf("lseek: Successful.\n");

    if (stat("/dev/null", &st) == 0)
        printf("stat: File information retrieved.\n");
    else
        printf("stat failed.\n");

    close(fd);

    dir = opendir("/");

    if (dir == NULL)
    {
        perror("opendir failed");
        return 1;
    }

    printf("\nDirectory contents:\n");

    while ((entry = readdir(dir)) != NULL)
        printf("%s\n", entry->d_name);

    closedir(dir);

    printf("\nDirectory closed successfully.\n");

    return 0;
}
