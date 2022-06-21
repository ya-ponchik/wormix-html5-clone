# wormix-html5-clone

Делаю клон игрушки «[Вормикс](https://web.archive.org/web/20220331113455/https://wormix.fandom.com/ru/wiki/%D0%98%D0%B3%D1%80%D0%B0_%D0%92%D0%BE%D1%80%D0%BC%D0%B8%D0%BA%D1%81)» (написана на Flash), чтобы попрактиковаться в TypeScript и HTML5 Canvas. Специально не использую готовый игровой или физический движок/фреймворк.

Тестировалось только в **последней версии Google Chrome** на **ПК** с **обычным 1080p монитором.**

# Планы

- Добавить еще чутка оружек и инструментов.
- PvP (сервер на Go плюс [Centrifugo](https://centrifugal.dev/)).
- Полировка и публикация кода.

# Демо

[https://ya-ponchik.github.io/wormix-html5-clone/public/](https://ya-ponchik.github.io/wormix-html5-clone/public/)

# Что сделано

to-do: часть текста ниже потереть (уже немног потер), в будущем тут будет ссылка на видеодемонстрацию и немного технических подробностей
побегать, попрыгать, пострелять из всех оружек и тд

- Рендеринг в `<canvas>`.
- Разрушаемый террейн, представляющий собой [набор полигонов](https://github.com/ya-ponchik/wormix-html5-clone/blob/main/public/villianBase.json). Написал небольшой скрипт, который преобразует [векторное изображение](https://raw.githubusercontent.com/ya-ponchik/wormix-html5-clone/main/public/wormix/levels/treesRewamp/ground.svg) в него.
- Камера (перемещение и приближение/отдаление мышкой).
- Отвязанные от FPS рендера спрайтовые анимациии.
- Обнаружение столкновений с террейном и их разрешение — отскок с учетом вектора скорости, нормали к поверхности, коэффициентов трения и упругости.
- Игровая логика вынесена в отдельный поток (и как следствие, отвязана от FPS). рендер отвязан от игры, это вроде как круто

# Похожие проекты
Я, признаться, в их код не заглядывал — не интересно.

- [https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone](https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone)
- [https://github.com/search?q=wormix&type=](https://github.com/search?q=wormix&type=)
- [https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?q=worms+game&type=repositories](https://github.com/search?q=worms+game&type=repositories)
- [https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com](https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com)
- [https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com](https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com)
