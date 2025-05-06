# azure-maquinas-virtuais
Informações relevantes para melhorar a eficiência e escalabilidade.

# 🌩️ Azure na Prática: SLA, Alta Disponibilidade e Estratégias de Implantação

Este guia resume os principais conceitos sobre **Service Level Agreement (SLA)**, estratégias de **alta disponibilidade**, **replicação** e boas práticas no uso do **Microsoft Azure**, conforme apresentado em laboratório prático.

---

## 🛡️ SLA (Service Level Agreement)

O SLA define o **nível mínimo de disponibilidade garantido pela Microsoft**. Abaixo está um quadro ilustrativo com os principais percentuais e o tempo máximo de inatividade mensal permitido para cada nível:

Exemplo de conteúdo do quadro:
![image](https://github.com/user-attachments/assets/bfe00d32-3758-4d90-bb03-65a4da5a6d90)

- Quanto mais "noves" no SLA, **menor o tempo de tolerância para falhas**.
- O SLA varia conforme o tipo de recurso criado e sua configuração (gerenciado ou manual).
- Recursos com alta disponibilidade oferecem **reembolsos** se não cumprirem o SLA (em contas comerciais).

---

## ⚙️ Estratégias de Alta Disponibilidade

### 🏗️ Conjuntos e Zonas de Disponibilidade

- **Availability Sets**: Agrupam VMs em domínios de falha e atualização.
- **Availability Zones**: Garantem distribuição entre zonas físicas isoladas na mesma região.
- Usar múltiplas zonas → **Alta resiliência** e **redução de downtime**.

---

## 💾 Tipos de Replicação de Armazenamento

| Tipo   | Descrição |
|--------|-----------|
| **LRS** | (Locally Redundant Storage) – Replicação local no mesmo datacenter. |
| **ZRS** | (Zone Redundant Storage) – Replicação entre zonas na mesma região. |
| **GRS** | (Geo-Redundant Storage) – Replicação entre regiões geográficas distintas. |
| **RA-GRS** | GRS com leitura adicional da réplica secundária habilitada. |

> 📌 **Quanto mais robusta a replicação, maior o custo — porém maior a segurança dos dados.**

---

## 💸 Custo x Disponibilidade

- A escolha de **replicação e disponibilidade** influencia diretamente no orçamento.
- Ambientes de **produção crítica** devem adotar estratégias de maior SLA.
- Ambientes de **teste ou homologação** podem utilizar configurações mais simples e econômicas.

---

## 🧠 Boas Práticas de Arquitetura

Antes de criar qualquer recurso, questione:

- _Qual é o SLA necessário para este sistema?_
- _Qual é o objetivo do ambiente? (Teste? Produção?)_
- _Quanto downtime é aceitável?_

> 🔍 Utilize os ícones de ajuda e links para a documentação oficial no portal Azure durante a criação de recursos.
> ![image](https://github.com/user-attachments/assets/9edea468-719b-419a-9835-af8f408649f0)


---

## ✅ Conclusão

A compreensão dos **níveis de SLA, estratégias de alta disponibilidade e replicações** é essencial para projetar soluções eficientes, resilientes e alinhadas ao custo em nuvem.

> _"Projetar com clareza evita custos inesperados e garante estabilidade no ambiente em produção."_


