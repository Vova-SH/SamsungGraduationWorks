# Супер список популярных фильмов
<a href="https://github.com/Vova-SH/Samsung-Bootcamp-2021/actions/workflows/android.yml"><img src="https://github.com/Vova-SH/Samsung-Bootcamp-2021/actions/workflows/android.yml/badge.svg" align="left" alt="Android CI"></a>
<p align="right">
  <a href="./README.en-US.md">English</a>
  |
  <a href="./README.md">Русский</a>
</p>

## О приложении
<img src="https://github.com/Vova-SH/Samsung-Bootcamp-2021/blob/main/screenshots/app.gif" width = "260" align="right">

Приложение разработано в рамках обучаючающего интенсива [Samsung Innovation Campus Bootcamp: Kotlin for Android](https://youtube.com/playlist?list=PLa2T1zmZ6w5KzKoh9M91vk1LBqpc-WtoS). Мастер-класс "[Использование паттерна MVVM при разработке приложений. Классы ViewModel и LiveData](https://youtu.be/8MmeLVi-7yU)".

Функционал представляет простейший список популярных фильмов и информацию о каждом фильме. Доступ к информации о фильмах осуществлён с помощью сервиса [The Movie DB](https://www.themoviedb.org) с использованием соответствующего [API](https://www.themoviedb.org/documentation/api/).

Презентационные и другие дополнительные материалы находятся [здесь](https://github.com/Vova-SH/Samsung-Bootcamp-2021/tree/master/docs).

**Шаблон проекта находится в ветке template или его можно скачать** [здесь](https://github.com/Vova-SH/Samsung-Bootcamp-2021/archive/refs/heads/template.zip).

## Средства разработки
Приложение написано на Kotlin и использует систему сборки Gradle.

Чтобы собрать приложение используйте команду `gradlew build` или используйте "Import Project" в Android Studio. Требуется стабильная версия Android Studio 4.2.1 или новее, загрузить которую можно [здесь](https://developer.android.com/studio/).

## Архитектура
Архитектура построена вокруг [Android Architecture Components](https://developer.android.com/topic/libraries/architecture/).

Были использованы рекомендации, описанные в [Руководстве по архитектуре приложений](https://developer.android.com/jetpack/docs/guide) при принятии решения об архитектуре приложения. Бизнес-логика приложения была вынесена из Activity и Fragment'ов в [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel).

Подписка на обновление данных было реализовано с использованием [LiveData](https://developer.android.com/topic/libraries/architecture/livedata), а для хранения и управления кэшем фильмов была использована [Room](https://developer.android.com/jetpack/androidx/releases/room).

Был использован [Koin](https://github.com/InsertKoinIO/koin) для внедрения ViewModel'ей во Fragment'ы.

## The Movie Database API
Для демонстрации работы с клиент-серверной архитектурой используется данное API. Данные и изображения лицензированы в соответствии с [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/). С полными правилами использования API можно ознакомиться [здесь](https://www.themoviedb.org/documentation/api/terms-of-use).

Для работоспособности необходимо выполнить следующие шаги:
1. Получить ключ по [следующей инструкции (EN)](https://developers.themoviedb.org/3/getting-started/introduction).
2. Добавить ключ в файл `Constants.kt` в константу `API_KEY`

В приложении используются следующие запросы:
- `GET` [/movie/{movie_id}](https://developers.themoviedb.org/3/movies/get-movie-details) - получение информации о фильме.
- `GET` [/movie/{movie_id}/credits](https://developers.themoviedb.org/3/movies/get-movie-credits) - получение информации об актёрах и съёмочной группе фильма.
- `GET` [/movie/popular](https://developers.themoviedb.org/3/movies/get-popular-movies) - получение списка популярных фильмов постранично.