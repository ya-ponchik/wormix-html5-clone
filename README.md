# wormix-html5-clone

Делаю клон игрушки «[Вормикс](https://web.archive.org/web/20220331113455/https://wormix.fandom.com/ru/wiki/%D0%98%D0%B3%D1%80%D0%B0_%D0%92%D0%BE%D1%80%D0%BC%D0%B8%D0%BA%D1%81)» (написана на Flash), чтобы попрактиковаться в решении задач на TypeScript и HTML5 Canvas. Специально не использую готовый игровой или физический движок/фреймворк.

Тестировалось только на **ПК** с **обычным 1080p монитором.** В основном в **последней версии Google Chrome**, изредка — в Firefox.


# Планы

- PvP (сервер на Go плюс [Centrifugo](https://centrifugal.dev/)).
- Управление для мобилок.
- Полировка и публикация кода;

# Демо

[https://ya-ponchik.github.io/wormix-html5-clone/public/](https://ya-ponchik.github.io/wormix-html5-clone/public/)

to-do: в будущем тут будет ссылка на видеодемонстрацию. побегать, попрыгать, поиграть камерой, пострелять из всех оружек и тд

# Управление

### Игра

- **Левая кнопка мыши** — двигать камеру;
- **Колесико мыши** — приблизить/отдалить камеру;
- **A** — бег влево;
- **D** — бег вправо;
- **F** — прыжок вперед;
- **R** — прыжок назад;
- **W** — двигать прицел вверх;
- **S** — двигать прицел вниз;
- **Пробел** — накопление силы выстрела;
- **1** — выбрать гранату;
- **2** — выбрать базуку (ветер дует сильно влево);
- **3** — выбрать ружье;
- **4** — выбрать веревку (еще дорабатывается);
- **C** — смена персонажа (обработчик клавиш пока думает, что перс только один, и может заглючить).

### Дебаг

- **F2** — активировать дебаг и показать/скрыть отладочную информацию;
- **Правая кнопка мыши** — рисовать или разрушить террейн;
- **F5** — смена режима (рисование или разрушение).

# Принимали участие
### Разработчики
* [@ya-ponchik](https://github.com/ya-ponchik)
### Тест, консультации
* ghard - [vk.com/id285852849](https://vk.com/id285852849)
* Алексей Могучев - [vk.com/id319494094](https://vk.com/id319494094)

# Технические подробности

- Террейн представляет собой [набор полигонов](https://github.com/ya-ponchik/wormix-html5-clone/blob/main/public/villianBase.json). Написан небольшой скрипт, который может преобразовывать некоторые экспортированные из оригинальной игры [векторные изображения](https://raw.githubusercontent.com/ya-ponchik/wormix-html5-clone/main/public/wormix/levels/treesRewamp/ground.svg) в него.
- Отвязанные от FPS рендера анимациии. Используются оригинальные векторные кадры из игры, что дает возможность динамически менять контент в них — убирать лишние лапы, менять шапки и артефакты.
- Игровая логика вынесена в отдельный поток (Web Worker) и, как следствие, рендер отвязан от игры — что вроде как круто.

# Похожие проекты
Я, признаться, в их код не заглядывал — не интересно.

- [https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone](https://github.com/CiaranMcCann/Worms-Armageddon-HTML5-Clone)
- [https://github.com/search?q=wormix&type=](https://github.com/search?q=wormix&type=)
- [https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=TypeScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories](https://github.com/search?l=JavaScript&q=destructible+terrain&type=Repositories)
- [https://github.com/search?q=worms+game&type=repositories](https://github.com/search?q=worms+game&type=repositories)
- [https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com](https://www.google.ru/search?q=worm+like+terrain+site:www.reddit.com)
- [https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com](https://www.google.ru/search?q=worm+like+terrain+site:gamedev.stackexchange.com)
