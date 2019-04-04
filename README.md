# Projeto 1 - M de Maravilhosa

# Cronograma
- **01/04**: 
  - Manhã - Revisão.
  - Tarde: Introdução do projeto. Passo-a-passo de versionamento e *Git* flow.
- **02/04**: Desenvolvimento do projeto.
- **03/04**:  Desenvolvimento do projeto.
- **04/04**:
  - Manhã: Desenvolvimento do projeto.
  - Tarde: [Teoria] Fetch, rebase e pull request. Como resolver conflitos e aceitar o PR.
- **05/04**:
  - Manhã: Finalização e visualização do projeto.
  - Tarde: [Teoria] Internet, servidores, carreira front vs. back.

## Mock up do Projeto
https://www.figma.com/file/XBEywzd2yF47RaWm0Gw4t7Tz/M-de-Maravilhosa?node-id=0%3A1


## Etapas do projeto
1. Página de Personalidades
2. (Opcional) Página da Autora

---------------


## Orientações para o pull request
### Copiar os arquivos do repositório da reprograma
1. Façam o _fork_ desse repositório;
2. Façam um _clone_ do repositório de vocês (o que vocês criaram através do fork);
3. Criar um branch com o seu nome, por exemplo *mell-yonashiro*.
```
git clone git@github.com:seu-username/T7-projeto-1-m-de-maravilhosa.git

git checkout -b mell-yonashiro
```

4. Leiam e entendam o código do projeto. Depois disso, façam as alterações da sua personalidade.


> O que deve ser alterado?
>
> Dentro da pasta **personalidade**, criar um arquivo .html com o nome da sua personalidade. Exemplo: minha personalidade é Ada Lovelace, então crie um arquivo ada-lovelace.html e insira dentro dessa pasta (personalidade/ada-lovalace.html). As imagens da sua personalidade devem ficar na pasta **personalidade/img**. Na hora de fazer a conexão na sua página, não esqueça do caminho da imagem.
> Dentro da pasta **autora**, criar um arquivo .html com o seu nome. Exemplo: meu nome é Mellina Yonashiro, então criei um arquivo mellina-yonashiro.html e inseri dentro dessa pasta (autora/mellina-yonashiro.html).
>
> Para o **index.html**, você deve colocar uma imagem quadrada da personalidade na pasta **img/home-personalidade** (criar pasta com mesmo nome). No arquivo **index.html**, mude o nome da personalidade e também mude o link para ir para sua página (elas estão organizadas por nome de personalidade e em ordem alfabética). Por exemplo, personalidade/ada-lovelave/index.html (ou simplesmente personalidade/ada-lovelace).
>

----------

### Atualizando suas alterações
Depois de realizar suas alterações no seu computador (local), você tem que subir para o Github.com.
* Após feitas as alterações, salve, faça um commit e push para o **seu** repositório.
```
git add .

git commit -m "Informações sobre as alterações"

git push origin mell-yonashiro

```

---------------

### Atualizando o seu fork de acordo com o repositório central (reprograma)
Pode ser que o repositório da Reprograma seja atualizado *depois* que você fez o fork. Nesse caso, o seu repositório não atualiza automaticamente de acordo com o repositório central. Pra isso, existem alguns passos a serem seguidos.
1. Determinar o seu repositório central, através do *upstream*.
```
git remote add upstream git@github.com:reprograma/T7-projeto-1-m-de-maravilhosa.git

git remote -v 
// output
// origin  git@github.com:yogmel/T7-projeto-1-m-de-maravilhosa.git (fetch)
// origin  git@github.com:yogmel/T7-projeto-1-m-de-maravilhosa.git (push)
// upstream        git@github.com:reprograma/T7-projeto-1-m-de-maravilhosa.git (fetch)
// upstream        git@github.com:reprograma/T7-projeto-1-m-de-maravilhosa.git (push)
```
2. Atualizar a master do seu repositório de acordo com o repositório central.
```
git fetch upstream
```
3. Mesclar as atualizações do repositório central com o seu pessoal.
```
git merge upstream/master
```
4. Atualizar a sua branch pessoal com as atualizações vindas da master.
```
git checkout mell-yonashiro

git merge master
```
5. Resolver possíveis conflitos.

-------------

### Enviar um Pull Request para atualizar o repositório central

5. Depois te terminar todas as suas páginas: na sua página do github, faça um **pull request** para o repositório da Reprograma.


---------------


## Orientações para o projeto
1. O site deve conter no total **3 páginas** (homepage, que já está pronta, personalidade e autora). Todas as páginas devem ser responsivas.
2. Não existe o layout para aparelhos menores. Vocês devem definir como será a disposição dos elementos em tablets e celulares.
3. A **estrutura de pastas** deve ser mantida e as pastas inseridas conforme a sugestão acima. Exemplo de uma estrutura de arquivos e pastas é:
```
index.html
css/
  style.css
img/
  home-personalidade/
    ada-lovelace-home.png

personalidade/
  ada-lovelace/
    index.html
    css/
      style.css
    img/
      ada-lovelace-perfil.png
      al-bg.png
      al-historia.png

autora
  mell-yonashiro/
    index.tml
    css/
      style.css
    img/
    mell-yonashiro-perfil.png
```
4. Fique à vontade para modificar a sua **página de autora**. A única exigência é que na parte ***Outras Maravilhosas***, vocês coloquem o link (da página e da imagem) pra outras 3 personalidades, seguintes no alfabeto. Por exemplo, na página de Ada Lovelace, existiriam links para os perfis de Bella Lovelace, Caroline Lovelace e Danielle Lovelace, porque elas são as mais próximas no alfabeto. Se não existem perfis seguintes ao seu, vá ao início da lista e faça o link para as primeiras personalidades.
