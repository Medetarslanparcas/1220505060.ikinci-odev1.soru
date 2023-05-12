# 1220505060.ikinci-odev1.soru
Linear Search fonksiyonu

#include <stdio.h>

// Linear Search fonksiyonu
int linearSearch(int arr[], int n, int x) {
    int i;
    for (i = 0; i < n; i++) {
        if (arr[i] == x) {
            return i;
        }
    }
    return -1;
}

int main() {
    int n, x, result, i;

    // Dizinin boyutunu kullanıcıdan isteme
    printf("Dizinin boyutunu girin: ");
    scanf("%d", &n);

    int arr[n];

    // Elemanları kullanıcıdan alma
    printf("Dizinin elemanlarini girin:\n");
    for (i = 0; i < n; i++) {
        printf("arr[%d]: ", i);
        scanf("%d", &arr[i]);
    }

    // Aranacak elemanı kullanıcıdan alma
    printf("Aranacak elemani girin: ");
    scanf("%d", &x);

    // Linear Search kullanarak elemanın dizide olup olmadığını kontrol etme
    result = linearSearch(arr, n, x);

    if (result == -1) {
        printf("Eleman dizide bulunamadi.\n");
    } else {
        printf("Eleman dizinin %d. indeksinde bulundu.\n", result);
    }

    return 0;
}


