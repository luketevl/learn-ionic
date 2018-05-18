# IONIC FRAMEWORK

## MODULO 4

### COMANDOS 
- Executa um servidor para EXECUTAR no **navegador**
```shell
ionic serve
ionic serve --lab
```

- Executa o APP em um **SIMULADOR EMULADOR(ios, android)**
  - Executa o código, baixa os pacotes e abre no emulador
```shell
ionic emulate ios
ionic emulate android
```

- Executa o APP no **CELULAR(ios, android)**
  - Executa o código, baixa os pacotes e executa no celular via USB
```shell
ionic run ios --device
ionic run android --device
```

- Adiciona uma nova plataforma (ios, android, web)
  - Instalar os recursos necessários
```shell
ionic platform add ios
ionic platform add android
```

- Atualizar uma plataforma (ios, android, web)
```shell
ionic platform update ios --save
ionic platform update android --save
```

- Lista uma nova plataforma (ios, android, web)
```shell
ionic platform list
```


### REST
- **Recurso** é tudo aquilo que pode salvar
  - Produtos
  - Categorias
- Utiliza as seguintes **ações**
  - **POST** | Cria um novo(recurso)
    - Envia os DADOS no **CORPO(Body)**
    - Precisa enviar TODOS os dados
    - Exemplo: http://pucminas.br/matriculas/
  - **PUT** | Edita uma informação(recurso) existente
    - Envia os DADOS no **CORPO(Body)** e o **id** no **GET(URL)**
    - **NÃO** Precisa enviar TODOS os dados
    - Exemplo: http://pucminas.br/alunos/33
  - **GET** | Busca dados(recursos)
    - Exemplo: http://pucminas.br/cursos/
  - **DELETE** | Apaga recurso
    - Exemplo: http://pucminas.br/matriculas/3422
- Exemplos de **recursos**
  - `caminho/recurso/` | Busca uma lista de **recursos**
  - `caminho/recurso/id`| Busca um **recurso**

### PROMISE
- Usada para chamadas de funções **ASSINCRONAS**
- Possui **2** metodos:
  - **then**(quando termina o ajax)
  - **catch**(quando acontece algum erro ajax)
```js
  this.http.get('http://teste.com/tarefas')
    .toPromise()
    .then( function(resposta){
      let dados = resposta.json();
    })
    .catch( function(erro){
      console.log(erro);
    })
```
> Permite tratar **respostas ASSÍNCRONAS** por meio de funções de **RESOLUÇÃO(resolve)** e de **REJEIÇÃO(rejection)**.



### HTTP
- Para fazer requisições e necessário importar e chama-lo no construtor
```js
import { Http } from '@angular/http';

constructor(public: http : Http){}
```
- Busca um recurso
```js
this.http.get('http://teste.com/tarefas');
```
### CICLO DE VIDA
- Quando a classe for **CRIADA** `constructor`
  - Se atualizar os dados de uma tela que **JÁ FOI CARREGADA** ele não irá atualizar a listagem por exemplo.
```js
constructor(){}
```
- Quando a página  **FOI CARREGADA** `ionViewDidEnter`
  - Sempre chama quando ENTRAR na TELA, ou seja se atualizar um dado e voltar na tela aquele dado será atualizado.
```js
ionViewDidEnter(){}
```

### PACOTES
- **ionic-angular** 
  - Um conjunto de **COMPONENTES** para a **criação e controle de uma aplicação híbrida**
- **ionic-native**
  - Um conjunto de **RECURSOS** para acesso a **RECURSOS NATIVOS** dos dispositivos

### Observações
- Podemos converter **Observable** para **Promise**
  - Para devemos importar o `toPromise` e chama-lo
```js
import 'rxjs/add/operator/toPromise';
this.http.get('http://teste.com/tarefas')
    .toPromise()
```
- Caso apareça assim: `constructor(private callNumber: CallNumber) { }`` use o nome em minusculo `callNumber`