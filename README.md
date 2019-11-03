# C_homework1
It is a calculator. This is my first project in C. It include basic (like addition etc.) and anvanced (like sin, squareroot etc.) mathematical process. Project language is Turkish. 
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

#define PI 3.14159265

// Esma Nisa Candan 18010011060
int main()
{
    int secim1, secim2, secim3,a, mod, sonuc1;
    float toplam=0, sonuc, deger, i, carpim=1,x,y;
    float root, num, bolme, adet;

    printf("\n*****HESAP MAKINESI*****\n");
    printf("\nBasit hesap makinasi icin: 1\n");
    printf("\nBilimsel hesap makinasi icin: 2\n");
    printf("Seciminiz: ");
    scanf("%d", &secim1);

    if(secim1==1)
    {
        printf("\n***BASIT HESAP MAKINESI***\n");
        printf("\nToplama icin: 1\n");
        printf("\nCikarma icin: 2\n");
        printf("\nCarpma icin: 3\n");
        printf("\nBolme icin: 4\n");
        scanf("%d", &secim2);

        if (secim2==1)
        {
            printf("\nToplama islemini sectiniz...\n");
            printf("Kac tane sayi toplamak istiyorsunuz? ");
b:
            scanf("%f", &num);
            if(num<0)
            {
                printf("Lutfen pozitif bir tamsayi giriniz!");
                goto b;
            }
            else
            {
                for (i = 1; i <= num; i++)
                {
                    printf("Sayiyi giriniz:", num);
                    scanf("%f", &deger);
                    toplam = toplam + deger;
                }
            }

            printf("Sayilarin toplami = %0.2f\n", toplam);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }

        }

        else if (secim2==2)
        {
            printf("\nCikarma islemini sectiniz...\n");
            printf("Kac tane sayi cikarmak istiyorsunuz? ");
c:
            scanf("%f", &adet);
            if(adet<0)
            {
                printf("Lutfen pozitif bir tamsayi giriniz!");
                goto c;
            }
            else
            {
                printf("Sayi giriniz: ");
                scanf("%f",&num);
                sonuc=0;
                sonuc=num-sonuc;

                for(i=1; i<adet; i++)
                {
                    printf("Sayi giriniz: ");
                    scanf("%f",&num);
                    sonuc=sonuc-num;
                }
            }

            printf("Sonuc: %0.2f\n", sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }

        else if(secim2==3)
        {
            printf("Carpma islemini sectiniz...\n");
            printf("Kac tane sayi carpmak istiyorsunuz? \n");
d:
            scanf("%f", &adet);
            if(adet<0)
            {
                printf("Lutfen pozitif bir tamsayi giriniz!");
                goto d;
            }

            else
            {
                for (i=1; i<=adet; ++i)
                {
                    printf("Sayilari giriniz: ", adet);
                    scanf("%f", &deger);
                    carpim=carpim*deger;
                }
            }
            printf("Sonuc:%0.2f\n", carpim);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }
        else
        {
            printf("\nBolme islemini sectiniz...\n");
            printf("Kac tane sayi bolmek istiyorsunuz? ");
e:
            scanf("%f", &adet);
            if(adet<0)
            {
                printf("Lutfen pozitif bir tamsayi giriniz!");
                goto e;
            }
            else
            {
                bolme=1;
                printf("Sayi giriniz:");
                scanf("%f",&deger);
                bolme=deger/bolme;
                for (i=1; i<adet; i++)
                {
x:
                    printf("Sayi giriniz:");
                    scanf("%f", &deger);
                    if(deger==0)
                    {
                        printf("Gecersiz deger girdiniz!!\n");
                        goto x;

                    }
                    else
                        bolme=bolme/deger;
                }
            }
            printf("Sonuc:%.02f\n", bolme);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }
    }

    else if(secim1==2)

    {
        printf("\n***BILIMSEL HESAP MAKINESI***\n");
        printf("\nMod almak icin: 1\n");
        printf("\nUs almak icin: 2\n");
        printf("\nKarekok almak icin: 3\n");
        printf("\n10 tabaninda logaritma almak icin: 4\n");
        printf("\ne tabaninda logaritma almak icin: 5\n");
        printf("\nSinus icin: 6\n");
        printf("\nCosinus icin: 7\n");
        scanf("%d", &secim2);

        if (secim2==1)
        {
            printf("\nMod alma islemini sectiniz...\n");
            printf("Sayi Giriniz: ");
            scanf("%d", &a);
            printf("Alinacak Mod degerini giriniz: ");
f:
            scanf("%d", &mod);
            if(mod>0)
            {
                sonuc1 = a % mod;
                printf("%d(%d)= %d\n",a, mod, sonuc1);
            }
            else
            {
                printf("Lutfen pozitif bir deger giriniz!");
                goto f;
            }

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }

        else if (secim2==2)
        {
            printf("\nUs alma islemini sectiniz...\n");
            printf("Taban degerini giriniz: ");
            scanf("%f", &x);
            printf("Us degerini giriniz: ");
            scanf("%f", &y);

            sonuc = pow(x,y);
            printf("Sonuc: %.02f\n", sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz:");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }

        else if (secim2==3)
        {
            printf("\nKarekok alma islemini sectiniz...\n");
            printf("Karekokunu almak istediginiz sayiyi giriniz: ");
g:
            scanf("%f", &num);
            if(num<0)
            {
                printf("Lutfen pozitif bir deger giriniz!");
                goto g;
            }
            else
            {
                root = sqrt(num);
            }
            printf("Girilen deger:%.02f\n", num);
            printf("Karekoku:%.02f\n", root);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }

        }
        else if (secim2==4)
        {
            printf("\n10 tabaninda logaritma almayi sectiniz...\n");
            printf("Logaritmasini almak istediginiz sayiyi girin:\n");
h:
            scanf("%f", &num);
            if(num<0)
            {
                printf("Lutfen pozitif bir deger giriniz!");
                goto h;
            }
            else
            {
                sonuc=log10(num);
            }
            printf("Sonuc:%.02f\n", sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }
        else if(secim2==5)
        {
            printf("\ne tabaninda logaritma almayi sectiniz...\n");
            printf("Logaritmasini almak istediginiz sayiyi girin: ");
k:
            scanf("%f", &num);
            if(num<0)
            {
                printf("Lutfen pozitif bir deger giriniz!");
                goto k;
            }
            else
            {
                sonuc=log(num);
            }
            printf("Sonuc:%lf\n", sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }
        else if(secim2==6)
        {
            printf("\nSinus alma islemini sectiniz...\n");
            printf("Bir aci degeri girin: ");
            scanf("%f", &num);
            deger=PI/180;
            sonuc=sin(num*deger);
            printf("Sonuc:%lf sinusu %lf dir...\n",num, sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }
        }
        else
        {
            printf("\nCosinus alma islemini sectiniz...\n");
            printf("Bir aci degeri girin: ");
            scanf("%f", &num);
            deger=PI/180;
            sonuc=cos(num*deger);
            printf("%lf cosinusu %lf dir...\n", num, sonuc);

            printf("Cikmak icin 0 degerini girin...\n");
            printf("Hesap makinesine donmek icin 1 degerini girin...\n");
            printf("Seciminiz: ");
            scanf("%d", &secim3);

            if (secim3==0)
            {
                return;
            }
            else
            {
                main();
            }

        }

    }

    else
    {
        printf("Yanlis secim yaptiniz!!!\n");
    }

    return 0;
}



