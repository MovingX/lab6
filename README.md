<h1 align="center"> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<p align="center">Лабораторная работа №6 "CSS" </p>

<p align="right">Выполнил: Морошкин Максим Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">Лабораторная работа по созданию скриптов на языке JavaScript.</p>

<h2>Цели и задачи</h2>
1.	Придумайте селектор, который выберет абзацы ’p’ внутри дивов ’div’. <br>
2.	Придумайте селектор, который выберет все ’h2’ внутри дивов ’div’.<br>
3.	Придумайте селектор, который выберет все абзацы ’p’ из элемента с id=test.<br>
4.	Придумайте селектор, который выберет все ’h2’ из элемента с id=test.<br>
5.	Выберите все элементы с классом bbb.<br>
6.	Выберите все элементы с классом bbb из элемента с id=test.<br>
7.	Выберите все абзацы ’p’ с классом bbb.<br>
8.	Выберите все ’h2’ с классом bbb.<br>
9.	Выберите все абзацы ’p’ с классом bbb из элемента с id=test.<br>
10.	Выберите все элементы с классом bbb и элементы с классом xxx одновременно.<br>
11.	Выберите все абзацы ’p’ с классом bbb и ’h2’ с классом xxx одновременно.<br>
12.	Выберите все абзацы ’p’ с классом bbb из id=test и все абзацы ’p’ с классом xxx из id=test одновременно.<br>
13.	Выберите все элементы из класса fff.<br>
14.	Выберите все абзацы ’p’ из класса fff.<br>
15.	Выберите все абзацы ’p’ с классом fff.<br>
16.	Выберите все элементы с классом bbb из класса fff.<br>
17.	Выберите все ’h2’ с классом bbb из класса fff.<br>
18.	Сделайте селектор, который выберет все ссылки из id=test, с состояния link и visited сделайте неподчеркнутыми и красными, а состояние hover - подчеркнутым и голубым.<br>
19.	 Сделайте селектор, который выберет все ссылки с классом www, состояния link и visited сделайте подчеркнутыми и голубыми, а состояние hover - неподчеркнутым.<br>
20.	 Сделайте селектор, который выберет все ссылки из id=test с классом www. Цвета состояний выберите самостоятельно.<br>
21.	 Сделайте селектор, который выберет все ссылки из class=eee с классом www. Цвета состояний выберите самостоятельно.<br>
22-27. Повторите страницу по данному по образцу<br>

<h2>Решение задач</h2>


```html
<pre>
  <style>
				
				#test a:link, #test a:visited {
					color: red;
					text-decoration: none;
				}
				
				#test a:hover {
					color: blue;
					text-decoration: underline;
				}
				
				
				
				a.www:link, a.www:visited {
					color: blue;
					text-decoration: underline;
				}
				
				a.www:hover {
					text-decoration: none;
				}
				
				
				#test a.www:link,#test a.www:visited {
					color: red;
					text-decoration: none;
				}
				
				#test a.www:hover {
					color: blue;
					text-decoration: underline;
				}
				
				
				.eee a.www:link,.eee a.www:visited {
					color: blue;
					text-decoration: underline;
				}
				
				.eee a.www:hover {
					color: black;
					text-decoration: none;
				}				
				
			</style>
			
			<!--1.Селектор: div p{}-->
			<div>
				<p>Text</p>
			</div>
			
			<!--2.Селектор: div h2{}-->
			<div>
				<h2>Heading</h2>
			</div>
			
			<!--3.Селектор: #test p{}-->
			<div id="test">
				<p>Text</p>
			</div>
			
			<!--4.Селектор: #test h2{}-->
			<div id="test">
				<h2>Heading</h2>
			</div>
			
			<!--5.Селектор:.bbb{}-->
			<div class="bbb">Text</div>
			
			<!--6.Селектор: #test .bbb{}-->
			<div id="test">
				<div class="bbb">Text</div>
			</div>
			
			<!--7.Селектор: p.bbb{}-->
			<p class="bbb">Text</p>
			
			<!--8.Селектор: h2.bbb{}-->
			<h2 class="bbb">Heading</h2>
			
			<!--9.Селектор: #test p.bbb{}-->
			<div id="test">
				<p class="bbb">Text</p>
			</div>
			
			<!--10.Селектор: .bbb,.xxx{}-->
			<div class="bbb">Text</div>
			<div class="xxx">Heading</div>
			
			<!--11.Селектор: p.bbb,h2.xxx{}-->
			<p class="bbb">Text</p>
			<h2 class="xxx">Heading</h2>
			
			<!--12.Селектор: #test p.bbb,#test p.xxx{}-->
			<div id="test">
				<p class="bbb">Text</p>
				<p class="xxx">Heading</p>
			</div>
			
			<!--13.Селектор: .fff{}-->
			<div class="fff">Text</div>
			
			<!--14.Селектор: .fff p{}-->
			<p class="fff">Text</p>
			
			<!--15.Селектор: p.fff{}-->
			<p class="fff">Text</p>
			
			<!--16.Селектор: .fff.bbb{}-->
			<div class="fff">
				<div class="bbb">Text</div>
			</div>	
			
			<!--17.Селектор: .fff h2.bbb{}-->
			<div class="fff">
				<h2 class="bbb">Heading</h2>
			</div>
			
			<!--18.Селектор: #test a:link, #test a:visited-->
			<div id="test">
				<a href="#" class="www">Link</a>
				<a href="#" class="www">Visited link</a>
			</div>
			
			<!--19.Селектор: a.www:link, a.www:visited-->
			<a href="#" class="www">Link</a>
			<a href="#" class="www">Visited link</a>
			
			<!--20.Селектор: #test a.www:link,#test a.www:visited{}-->
			<div id="test">
				<a href="#" class="www">Ссылка с классом www внутри элемента с id=test</a>
			</div>
			
			<!--21.Селектор: .eee a.www:link, .eee a.www:visited{}-->
			<div class="eee">
				<a href="#" class="www">Ссылка с классом www внутри элемента с классом eee</a>
			</div>
      
  <style>
				.frame{
					margin:auto;
					border: 2px dotted black;
					width: 500px;
					height: auto;
					text-align: justify;
					margin-bottom: 20px;
				}
				
				.task23{
					margin-left: 10px;
					margin-top: 10px;
					margin-bottom: 10px;
					border: 1px solid red;
					width: 100px;
					height: 100px;	
				}
				
				.task24{
					margin-left: 10px;
					margin-top: 10px;
					margin-bottom: 10px;
					border: 2px dotted blue;
					width: 300px;
					height: 100px;
				}
				
				.task25{
					margin-left: 10px;
					margin-top: 10px;
					margin-bottom: 10px;
					border: 2px dotted green;
					border-radius: 10px 20px 10px 20px;
					width: 200px;
					height: 200px;	
				}
				
				.task26{
					margin-left: 10px;
					margin-top: 10px;
					margin-bottom: 10px;
					border: 1px solid red;
					border-radius: 100px;
					width: 100px;
					height: 100px;	
				}
				
			</style>
			
			<div class="frame">
				<p style="text-decoration: underline">Привет мир!</p>
				<p style="text-decoration: line-through">Привет мир!</p>
				<p style="text-decoration: overline">Привет мир!</p>
			</div>
			
			<div class="frame">
				<div class="task23"> </div>
			</div>
			
			<div class="frame">
				<div class="task24"> </div>
			</div>
			
			<div class="frame">
				<div class="task25"> </div>
			</div>
			
			<div class="frame">
				<div class="task26"> </div>
			</div>		

			<div class="frame">
				<p><a href="#" style="margin-left:10px; text-decoration:underline; color:green;">ссылка</a></p>
				<p><a href="#" style="margin-left:10px; text-decoration:underline; color:red;">ссылка</a></p>
				<p><a href="#" style="margin-left:10px; text-decoration:none; color:black;">ссылка</a></p>
			</div>
</pre>
```
<p>Задачи CodeWars</p>

```JavaScript
1 Задача CodeWars
function add(...args) {
  if (args.length == 0) {
    return 0;
  }
  var sum = 0;
  for (var i = 0; i < args.length; i++) {
    sum += args[i] / (i + 1);
  }
  return Math.round(sum);
}
```

<h2>Вывод</h2>
Я научился работать с классами, тэгоми, селекторами.
