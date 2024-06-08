![RPA Suite](https://raw.githubusercontent.com/CamiloCCarvalho/rpa_suite/3e1ccd0acad654916466f03c2b8f166dc8d360d4/logo-rpa-suite.svg)


<h1 align="left">
    RPA Suite
</h1>
<br>

![PyPI Latest Release](https://img.shields.io/pypi/v/rpa-suite.svg)
![PyPI Downloads](https://img.shields.io/pypi/dm/rpa-suite.svg?label=PyPI%20downloads)

-----------------

## O que é?
**RPA Suite:** um conjunto abrangente de ferramentas projetadas para simplificar e otimizar o desenvolvimento de projetos de automação RPA com Python. Embora nossa suíte seja um conjunto de Ferramentas de RPA especializado, sua versatilidade a torna igualmente útil para uma ampla gama de projetos de desenvolvimento. Esta desenvolvendo com Selenium, Botcity ou Playwright? Experimente a RPA Suite e descubra como podemos facilitar seu projeto, ou qualquer projeto de Robôs de Software.

## Sumário do conteudo

- [Destaque](#destaque)
- [Objetivo](#objetivo)
- [Instalação](#instalação)
- [Exemplo](#exemplo)
- [Dependências](#dependências)
- [Estrutura do módulo](#estrutura-do-módulo)
- [Versão do projeto](#versão-do-projeto)
- [Mais Sobre](#mais-sobre)

## Destaque

**Versátil**: Além da Automação de Processos e criação de BOT em RPA, mas também para uso geral podendo  ser aplicadas em outros modelos de projeto, *além do RPA*.

**Simples**: Construímos as ferramentas de maneira mais direta e assertiva possível, utilizando apenas bibliotecas conhecidas no mercado para garantir o melhor desempenho possível.

## Objetivo

Nosso objetivo é se tornar a Biblioteca Python para RPA referência. Tornando o desenvolvimento de RPAs mais produtivo, oferecendo uma gama de funções para tal:

- Envio de emails (já configurado e personalizavel)
- Validação de emails (limpeza e tratamento)
- Busca por palavras, strings ou substrings (patterns) em textos.
- Criação e deleção de pasta/arquivo temporário com um comando
- Console com mensagens de melhor visualização com cores definidas para alerta, erro, informativo e sucesso.
- E muito mais

## Instalação
Para **instalar** o projeto, utilize o comando:

~~~python
>>> python -m pip install rpa-suite
~~~
ou no conda:
~~~python
conda install -c conda-forge rpa-suite
~~~

Após instalação basta fazer a importação do modulo e instanciar o Objeto ``suite``:
~~~~python
from rpa_suite import suite as rpa
~~~~

Feito isso já estará pronto para o uso:
~~~~python
# function send mail by SMTP 
rpa.send_mail(...)
~~~~

>[!NOTE]
>
>Para **desinstalar** o projeto, utilize o comando abaixo.
>**Obs.:** como usamos algumas libs no projeto, lembre-se de desinstar elas caso necessário.

~~~~python
>>> python -m pip uninstall rpa-suite
~~~~

>[!IMPORTANT]
>
>Opcionalmente você pode querer desinstalar as libs que foram inclusas no projeto, sendo assim:

~~~~python
>>> python -m pip uninstall loguru mail_validator colorama
~~~~


## Exemplo
Do módulo principal, importe a suite. Ela retorna uma instância do Objeto de classe Rpa_suite, onde possui variáveis apontando para todas funções dos submódulos:

    from rpa_suite import suite as rpa

    # Usando a função de envio de email por SMTP default
    rpa.send_email(my_email, my_pass, mail_to, subject, message_body)


    # Usando submódulo clock para aguardar 30 (seg) e então executar uma função
    time = 30
    rpa.wait_for_exec(time, my_function, param1, param2)


## Dependências
No setup do nosso projeto já estão inclusas as dependências, só será necessário instalar nossa **Lib**, mas segue a lista das libs usadas:
- colorama
- loguru
- email-validator
  
## Estrutura do módulo
O módulo principal do rpa-suite é dividido em categorias. Cada categoria contém módulos com funções destinadas a cada tipo de tarefa
- **rpa_suite**
    - **clock**
        - **waiter** - Funções para aguardar em relação a execução de uma função, podendo ser antes ou depois
        - **exec_at** - Funções para executar em momentos pré determinados
    - **date**
        - **date** - Funções para capturar data, mês, ano, hora, minutos de forma individual em apenas uma linha
    - **email**
        - **sender_smtp** - Funções para envio de email SMPT 
    - **file**
        - **counter** - Funções para contagem de arquivos
        - **temp_dir** - Funções para diretórios temporários
    - **log**
        - **loggin** - Funções decoradoras com log de execução das funções
        - **printer** - Funções print personalizados (alerta, erro, sucesso, informativo)
    - **regex**
        - **list_from_text** - Funções para gerar listas, dividindo texto usando padrão regex
    - **validate**
        - **mail_validator** - Funções para validação de emails
        - **string_validator** - Funções para validação/varredura (strings, substrings, palavras)

## Release
Versão: **Alpha 0.9.3**

Lançamento: *20/02/2024*

Status: Em desenvolvimento.


## Mais Sobre

Para mais informações, visite nosso projeto no Github ou PyPi:
<br>
<a href='https://github.com/CamiloCCarvalho/rpa_suite' target='_blank'>
    Ver no GitHub.
</a>
<br>
<a href='https://pypi.org/project/rpa-suite/' target='_blank'>
    Ver projeto publicado no PyPI.
</a>

<hr>
