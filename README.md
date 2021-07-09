# diarization-guide

SoundHelper.py - Код для работы с аудиозаписями (объединение, наложение и т.д.)
Используется библиотека pydub. 
Установка: `$ pip install pydub`

Diarization.py - Код для запуска диаризации файла фреймворком pyannote-audio.
Установка библиотеки: `$ pip install pyannote.audio==1.1.1` 
Так же pyannote-audio базируется на работе фреймворка машинного обучения PyTorch. Для работы требуется данный фреймворк.
Установка: `$ pip install torch`

Для диаризации фреймворком pyAudioAnalysis, требуется клонировать репозиторий по [ссылке](https://github.com/tyiannak/pyAudioAnalysis.git),
через консоль зайти в папку с репозиторием, ввести команду `$ pip install -r ./requirements.txt` и `$ pip install -e .`
Инструкция по установке так же имеется в описании репозитория.
В репозитории, по пути pyAudioAnalysis/data хранятся записи и файлы их сегментации(разметка). Добавим в папку свои записи и разметки.
Запуск из папки pyAudioAnalysis: `python3 audioAnalysis.py speakerDiarization -i data/diarizationExample.wav --num 0`.
Важно! Файл записи должен иметь расширение wav, а файл разметки должен иметь такое же имя, как и аудиофайл.
