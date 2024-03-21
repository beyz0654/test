#include <stdio.h>
#include <stdlib.h>
#include <conio.h>


void kitapal();
void kitapiade();
void kitaphakki();


int hak = 5;

int main() {    
    char ad[50];
    char soyad[50];

    printf("Adinizi giriniz: ");
    scanf("%s", ad);

    printf("Soyadinizi giriniz: ");
    scanf("%s", soyad);

    printf("\n\nHosgeldiniz.\nAdiniz Soyadiniz: %s %s\n", ad, soyad);

    
    int islem;

    do {
        
        printf("\n\n1. Kitap Alma\n");
        printf("2. Kitap İade\n");
        printf("3. Kitap Hakki\n");
        printf("4. Çıkış\n");
        printf("Lütfen secim yapiniz:");
        scanf("%d", &islem);

     
        switch (islem) {
            case 1:
                kitapal();
                break;
            case 2:
                kitapiade();
                break;
            case 3:
                kitaphakki();
                break;
            case 4:
                printf("Uygulama kapatiliyor\n");
                break;
            default:
                printf("Geçersiz islem\n");
        }
    } while (islem != 4);

    return 0;
}


void kitapal() {
    int tercih;


    printf("\n\n alinmak istenen kitap turu:");
    printf("\n1. tarih");
    printf("\n2. roman");
    printf("\n3. klasik\n");
    printf("Seciminiz: ");
    scanf("%d", &tercih);

  
    switch (tercih) {
        case 1:
            printf("Tarih turu ekle\n");
            break;
        case 2:
            printf("Roman turu ekle\n");
            break;
        case 3:
         
            printf("Klasik turu ekle\n");
            break;
        default:
            printf("Geçersiz islem\n");
            return; 
    }

    
    if (hak == 0) {
        printf("\nDaha fazla alamazsiniz.\n");
    } else {
        hak--;
        printf("\nKalan kitap hakki: %d\n", hak);
    }
}


void kitapiade() {
    int adet;

 
    printf("\n\nIade edilicek kitap sayisi? ");
    scanf("%d", &adet);

    hak += adet;
    printf("\nKalan kitap hakki: %d\n", hak);
}


void kitaphakki() {
    printf("\n\nKalan kitap hakki: %d\n", hak);
}
