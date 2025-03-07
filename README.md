# Digitalizar Documentos de Várias Páginas com AppGED - Indoor

**AppGED - Indoor** é um SDK projetado para digitalizar documentos de várias páginas. Ele integra a funcionalidade do **Dynamsoft Document Scanner (DDS)** enquanto oferece recursos adicionais, como gerenciamento de múltiplos documentos, anotações e upload, tornando-o uma solução abrangente para gerenciar fluxos de trabalho complexos de documentos.

> Veja em ação com a [Demonstração do AppGED - Indoor](https://pecsolucoes.appged/).

Este guia orienta você na construção de uma aplicação web que digitaliza documentos de várias páginas usando o **AppGED - Indoor**, com **configurações predefinidas**.

> Se você está procurando uma solução para digitalizar documentos de página única, leia o [Guia do Usuário do Dynamsoft Document Scanner](https://www.dynamsoft.com/mobile-web-capture/docs/guides/document-scanner.html) em vez disso.

**Índice**
- [Licença](#licença)
  - [Obter uma Licença de Avaliação](#obter-uma-licença-de-avaliação)
  - [Obter uma Licença Completa](#obter-uma-licença-completa)
- [Início Rápido](#início-rápido)
  - [Opção 1: Compilar a Partir do Código-Fonte](#opção-1-compilar-a-partir-do-código-fonte)
  - [Opção 2: Usar Script Pré-compilado](#opção-2-usar-script-pré-compilado)
- [Explicação do Exemplo Hello World](#explicação-do-exemplo-hello-world)
  - [Referenciar o AppGED - Indoor](#referenciar-o-appged---indoor)
  - [Instanciar o AppGED - Indoor](#instanciar-o-appged---indoor)
  - [Iniciar o AppGED - Indoor](#iniciar-o-appged---indoor)
- [Próximo Passo](#próximo-passo)

## Licença

### Obter uma Licença de Avaliação

Se você ainda não solicitou uma avaliação do **DDS**, pode experimentar o **AppGED - Indoor** solicitando uma licença de avaliação através do nosso [portal do cliente](https://www.dynamsoft.com/customer/license/trialLicense?product=mwc&source=guide). A avaliação pode ser renovada duas vezes, oferecendo até dois meses de acesso gratuito.

> O **DDS** e o **AppGED - Indoor** compartilham as mesmas chaves de licença. Se você já possui uma licença do **DDS**, pode usá-la para o **AppGED - Indoor**, e vice-versa.

### Obter uma Licença Completa

Para adquirir uma licença completa, [entre em contato conosco](https://www.dynamsoft.com/company/contact/).

## Início Rápido

Para usar o **AppGED - Indoor**, o primeiro passo é obter os **arquivos da biblioteca**. Você pode adquiri-los de uma das seguintes fontes:

1. [**GitHub**](https://github.com/Dynamsoft/mobile-web-capture) – Contém os arquivos de origem do SDK do **AppGED - Indoor**, que podem ser compilados em arquivos de biblioteca.
2. [**npm**](https://www.npmjs.com/package/dynamsoft-mobile-web-capture) – Fornece arquivos de biblioteca pré-compilados via **npm** para uma instalação mais fácil.
3. [**CDN**](https://cdn.jsdelivr.net/npm/dynamsoft-mobile-web-capture) – Disponibiliza arquivos de biblioteca pré-compilados através de um **CDN** para uma integração rápida e sem complicações.

Você pode escolher um dos seguintes métodos para configurar uma página **Hello World**:

1. **Compilar a Partir do Código-Fonte** – Baixe os arquivos de origem do **GitHub** e compile o script de recursos você mesmo.
2. **Usar Script Pré-compilado** – Utilize os scripts de recursos pré-compilados do **npm** ou do **CDN** para uma configuração mais rápida.

### Opção 1: Compilar a Partir do Código-Fonte

Esse método obtém todos os **arquivos de origem do AppGED - Indoor** a partir de seu [Repositório no GitHub](https://github.com/Dynamsoft/mobile-web-capture), compila-os em um pacote distribuível e, em seguida, executa uma página de exemplo **Hello World** pronta incluída no repositório.

Siga estes passos:

1. **Baixe** o **AppGED - Indoor** do [GitHub](https://github.com/Dynamsoft/mobile-web-capture) como uma pasta compactada.
   > Alternativamente, você pode [baixar o mesmo arquivo no site da Dynamsoft](https://www.dynamsoft.com/mobile-web-capture/downloads/).
2. **Extraia** o conteúdo do arquivo compactado.
3. **Abra** o diretório raiz em um editor de código.
   > Recomendamos usar o [VS Code](https://code.visualstudio.com) para acompanhar este guia, embora qualquer editor de código funcione.
4. **Insira** a chave de licença recebida em [Obter uma Licença de Avaliação](#obter-uma-licença-de-avaliação).
   > Abra o exemplo Hello World localizado em [`/samples/hello-world.html`](https://github.com/Dynamsoft/mobile-web-capture/blob/main/samples/hello-world.html). Procure por `"YOUR_LICENSE_KEY_HERE"` e substitua pela sua chave de licença real.
5. **Instale** as dependências do projeto
    No terminal, navegue até o diretório raiz do projeto e execute:
    ```bash
    npm install
    ```
6. **Compile** o projeto
    Após a instalação das dependências, compile o projeto executando:
    ```bash
    npm run build
    ```
7. **Sirva** o projeto localmente
    Inicie o servidor local executando:
    ```bash
    npm run serve
    ```
Quando o servidor estiver em execução, abra a aplicação em um navegador usando o endereço fornecido na saída do terminal após executar `npm run serve`.
> Veja os detalhes da configuração do servidor em [`/dev-server/index.js`](https://github.com/Dynamsoft/mobile-web-capture/blob/main/dev-server/index.js).

### Opção 2: Usar Script Pré-compilado

Como os **arquivos da biblioteca do AppGED - Indoor** estão publicados no [**npm**](https://www.npmjs.com/package/dynamsoft-mobile-web-capture), é fácil referenciá-los a partir de um CDN.

Para usar o script pré-compilado, simplesmente inclua a seguinte URL em uma tag `<script>`:
```html
<script src="https://cdn.jsdelivr.net/npm/dynamsoft-mobile-web-capture@3.0.1/dist/mwc.bundle.js"></script>
```

Abaixo está a página de exemplo **Hello World** completa que usa esse script pré-compilado de um CDN.
> Este código é idêntico ao arquivo [`/samples/hello-world.html`](https://github.com/Dynamsoft/mobile-web-capture/blob/main/samples/hello-world.html) mencionado na seção [Compilar a Partir do Código-Fonte](#opção-1-compilar-a-partir-do-código-fonte), exceto pela fonte do script.
>
> **Não se esqueça** de substituir `"YOUR_LICENSE_KEY_HERE"` pela sua chave de licença real.

```html
<!DOCTYPE html>
<html lang="pt">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>AppGED - Indoor - Hello World</title>
    <script src="https://cdn.jsdelivr.net/npm/dynamsoft-mobile-web-capture@3.0.1/dist/mwc.bundle.js"></script>
  </head>
  <body>
    <script>
      // Instanciar um Objeto AppGED - Indoor
      const appGEDIndoor = new Dynamsoft.MobileWebCapture({
        license: "DLS2eyJoYW5kc2hha2VDb2RlIjoiMTAzNzczMjYzLVRYbFhaV0pRY205cSIsIm1haW5TZXJ2ZXJVUkwiOiJodHRwczovL21kbHMuZHluYW1zb2Z0b25saW5lLmNvbSIsIm9yZ2FuaXphdGlvbklEIjoiMTAzNzczMjYzIiwic3RhbmRieVNlcnZlclVSTCI6Imh0dHBzOi8vc2Rscy5keW5hbXNvZnRvbmxpbmUuY29tIiwiY2hlY2tDb2RlIjotMzU0MDk1MjR9", // Substitua isso pela sua chave de licença real
      });
      (async () => {
        // Iniciar a Instância do AppGED - Indoor
        const fileName = `Novo_Documento_${Date.now().toString().slice(-5)}`;
        await appGEDIndoor.launch(fileName);
      })();
    </script>
  </body>
</html>
```

Para executar o exemplo, crie um novo arquivo chamado `hello-world.html`, copie e cole o código acima no arquivo. Em seguida, sirva a página diretamente implantando-a em um servidor.

Se você estiver usando o VS Code, uma maneira rápida e fácil de servir o projeto é usar a extensão [**Five Server** do VSCode](https://marketplace.visualstudio.com/items?itemName=yandeu.five-server). Basta instalar a extensão, abrir o arquivo `hello-world.html` no editor e clicar em "Go Live" no canto inferior direito do editor. Isso servirá a aplicação em `http://127.0.0.1:5500/hello-world.html`.

Alternativamente, você pode usar outros métodos como `IIS` ou `Apache` para servir o projeto, embora não os abordemos aqui por brevidade.

## Explicação do Exemplo Hello World

Vamos analisar o código do exemplo **Hello World** para entender como ele funciona.

> Em vez de usar o código acima, uma maneira alternativa de visualizar o código completo é visitar o [Exemplo Hello World do AppGED - Indoor](https://github.com/Dynamsoft/mobile-web-capture/blob/main/samples/hello-world.html).

### Referenciar o AppGED - Indoor

```html
<!DOCTYPE html>
<html lang="pt">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>AppGED - Indoor - Hello World</title>
    <script src="../dist/mwc.bundle.js"></script>
    <!--Alternativamente, referencie o script a partir do CDN
    <script src="https://cdn.jsdelivr.net/npm/dynamsoft-mobile-web-capture@3.0.1/dist/mwc.bundle.js"></script>
    -->
  </head>
```

Nesta etapa, o **AppGED - Indoor** é referenciado usando um caminho local relativo na seção `<head>` do HTML.

```html
<script src="../dist/mwc.bundle.js"></script>
```

Alternativamente, o script pode ser referenciado a partir de um CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/dynamsoft-mobile-web-capture@3.0.1/dist/mwc.bundle.js"></script>
```

O **AppGED - Indoor** encapsula todos os seus scripts de dependência, então um projeto do **AppGED - Indoor** só precisa incluir o próprio **AppGED - Indoor** como um único script. Não são necessários scripts de dependência adicionais.

> ⚠**IMPORTANTE**: Mesmo se você referenciar o script localmente, recursos de suporte como arquivos de motor `.wasm` **ainda são carregados do CDN em tempo de execução**. Se você precisar de uma **configuração totalmente offline**, siga as instruções em [Hospedagem Própria de Arquivos de Recursos](https://www.dynamsoft.com/mobile-web-capture/docs/guides/mobile-web-capture-customization.html#self-hosting-resource-files).

### Instanciar o AppGED - Indoor

```javascript
// Instanciar um Objeto AppGED - Indoor
const appGEDIndoor = new Dynamsoft.MobileWebCapture({
    license: "DLS2eyJoYW5kc2hha2VDb2RlIjoiMTAzNzczMjYzLVRYbFhaV0pRY205cSIsIm1haW5TZXJ2ZXJVUkwiOiJodHRwczovL21kbHMuZHluYW1zb2Z0b25saW5lLmNvbSIsIm9yZ2FuaXphdGlvbklEIjoiMTAzNzczMjYzIiwic3RhbmRieVNlcnZlclVSTCI6Imh0dHBzOi8vc2Rscy5keW5hbXNvZnRvbmxpbmUuY29tIiwiY2hlY2tDb2RlIjotMzU0MDk1MjR9", // Substitua isso pela sua chave de licença real
});
```

Referência da API: [`MobileWebCapture()`](https://www.dynamsoft.com/mobile-web-capture/docs/api/mobile-web-capture.html#mobilewebcapture)

Esta etapa cria a interface de usuário do **AppGED - Indoor**, que, quando iniciada, ocupa por padrão toda a área visível da janela do navegador. Se necessário, você pode especificar um contêiner para restringir o tamanho da interface de usuário. Para mais detalhes, consulte [Especificar o Contêiner da Interface de Usuário](https://www.dynamsoft.com/mobile-web-capture/docs/guides/mobile-web-capture-customization.html#example-1-specify-the-ui-container).

> Uma **chave de licença** é necessária para a instanciação.

### Iniciar o AppGED - Indoor

```javascript
const fileName = `Novo_Documento_${Date.now().toString().slice(-5)}`; // Gera um nome de arquivo único para usar como nome inicial do documento
await appGEDIndoor.launch(fileName);
```

Referência da API: [`launch()`](https://www.dynamsoft.com/mobile-web-capture/docs/api/mobile-web-capture.html#launch)

Esta etapa inicia a interface de usuário, começando no **`DocumentView`**, onde o usuário pode começar a construir um documento de duas maneiras:
> Nota: O `DocumentView` requer um nome de documento, que é passado como parâmetro no método `launch()`.

1. **Capturar**: Capturar imagem(ns) das páginas do documento.
2. **Importar**: Importar uma ou várias imagens ou arquivos PDF.

Após a criação de um documento, o usuário pode navegar entre três visualizações:

#### A Visualização de Documentos (DocumentView)
O usuário pode:

1. **Compartilhar**: Compartilhar o documento como um arquivo PDF de várias páginas.
   > O **Download** é habilitado onde o **Compartilhar** não é suportado (por exemplo, no Firefox).
2. **Gerenciar**: Selecionar uma ou várias páginas para ações adicionais.
3. **Gerenciar** → **Selecionar Tudo**: Selecionar todas as páginas.
4. **Gerenciar** → **Excluir**: Excluir as páginas selecionadas do documento.
5. **Gerenciar** → **Compartilhar**: Compartilhar páginas individuais como imagens (**.PNG**).
   > O **Download** é habilitado onde o **Compartilhar** não é suportado (por exemplo, no Firefox).

O usuário também pode habilitar o recurso de **"Upload"**. Confira [Habilitar Upload de Arquivos](https://www.dynamsoft.com/mobile-web-capture/docs/guides/mobile-web-capture-customization.html#enable-file-upload).

#### A Visualização de Página (PageView)
Quando o usuário pressiona uma imagem, a `PageView` é iniciada para aquela página, onde o usuário pode:

1. **Excluir**: Remover a página atual.
2. **Adicionar Página**: Adicionar mais páginas ao documento.
3. **Compartilhar**: Compartilhar a página atual como uma imagem (**.PNG**).
   > O **Download** é habilitado onde o **Compartilhar** não é suportado (por exemplo, no Firefox).
4. **Editar**: Exibir recursos de edição adicionais para processar ainda mais a página.
5. **Editar** → **Cortar**: Selecionar uma parte da página e cortar.
6. **Editar** → **Girar**: Girar a página **90 graus no sentido anti-horário**.
7. **Editar** → **Filtrar**: Ajustar os pixels da página.
8. **Editar** → **Anotar**: Adicionar anotações à página.

O usuário também pode habilitar o recurso de **"Upload"**. Confira [Habilitar Upload de Arquivos](https://www.dynamsoft.com/mobile-web-capture/docs/guides/mobile-web-capture-customization.html#enable-file-upload).

## Próximo Passo

O **AppGED - Indoor** oferece amplas opções de personalização. Continue lendo para explorar as personalizações disponíveis no [Guia de Personalização do AppGED - Indoor](https://www.dynamsoft.com/mobile-web-capture/docs/guides/mobile-web-capture-customization.html).

---

Essa tradução mantém a estrutura original do documento e substitui todas as instâncias de "Mobile Web Capture (MWC)" por "AppGED - Indoor". Se precisar de ajustes adicionais ou de outro formato, é só avisar!
