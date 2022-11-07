## O que estou fazendo

### Banco de dados

Primeira coisa é dar um npm init e instalar o typescript no modo desenvolvedor. E com isso vou criar o ambiente do typescript dando início a ela com "npx tsc --init". Instalo também o tsx no modo desenvolvedor que é um pacote que automatiza o processo de compilar e executar, não fazendo mais manualmente.

"dev": "tsx src/server.ts" - Comando para inicializar o server pelo NPM. E se passar o "watch" entre o caminho e o tsx ele irá atualizar a cada mudança no código.

npm i prisma -D - Prisma é interface em linha de comando que irá automatizar algumas tarefas
npm i @prisma/client - É o pacote que irá conectar o banco de dados com a aplicação
npx prisma init --datasource-provider SQLite - comando para utilizar o banco de dados SQLite
npx prisma migrate dev - vai detectar que foi criado uma nova tabela

migration - É onde tratamos o caso de controle de versionamento do BD

npx prisma studio - Comando para visualizar meu banco de dados pelo navegador.

npm i prisma-end-generator @mermaid-js/mermaid-cli -D - Irá instalar duas bibliotecas conjuntas para criar um diagrama através de código.
npx prisma generate - Irá gerar o diagrama.


npm i @fastify/cors - É um mecanismo de segurança para quais aplicações estão apitas a consumir o back-end.

### Aula 2

npx prisma migrate dev - Para criar as novas tabelas no banco

new Date().toISOString() - Dando esse comando no console do chorme você irá obter o date atual completo. 

criei esse code no package.json para chamar no comando "npx prisma db seed"
"prisma": {
    "seed": "tsx prisma/seed.ts"
  },

npx prisma db seed - Irá executar no banco de dados

npm i zod - É uma biblioteca de schema Validation

npm i short-unique-id - É um gerador de id(caso o banco não escale muito)

Tive um problema com o fetch nativamente, pois apresentou bugs para fazer as requisições, ai solucionei instalando o fetch por fora.

npm install node-fetch
import fetch from 'node-fetch';

npm i @fastify/jwt - Um gerador de tokens de validação em hash