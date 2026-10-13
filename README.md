1.Hollow Diamond Pattern
**Code:**

```c
#include <stdio.h>

int main() {
    int n = 4, i, j;

    for (i = 1; i <= n; i++) {
        for (j = i; j < n; j++)
            printf("  ");

        for (j = 1; j <= 2 * i - 1; j++) {
            if (j == 1 || j == 2 * i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    for (i = n - 1; i >= 1; i--) {
        for (j = n; j > i; j--)
            printf("  ");

        for (j = 1; j <= 2 * i - 1; j++) {
            if (j == 1 || j == 2 * i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```

**Output:**

```text
      *
    *   *
  *       *
*           *
  *       *
    *   *
      *
2.Hourglass Pattern
**Code:**

```c
#include <stdio.h>

int main() {
    int i, j, n = 4;

    for (i = n; i >= 1; i--) {
        for (j = n; j > i; j--)
            printf("  ");

        for (j = 1; j <= 2 * i - 1; j++)
            printf("* ");

        printf("\n");
    }

    for (i = 2; i <= n; i++) {
        for (j = n; j > i; j--)
            printf("  ");

        for (j = 1; j <= 2 * i - 1; j++)
            printf("* ");

        printf("\n");
    }

    return 0;
}
```

**Output:**

```text
* * * * * * *
  * * * * *
    * * *
      *
    * * *
  * * * * *
* * * * * * *
3.Pascal Triangle
**Code:**

```c
#include <stdio.h>

int main() {
    int i, j, space;
    int n = 5;
    int num;

    for (i = 0; i < n; i++) {
        for (space = 0; space < n - i - 1; space++)
            printf("  ");

        num = 1;

        for (j = 0; j <= i; j++) {
            printf("%4d", num);
            num = num * (i - j) / (j + 1);
        }

        printf("\n");
    }

    return 0;
}
```

**Output:**

```text
        1
      1   1
    1   2   1
  1   3   3   1
1   4   6   4   1

