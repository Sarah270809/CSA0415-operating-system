
#include <stdio.h>

int main()
{
    int index[50], n, i, record;

    printf("Enter number of records: ");
    scanf("%d", &n);

    printf("Enter block numbers:\n");
    for (i = 0; i < n; i++)
        scanf("%d", &index[i]);

    printf("Enter record position to access: ");
    scanf("%d", &record);

    if (record < 1 || record > n)
    {
        printf("Invalid record position\n");
        return 0;
    }

    printf("Index Block contains:\n");

    for (i = 0; i < n; i++)
        printf("Entry %d = %d\n", i + 1, index[i]);

    printf("Record %d is stored in block %d\n",
           record, index[record - 1]);

    return 0;
}
