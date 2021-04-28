Глава 6 CSS Сетки стр. 181

	chrome://flags
	Experimental Web Platform Features
	Эксперементальные возможности в хром

	fr аналогичен flex-grow но можно использовать и др ед измерения px, em, %.

	grit-gap: x y;//Промежутки

	grid-template-columns
	grid-template-rows

	grid-column
	grid-row

	grid-row: span 1;//Занять одну полосу сетки (автоматически)	
	

6.3.1. Присвоение имен линиям сетки.

	grid-template-columns: [start] 2fr [center] 1fr [end];
 	grid-template-columns: start/center; 

 	grid-template-rows: repeat(4, [row] auto);//дает имена линиям кроме последней (repeat без пробела);

 	grid-template-columns: 
 				[left-start] 2fr 
 				[left-end right-start] 1fr 
 				[right-end];
 	//Можно использовать left(left-start left-end) right(right-start right-end)

 	grid-template-columns: repeat(3, [col] 1fr 1fr);
 	grid-column: col 2 / span 2;


6.3.2. Присвоение имен областям сетки.

	grid-template-areas:
	grid-area:

	Каждая именованая область должна формировать прямоугольник.

	Можно оставить ячейку пустой задействуя точку в качестве имени.


6.4 Явная и неявная сетки.

	grid-auto-columns//Указание размерности неявных полос сетки
	grid-auto-rows

	<figure>
		<img/>
		<figcaption>Подпись к картинке</figcaption>
	</figure>

	grid-template-columns: repeat(auto-fill, minmax(200px, 2fr));
		minmax(200px, 1fr);//Ширина полосы не менее 200px
		auto-fill//Заполнить колонками протстранство без нарушения minmax
		auto-fit//Заполнить пространство путем растяжения непустых колонок

	grid-auto-flow: row(def)
									column
									dense
									row dense
									column dense
		//Автоматически заполняет строки столбцы или более мелкие перемещает как угодно для лучшего заполнения.

	img{
		object-fit: fill(def)//Размер изменяется до заполнения контейнера 
								contain//Размер изменяется для умещения изображения
								cover//Размер изменяется до заполнения контейнера(без искажений но часть изображения будет обрезана)
	}	

	@supports (объявление){правила}//Применяются правила если поддерживается объявление.
	@supports not(){}//Применяются правила если не поддерживается объявление.
	@supports not() or(){}//Применять правило если поддерживается хотябы одно объявление.
	@supports not() and(){}//Применять правило если поддерживается если поддерживаютя оба объявления.


6.6 Выравнивание. стр. 213
	
	Контейнер сетки (элементы внутри областей сетки):
	justify-items - горизонтально
	align-items 	- вертикально

	Контейнер сетки (полосы сетки внутри контейнера):
	justify-content	- горизонтально
	align-content		- вертикально

	Элемент сетки (элемент внутри области сетки):
	justify-self
	align-self


Итоги главы:
	- Использовать css сетку совместно с flexbox;
	- Использовать свойства auto-fill auto-fit и неявные сетки для создания разметки с неизвестным количеством элементов;
	- Применять запросы функций для пронгрессивного усовершенствования.
	