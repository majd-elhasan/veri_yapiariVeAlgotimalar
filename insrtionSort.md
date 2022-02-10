# Proje 1

## [22,27,16,2,18,6] -> Insertion Sort
```python
1	for (i = 1; i < n; i++)                      // n x işlem
2	{
3		deger = arr[i];             			// 1 işlem
4		   j = i-1;								// 1 işlem
5                                                
6		   while (j >= 0 && arr[j] > deger)		// karşılaştırılan sayının sıralı listedeki konumuna gitmesi , en kötü ihtimal i işlem
7		   {                                     
8			   arr[j+1] = arr[j];				// 1 işlem
9			   j--;								// 1 işlem
10		   }                                     
11		   arr[j+1] = deger;					// 1 işlem
12		}
```

	{, *27*, 16, 2, 18, 6}    " 3 + 0 "
	{*16*, 22,<span style="color:red"> 27</span>, 2, 18, 6}	" 3 + 2 x 2 "
	{*2*, 16, 22,<span style="color:red"> 27</span>, 18, 6}	" 3 + 2 x 3 "
	{2, 16, *18*, 22,<span style="color:red"> 27</span>, 6}	" 3 + 2 x 2 "
	{2, *6*, 16, 18, 22,<span style="color:red"> 27</span>}	" 3 + 2 x 4 "
	
									işlem sayısı = 37
____________________________________________________________________________________________
	
	3 + 2 x 1
	3 + 2 x 2
	3 + 2 x 3
	3 + 2 x 4
	3 + 2 x 5
	
	worst case  sayıların büyükten küçüğe doğru sıralanmış olması {27 ,22 ,18 ,16 ,6 ,2}
			worst case TimeComplexity =	o(n²)  ,işlem sayısı = 45
	best case 	sayıların küçükten büyüğe doğru sıralanmış olması {2, 6, 16, 18, 22, 27}
			best case TimeComplexity = o(n) ,işlem sayısı = 5
			
____________________________________________________________________________________________
### Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? 

{2, 6, 16, 18, 22, 27}  dizi sıralıyken 18 sayısı average case kapsamına girer .

____________________________________________________________________________________________
### [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

{'3', 7, 5, 8, 2, 9, 4, 15, 6}
{3, '5', 7, 8, 2, 9, 4, 15, 6}
{3, 5, 7, '8', 2, 9, 4, 15, 6}
{'2', 3, 5, 7, 8, 9, 4, 15, 6}