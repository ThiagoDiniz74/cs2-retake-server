# Revisão antes de publicar

1. Use este repositório apenas para documentação e exemplos preparados para publicação. Não copie diretórios reais do Umbrel ou do CS2 para cá.
2. Confira os arquivos: `git status --short` e `git diff --cached --name-only`.
3. Leia o conteúdo inteiro que será publicado: `git diff --cached`.
4. Procure por termos sensíveis nos arquivos preparados: `git grep -n -i -E 'password|passwd|token|secret|api[_-]?key|webhook|rcon|gslt|steam' -- ':!SEGURANCA.md'` e revise cada resultado. Uma busca sem resultados não garante ausência de segredos.
5. Confira manualmente IP público, domínio privado, email pessoal, nomes de usuário e caminhos que revelem dados pessoais.
6. Se algo sensível estiver no stage, use `git restore --staged CAMINHO` e revise o arquivo antes de continuar. Se um segredo já foi publicado, remova-o e revogue ou troque a credencial; um commit posterior não apaga o histórico.
