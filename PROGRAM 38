
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n, req[50], head, i, total = 0;

    printf("Enter number of requests: ");
    scanf("%d", &n);

    printf("Enter request sequence: ");
    for (i = 0; i < n; i++)
        scanf("%d", &req[i]);

    printf("Enter initial head position: ");
    scanf("%d", &head);

    printf("Seek sequence: %d ", head);

    for (i = 0; i < n; i++)
    {
        total += abs(head - req[i]);
        head = req[i];
        printf("-> %d ", head);
    }

    printf("\nTotal seek operations = %d\n", total);

    return 0;
}
