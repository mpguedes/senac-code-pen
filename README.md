# senac-code-pen
Aula Senac CodePen

Acessar o site [Code Pen](https://codepen.io/)

Iniciar com os seguintes conteúdos:

### HTML
```html
<button class="button-001" value="Teste" onclick="userAction()">Teste</button>
<hr/>
<div class="div-001" id="container">-</div>
```

### CSS
 ```css
body {
  font-family: Courier;
}
.button-001 {
  color: red;
  font-family: Courier;
}
.div-001 {
  color: blue;
}
 ```
 
 ### JS
 ```javascript
const userAction = async () => {
   const div = document.getElementById("container");
   div.innerHTML = "Consultando....";
   const response = await fetch('https://api.exchangerate.host/latest');
   const myJson = await response.json(); 
   const brl = myJson["rates"]["BRL"];
   div.innerHTML = `1 Euro vale ${new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(brl)} hoje`; 
}
 ```
