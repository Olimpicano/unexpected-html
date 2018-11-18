# Адаптивная верстка

Наш сайт может оказаться на совершенно различных устройствах: компьютеры, телевизоры, ноутбуки, планшеты, мобильные.
Конструкция  media позволяет подключать различные участки CSS, для различных ситуаций

@media screen and (min-width: 480px) {
	body {
		background-color: lightgreen;
	}
}
В данном случае, если наш сайт окажется на экране(screen), с шириной от 480px к нему применится цвет фона lightgreen

Мы можем формировать целые условия
@media all and (max-width: 699px) and (min-width: 520px) {
  #sidebar ul li a {
    padding-left: 21px;
    background: url(../images/email.png) left center no-repeat;
  }
}
ИЛИ
Выставляется через запятую

@media (max-width: 600px), (min-width: 800px) {
  html { background: red; }
}

Практика
1) Изменение цвета блока при сужении
2) Изменение фоновой фотографии с горизонтальной на вертикальную при сужении
3) Замена меню на иконку при сужении
4) Создание адаптивного шаблона
 

Viewport
На мобильных устройствах сайт строится не под реальный физический экран, а под виртуальный, так называемый viewport

Например, на iPhone 4s ширина устройства 240px,  но сайт будет строиться под 980px. Это может привести к тому, что наши условия для адаптивности не сработают

Чтобы изменить ситуацию воспользуемся meta-тегом viewport и установим ширину виртуального экрана под количество пикселей на устройстве
<meta name="viewport" content="width=device-width, initial-scale=1.0">

Если наш сайт и так хорошо смотрится на устройстве, мы можем выставить блокировку увеличения экрана

<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

orientation
Мобильное устройство может находится в двух режимах портретный и альбомный
Добавляем учет ориентации устройства в пространстве
@media (orientation: landscape) {
	Background-color:red;

}

Для устройств с высокой плотностью пикселей можем воспользоваться свойством resolution


Эмулятор Android
developer.android.com/sdk/index.html


