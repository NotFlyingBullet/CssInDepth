Глава 14 Переходы.

	transition: color 0.3s linear 0.5s;
	transition-property - свойства
	transition-duretion - продолжитльность
	transition-function - функция времени
	transition-delay - задержка

	для времени 0 обязательно указывать размерность s ms.

	Функции времени:
	- ease-in ease-out linear..
	- cubic-bezier(0.57, 0.39, 0.82, 1.29);
	- steps().

	steps(2, end);// end def
	steps(2, start);
	cssrticks.com/clever-uses-step-easing/

	cubic-bezier.com

	visibility: hidden;//Удаляет элемент со страницы но оставляет в потоке.
	В отличие от display свойство анимируется.


Итоги главы:
- Ускоряющееся движение привлекает внимание;
- Замедляющееся движение для информирования, что действие вступило в силу.
 