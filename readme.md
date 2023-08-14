## Virtualenv

O **virtualenv** (ambiente virtual) é uma ferramenta Python que permite criar ambientes `isolados` e `independentes` nos quais você pode instalar pacotes e bibliotecas Python específicos para um projeto, sem afetar o ambiente global do sistema ou outros projetos. 
Isso é especialmente útil quando você está trabalhando em vários projetos que podem ter dependências conflitantes ou versões diferentes das mesmas bibliotecas.



Aqui estão os passos básicos para usar o virtualenv:

1. **Instalação**: Antes de tudo, você precisa instalar o virtualenv se ainda não estiver instalado. Você pode fazer isso usando o gerenciador de pacotes *pip*, que normalmente já vem com a instalação do Python. 
Execute o seguinte comando no terminal:
```
sudo apt install python3-virtualenv
```
Ou no windows
```
pip install virtualenv
```
___
2. **Criação de um ambiente virtual**: Navegue até o diretório do seu projeto e crie um ambiente virtual usando o seguinte comando:
```
virtualenv nome_ambiente
```
Isso criará um diretório chamado `nome_ambiente` no seu diretório de projeto.

___
3. **Ativação do ambiente virtual**: Após criar o ambiente virtual, você precisa ativá-lo. O comando para isso varia de acordo com o sistema operacional:

No macOS e Linux:
```
source nome_ambiente/bin/activate
```
No Windows:
```
nome_do_ambiente\Scripts\activate
```
Após a ativação, você verá o nome do ambiente virtual no início do seu prompt de comando, indicando que você está trabalhando dentro desse ambiente.
![Terminal](https://raw.githubusercontent.com/pedrohenriquecordeiro/virtualenv_python/main/image_env.png "Terminal")

No exemplo acima, criei e ativei um ambiente virtual chamado virtual_projeto_dask.
___

4. **Instalação de pacotes**: Com o ambiente virtual ativado, você pode usar o pip normalmente para instalar pacotes e bibliotecas Python específicos para o seu projeto. As `instalações serão feitas apenas dentro deste ambiente isolado`, não afetando o ambiente global do sistema.
>É recomendado também instalar os pacotes a partir do arquivo requirements. O requirements é um arquivo de texto simples que lista todas as dependências do seu projeto, ou seja, as bibliotecas e pacotes externos necessários para que o seu código funcione corretamente.
```py
requests==2.26.0
numpy==1.21.1
matplotlib==3.4.3
pandas==2.0.1
dask==2023.7.0
```

Para instalar as dependências listadas no arquivo `requirements.txt`, você deve executar o seguinte comando no terminal:
```
pip install -r requirements.txt
```
___
6. **Desativação do ambiente virtual**: Quando você terminar de trabalhar no projeto ou quiser sair do ambiente virtual, basta executar o seguinte comando:
```
deactivate
```
