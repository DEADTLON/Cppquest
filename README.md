#include <stdio.h>
#include <math.h>

int main() {
    float x1, x2, px, a, b, c;
    float x, F;
    int n;

    printf("Input x1: ");
    scanf("%f", &x1);

    printf("Input x2: ");
    scanf("%f", &x2);

    printf("Input px: ");
    scanf("%f", &px);

    printf("Input a: ");
    scanf("%f", &a);

    printf("Input b: ");
    scanf("%f", &b);

    printf("Input c: ");
    scanf("%f", &c);

    x = x1;
    n = 0;

    printf("\nResults:\n");

    while (x < x2) {
        n = n + 1;

        if ((c + b < 0) && (a != 0)) {
            F = (a * x - c) / (b * b + cos(x));
        } else if ((c + b > 0) && (a == 0)) {
            F = (a * x + sin(b * x)) / (b * b + c * x);
        } else {
            F = (3 * log(x) + 2 * x) / (a * a + c - b * x);
        }

        printf("%i: x = %.3f \t F = %.3f \n", n, x, F);
        x = x + px;
    }

    return 0;
}
