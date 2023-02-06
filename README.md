# Seth - чат-бот с нейросетью для помощи людям.
## Актуальность работы
На данный момент времени актуальность нейросетей востребована от обычного развлечения, например рисования картинок, до серьезных задач связанных с программированием, консультацией клиентов, поддержкой человека в трудную минуту.

## Основная цель проекта
Этот проект предназначен в развлекательных целях, в целях помощи одиноким людям.

## Цель работы
1. Cоздать чат-бота с нейросетью.
2. Провести иследование и тесты с первой версии нейросети.

## Выполненные задачи
Выполнена задача с созданием оболочки для чат-бота. Кроме этого была выполнена задача с иследованием нейросети Seth.

## Обучение 
Обучение происходило на долговременной и кратковременной памятю (англ. [Long short-term memory](https://habr.com/ru/company/wunderfund/blog/331310/)).
Благодоря такому виду обучения я смог достич того что нейросеть может неплохо отвечать на ответы пользователю.

Я добился того что теперь нейросеть обучаеться на GRU(тоже относиться к LSTM нейросетям) и благодоря этому его точность повысилось в двое.
Также благодоря тому что я усовершенствовал векторизацию данных, я смог достичь намного лучших резултатов.

Раньше нейросеть на обучающей выборк нужно было около 800-1000 эпох для того, чтобы обучиться.

Как мы видем на нижнем графике это обучение происходило у старой модели с точностью.

![title](/data/epoch_accuracy%20(1).svg)

Как мы видем на нижнем графике это обучение происходило у старой модели с потерями.

![title](/data/epoch_loss%20(1).svg)


Это обучение в принципе неплохое, но к сожалению на практике дсовсем подругому.

__2/2 [==============================]__ __- ETA: 0s - loss: 51732223950323712.0000 - accuracy: 0.2143__

Выше мы видем тест. Он показывает огоромные потери и очень маленькую точность. Из-за этого я стал сомневаться в этой модели и в данных которые я делал.

Мне пришлось провести куча эксперементов и тунингов модели для того, чтобы выяснить проблему.
Проблема заключалась в данных и в модели которую я сделал.

Как мы видем на нижнем графике это обучение происходило у новой модели с точностью.

![title](/data/epoch_accuracy%20(2).svg)

Как мы видем на нижнем графике это обучение происходило у новой модели с потерями.

![title](/data/epoch_loss%20(2).svg)

Казалось бы у модели очень низкая точность и высокие потери с очень огромными проблемами, но к моему удевлению точность этой модели показала следующее.

__1/1 [==============================] - 0s 430ms/step - loss: 0.4421 - accuracy: 0.8400__

Я был очень удевлен тому факту что модель на практике показала отличный результат.

Модель мне спокойно может выдавать данные которые я и хотел от него ожидать.

Теперь у новой нейросети достаточно 55 эпох для того, чтобы обучиться.

## О подобных туториалах и статьях на различных сайтов и YouTube

Как по мне подобные туториалы "полезны" для начинающих в машинном обучении.

На практике подобного рода статьи практически не дают каких-либо знаний так как они не упомниаю про RNN нейросети или на крайний случай не объясняют как это работает.
Примеру тому служит статья из [Geeks For Geeks](https://www.geeksforgeeks.org/deploy-a-chatbot-using-tensorflow-in-python/) тут не объясняютьяс моменты с полносвязной нейросетью. 
Также мне в этой статье не понравилась как автор объясняет или усложняет то что можно было бы упростить до нескольких строчик кода.

Из плюсов мне понравилось то что автор сделал хорошую токенизацию данных. Я даже ею воспользовался для того, чтобы токенизировать данные для своей нейросети. 

Вобще я советую искать информацию в проверянных источниках и искать разные статьи на тему RNN нейросетей, сверточных нейросетей и подобных им.

Хорошой как по мне площадкой являеться англо. язычные стать и статьи на [Habr](https://habr.com/).

## Итоги
Чего я смог достич.

1. Я смог создать нейросеть на RNN.
2. Я смог провести иследование в области чат-ботов с нейросетями.
3. Я смог создать оболочку для нейросети.
4. Я смог обучиться делать не только чат-ботов с нейросетью, но и теперь могу создовать нейросети на RNN. 

## Источники используемые в работе
[LSTM – сети долгой краткосрочной памяти](https://habr.com/ru/company/wunderfund/blog/331310/) - wunder_editor

[Intelligent AI Chatbot in Python](https://youtu.be/1lwddP0KUEg) - NeuralNine

[Keras Tuner](https://www.tensorflow.org/tutorials/keras/keras_tuner) - Keras

[Tensorboard](https://www.tensorflow.org/tensorboard) - TensorFlow

## Технологии которые используются в работе
pip install [nltk](https://github.com/nltk/nltk)==3.7

pip install [tensorflow](https://github.com/tensorflow/tensorflow)==2.10.0

pip install [nextcord](https://github.com/nextcord/nextcord)==2.1.0

pip install [numpy](https://github.com/numpy/numpy)==1.23.1

pip install [scikit-learn](https://github.com/scikit-learn/scikit-learn)==1.1.3

## Версия 
### Seth-AI v. 0.2
