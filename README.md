Этот код создаёт систему для классификации изображений, которая использует нейронную сеть для распознавания объектов, основанную на сверточных слоях (CNN). Процесс начинается с загрузки и подготовки данных — изображения загружаются с Google Drive, где они могут быть расположены в отдельной папке. Для работы с изображениями используется библиотека TensorFlow, а также OpenCV для предварительной обработки данных.
Сначала изображения нормализуются, чтобы привести их пиксели к диапазону от 0 до 1, что помогает нейронной сети быстрее обучаться. Также применяется аугментация данных, что увеличивает объём тренировочного набора путём случайных трансформаций изображений, что помогает улучшить обобщающую способность модели.
Затем создается и обучается нейронная сеть с несколькими сверточными слоями (Conv2D), которые извлекают особенности изображений, и слоями подвыборки (MaxPooling2D), которые уменьшают размерность данных. Сеть заканчивается полносвязными слоями, которые на основе извлечённых признаков делают предсказания. Модель обучается на классификацию с использованием функции потерь sparse_categorical_crossentropy.
После обучения модель сохраняется на Google Drive, что позволяет её использовать для предсказаний. Для этого создается функция, которая принимает путь к изображению, обрабатывает его и передаёт в модель для предсказания. Модель возвращает класс с наибольшей вероятностью, что позволяет классифицировать изображение по заранее заданным категориям.

![Examination](https://github.com/user-attachments/assets/b0943d46-d73d-40f2-af22-441c8685b9ea)
