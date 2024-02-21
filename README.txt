Главная страница:
- Доставка
(
Заголовок: Delivery
Текст:
At Milk Bliss, we proudly deliver premium dairy products across India. From bustling cities to tranquil countryside, we ensure timely delivery to every corner of the country.
Experience the convenience of shopping from home and enjoy our exceptional quality products delivered fresh to your doorstep. Join satisfied customers nationwide and let Milk Bliss bring bliss to your home.
)
Страница контактов:
- О нас
(
	Заголовок: About Milk Bliss
	Текст:
At Milk Bliss, our passion lies in creating dairy products that elevate every moment. Rooted in the belief that the purest ingredients yield the most exquisite flavors, we've dedicated ourselves to crafting premium-quality offerings that not only tantalize the taste buds but also nurture the body and soul.

Our commitment to excellence transcends product creation; it encompasses every facet of our operations. From meticulously sourcing ingredients to embracing sustainable practices, we uphold integrity and environmental stewardship. Transparency is paramount as we endeavor to foster trust through unwavering dedication to quality and service.

Yet, Milk Bliss is more than a mere brand; it's a thriving community. We deeply value the relationships forged with our customers, partners, and team members, recognizing their invaluable support. Together, we revel in life's simple pleasures, savoring each delightful sip.

Embark on our journey to spread joy through dairy, and immerse yourself in the blissful world of Milk Bliss.
)
- Контакты
Phone number: +91-241-8371386
Address: Ground, 1st And 2,d Floor, Lily Trade, Jahangirabad, Neelam Park, Madhya Pradesh, India
Email: milkbliss@gmail.com
Страница о нас
- Наша продукция

Документация: 

//------------------------------------------------------------------------------

Команды терминала

Установка:
npm i
или
npm i --legacy-peer-deps
(i) флаг --legacy-peer-deps позволит продолжить установку при возникновении 
конфликтов зависимостей (версий пакетов).

Запуск режима разработчика (c запуском сервера)
npm run dev

Запуск сборки проекта (без запуска сервера, только финальная сборка)
npm run build

Запуск сборки проекта и выгрузка результата на сервер по FTP. (без запуска локальконо сервера)
Конфигурация FTP находится в файле config/gulp-settings.js
npm run deploy

Запуск сборки проекта и создание zip архива с именем проекта. (без запуска локальконо сервера)
npm run zip

Запуск сборки проекта но без создания webp картинок. (без запуска сервера, только финальная сборка)
npm run devbuild

Запуск создания SVG спрайта. Иконки нужно положить в папку src/svgicons,
готовый спрайт появится в папке src/img/icons/icons.svg
Изменения в папке src/svgicons не отслеживаются в dev режиме, при необходимости можно запустить повтоврую сборку спрайта
запускать создание спрайта стоит перед началом работ командой:
npm run sprite

//------------------------------------------------------------------------------

Основные файлы для работы с шаблоном:
js/app.js
scss/style.scss

index.html - разводящая страница (содержание)
home.html - главная страница
файлы html/*.htm - подключаемые части

//------------------------------------------------------------------------------

Используются псевдонимы пути к папкам:
@img = src/img
@scss = src/scss
@js = src/js

Плагин для VS Code - Path Autocomplete
Настройки. Нажать в реждакторе F1, найти настройки Settings JSON, добавить код:
"path-autocomplete.pathMappings": {
	"@img": "${folder}/src/img", // псевдоним для папки img
	"@scss": "${folder}/src/scss", // псевдоним для папки scss
	"@js": "${folder}/src/js", //  псевдоним для папки js
}

//------------------------------------------------------------------------------

При возникновении ошибок убедитесь что:
1) У вас установлен Node.js последней версии
2) Терминал открыт с правами администратора
3) В названиях папок на всем пути к проекту нет символа # или !
4) Папки и файлы должны быть названы латиницей без пробелов
5) Тег img и его содержимое должны быть записаны в одну строку без переносов
6) В атрибуте src должен быть указан путь к существующей картинке

//------------------------------------------------------------------------------

Прочие проблемы и их решения:
//-----------------------------------
Ошибка "unable to resolve dependency tree"
Решение:
npm i --legacy-peer-deps
//-----------------------------------
Ошибка node-sass.
Решения:
npm rebuild node-sass
и/или
npm install sass gulp-sass --save-dev
//-----------------------------------
Ошибка Python
Решени:
npm install --global windows-build-tools
//------------------------------------------------------------------------------