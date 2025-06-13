#include <stdio.h>
 
int main() {
    int k; 
    int inst = 1;
    scanf("%d", &k); 
    
    while (k--) {
        int S[9][9];
        int valido = 1;
        
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                scanf("%d", &S[i][j]);
            }
        }
        
        for (int i = 0; i < 9 && valido; i++) {
            int marca[10] = {0};
            for (int j = 0; j < 9; j++) {
                int val = S[i][j];
                if (val < 1 || val > 9 || marca[val]) {
                    valido = 0;
                    break;
                }
                marca[val] = 1;
            }
        }
        for (int j = 0; j < 9 && valido; j++) {
            int marca[10] = {0};
            for (int i = 0; i < 9; i++) {
                int val = S[i][j];
                if (val < 1 || val > 9 || marca[val]) {
                    valido = 0;
                    break;
                }
                marca [val] = 1;
            }
        }
        for (int i = 0; i < 9 && valido; i += 3) {
            for (int j = 0; j < 9 && valido; j += 3) {
                int marca[10] = {0};
                for (int k = 0; k < 3; k++) {
                    for (int l = 0; l < 3; l++) {
                        int val = S[i +k][j +l];
                        if (val < 1 || val > 9 || marca[val]) {
                            valido = 0;
                            break;
                        }
                        marca[val] = 1;
                    }
                }
            }
        }
        
        printf("Instancia %d\n", inst++);
        if (valido) {
            printf("SIM\n");
        }
        else {
            printf("NAO\n");
        }
        printf("\n");
    }
    
    return 0;
}
