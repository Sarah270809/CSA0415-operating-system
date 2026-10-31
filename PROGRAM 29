#include <stdio.h>

int mutex = 1;
int full = 0;
int empty = 1;
int item = 0;

void wait(int *s)
{
    (*s)--;
}

void signal(int *s)
{
    (*s)++;
}

void producer()
{
    wait(&empty);
    wait(&mutex);

    item++;
    printf("Producer produced item %d\n", item);

    signal(&mutex);
    signal(&full);
}

void consumer()
{
    wait(&full);
    wait(&mutex);

    printf("Consumer consumed item %d\n", item);
    item--;

    signal(&mutex);
    signal(&empty);
}

int main()
{
    printf("Producer-Consumer Problem\n\n");

    producer();
    consumer();

    producer();
    consumer();

    printf("\nSynchronization completed.\n");

    return 0;
}
