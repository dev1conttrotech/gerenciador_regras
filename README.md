# Gerenciador de Regras para Importação de Dados do Excel para o Banco de Dados

## Objetivo
O objetivo deste sistema é permitir que os usuários cadastrem regras que definam como os dados de um arquivo Excel devem ser importados e inseridos em um banco de dados. Isso facilitará o processo de importação e tornará a operação mais flexível e configurável.

## Colunas para a Regra
As regras são configuradas com as seguintes colunas:

### 1. id_regra: UUID
   - Descrição: Identificador único da regra cadastrada no banco de dados.
   - Tipo de Dado: UUID (Universally Unique Identifier)

### 2. nome_regra: String
   - Descrição: Nome descritivo da regra que será apresentado aos usuários para seleção.
   - Tipo de Dado: String

### 3. excel_de: CHAR
   - Descrição: Representa a coluna do Excel da qual os dados serão extraídos.
   - Tipo de Dado: CHAR

### 4. banco_para: String
   - Descrição: Representa a coluna do banco de dados para a qual os dados extraídos do Excel serão gravados.
   - Tipo de Dado: String

## Exemplo de Regra
Para ilustrar o funcionamento das regras, consideremos um exemplo:

Suponha que um cliente selecione a regra com as seguintes configurações:
- excel_de: 'A'
- banco_para: 'fornecedor'

Neste caso, quando o cliente fizer o upload de uma planilha Excel e selecionar essa regra, o sistema interpretará que a coluna 'A' no Excel corresponde à coluna 'fornecedor' no banco de dados. Isso significa que os dados da coluna 'A' do Excel serão importados e inseridos na coluna 'fornecedor' do banco de dados.

O sistema permitirá aos usuários configurar várias regras diferentes para se adequar a diferentes formatos de planilhas e requisitos de importação.

Este gerenciador de regras simplificará o processo de importação de dados do Excel, tornando-o mais eficiente e personalizável para atender às necessidades específicas dos usuários.
