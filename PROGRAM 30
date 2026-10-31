#include <stdio.h>
#include <pthread.h>

pthread_t thread1, thread2;

void *function1(void *arg)
{
    printf("Thread 1 is running.\n");

    pthread_exit(NULL);
}

void *function2(void *arg)
{
    printf("Thread 2 is running.\n");

    return NULL;
}

int main()
{
    pthread_create(&thread1, NULL, function1, NULL);
    pthread_create(&thread2, NULL, function2, NULL);

    printf("Threads created successfully.\n");

    if (pthread_equal(thread1, thread2))
        printf("Both threads are equal.\n");
    else
        printf("Both threads are not equal.\n");

    pthread_join(thread1, NULL);
    pthread_join(thread2, NULL);

    printf("Threads joined successfully.\n");

    printf("Thread execution completed.\n");

    return 0;
}
