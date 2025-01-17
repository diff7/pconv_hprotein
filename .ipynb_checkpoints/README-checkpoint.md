# Pconv - human protein
- Основая статья: https://arxiv.org/pdf/1804.07723.pdf
- Реопозиторий имплементации: https://github.com/naoto0804/pytorch-inpainting-with-partial-conv
 
# Мотивация и постановка задачи
- В качестве тестового задания я выбрал задачу восстановления изображений. Задача соревнования на Kaggle классификация, но классификация бы свелась к файнтьюнингу того же резнета, а хотелось чего-то более интересного. К тому же показалось что тестовое задание было в более или менее свободной форме.

- С другой стороны, задача восстановления изображений более сложная чем классификация, а собирать модели по статьям за выходные я еще не умею, поэтому я взял готовую реализиацию Pconv от Nvidia на Github.

# Описание:
- results.ipynb

    - Описание результатов
    - Параметров обучения
    - Частичные свертки - описание (одна из основных идей статьи)
    - Описание лосс функций и их графики
    - Выводы
    - Идеи что еще можно было бы сделать


- train_test.ipynb

    - В этом ноутбуке я смотрю на изображения и разбиение по классам
    - Сохраняю часть изображений в RGB и разбиваю их на train, test, val
    - Генерирую случайный шум
    - Тестирую генератор данных с масками шума
    
- train.ipynb
- Возможно менее интересный с точки зрения тестового задания, но достаточно важный с точки зрения модели и процессе обучения.

# Структурка проекта:
    - logs - логи для тензорборда
    - snapshots - здесь сохраняются промежуточные веса модели
    - masks - сюда генерируем маски 
    - train - датасент human protein
    - my_train - сюда сохраняются разбитые train, test, val данные для всего в RGB
