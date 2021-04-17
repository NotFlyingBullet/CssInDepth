Глава 5. Flexbox-верстка. стр.149
	
	display: flex; //Превращает элемент во flex контейнер, а его потомков во flex элементы.

	Возможно использование inline-flex;

	Главная и поперечная оси.

	> комбинатор прямых потомков.

	Autoprefixer github.com/postcss/autoprefixer

	Превращать ссылку в блок для добавления высоты родительския элементам.

	.site-nav>li>a{} Пременять стили к <a> не к <li>.

	margin-left: auto;// Сдвиг вправо.

	.login-forminput: not([type=checkbox]):not([type=radio]){}
	псевдокласс :not() 
	селектор атрибутов: [type=radio]


	Свойства Flex контейнеров

	flex-direction: row column -reverse;

	flex-wrap: wrap nowrap wrap-reverse; 
	
	flex-flow: <fd><fw>;
	
	justify-content: flex-start flex-end center space-between space-around   

	aligne-items: flex-start flex-end center stretch baseline;

	aline-content: flex-start flex-end center stretch space-between space-around


	Свойства flex элементов 

	flex-grow: >=0; [def:0]

	flex-shrink: >=0; [def:1]

	flex-basis: как width если 0 то auto (px % em) [def:auto]

	flex: <flex-grow> <flex-shrink> <flex-basis>;

	align-self: auto flex-start flex-end center stretch baseline;

	order: >=0; [def:0]


	flexbox верстку начинают с:
	- display: flex;
	- flex-direction;
	- объявить поля и размеры flex элементов.

	Итоги главы:

	- Использовать autoprefixer;
	- Задействовать свойства aligne-items aligne-self для ветикального центрирования flex элементов.