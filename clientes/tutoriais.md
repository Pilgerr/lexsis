### CORREÇÃO DE NOTAS RETORNADAS COM ERRO  

1. Abrir o Touch
2. Opções (F10)
3. Consulta NFC-e
4. Status de envio: Selecionar apenas "Retornadas com erro" (obs.: clicando com o botão direito tem como selecionar e não selecionar todas)
5. Selecionar data inicial e data final para a consulta (PERÍODO)
6. Pesquisar (F4)
7. Validação de itens
8. Corrige o(s) item(s) com base nas informações do escritório de contabilidade
9. Aplicar
10. Seleciona todas as notas depois de corrigir os itens (obs.: clicando com o botão direito tem como selecionar e não selecionar todas)
11. *EXECUTAR SOMENTE COM O AVAL DA CONTABILIDADE* Processar (F2)
12. Botão direito no Watchdog > Executar > Agente_Lexsis.exe

### EMISSÃO DAS NFC-E EMITIDAS  

1. Abrir o Touch (pode ser em outros módulos, mas vamos usar o Touch)
2. Opções (F10)
3. Relatórios
4. NFC-e emitidas (4ª linha, 3ª coluna)
5. Seleciona o período e formata conforme necessário (contabilidade vai solicitar algum parâmetro específico, caso não tenha solicitado é só confirmar)
6. Confirma
7. Prontinho, agora só imprimir!

### EXPORTAR XML  

1. Abrir o Touch
2. Opções (F10)
3. Consulta NFC-e
4. Status de envio: Selecionar apenas "Retornadas com erro" (obs.: clicando com o botão direito tem como selecionar e não selecionar todas)
5. Selecionar data inicial e data final para a consulta (PERÍODO)
6. Pesquisar (F4) *SE NÃO RETORNAR NENHUMA NOTA PULAR PARA O PASSO 13*
7. Validação de itens
8. Corrige o(s) item(s) com base nas informações do escritório de contabilidade
9. Aplicar
10. Seleciona todas as notas depois de corrigir os itens (obs.: clicando com o botão direito tem como selecionar e não selecionar todas)
11. *EXECUTAR SOMENTE COM O AVAL DA CONTABILIDADE* Processar (F2)
12. Botão direito no Watchdog > Executar > Agente_Lexsis.exe
13. Gerar XML (na própria tela da consulta)
14. Selecionar o período e a empresa
15. Exportar
16.  Selecionar onde quer salvar (exemplo: área de trabalho > Botão direito > Novo > Pasta > Nomear a pasta com esse padrão: "XML_MESANO_EMPRESA" > Selecionar essa pasta
17. Digita "xml" e clica em salvar
18. Clica com o botão direito na pasta > Enviar para > Pasta compactada


### IMPRESSORA PADRÃO  

1. Painel de controle
2. Dispositivos e impressoras
3. Seleciona a impressora "Microsoft print to PDF" e define como padrão
4. Abre o relatório novamente
5. Define a impressora que estava como padrão anteriormente de novo


### TAXAS DE ENTREGA - TELE  

1. Abrir Tele
2. Utilitários (F2)
3. Cadastros
4. Áreas - Taxas

F5 | Incluir nova taxa.
F3 | Editar taxa existente.
F8 | Excluir taxa.
F9 | Cancelar.
F12 | Confirmar.

CAMPOS:

- Área: Preencher com a área de entrega (geralmente copiar de outra taxa existente).
- Taxa: Valor da taxa.
- Loja: Preencher com o número da loja correspondente à taxa.

### ADICIONAR ITEM NA TELA - NÃO APARECE NO PDV MÓVEL  

1. Abrir Cosmos
2. Estoque
3. Cadastros
4. Itens de Venda (PDV)
5. Seleciona o subgrupo
6. Incluir item
7. Pesquisa e seleciona o item e confirma
8. Confirmar

### CRIAÇÃO DE USUÁRIO  

1. Abrir Cosmos
2. Configurações
3. Usuários
4. Seleciona um usuário já existente do grupo desejado
5. Clica em "Copiar"
6. Preenche o campo do usuário e da senha
7. (SE JA TIVER O COLABORADOR CADASTRADO IR PARA O PASSO 8) Clica no link "Nome" preenche nome e sobrenome do colaborador, grava e clica em sair
8. Seleciona o colaborador que foi criado na lista

### DESFAZER EXCLUSÃO - DIÁRIAS  

1. Abrir Cosmos
2. Hospedagem
3. Selecionar a reserva > Abrir gerenciador de contas
4. Marcar checkbox "Estornados"
5. Clicar em estornar

### DESFAZER EXCLUSÃO - RESERVAS  

1. Abrir Cosmos
2. Hospedagem
3. Pesquisa > Marcar checkbox "Reservas canceladas" > Preencher campo "estada" (ou o que tiver) e filtrar
4. Dois cliques
5. Clicar no símbolo de estorno, se não aparecer rodar o script: 

"insert into configuracoes (modulo,descricao, valor)
values('HOSPEDAGEM','COPIAR RESERVA EXCLUIDA', CONVERT(VARBINARY, 'S'))"

e se não tiver permissão:
Aba Hospedagem > 3ª coluna / Penúltima linha "Copiar reserva excluída"

### BUSCAR CAIXA ONDE A ESTADA FOI FINALIZADA 

1. Abrir Cosmos
2. Hospedagem
3. Caixa
4. Consulta
5. Busca por "descrição"
6. Digita o número da estada
7. Enter
8. Dois cliques e pronto: vai aparecer o caixa e os lançamentos

### CADASTRO DE CRACHÁ
1. Abrir Cosmos
2. Configurações
3. Usuários
4. Seleciona o usuário > Alterar
5. Bipar o crachá no campo "Senha" 
6. Clicar no link "Nome" em azul > Alterar > Bipar o crachá no campo "Crachá" da tela de colaboradores > Gravar > Gravar

Lembrando que agora a senha é o conteúdo da leitura do crachá, se em algum dispositivo não tiver o leitor,
é interessante bipar em um bloco de notas anteriormente e anotar para preencher manualmente nesses casos.
