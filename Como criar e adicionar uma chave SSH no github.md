## Git Bash
### Gerar a chave
> ssh-keygen -t ed25519 -C [your-email-github]

**!! Fique atento aos caracteres (Caixa Alta ou Baixa)**

- Pressione Enter para confirmar que arquivo será salvo no caminho especificado. **(c:/Users/[user]/.ssh)**
- Entre com uma senha e confirme-a

**Sua chave foi gerada!**

### Adiciona-la às chaves ssh no github 
Vá até o caminho onde foi salva a sua chave, abra o arquivo com final .pub e copie o conteúdo.

Para criar uma nova chave ssh, entre no seu perfil, vá até configurações clicando no seu avatar, navege no menu e selecione **SSH e chaves GPG**. Clique em **Nova chave ssh**, adicione um nome de sua preferência e cole o conteúdo que você copiou.

## Agora é preciso ativa-la.
### Ativando a chave SSH
Vá até a pasta onde está sua chave (.ssh)

Digite o comando abaixo que iniciará o processo

> eval $(ssh-agent -s)

- você deve receber como retorno:

> Agent pid [id]   
> // o númerno varia a cada execução 

Logo após digite:

> ssh-add id_ed25519 (é necessário estar na pasta .ssh para funcionar dessa maneira)

Entre com a senha definida anteriormente e o retorno deverá ser:
> Identity added: id_ed25519 ([your-email])

### Pronto! Sua chave SSH está pronta para usar.

<br>
---------------    

## Linux
Os mesmos passos podem ser executados no terminal linux, o que difere é o caminho da chave gerada que será:
> **/home/[user]/.ssh**