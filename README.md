Данная программа учится распознавать болезнь по рентгеновским снимкам грудной клетки.
Тест1 - это исходная свёрточная нейронная сеть состоящая из 2 свёрточных слоёв Conv2D(filters=8, kernel_size=3), двух слоёв операции подвыборки MaxPool2D() и одного слоя Flatten(), после 200 эпох обучения получились следующие графики:
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test1%20TensorBoard(1).png) 
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test1%20TensorBoard(2).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test1%20TensorBoard(3).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test1%20TensorBoard(4).png)        
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test1%20Tensorboard(5).png)
                                                                                                                           
Тест2 - Добавил ещё один такой же свёрточный слой Conv2D(filters=8, kernel_size=3) и MaxPool2D() после него, а так же во всех последующих тестах количество эпох установил равное 100. Результат:         
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test2%20TensorBoard(1).png) 
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test2%20TensorBoard(2).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test2%20TensorBoard(3).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test2%20TensorBoard(4).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test2%20TensorBoard(5).png)

Тест3 - изменил параметр filters=8 в первом свёрточном слое на filters=4. Результат:                            
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test3%20TensorBoard(1).png) 
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test3%20TensorBoard(2).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test3%20TensorBoard(3).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test3%20TensorBoard(4).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test3%20TensorBoard(5).png)

Тест4 - Добавил 4-ый свёрточный слой Conv2D и установил параметр filters во всех четырёх свёрточных слоях равными 8, 16, 8, 4 начиная с первого и соответственно. Результат:                         
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test4%20TensorBoard(1).png) 
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test4%20TensorBoard(2).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test4%20TensorBoard(3).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test4%20TensorBoard(4).png)
![Image alt](https://github.com/BabeyKirill/SMOMI/blob/lab2/Test4%20TensorBoard(5).png)

Вывод: все изменения исходного кода привели не к улучшению показателя точности программы, а наоборот к её ухудшению. Как видно по графикам тестов 2-4, точность падает с каждой эпохой. Опыт неудачный
