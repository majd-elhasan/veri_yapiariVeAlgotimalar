# Proje 1

## [22,27,16,2,18,6] -> Insertion Sort
```python
1	for (i = 1; i < n; i++)                      // n x i?lem
2	{
3		deger = arr[i];             			// 1 i?lem
4		   j = i-1;								// 1 i?lem
5                                                
6		   while (j >= 0 && arr[j] > deger)		// kar??la?t?r?lan say?n?n s?ral? listedeki konumuna gitmesi , en k?t? ihtimal i i?lem
7		   {                                     
8			   arr[j+1] = arr[j];				// 1 i?lem
9			   j--;								// 1 i?lem
10		   }                                     
11		   arr[j+1] = deger;					// 1 i?lem
12		}
```

	{22, 27, 16,  2, 18, 6}    " 3 + 0 "
	 __  ..
	{16, 22, 27,  2, 18,  6}	" 3 + 2 x 2 "
	 ..		 __
	{ 2, 16, 22, 27, 18,  6}	" 3 + 2 x 3 "
	 ..          __
	{ 2, 16, 18, 22, 27,  6}	" 3 + 2 x 2 "
             ..      __
	{ 2,  6, 16, 18, 22, 27}	" 3 + 2 x 4 "
         ..              __
	
									i?lem say?s? = 37
____________________________________________________________________________________________
	
	3 + 2 x 1
	3 + 2 x 2
	3 + 2 x 3
	3 + 2 x 4
	3 + 2 x 5
	
	worst case  say?lar?n b?y?kten k????e do?ru s?ralanm?? olmas? {27 ,22 ,18 ,16 ,6 ,2}
			worst case TimeComplexity =	o(n?)  ,i?lem say?s? = 45
	best case 	say?lar?n k???kten b?y??e do?ru s?ralanm?? olmas? {2, 6, 16, 18, 22, 27}
			best case TimeComplexity = o(n) ,i?lem say?s? = 5
			
____________________________________________________________________________________________
### Dizi s?raland?ktan sonra 18 say?s? hangi case kapsam?na girer? 

	{2, 6, 16, 18, 22, 27}  dizi s?ral?yken 18 say?s? average case kapsam?na girer .

____________________________________________________________________________________________
### [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a g?re ilk 4 ad?m?n? yaz?n?z.

	{ 3, 7, 5, 8, 2, 9, 4, 15, 6}
     .. __
	{ 3, 5, 7, 8, 2, 9, 4, 15, 6} 
        .. __
	{ 3, 5, 7, 8, 2, 9, 4, 15, 6} 
           __ ..  
	{ 2, 3, 5, 7, 8, 9, 4, 15, 6} 
	 ..          __
