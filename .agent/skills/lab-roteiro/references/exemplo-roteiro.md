# Atividade 1.1 — Gestão de Usuários no Linux

## Objetivo

Nesta atividade você vai criar um usuário local no Linux, definir sua senha, configurar permissões administrativas via `sudoers` e verificar cada etapa pelo terminal. Gerenciar usuários é uma das tarefas mais básicas — e mais críticas — de qualquer administrador de sistemas: todo acesso indevido começa, em algum momento, por uma conta mal configurada.

Ao final, você terá um usuário funcional com capacidade de executar comandos como root de forma controlada e auditável.

---

## Pré-requisitos

- Sistema Linux com Ubuntu 22.04 (ou compatível)
- Acesso ao terminal com um usuário que tenha permissões de `sudo`
- Conhecimento básico de navegação por linha de comando

> ⚠️ **Atenção:** Os comandos desta atividade modificam contas de usuário do sistema. Execute em um ambiente de laboratório, nunca em produção sem autorização.

---

## Roteiro

### Passo 1 — Criar o usuário

Crie um novo usuário no sistema. O comando abaixo cria a conta, o diretório home e configura o shell padrão.

> 📝 **Adapte:** Substitua `[nome_usuario]` pelo nome que você deseja criar. Use apenas letras minúsculas e sem espaços (ex: `labuser`).

```bash
sudo useradd -m -s /bin/bash [nome_usuario]
```

**Resultado esperado:**
```
(sem saída — o comando executou silenciosamente)
```

---

Confirme que o usuário foi criado verificando sua entrada no arquivo de contas do sistema.

```bash
grep [nome_usuario] /etc/passwd
```

**Resultado esperado:**
```
labuser:x:1001:1001::/home/labuser:/bin/bash
```

> Os números `1001:1001` representam o UID e GID atribuídos automaticamente ao usuário. **Anote o UID** — ele será usado nas questões finais.

---

### Passo 2 — Definir a senha do usuário

Defina uma senha para o novo usuário. O sistema pedirá que você digite e confirme a senha (os caracteres não aparecem na tela — isso é normal).

> 📝 **Adapte:** Substitua `[nome_usuario]` pelo nome do usuário que você criou no Passo 1.

```bash
sudo passwd [nome_usuario]
```

**Resultado esperado:**
```
Nova senha: 
Redigite a nova senha: 
passwd: senha atualizada com sucesso
```

---

### Passo 3 — Verificar o diretório home

Confirme que o diretório pessoal do usuário foi criado corretamente com as permissões adequadas.

```bash
ls -la /home/
```

**Resultado esperado:**
```
total 16
drwxr-xr-x  4 root    root    4096 jan 15 10:32 .
drwxr-xr-x 20 root    root    4096 jan 15 10:00 ..
drwxr-xr-x  2 labuser labuser 4096 jan 15 10:32 labuser
drwxr-xr-x  5 seu_usuario seu_usuario 4096 jan 10 08:15 [seu_usuario]
```

> O diretório `[nome_usuario]` deve aparecer com o próprio usuário como dono (`labuser labuser`). Se aparecer como `root root`, o diretório não foi criado corretamente — refaça o Passo 1 com a flag `-m`.

---

### Passo 4 — Conceder permissões sudo via sudoers.d

A forma mais segura de conceder permissões administrativas é criar um arquivo dedicado no diretório `/etc/sudoers.d/`, em vez de editar o arquivo `/etc/sudoers` diretamente. Isso facilita auditoria e remoção de permissões.

> 📝 **Adapte:** Substitua `[nome_usuario]` pelo nome do usuário criado.

```bash
sudo bash -c 'echo "[nome_usuario] ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/[nome_usuario]'
```

**Resultado esperado:**
```
(sem saída — o arquivo foi criado silenciosamente)
```

---

Ajuste as permissões do arquivo criado. O `sudoers.d` exige permissão `440` — caso contrário, o sudo ignora o arquivo.

> 📝 **Adapte:** Substitua `[nome_usuario]` pelo nome do usuário.

```bash
sudo chmod 440 /etc/sudoers.d/[nome_usuario]
```

**Resultado esperado:**
```
(sem saída — permissões aplicadas com sucesso)
```

---

Verifique o conteúdo do arquivo criado para confirmar que está correto.

```bash
sudo cat /etc/sudoers.d/[nome_usuario]
```

**Resultado esperado:**
```
labuser ALL=(ALL) NOPASSWD:ALL
```

---

### Passo 5 — Testar o acesso sudo do novo usuário

Alterne para o novo usuário e execute um comando que exige privilégios administrativos para confirmar que as permissões estão funcionando.

> 📝 **Adapte:** Substitua `[nome_usuario]` pelo nome do usuário criado.

```bash
su - [nome_usuario]
```

**Resultado esperado:**
```
[nome_usuario]@hostname:~$
```

---

Com o novo usuário ativo, execute um comando administrativo para testar o sudo.

```bash
sudo whoami
```

**Resultado esperado:**
```
root
```

> Se o resultado for `root`, as permissões estão configuradas corretamente. Se aparecer uma solicitação de senha ou mensagem de erro, revise o Passo 4.

---

Volte ao usuário original após o teste.

```bash
exit
```

**Resultado esperado:**
```
logout
[seu_usuario]@hostname:~$
```

---

## Verificação Final

Antes de responder às questões, confirme:

- [ ] O usuário foi criado e aparece em `/etc/passwd`
- [ ] O diretório `/home/[nome_usuario]` existe com o dono correto
- [ ] O arquivo `/etc/sudoers.d/[nome_usuario]` existe com permissão `440`
- [ ] O comando `sudo whoami` retornou `root` ao ser executado como o novo usuário

---

## 📝 Questões de Verificação

Responda às questões abaixo. As respostas só podem ser obtidas executando o roteiro.

**1. Qual é o UID (User ID) atribuído ao usuário que você criou nesta atividade?**

a) 0  
b) 1000  
c) [valor que apareceu na saída do `grep` no Passo 1] *(gabarito — valor varia por ambiente)*  
d) 65534  

> 💡 *Nota para o instrutor: o gabarito desta questão é o UID exibido na saída do comando `grep [nome_usuario] /etc/passwd` no Passo 1. Em ambientes limpos, tipicamente será `1001`.*

---

**2. Qual permissão (em notação octal) foi aplicada ao arquivo criado em `/etc/sudoers.d/`?**

a) 777  
b) 755  
c) 600  
d) 440 *(gabarito)*  

---

**3. Ao executar `sudo whoami` como o novo usuário, qual foi a saída exibida no terminal?**

a) `[nome_usuario]`  
b) `sudo`  
c) `root` *(gabarito)*  
d) `wheel`  

---

*Atividade 1.1 | Administração de Sistemas Linux | v1.0*
