Refinamento do Banco de Dados para E-commerce

Este repositório descreve a estrutura refinada do banco de dados para um sistema de e-commerce, otimizado para organização, desempenho e integridade dos dados. As principais alterações são detalhadas a seguir:

**Principais Alterações:**

1.  **Tabela `Cliente`:** Expandida com `PNome` (primeiro nome), `FNome` (último nome), `CPF`, `Bairro`, `Cidade`, `Email` e `Tipo` (cliente físico/jurídico).

2.  **Tabela `Pedido`:** Aprimorada com `Data_do_pedido`, `Produto_idProduto`, `Quantidade` (eliminando a tabela intermediária `Relação_de_Produto_pedido`), `Codigo_Rastreio`, `Status_Entrega`, `Pagamento_idPagamento` e `Vendedor_idVendedor`.

3.  **Tabela `Produto`:** Refinada com `Descrição`, `Preco` (DECIMAL(10,2) para precisão), `Quantidade` e `Fornecedor_idFornecedor`.

4.  **Tabela `Fornecedor`:** Adicionados `Endereço`, `Bairro`, `Cidade`, `Fone` e `Email`.

5.  **Tabela `Estoque`:** Mantida para controle de inventário (sem alterações significativas).

6.  **Tabela `Pagamento`:** Nova tabela com `idPagamento` (chave primária) e `Forma_Pagamento` (ENUM para métodos de pagamento).

7.  **Tabela `Terceiro_Vendedor` → `Vendedor`:** Renomeada e expandida com `PNome`, `MNome`, `FNome`, `CPF`, `Endereço`, `Bairro`, `Cidade`, `Fone` e `Email`.

**Impactos:**

*   Maior eficiência nas consultas SQL.
*   Melhor integridade referencial.
*   Facilidade de manutenção.
*   Expansão de funcionalidades (controle de pagamento e rastreamento de pedidos).

**Conclusão:**

O refinamento otimiza a estrutura do banco de dados para atender às necessidades do e-commerce, garantindo performance, escalabilidade e organização dos dados. O sistema agora é mais robusto e capaz de suportar um volume maior de transações.
