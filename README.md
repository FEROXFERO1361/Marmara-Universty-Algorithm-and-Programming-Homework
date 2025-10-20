# Marmara-Universty-Algorithm-and-Programming-Homework
#include <stdio.h>
#include <conio.h>
int main()
{
    int baslangic, bitis;
    int sayi, bolen, asalMi;
    int toplam = 0;

    printf("Iki sayi gir: ");
    scanf("%d %d", &baslangic, &bitis);

    if (baslangic > bitis) 
	{
        int gecici = baslangic;
        baslangic = bitis;
        bitis = gecici;
    }

    for (sayi = baslangic; sayi <= bitis; sayi = sayi + 1) 
	{
        if (sayi >= 2) 
		{
            asalMi = 1;

            for (bolen = 2; bolen * bolen <= sayi && asalMi == 1; bolen = bolen + 1) 
			{
                if (sayi % bolen == 0) 
				{
                    asalMi = 0;
                }
            }

            if (asalMi == 1) 
			{
                toplam = toplam + sayi;
            }
        }
    }

    printf("Asal sayilarin toplami: %d", toplam);
}
