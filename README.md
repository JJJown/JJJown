#include <stdio.h>
#include <ctype.h>

int main() {
    int counts[26] = {0};
    char input;

    while (scanf("%c", &input) == 1) {
        if (isalpha(input)) {
            int index = toupper(input) - 'A';
            counts[index]++;
        } else {
            break;
        }
    }

    for (int i = 0; i < 26; i++) {
        if (counts[i] > 0) {
            printf("%c: %d\n", i + 'A', counts[i]);
        }
    }

    return 0;
}
