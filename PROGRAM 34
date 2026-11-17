
#include <stdio.h>

int main()
{
    int n, f, pages[50], frames[10];
    int i, j, k, pos, faults = 0, hits = 0;
    int found, farthest, next;

    printf("Enter number of pages: ");
    scanf("%d", &n);

    printf("Enter page reference string: ");
    for (i = 0; i < n; i++)
        scanf("%d", &pages[i]);

    printf("Enter number of frames: ");
    scanf("%d", &f);

    for (i = 0; i < f; i++)
        frames[i] = -1;

    for (i = 0; i < n; i++)
    {
        found = 0;

        for (j = 0; j < f; j++)
        {
            if (frames[j] == pages[i])
            {
                found = 1;
                hits++;
                break;
            }
        }

        if (!found)
        {
            pos = -1;
            farthest = -1;

            for (j = 0; j < f; j++)
            {
                if (frames[j] == -1)
                {
                    pos = j;
                    break;
                }

                next = n + 1;

                for (k = i + 1; k < n; k++)
                {
                    if (pages[k] == frames[j])
                    {
                        next = k;
                        break;
                    }
                }

                if (next > farthest)
                {
                    farthest = next;
                    pos = j;
                }
            }

            frames[pos] = pages[i];
            faults++;
        }
    }

    printf("Total Page Faults = %d\n", faults);
    printf("Total Page Hits = %d\n", hits);

    return 0;
}
