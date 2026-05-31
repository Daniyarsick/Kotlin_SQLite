# Kotlin SQLite

Android-приложение на Kotlin с регистрацией, авторизацией через локальную SQLite-базу и экраном списка товаров. Проект демонстрирует базовую работу с несколькими Activity, локальным хранением данных, RecyclerView и передачей данных между экранами.

## Возможности

- Регистрация пользователя с логином, email и паролем.
- Сохранение пользователя в локальную SQLite-базу.
- Авторизация по логину и паролю.
- Переход к экрану со списком товаров после успешного входа.
- Отображение товаров в `RecyclerView`.
- Открытие детальной страницы товара.
- Передача названия и описания товара через `Intent`.

## Технологии

- Kotlin
- Android SDK
- SQLiteOpenHelper
- RecyclerView
- AppCompat
- Material Components
- ConstraintLayout
- Gradle Kotlin DSL

## Структура проекта

```text
app/src/main/java/com/example/kotlinsqlite
├── MainActivity.kt      # регистрация пользователя
├── AuthActivity.kt      # авторизация пользователя
├── DbHelper.kt          # работа с SQLite
├── ItemsActivity.kt     # список товаров
├── ItemActivity.kt      # детальная страница товара
├── ItemsAdapter.kt      # RecyclerView adapter
├── User.kt              # модель пользователя
└── Item.kt              # модель товара
```

## Основной сценарий

1. Пользователь регистрируется на стартовом экране.
2. Данные сохраняются в SQLite.
3. Пользователь переходит на экран авторизации.
4. После успешной авторизации открывается список товаров.
5. Пользователь нажимает на товар и переходит на страницу с подробным описанием.

## Скриншоты

![Экран регистрации](https://github.com/Daniyarsick/Kotlin_SQLite/assets/124454981/c2c8efde-7086-42ac-902c-d4e33de7c256)

![Экран авторизации](https://github.com/Daniyarsick/Kotlin_SQLite/assets/124454981/52750fea-01b4-4b77-9dec-2950b30ed0ed)

![Список товаров](https://github.com/Daniyarsick/Kotlin_SQLite/assets/124454981/83e33973-ed4b-4d27-a600-7db92adc43f7)

![Детальная страница товара](https://github.com/Daniyarsick/Kotlin_SQLite/assets/124454981/cdae7816-27b7-43c3-8660-0e7a8506800e)

## Сборка

Требования:

- Android Studio или Android SDK
- JDK 17
- Gradle Wrapper из репозитория

Команда для сборки:

```bash
./gradlew assembleDebug
```

На Windows:

```powershell
.\gradlew.bat assembleDebug
```

APK после сборки:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Примечания

Проект учебный. Для production-версии стоит доработать хранение паролей, заменить строковую сборку SQL-запроса на параметризованный запрос, добавить валидацию email и вынести данные товаров в отдельный источник данных.

## Статус

Учебный Android-проект для демонстрации базовой работы с Kotlin, SQLite, RecyclerView и навигацией между Activity.
