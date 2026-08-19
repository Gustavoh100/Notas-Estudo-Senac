# GitHub

## 1. Verificar a versão do Git

Abra o **CMD (Terminal de Comando)** do computador.

Execute:

```bash
git --version
```

Verifique o número da versão instalada. Caso esteja abaixo da versão **2.53.0**, baixe a versão mais atualizada do Git pelo Google/site oficial.

## 2. Configurar seu nome

No Terminal, utilize:

```bash
git config --global user.name "Seu Nome"
```

Substitua **"Seu Nome"** pelo nome que deseja utilizar no Git. Esse nome ficará configurado na máquina para identificar seus commits.

## 3. Configurar seu e-mail

Utilize:

```bash
git config --global user.email "seuEmail@gmail.com"
```

Coloque o mesmo e-mail que você utiliza ou pretende utilizar na sua conta do **GitHub**.

# Git Bash

## 1. Verificar se já existe uma chave SSH

Para verificar se existe alguma chave SSH na sua máquina, utilize:

```bash
ls -al ~/.ssh
```

## 2. Criar uma chave SSH

Utilize:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Substitua `your_email@example.com` pelo e-mail utilizado no GitHub.

## 3. Iniciar o SSH Agent

Execute:

```bash
eval "$(ssh-agent -s)"
```

## 4. Adicionar a chave SSH

Execute:

```bash
ssh-add ~/.ssh/id_ed25519
```

## 5. Copiar a chave pública

No Git Bash, utilize:

```bash
clip < ~/.ssh/id_ed25519.pub
```

A chave pública será copiada para a área de transferência. Depois, você poderá colá-la nas configurações de **SSH Keys** da sua conta do GitHub.
