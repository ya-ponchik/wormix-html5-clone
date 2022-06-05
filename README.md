# wormix-html5-clone

Делаю клон игрушки «[Вормикс](https://web.archive.org/web/20220331113455/https://wormix.fandom.com/ru/wiki/%D0%98%D0%B3%D1%80%D0%B0_%D0%92%D0%BE%D1%80%D0%BC%D0%B8%D0%BA%D1%81)» (написана на Flash), чтобы попрактиковаться в TypeScript и HTML5 Canvas. Специально не использую готовый игровой или физический движок/фреймворк.

Исходный код с доработками выложу позже.

Тестировалось только в **последней версии Google Chrome** на **ПК** с **обычным 1080p монитором.**

# Демо

[https://ya-ponchik.github.io/wormix-html5-clone/public/](https://ya-ponchik.github.io/wormix-html5-clone/public/)

![2022-03-31 02-32-53](https://user-images.githubusercontent.com/102679269/161050964-7e197d78-74a1-4ced-9fbd-d4275387c2e5.gif)


# Что сделано

- Рендеринг в `<canvas>`.
- Разрушаемый террейн, представляющий собой [набор полигонов](https://github.com/ya-ponchik/wormix-html5-clone/blob/main/public/TreesRewamp.json). Написал небольшой скрипт, который преобразует [векторное изображение](https://raw.githubusercontent.com/ya-ponchik/wormix-html5-clone/main/public/wormix/levels/treesRewamp/ground.svg) в него.
- Камера (перемещение и приближение/отдаление мышкой).
- Отвязанные от FPS рендера спрайтовые анимациии.
- Ходьба и прыжки.
- На сущности действует сила гравитации, из-за чего двигаются они по баллистической траектории.
- Обнаружение столкновений с террейном и их разрешение — отскок с учетом вектора скорости, нормали к поверхности, коэффициентов трения и упругости.
- Игровая логика вынесена в отдельный поток (и как следствие, отвязана от FPS).
- Визуальное отображение оружия в руках.
- Прицеливание с накоплением силы выстрела как в оригинальной игре.
- Граната. Анимация вращения, зависящая от скорости и направления гранаты. При взрыве рушит землю и подбрасывает сущности вблизи. Звук при взаимодействии с окружением.
- Базука. Зависима от силы и направления ветра. Снаряд вылетает точно из ствола. При взрыве рушит землю и подбрасывает сущности вблизи. Звук при взаимодействии с окружением.

# Что хочется сделать

- Сетевая синхронизация (сервер на Go плюс [Centrifugo](https://centrifugal.dev/)).
- Реализовать побольше оружек и инструментов.
- Физика верёвки (ninja rope).

# Проблемы

- Через какое-то время стабильно багаются коробки.
- Очень редко граница разрушения становится прозрачной.
- Ходьба в некоторых случаях дико тормозит.
- Время от времени ломаются анимации прыжка.

# Похожие проекты
Я, признаться, в их код не заглядывал — не интересно.

- [https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone](https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone)
- [https://github.com/search?q=wormix&type=](https://github.com/search?q=wormix&type=)
- [https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?q=worms+game&type=repositories](https://github.com/search?q=worms+game&type=repositories)
- [https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com](https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com)
- [https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com](https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com)
