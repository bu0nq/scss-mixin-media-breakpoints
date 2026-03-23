# SCSS Mixin Media Breakpoints

Пакет для интеграции миксина для создания медиа-запросов.

Документация: [EN](README.md) | [RU](README.RU.md)

___

## Установка

Вы можете установить пакет автоматически с помощью NPM:

```
npm i @bu0nq/scss-mixin-media-breakpoints
```

## Использование

Чтобы использовать этот пакет, импортируйте его в свой проект:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as *;

.demo {
    @include media-breakpoint-min(xl) {
        width: 100%;
    };
}
```

## Миксины

В пакете представлены следующие миксины для использования:

| Название                 | Переменные                                          |
|--------------------------|-----------------------------------------------------|
| media-breakpoint-min     | breakpoint-min, breakpoint-baseline                 |
| media-breakpoint-max     | breakpoint-max, breakpoint-baseline                 |
| media-breakpoint-min-max | breakpoint-min, breakpoint-max, breakpoint-baseline |

`brekpoint-min`, `breakpoint-max`: могут принимать следующие значения: xxs, xs, sm, md, lg, xl, xxl.

`breakpoint-baseline`: принимает значение при преобразовании `px` в `rem`, значение по умолчанию установлено равным 16 пикселям. 

## Изменение пространства имен

Вы можете изменить пространство имен во время импорта миксина и использовать миксин с другим пространством имен:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as mixin;

.demo {
    @include mixin.media-breakpoint-min(xl) {
        width: 100%;
    };
}
```

## Изменение переменных

Вы можете переопределить значения по умолчанию для указанных переменных при импорте миксина:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as * with (
    $breakpoint-xxs: 480px,
    $breakpoint-xs: 640px,
    $breakpoint-sm: 768px,
    $breakpoint-md: 1024px,
    $breakpoint-lg: 1280px,
    $breakpoint-xl: 1440px,
    $breakpoint-xxl: 1536px,
    $breakpoint-baseline: 16,
);
```
