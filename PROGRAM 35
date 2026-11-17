
#include <stdio.h>

int main()
{
    int n, blocks[50], i, record;

    printf("Enter number of records: ");
    scanf("%d", &n);

    printf("Enter block numbers:\n");
    for (i = 0; i < n; i++)
        scanf("%d", &blocks[i]);

    printf("Enter record position to access: ");
    scanf("%d", &record);

    if (record < 1 || record > n)
    {
        printf("Invalid record position\n");
        return 0;
    }

    printf("Sequentially allocated blocks: ");
    for (i = 0; i < n; i++)
        printf("%d ", blocks[i]);

    printf("\nAccessing record %d\n", record);
    printf("Blocks read: ");

    for (i = 0; i < record; i++)
        printf("%d ", blocks[i]);

    printf("\nRecord found in block %d\n", blocks[record - 1]);

    return 0;
}
