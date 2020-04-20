Данная лабораторная работа является продолжением прошлой, здесь к модели VGG16 из предыдущей лабораторной работы нужно было применить разные методы аугментации с целью увеличения датабазы тренировочных картинок. В последующем для всех графиков lr = 10^-10, batch size = 8. Вот конечные графики из предыдущей лабораторной работы для сравнения:
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/Unfreezed160-10.png)

a) Первый способ - это случайное отражение картинки по вертикали, он реализован в файле train_a.py. Вот получившиеся для него графики:
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/A_Ep90_lr-10.png)                                               
Смотря на них, сложно сказать, улучшилась ли точность, она почти такая-же.

b) Далее идёт метод поворота картинки на случайный угол от 0 градусов до заданного значения, он реализован в файле train_b.py. Вот графики:                                                                                                                 
15 градусов:                                                                                                                                       
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/b15_Ep120_lr-10.png)                                                                 
30 градусов:                                                                                                                                                                                                                                             
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/b30_Ep120_lr-10.png)                                                      
45 градусов:                                                                                                                                   
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/b45_Ep120_lr-10.png)                                                                                          
Из этих трёх лучше всех выглядят графики для 15 градусов, но по сравнению с исходными графиками изменения незначительны.

с) Третий способ - это случайное изменение яркости и контрастности картинки с 1 на 1 +-значение от 0 до заданного, он реализован в файле train_c.py. Вот графики:                                                                                                  
0.2 :                                                                                                                                            
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/c02_Ep120_lr-10.png)                                                                             
0.4 :                                                                                                                                        
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/%D1%8104_Ep120_lr-10.png)                                                                 
0.6 :                                                                                                                                        
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/c06_Ep120_lr-10.png)                                                                                                                           
Графики для 0,2 и 0,4 могут показаться одинаковыми, если не всмотреться, а 0.6 чуть хуже их. По сравнению с исходными графиками точность опять же изменилась незначительно.

d) Четвёртый способ - это случайное обрезание картинки до заданных размеров. Исходная картинка 224х224, способ реализован в файле train_d.py. Вот графики:                                                                                                           
180х200:                                                                                                                                     
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/d40_20_Ep90_lr-10.png)                                                                     
160x180:                                                                                                                                      
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/d60_40_Ep120_lr-10.png)                                                                                      
140x160:                                                                                                                                      
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/d80_60_Ep120_lr-10.png)                                                                                                           
Из этих трёх лучше всех выглядят графики для 160х180, но по сравнению с исходными графиками изменения незначительны.

e) И наконец использование всех четырёх методов с лучшими параметрами вместе, это a), b)15 градусов, c)0.2, d)160x180. Файл в котором это реализовано называется train_abcd.py. Вот получившиеся графики:                                                                                                       
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab4/abcd15_02_60_40_Ep160_lr-10.png)                                                                 

Как итог нельзя сказать наверняка, улучшились ли результаты: во первых рост точности замедлился по сравнению с исходными графиками, во вторых график точности для 160 эпох в пункте e) выглядит как часть исходного графика от 0 до 100 эпох. В работе в качестве результата ожидалось существенное улучшение точности чего я не наблюдаю.
