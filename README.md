# Old-Fashioned-English-Pound

Given the old english monetary system (used until 1971) where 1 pound was divided into 20 shillings and 1 shilling was divided into 12 pennies, implement a PHP class that is able to handle addition and subtraction of 2 values that the class will always receive in the following format: “5p 17s 8d” (in this case representing 5 pounds 17 shillings and 8 pennies) 
The result returned by the class should be in the very same format: 
5p 17s 8d + 3p 4s 10d = 9p 2s 6d
9p 2s 6d - 5p 17s 8d = 3p 4s 10d
This class will handle multiplication and division as well but only by an integer value:
5p 17s 8d * 2 = 11p 15s 4d 
5p 17s 8d / 3 = 1p 19s 2d (2d) 18p 16s 1d / 15 = 1p 5s 0d (1s 1d) 
As shown above in division examples you need to report as well the remainder (if any) in round brackets. 
Extra points 
Although this test requires just the implementation of a class that manages the 4 operations mentioned above, it would be quite distinctive to design the class in a way that creates instances of itself in which it is possible to call methods upon with the possibility to chain them together: 
$priceA = new OldEnglishPound(“5p 17s 8d”); $priceB = new OldEnglishPound(“3p 4s 10d”); 
$sum = $priceA.sum($priceB); 
$result = $priceA.sum($priceB).multiply(2).div(3);
