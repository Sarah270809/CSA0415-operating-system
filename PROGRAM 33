
#include <stdio.h>

int main()
{
    int n, f, pages[50], frames[10], time[10];
    int i, j, pos, faults = 0, hits = 0, found, t = 0;

    printf("Enter number of pages: ");
    scanf("%d", &n);

    printf("Enter page reference string: ");
    for (i = 0; i < n; i++)
        scanf("%d", &pages[i]);

    printf("Enter number of frames: ");
    scanf("%d", &f);

    for (i = 0; i < f; i++)
    {
        frames[i] = -1;
        time[i] = 0;
    }

    for (i = 0; i < n; i++)
    {
        found = 0;
        t++;

        for (j = 0; j < f; j++)
        {
            if (frames[j] == pages[i])
            {
                found = 1;
                time[j] = t;
                hits++;
                break;
            }
        }

        if (!found)
        {
            pos = 0;

            for (j = 1; j < f; j++)
            {
                if (frames[j] == -1 ||
                    (frames[pos] != -1 && time[j] < time[pos]))
                    pos = j;
            }

            frames[pos] = pages[i];
            time[pos] = t;
            faults++;
        }
    }

    printf("Total Page Faults = %d\n", faults);
    printf("Total Page Hits = %d\n", hits);

    return 0;
}
