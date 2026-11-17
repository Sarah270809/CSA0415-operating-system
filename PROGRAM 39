
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int req[50], n, head, i, j, total = 0;
    int temp, size = 200;

    printf("Enter number of requests: ");
    scanf("%d", &n);

    printf("Enter request sequence: ");
    for (i = 0; i < n; i++)
        scanf("%d", &req[i]);

    printf("Enter initial head position: ");
    scanf("%d", &head);

    for (i = 0; i < n - 1; i++)
    {
        for (j = 0; j < n - i - 1; j++)
        {
            if (req[j] > req[j + 1])
            {
                temp = req[j];
                req[j] = req[j + 1];
                req[j + 1] = temp;
            }
        }
    }

    printf("Seek sequence: %d ", head);

    for (i = 0; i < n; i++)
    {
        if (req[i] >= head)
        {
            total += abs(head - req[i]);
            head = req[i];
            printf("-> %d ", head);
        }
    }

    total += abs(head - (size - 1));
    head = size - 1;
    printf("-> %d ", head);

    for (i = n - 1; i >= 0; i--)
    {
        if (req[i] < head && req[i] < (size - 1))
        {
            total += abs(head - req[i]);
            head = req[i];
            printf("-> %d ", head);
        }
    }

    printf("-> 0");
    total += head;

    printf("\nTotal seek operations = %d\n", total);

    return 0;
}
