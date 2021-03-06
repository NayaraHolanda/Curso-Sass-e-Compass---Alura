# Curso-Sass-e-Compass---Alura

O Sass é um pré-processador CSS, facilitando a vida do programador.
Podemos utilizar dois tipos de sintaxe: sass e scss
- Por o scss ser mais próximo da sintaxe do CSS, vamos utilizá-lo. Já o sass é mais padrão.

Para instalá-lo, deve ser através de um gerenciador de pacotes, como por exemplo o npm do node.js.

O arquivo deve conter a extensão .scss, e depois no terminal (dentro da pasta do arquivo) deve-se compilar através do comando:
    - sass estilos.scss:estilos.CSS
    - sass --watch estilos.scss:estilos.CSS (para qualquer alteração no arquivo .scss já ser compilada automaticamente)

-Criação de variável com sass:
    Deve colocar o $ antes, tanto para criar como para utilizar.

- Compass: framework focado em Sass.

- Posso também salvar algum trecho de código no mixin do sass. Ex.:
    @mixin nome {}
    E para chamar é só utilizar o @include nome;
    É possível passar parâmetro. Se quiser definir um padrão, não precisa criar uma variável, apenas colocar diretamente no parâmetro do mixin. Caso queira mudar o valor padrão, é só passar o valor desejado por parâmetro na hora do include.

- Comentários para aparecer apenas no Sass: //

- Aninhamento do Sass: os elementos de determinada classe, por exemplo, podem ser colocados todos dentro da mesma chave da classe, quando tem o hover, colocar: &:hover, dentro do elemento pai.

- Uma boa prática é separar as partes do código do css do site em arquivos, e também em pastas, de acordo com o conteúdo. Depois pra chamar os arquivos no arquivo principal que compilar o scss para o css, é fazer o:
    @import "pasta/nome-do-arquivo"; (não precisa da extensão .scss)

- O Sass tem diversas funções para cores. Ex.:
    - darken(#código-da-cor, porcentagem%); // deixa a cor mais escura
    - lighten(#código-da-cor, porcentagem%); // deixa a cor mais clara
    - complement(#código-da-cor);
    - saturate(#código-da-cor, porcentagem%);
    - adjust-hue(#código-da-cor, porcentagem%);

- O PLACEHOLDER é uma forma de evitar repetições, quando usamos o mixin, ou seja, um código css igual em diferentes elementos.
    Para declarar é só usar o %nome{}, e quando for chamar utiliza o @extend %nome;
    - IMPORTANTE: QUANDO É NECESSÁRIO O USO DE PARÂMETRO, É NECESSÁRIO UTILIZAR O MIXIN.

- Os medias-queries podem ser colocados diretamente no arquivo .scss para ser no seus respectivos elementos, para ser compilado pro arquivo .css padrão.

- Para colocar uma variável para receber string no scss, deve-se utilizar as aspas, e quando for utilizada:
    #{variável};

- COMPASS é um framework CSS baseado em Sass
    - Depois de instalado, deve ser dado um "compass create" dentro da pasta dos arquivos.
    - Assim como o Sass, para ele ficar assistindo as mudanças de código, deve ser feito da seguinte maneira: compass watch css/estilos.scss
    - Tem diversos códigos css prontos pra usar no site do compass, basta apenas fazer o import no mixins.scss e utilizar no local desejado, como mostra no site.
    - Há uma técnica CSS que visa diminuir o número de requisições para o servidor. Ela junta várias imagens em uma só e a importa no CSS. Essa técnica chama-se sprite. Coloca as imagens que quer juntar numa pasta chamada sprite, e depois é só colocar o import da pasta no estilos.scss.
        - é bom colocar a variável $sprite-spacing: 5px; (que dá o espaçamento de 5px entre as imagens);
        - deve-se colocar no arquivo que utilizar o sprite: @include all-sprite-sprites; (pois a cada imagem gerada, um novo nome é colocado, então com essa linha de código, o compass faz automaticamente).
        - OBS.: o nome da imagem deve ser igual ao nome da classe. E a classe deve conter o "sprite-" antes do nome, lá no HTML, pois por padrão o compass coloca esse prefixo antes na criação das classes lá no .css

- CANIUSE -> SITE PARA SABER SE DETERMINADO ELEMENTO É COMPATÍVEL COM QUAIS BROWSERS.

- No Sass também tem funções, para declarar é só fazer assim:
    @function nome (variável-parâmetro) {
        @return algo;
    }

    Serve para fazer cálculos.

- É possível fazer operações matemáticas no Sass.

- round() -> função para arrendondar valores.
