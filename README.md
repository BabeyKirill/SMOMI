Это нейронная сеть из 5 полносвязных слоёв Dense. В программе использовались оптимизатор 'adam' и функция потерь SparceCategoricalCrossentropy. Количество обрабатываемых объектов в одном цикле обучения = 50000, всего 10 классов объектов 'airplane', 'automobile', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck'. Объекты представляют из себя изображения размером 255х255 пикселей, набор объектов выбирается случайно из базы размером около 1.5млн. Я перепробовал разные количества слоёв и нейронов, а так же разные акцтивации. В итоге лучший результат у меня получился при 256, 128, 64, 32 и 10 нейронах у каждого слоя соответственно, рост точности сильно замедляется уже на 20-ом цикле обучения, а лучшей активацией оказалась 'elu'. Графики были получены с помощью tensorboard.

