Este é um projeto de exemplo usado em posts do blog [Mind Share](http://fabiolnm.blogspot.com).

# Preparação do Projeto

Execute o comando abaixo para configuração automática do ambiente (os comandos executados neste script são explicados na sequencia).

```
source App-Contatos-Django/setup-project
```

## Pré-requisitos automatizados com script setup-project
* Na raiz deste projeto, existe um arquivo .rvmrc, um script que é executado automaticamente ao entrar no diretório do projeto.
* Este script contém o seguinte comando:

```
source ~/.virtualenv/ambiente_app_contatos/bin/activate
```

* Este comando serve para ativar o ambiente python "ambiente_app_contatos".
* Após a ativação do ambiente, o terminal passa a exibir entre parênteses o nome do ambiente virtual python ativado:

```
(ambiente_app_contatos)fabio@fabio-vbox:~/App-Contatos-Django
```

* O carregamento automático via .rvmrc dispensa o desenvolvedor de ativar o ambiente manualmente no terminal.
* Para o carregamento automátio do .rvmrc funcionar, é necessário instalar o RVM.
* A instalação do RVM é feita pelos seguintes comandos no arquivo setup-project:

```
cd $HOME
bash < <(curl -s https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer)
source $HOME/.bashrc
```

* No setup-project também estão presentes os comandos de instalação do VirtualEnv:

```
mkdir $HOME/.virtualenv
cd $HOME/.virtualenv
curl -O https://raw.github.com/pypa/virtualenv/master/virtualenv.py
python virtualenv.py ambiente_app_contatos --no-site-packages
```

* Por fim, os comandos para entrar no diretório do projeto e instalar as suas dependências.

```
cd $HOME/App-Contatos-Django
pip install -r requirements.txt
```
