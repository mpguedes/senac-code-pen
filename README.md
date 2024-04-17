# senac-code-pen
Aula Senac CodePen

Acessar o site [CODEPEN](https://codepen.io/)

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
   const response = await fetch('https://api.freecurrencyapi.com/v1/latest?apikey=fca_live_Y1R9HTwgr7yG7Runcn6CNgM4gVMGUa3vnuZ9xVUl');
   const myJson = await response.json(); 
   const brl = myJson["data"]["BRL"];
   div.innerHTML = `1 Dollar vale ${new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(brl)} hoje`; 
}
 ```
