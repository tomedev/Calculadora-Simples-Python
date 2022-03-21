<h1> Calculadora-Simples-Python</h1>

from tkinter import *

<p>
root =tk()<br/>
root.title("Calculadora")<br/>
<p>
def click_soma():<br/>
  primeiro_numero = visor.get()<br/>
	global p_numero<br/>
	global matematica<br/>
	matematica = "soma"<br/>
	p_numero = float(primeiro_numero)<br/>
	visor.delete(0, END)<br/>
def click_sub():<br/>
	primeiro_numero = visor.get()<br/>
	global p_numero<br/>
	global matematica<br/>
	matematica = "subtracao"<br/>
	p_numero = float(primeiro_numero)<br/>
	visor.delete(0, END)<br/>
<p>
def click_div():<br/>
	primeiro_numero = visor.get()<br/>
	global p_numero<br/>
	global matematica<br/>
	matematica = "divisao"<br/>
	p_numero = float(primeiro_numero)<br/>
	visor.delete(0, END)<br/>
  <p>
def click_mult():<br/>
	primeiro_numero = visor.get()<br/>
	global p_numero<br/>
	global matematica<br/>
	matematica = "multiplicacao"<br/>
	p_numero = float(primeiro_numero)<br/>
	visor.delete(0, END)<br/>
<p>
def click_igual():<br/>
	segundo_numero = visor.get()<br/>
	visor.delete(0, END)<br/>
	if matematica == "soma":<br/>
		visor.insert(0, p_numero + float(segundo_numero))<br/>
	if matematica == "subtracao":<br/>
		visor.insert(0, p_numero - float(segundo_numero))<br/>
	if matematica == "multiplicacao":<br/>
		visor.insert(0, p_numero * float(segundo_numero))<br/>
	if matematica == "divisao":<br/>
		visor.insert(0, p_numero / float(segundo_numero))<br/>


<p>
def deletar():<br/>
	visor.delete(0,END)<br/>
<p>
def click_ponto():<br/>
	visor.insert(END, ".")<br/>

<p>
def click_button(numero):<br/>
	atual= visor.get()<br/>
	visor.delete(0,END)<br/>
	visor.insert(END, str(atual) + str(numero))<br/>

<p>
bt1=Button(root, text="1", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(1))<br/>
bt1.place(x=10, y=100)<br/>
<P>
bt2=Button(root, text="2", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(2))<br/>
bt2.place(x=10, y=155)<br/>
<p>
bt3=Button(root, text="3", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(3))<br/>
bt3.place(x=10, y=210)<br/>
<p>
bt0=Button(root, text="0", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(0))<br/>
bt0.place(x=10, y=265)<br/>

<p>
bt4 = Button(root, text="4", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(4))<br/>
bt4.place(x=60, y=100)<br/>
<p>
bt5 = Button(root, text="5", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(5))<br/>
bt5.place(x=60, y=155)<br/>
<p>
bt6 = Button(root, text="6", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(6))<br/>
bt6.place(x=60, y=210)<br/>
<p>
bpoint = Button(root, text ".", bg="lightblue", pady=44, pady=14, command=click_ponto())<br/>
bpoint.place(x=60, y=267)<br/>
<p>
bt7 = Button(root, text="7", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(7))<br/>
bt7.place(x=110, y=100)<br/>
<p>
bt8 = Button(root, text="8", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(8))<br/>
bt8.place(x=110, y=155)<br/>
<p>
bt9 = Button(root, text="9", bg="lightblue", pady=14, padx=14, bd=4, command=_lambda: click_button(9))<br/><br/>
bt9.place(x=110, y=210)
<p>
btsoma = Button(root, text="+", bg="lightblue", pady=14, padx=14, bd=4, command=click_soma)<br/>
btsoma.place(x=160, y=100)<br/>
<p>
btsub = Button(root, text="-", bg="lightblue", pady=14, padx=14, bd=4, command=click_sub)<br/>
btsub.place(x=160, y=155)<br/>
<p>
btmult = Button(root, text="x", bg="lightblue", pady=14, padx=14, bd=4, command=click_mult)<br/>
btmult.place(x=160, y=210)<br/>
<p>
btdiv = Button(root, text="/", bg="lightblue", pady=14, padx=14, bd=4, command=click_div)<br/>
btdiv.place(x=160, y=265)<br/>
<p>
btce = Button(root, text="CE", bg="lightblue", pady=119, padx=14, bd=4, command= deletar)<br/>
btce.place(x=210, y=100)<br/>
<p>
btigual = Button(root, text="=", bg="lightblue", pady=14, padx=119, bd=4, command=click_igual)<br/>
btigual.place(x=10, y=320)<br/>

<p>
lb1 = Label(root, text="CALCULADORA", font=("verdana", 20, "bold"), pady=10)  #bold negrito<br/>
lb1.pack()<br/>
<p>
visor = Entry(root, bg="lightblue")<br/>
visor.pack()<br/>
<p>
root.resizable(false, false)<br/>
root.geometry("288x388")<br/>
root.mainloop()<br/>

