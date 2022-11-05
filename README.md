# veriyap-lar-vealgoritmalar


# Insertion-Sort-Project

[Patika.dev](https://www.patika.dev/tr)


## [22,27,16,2,18,6] __>Insertion Sort

## 1.Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
     - [22,27,16,2,18,6]    n
     - [2,27,16,22,18,6]    n-1
     - [2,6,16,22,18,27]    n-2
     - [2,6,16,18,22,27]    1 
     
## 2.Big-O gösterimini yazınız.    
     - (n.(n+1))/2
     - (n^2+n)/2
     - O(n^2)
    
## 3.Time Complexity: 
     - Average case: Aradığımız sayının(18) ortada olması -->[2,6,16,18,22,27]
     - Worst case: Aradığımız sayının(2) sonda olması,   -->[27,22,18,16,6,2]
     - Best case: Aradığımız sayının(2) dizinin en başında olması. -->[2,6,16,18,22,27]
     
## 4.Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.
     - [2,6,16,18,22,27] Dizinin sıralanmış hali
     - Aradığımız sayı dizinin ortasında bulunduğu için Average case kapsamına girer.
   
## [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.
     -[7,3,5,8,2,9,4,15,6]    n
     -[2,7,5,8,3,9,4,15,6]    n-1
     -[2,3,5,8,7,9,4,15,6]    n-2
     -[2,3,4,8,7,9,5,15,6]    n-3
     



### [16,21,11,8,12,22] -> Merge Sort

#### 1. Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
###### Başlangıçta dizimizi ikiye bölüyoruz. Bölünen dizileri tekrar bölüyoruz. Tek eleman kalana kadar İşleme devam ediyoruz.

|                                                 |  |  |  |  |  |  |  |  |  |  |  |  |
|-----------------------------------------------  |- |- |- |- |- |- |- |- |- |- |- |- |
|Diziyi ikiye bölerek yeniden yazıyoruz           |  |  |  |16|21|11|8 |12|22|  |  |  |
|                                                 |  |  |  |  |  |  |  |  |  |  |  |  |
|Sol ve sağdaki dizileri tekrar ikiye böluyoruz.  |  |  |16|21|11|  |  |8 |12|22|  |  |
|                                                 |  |  |  |  |  |  |  |  |  |  |  |  |
|Tek eleman kalana kadar bir kez daha bölüyoruz.  |  |16|21|  |11|  |  |8 |  |12|22|  |
|                                                 |  |  |  |  |  |  |  |  |  |  |  |  |
|                                                 |16|  |21|  |11|  |  |8 |  |12|  |22|


######  Bölme işlemi bitikten sonra, tek elemanlı dizilerimizi ikili ikili birleştiriyoruz. Sıralı dizi elde edinceye kadar bu işleme devam ediyoruz.

|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|----------------------------------------------- |- |- |- |- |- |- |- |- |- |- |- |- |
|                                                |16|  |21|  |11|  |  |8 |  |12|  |22|
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|ikili ikili ikili sıralayarak birleştiriyoruz.  |  |16|21|  |11|  |  |8 |  |12|22|  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Tekrar ikili ikili sıralayarak birleştiriyoruz. |  |  |11|16|21|  |  |8 |12|22|  |  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Son birleştirmede dizimizi elde ediyoruz.       |  |  |  |8 |11|12|16|21|22|  |  |  |
    

#### 2. Big-O gösterimini yazınız.
Recursive bir fonksiyon olduğu için sürekli kendini çağırarak diziyi hep ikiye bölmektedir. Her bölünmüş dizinin Merge işlemi için de dizinin uzunluğu olan n işlem yapıldığından O(n*(logn)) --> O(6*(log6)) olacaktır.




### [7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.
##### İkili arama ağacı, her düğümün solundaki koldan ulaşılabilecek bütün verilerin düğümün değerinden küçük, sağ kolundan ulaşılabilecek verilerin değerinin o düğümün değerinden büyük olmasını şart koşar.

|     Açıklama    |  |  |  |
|--               |- |- |- |
|**root=7**       |  | 7|  |



**5 sayısı 7'den küçük olduğunda 7'nin soluna ekledik**
|   Açıklama  |     |  |  |
|--           |-    |- |- |
|             |     |  | 7|  
|             |     | /|  | 
|**5 ekledik**|**5**|  |  | 


**1 sayısı 5'ten ve 7'den küçük olduğunda 7 ve 5'in soluna ekledik** 
|     Açıklama  |     |  |  |  |  |
|             --|--   |--|- |- |- |
|               |     |  |  |  | 7|  
|               |     |  |  | /|  | 
|               |     |  | 5|  |  |  
|               |     | /|  |  |  | 
|**1 ekledik**  |**1**|  |  |  |  |

**8 sayısı 7'den büyük olduğunda 7'nin sağına ekledik** 
| Açıklama      |  |  |  |  |  |  |     |
|--             |--|--|- |- |- |- |-    |
|               |  |  |  |  | 7|  |     |  
|               |  |  |  | /|  |\ |     | 
|**8 ekledik**  |  |  | 5|  |  |  |**8**| 
|               |  | /|  |  |  |  |     | 
|               | 1|  |  |  |  |  |     |

**3 sayısı  7'den ve 5'ten küçük  olduğunda 5'in soluna, 1'den büyük olduğunda 1'in sağına ekledik**  
|  Açıklama     |  |  |     |  |  |  |  |
|--             |--|--|-    |- |- |- |- |
|               |  |  |     |  | 7|  |  |  
|               |  |  |     | /|  |\ |  | 
|               |  |  | 5   |  |  |  |8 | 
|               |  | /|     |  |  |  |  | 
|               | 1|  |     |  |  |  |  |
|               |  |\ |     |  |  |  |  |
|**3 ekledik**  |  |  |**3**|  |  |  |  |

**6 sayısı 7'den küçük  olduğunda 7'nin soluna, 5'ten büyük olduğunda 5'in sağına ekledik**  
| Açıklama      |  |  |  |  |     |  |  |
|--             |--|--|- |- |-    |- |- |
|               |  |  |  |  | 7   |  |  |  
|               |  |  |  | /|     |\ |  | 
|               |  |  | 5|  |     |  |8 | 
|               |  | /|  |\ |     |  |  | 
| **6 ekledik** | 1|  |  |  |**6**|  |  |
|               |  |\ |  |  |     |  |  |
|               |  |  | 3|  |     |  |  |

**0 sayısı  7'den, 5'ten ve 1'den küçük  olduğunda 1'in soluna ekledik**  
| Açıklama       |     |  |  |  |  |  |  |  |  |
|--              |--   |--|- |- |- |- |- |- |- |
|                |     |  |  |  |  |  | 7|  |  |  
|                |     |  |  |  |  | /|  |\ |  | 
|                |     |  |  |  | 5|  |  |  |8 | 
|                |     |  |  | /|  |\ |  |  |  |
|                |     |  | 1|  |  |  |6 |  |  |
|                |     | /|  |\ |  |  |  |  |  |
| **0 ekledik**  |**0**|  |  |  | 3|  |  |  |  |

**9 sayısı  7'den ve 8'den büyük olduğunda  8'in sağına ekledik**  
| Açıklama     |  |  |  |  |  |  |  |  |  |  |     |
|--            |--|--|- |- |- |- |- |- |- |- |-    |
|              |  |  |  |  |  |  | 7|  |  |  |     |  
|              |  |  |  |  |  | /|  |\ |  |  |     | 
|              |  |  |  |  | 5|  |  |  |8 |  |     | 
|              |  |  |  | /|  |\ |  |  |  |\ |     | 
| **9 ekledik**|  |  | 1|  |  |  |6 |  |  |  |**9**|
|              |  | /|  |\ |  |  |  |  |  |  |     |
|              | 0|  |  |  | 3|  |  |  |  |  |     |


**4 sayısı  7'den ve 5'ten küçük olduğunda 5'in soluna, 1'den ve 3'ten büyük olduğunda 3'ün sağına ekledik** 
| Açıklama    |  |  |  |  |  |  |     |  |  |  |  |
|--           |--|--|- |- |- |- |-    |- |- |- |- |
|             |  |  |  |  |  |  | 7   |  |  |  |  |  
|             |  |  |  |  |  | /|     |\ |  |  |  | 
|             |  |  |  |  | 5|  |     |  |8 |  |  | 
|             |  |  |  | /|  |\ |     |  |  |\ |  |
|             |  |  | 1|  |  |  |6    |  |  |  | 9|
|             |  | /|  |\ |  |  |     |  |  |  |  |
|             | 0|  |  |  | 3|  |     |  |  |  |  |
|             |  |  |  |  |  |\ |     |  |  |  |  |
|**4 ekledik**|  |  |  |  |  |  |**4**|  |  |  |  |

**2 sayısı  7'den ve 5'ten küçük olduğunda 5'in soluna, 1'den büyük olduğunda 1'in sağına ve 3'ten küçük olduğunda 3'ün soluna ekledik** 
| Açıklama    |  |  |     |  |  |  |  |  |  |  |  |
|--           |--|--|-    |- |- |- |- |- |- |- |- |
|             |  |  |     |  |  |  | 7|  |  |  |  |  
|             |  |  |     |  |  | /|  |\ |  |  |  | 
|             |  |  |     |  | 5|  |  |  |8 |  |  | 
|             |  |  |     | /|  |\ |  |  |  |\ |  | 
|             |  |  | 1   |  |  |  |6 |  |  |  | 9|
|             |  | /|     |\ |  |  |  |  |  |  |  |
|             | 0|  |     |  | 3|  |  |  |  |  |  |
|             |  |  |     | /|  |\ |  |  |  |  |  |
|**2 ekledik**|  |  |**2**|  |  |  |4 |  |  |  |  |

