# Estilizações básicas com CSS

## Cores
Existem diversas maneiras de definir cores pra estilizações de sites, dentre elas:

### Cores pré-definidas
São as cores já existentes no sistema. São 140 cores em que você só precisa colocar o nome delas. Para saber quais são as cores pré-definidas, basta acessar o site da [w3schools](https://www.w3schools.com/colors/colors_names.asp).

### RGB e RGBA
- **RGB**: sigla para *red, green and blue* (vermelho, azul e verde). É feita a mistura de cada uma dessas cores em variadas proporções, para que novas cores, inclusive além das 140 pré-estabelecidas, sejam utilizadas. Cada uma das três vai de 0 a 255, separadas por vírgula, e conforme for aumentando ou diminuindo, novas cores virão.
```
color: rgb(0, 255, 0);
```
- **RGBA**: Além do RGB, também pode acrescentar a letra A (alpha) na sigla, que é o que irá configurar a transparência, utilizando números de 0.0 (transparente) a 1.0 (sólido).
```
color: rgba(0, 255, 0, 0.5);
```

### Hexadecimal
É composto por "#" e mais seis dígitos, onde cada dígito aumenta de acordo com a seguinte ordem: 0,1,2,3,4,5,6,7,8,9,a,b,c,d,e,f.
>Os dois primeiros: vermelho (#ff0000);<br>
>Os dois do meio: verde (#00ff00);<br>
>Os dois últimos: azul (#0000ff).

Assim como RGB, diversas cores podem ser criadas.

### HSL e HSLA
Sigla de *hue, saturation and lightness* (matiz, saturação e luz) onde:
>**Hue (matiz)** é o grau na roda de cores - 0 a 360 graus:
> - 0 ou 360 é vermelho;
> - 120 é verde;
> - 240 é azul.<br><br>
>**Saturation (saturação)** usa-se valor percentual:
> - 0% tom de cinza;
> - 100% cor total.<br><br>
>**Lightness (luminosidade)** usa-se valor percentual:
> - 0% é preto;
> - 100% é branco.

Assim como RGBA, no HSL também pode acrescentar a transparência (A), com os mesmos valores: 0.0 (transparente) a 1.0 (sólido).

## Imagens
### Object-Fit
Ela determina como uma imagem deve ser redimensionada dentro de um "container". Ela tem que mostrar se imagem deve preservar a proporção ou distorcer para caber no container.

### Object-position
É usada em conjunto com a object-fit. Vai especificar como a imagem deve ser posicionada, tanto horizontal como verticalmente. Por padrão, ela é centralizada.

## Fundo dos elementos
### Redimensionando imagens de fundo
Haverão casos onde as imagens de fundo poderão ser maiores ou menores que o container, então como deixar ela ser totalmente visível? Utilizando a propriedade *background-size.* Com ela, algumas palavras-chave podem ser utilizadas em determinadas ocasiões:

| palavra-chave | definição |
|----------------|-----------|
auto| é o valor padrão, a imagem se ajusta automaticamente. Se a imagem for maior que o container, será cortada; se for menor, haverá espaço sobrando.
cover| a imagem ocupa totalmente o elemento, porém se for maior, será cortado o tamanho excedente e se for menor, repetirá a imagem.
contain| vai redimensionar a imagem para que apareça totalmente, mas é necessário se atentar ao formato, pois se por exemplo, a imagem é retangular e o elemento é um quadrado, ela poderá se repetir para estar totalmente preenchida.
unidades de medida| também podem utilizar as unidades de medida (px, %, etc) para redimensionar a imagem.

### Repetição das imagens de fundo
Se a imagem de fundo deve ou não se repetir, é utilizada a propriedade *background-repeat*.

### Posicionamento das imagens de fundo
Para alterar a posição da imagem de fundo, usa-se a propriedade *background-position*.

### Propriedade background-attachment
Ela tem o propósito de definir como a imagem de fundo ficará, conforme fazemos a rolagem em um site. Muito usado nos chamados *parallax*.

 ## Efeitos de sombra
 ### Nos elementos
 Como colocar sombras nas caixas dos elementos: com *box-shadow*.
 ```
box-shadow: 2 a 4 valores de tamanho, valor de desfoque, valor de distância, cor
 ```

Para usar sombra dentro de uma imagem PNG usa-se o <u>filter: drop-shadow.</u>
```
filter: drop-shadow(10 px 10px 5px gray);
 ```

 ### Nos textos
 Como colocar sombras nas caixas dos elementos: com *text-shadow*.
 ```
text-shadow: horizontal e vertical, valor de desfoque, cor
 ```