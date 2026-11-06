# Apostila de C com respostas por aluno (Firebase)

Arquivos: `index.html` (alunos), `professor.html` (painel), `conteudo.js` (textos e perguntas),
`firebase-config.js`, `style.css`, `firestore.rules`.

## 1. Criar o projeto no Firebase (gratuito)
1. Acesse console.firebase.google.com e crie um projeto.
2. Em **Authentication > Método de login**, ative **Anônimo** e **Google**.
3. Em **Firestore Database**, crie o banco (modo produção).
4. Em **Configurações do projeto > Seus apps**, adicione um app Web e copie o objeto de configuração para `firebase-config.js`.

## 2. Regras de segurança
1. Abra `firestore.rules`, troque `SEU_EMAIL@gmail.com` pelo e-mail Google que você usará no painel.
2. Em **Firestore > Regras**, cole o conteúdo e publique.

## 3. Publicar
Envie a pasta para a Vercel ou para o GitHub Pages (os arquivos precisam de um endereço https; abrir direto do computador não funciona).
Depois, em **Authentication > Configurações > Domínios autorizados**, adicione o domínio do seu site.

## 4. Usar
- Alunos: enviam o link de `index.html`, preenchem nome e turma e salvam cada bloco.
- Professor: abra `professor.html`, entre com o Google, filtre por turma e baixe o CSV.

## Observações
- O aluno é identificado por um login anônimo do navegador. Se trocar de navegador ou aparelho, cria um registro novo (o painel mostra pelo nome).
- Qualquer pessoa com o link pode enviar respostas; confira o nome e a turma no painel.
- A chave do Firebase no código é pública por natureza; a proteção está nas regras do Firestore.
