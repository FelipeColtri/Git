**Passos básicos para o uso do git em um sistema linux por terminal**

- Tendo o git devidamente instalado no Linux
sudo apt install git

- Para configurar o nome e email do usuário git:
git config --global user.name "Usuário"
git config --global user.email "usuario@email.com"

- Iniciar o git já dentro da pasta que será usada (criando no computador o repositório):
git init 

- Clonar uma pasta do GitHub (baixar ela para o seu computador):
git clone https://github.com/usuario/pasta

- Vericar o status do repositório (se falta algum arquivo para ser atualizado/monitorado, mais comandos a seguir):
git status

- Adicionar um arquivo no repositório (basicamente salva as modificações, mas não oficializa uma nova versão):
git add arquivo.queck

- Salvar devinitivamente uma nova versão (sempre nescessário ao atulizar algo importante no repositório):
git commit -m "Um comentário muito pertinente"
           -am "comentário" // add e comenta

- Subir um arquivo/pasta para o GitHub (upload e atualização dos arquivos):
git push origin master
	 github.com/Usuario/Repositorio branchDoProjeto

- Ver a modificações do repositório (mostra todos os commits)
git log
        --oneline // mostra em apenas uma linha cada commit
        --graph // mostra o grafo de ramos 
        --all // mostra toda a arvore 

- Mostra qual é o ramo que o projeto se encontra
git branch

- Move entre os ramos:
git checkout <num_da_versão>
             master // volta para o ramo principal
             -b <nome_novo_ramo> // cria novo ramo herdando do ramo master

- Motra o que houve de mudanças no projeto (deve ser feito antes de add):
git diff

- Desfaz mudanças depois de add, mas antes do commit (remove última alteração no ramo):
git reset HEAD
          --hard <num_da_versão>   

- Subir um ramo para um repositório ja existente:
git remote add <nome_ramo> <link_ramo.git>

- Sincronizar o repositório do GitHub para o Git local (deve estar vinculado):
git pull

- Sincroniza o repositório sem juntar os projetos (marge):
git fetch
