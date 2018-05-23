---
layout: page
title: Tick-tock. Tick-tock.
description: Self reminder.
keywords: self reminder, manifesto, tick-tock
---

<div class="clock-container">
<div class="clock">
  <div class="block" data-num="0"></div>
  <div class="block" data-num="1"></div>
  <div class="block" data-num="2"></div>
  <div class="block" data-num="3"></div>
  <div class="block" data-num="4"></div>
  <div class="block" data-num="5"></div>
  <div class="block" data-num="6"></div>
  <div class="block" data-num="7"></div>
  <div class="block" data-num="8"></div>
  <div class="block" data-num="9"></div>
  <div class="block" data-num="10"></div>
  <div class="block" data-num="11"></div>
  <div class="block" data-num="12"></div>
  <div class="block" data-num="13"></div>
  <div class="block" data-num="14"></div>
  <div class="block" data-num="15"></div>
  <div class="block" data-num="16"></div>
  <div class="block" data-num="17"></div>
  <div class="block" data-num="18"></div>
  <div class="block" data-num="19"></div>
  <div class="block" data-num="20"></div>
  <div class="block" data-num="21"></div>
  <div class="block" data-num="22"></div>
  <div class="block" data-num="23"></div>
  <div class="block" data-num="24"></div>
  <div class="block" data-num="25"></div>
  <div class="block" data-num="26"></div>
  <div class="block" data-num="27"></div>
  <div class="block" data-num="28"></div>
  <div class="block" data-num="29"></div>
  <div class="block" data-num="30"></div>
  <div class="block" data-num="31"></div>
  <div class="block" data-num="32"></div>
  <div class="block" data-num="33"></div>
  <div class="block" data-num="34"></div>
  <div class="block" data-num="35"></div>
  <div class="block" data-num="36"></div>
  <div class="block" data-num="37"></div>
  <div class="block" data-num="38"></div>
  <div class="block" data-num="39"></div>
  <div class="block" data-num="40"></div>
  <div class="block" data-num="41"></div>
  <div class="block" data-num="42"></div>
  <div class="block" data-num="43"></div>
  <div class="block" data-num="44"></div>
  <div class="block" data-num="45"></div>
  <div class="block" data-num="46"></div>
  <div class="block" data-num="47"></div>
  <div class="block" data-num="48"></div>
  <div class="block" data-num="49"></div>
  <div class="block" data-num="50"></div>
  <div class="block" data-num="51"></div>
  <div class="block" data-num="52"></div>
  <div class="block" data-num="53"></div>
  <div class="block" data-num="54"></div>
  <div class="block" data-num="55"></div>
  <div class="block" data-num="56"></div>
  <div class="block" data-num="57"></div>
  <div class="block" data-num="58"></div>
  <div class="block" data-num="59"></div>
  <div class="divider"></div>
</div>
</div>
<script>
const numbers = [
	[1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1],
	[1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 1],
	[1, 0, 1, 1, 1, 1, 0, 1, 0, 1, 1, 1, 1, 0, 1],
	[1, 0, 1, 0, 1, 1, 0, 1, 0, 1, 1, 1, 1, 1, 1],
	[1, 1, 1, 0, 0, 0, 0, 1, 0, 0, 1, 1, 1, 1, 1],
	[1, 1, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 1, 1, 1],
	[1, 1, 1, 1, 1, 1, 0, 1, 0, 1, 1, 0, 1, 1, 1],
	[1, 0, 0, 0, 0, 1, 0, 1, 1, 1, 1, 1, 0, 0, 0],
	[1, 1, 1, 1, 1, 1, 0, 1, 0, 1, 1, 1, 1, 1, 1],
	[1, 1, 1, 0, 1, 1, 0, 1, 0, 1, 1, 1, 1, 1, 1]
];

const blocks = [];
const digits = Array.from(document.querySelectorAll('.block'));

for (let i = 0; i < 4; i++) {
	blocks.push(digits.slice( i * 15, i * 15 + 15 ));
}

const setNum = (block, num) => {
	let n = numbers[num];
	for (let i = 0; i < block.length; i++) {
		 block[i].classList[ n[i] === 1 ?  'add' : 'remove']('active');
	}
};

const time = {
	s: '',
	m: '',
	h: '',
	p: null
};

const animator = () => {
	let d = new Date(),
		 h = d.getHours().toString(),
		 m = d.getMinutes().toString(),
		 s = d.getSeconds().toString();

	s = s.length === 1 ? '0' + s : s;
	m = m.length === 1 ? '0' + m : m;
	h = h.length === 1 ? '0' + h : h;
	
	if (s !== time.s) {
		for (let i = 0; i < digits.length; i++) {
			let d = digits[i];
			if (i === +s) {
				d.classList.add('second');
				if (time.p !== null)
					digits[time.p].classList.remove('second');
				time.p = i;
				time.s = s;
			}
		}
	}
	
	if (m !== time.m) {
		setNum(blocks[2], m[0]);
		setNum(blocks[3], m[1]);
		time.m = m;
	}
	
	if (h !== time.h) {
		setNum(blocks[0], h[0]);
		setNum(blocks[1], h[1]);
		time.h = h;
	}
 	window.requestAnimationFrame(animator);
};

window.requestAnimationFrame(animator);
</script>

```
El tiempo es lo mas importante
Tiempo no es dinero
Tiempo es igual a vida
Solo tenemos una oportunidad para hacerlo bien
Cada ser humano esta luchando una batalla interna
Es una obligacion ayudar e inspirar a otros
Sin importar que se haga,
Siempre se puede inspirar a alguien a hacer algo bueno
Nadie es mejor que nadie.
No soy mejor que alguien mas.
Humildad

Estar en la zona de confort es maravilloso,
pero nada crece alli.
Mantente estudiando.
Mantente creando.
Siempre habra alguien que te odiara por tener la tenecidad de crear algo nuevo.
No dejes que ellos te definan.
No dejes que ellos te detengan.
Solo bloquealos y sigue adelante.
No esperes que otros te hagan feliz.
Eres el unico responsable por tu felicidad.
No esperes al Viernes para disfrutar la vida.
Goza de cada cosa en la que estas presente.
Se amable con tus familiares.
Ellos te han dado muchas cosas.
Tener miles de personas admirandote no tiene ningun valor.
Si tu propia familia no te admira.
No sientas miedo por lo desconocido.
Teme por no conocer nada.
La vida es muy corta y cada dia cuenta.
Has lo que tengas que hacer ahora.
Tic-toc do pares
Tic-toc no esperes
```

<small style="opacity:0.5">Written by Zeno Rocha & Carol Moreschi.</small>
