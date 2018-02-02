# Selenium JavaScript
Instalação de selenium utilizando Node.JS

## Instalar/Baixar

### Java JRE

Link: https://www.java.com/pt_BR/download/

### Selenium standalone

Link: http://www.seleniumhq.org/download/

Deve ser salvo em uma pasta de facil acesso.

EX: C:\selenium

Abrir Prompt de Comando > Acessar pasta aonde está localizado o standalone > executar comando: java -jar {version}.jar

O standalone deve ser iniciado antes de rodar os testes.

### Navegadores

#### Google Chrome

Baixar ultima versão disponível.

Link: http://www.seleniumhq.org/download/

Deve ser salvo na pasta raiz do projeto a ser testado.

Ex:C:\selenium\modelo\

#### Firefox

Baixar ultima versão disponível.

Link: http://www.seleniumhq.org/download/

Deve ser salvo na pasta raiz do projeto a ser testado.

Ex:C:\selenium\modelo\

### Node

Link: https://nodejs.org/en/download/

Node é necessário pra rodar os teste em JS.

## Modelo de teste

### Pastas

Cada projeto deve ter seu conjunto de JS de teste.

### JavaScript

Documentação: http://seleniumhq.github.io/selenium/docs/api/javascript/module/selenium-webdriver/index.html

Ex:C:\selenium\modelo\modelo.js

modelo.js
```
var webdriver = require('selenium-webdriver'),
	By = webdriver.By,
	until = webdriver.until;

var driver = new webdriver.Builder()
     .forBrowser('firefox')
     .build();

console.log("Iniciando teste dos recursos do selenium-webdriver");
driver.get("https://www.google.com.br/");
driver.wait(until.elementLocated(By.id('lst-ib')), 5000);
driver.findElement(webdriver.By.id('lst-ib')).sendKeys('abacomm');
driver.findElement(webdriver.By.name('btnK')).click();
driver.sleep(2000);
driver.findElement(webdriver.By.linkText("Abacomm: Home")).click();
driver.sleep(5000);

driver.quit();
``` 

### IDE Selenium

#### Katalon

Dever instalar extensão no navegador firefox para gravar e exportar testes.



