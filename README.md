# Modelo EER de E-Commerce  
**Modelo conceitual refinado de banco de dados para um sistema de E-Commerce.**

---

## Sobre o Projeto
Este repositório apresenta o refinamento de um modelo **EER (Enhanced Entity-Relationship)** para um sistema de e-commerce, desenvolvido no MySQL Workbench. O objetivo foi aprimorar o modelo inicial, acrescentando regras de negócios e representações mais fiéis ao mundo real.

---

## 🎯 Objetivos do Refinamento
- **Cliente PJ e PF**  
  - Implementada a especialização da entidade `Cliente` em `Cliente_PF` e `Cliente_PJ`.  
  - Um cliente pode ser **Pessoa Física (PF)** ou **Pessoa Jurídica (PJ)**, mas nunca ambos.  

- **Pagamento**  
  - Criada a entidade `Pagamento`, permitindo que cada cliente cadastre **múltiplas formas de pagamento**.  
  - Cada pedido está vinculado a **um pagamento específico**.  

- **Entrega**  
  - Criada a entidade `Entrega`, associada ao `Pedido`.  
  - Relacionamento definido como **0..1**, representando que um pedido pode ou não gerar entrega.  *(ex.: produtos digitais).*
  - Implementado e configurado `Pedido_idPedido` como **nullable** e **UNIQUE**, garantindo que um pedido nunca tenha mais de uma entrega.  

---

## 🔑 Pontos de Destaque
- Uso de **tabelas associativas** (`Produtos em Estoque`, `Produtos por Vendedor`, `Disponibilizando um produto`, `Relação de Produto/Pedido`) para modelar relacionamentos N:N.  
- **Especialização de Cliente** com integridade garantida via relacionamentos 1:1.  
- Relacionamento **Pedido → Entrega** garantindo que cada pedido tenha no máximo uma entrega.  
- **Cliente → Pagamento** configurado para suportar múltiplos métodos de pagamento por cliente.  

---

## 🛠️ Ferramentas Utilizadas
- **MySQL Workbench** → modelagem conceitual e refinamento do diagrama.  
- **MySQL** → implementação das tabelas e constraints.  

---

## 📂 Estrutura do Repositório
📦 dio-projeto-ecommerce-eer   
┣ README.md  
┣ modelo_eer_e-commerce.png **# Diagrama EER exportado**   
┗ diagrama_e-commerce.mwb **# Arquivo nativo do MySQL Workbench**  

## 📝 Autor
Desenvolvido por **Fábio Barros de Oliveira** para o desafio DIO.