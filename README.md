# projeto-engenharia-app

# 🚀 Plataforma Antigravity Engenharia

[![Status](https://img.shields.io/badge/Status-Produção-success.svg)]()
[![Plataforma](https://img.shields.io/badge/Plataforma-Windows-blue.svg)]()
[![Licença](https://img.shields.io/badge/Licença-Proprietária-red.svg)]()

A **Plataforma Antigravity** é um ecossistema avançado de orquestração de cálculos de engenharia mecânica, integridade estrutural e segurança do trabalho. Projetada para eliminar o erro humano e centralizar memórias de cálculo, ela atua como um "Motor Canônico" que unifica a matemática de normas rigorosas (NBR, ASME, NR) com a geração automática de Dossiês e Laudos em PDF e HTML.

> **Aviso:** Este é um repositório de vitrine (Showcase). O código-fonte principal é fechado (Proprietário) e mantido em um repositório privado para proteção de propriedade intelectual e regras de negócio industriais. Os executáveis públicos para teste encontram-se na aba **Releases**.

---

## 🏗️ Domínios de Engenharia Suportados

A plataforma suporta múltiplos domínios através de motores independentes (Micro-arquitetura monolítica), garantindo validação estrita:

* 🏗️ **Pontes Rolantes e Pórticos (NBR 8400):** Dimensionamento de viga-caixão/perfil W, estabilidade, fadiga, dimensionamento do motor, freios e eficiência de cabos de içamento.
* 🛢️ **Vasos de Pressão e Caldeiraria (NR-13 / ASME VIII):** Cálculo de espessuras teóricas, avaliação de vida residual por ultrassom, PMTA e laudos de integridade.
* 🚡 **Elevadores de Tração (NBR NM 207):** Avaliação de cabos, aderência e escorregamento crítico de polias (Equação de Euler-Eytelwein).
* 🛠️ **Tubulações Industriais (ASME B31.3):** Validação paramétrica de espessuras de parede reta e limites operacionais.
* ❄️ **HVAC e PMOC:** Cálculo de Carga Térmica avançado.
* ⚠️ **Segurança de Máquinas (NR-12):** Avaliação de Risco (HRN) e geração de laudos de conformidade.

---

## ✨ Principais Funcionalidades

- **Orquestrador Multidomínio:** Consolida relatórios de diferentes engenharias (Mecânica, Elétrica, Segurança) em um único Dossiê de *As-Built*.
- **Conformidade Restrita:** Bloqueios automáticos no sistema (Status `PENDENTE` ou `NÃO CONFORME`) caso o engenheiro insira dados normativamente incorretos, omitidos ou inconsistentes com catálogos comerciais.
- **Rastreabilidade e Auditoria:** Cada cálculo gera um `calculation_id` atômico via Hash SHA-256 e UUID, rastreando entradas, versão do motor, saída e carimbo de tempo no banco de dados, prevenindo adulterações documentais.
- **Isolamento Multi-Tenant:** Arquitetura adaptada para segregar projetos, empresas e organizações de forma segura, com políticas estritas contra CORS e XSS.
- **Exportação Nativa:** Geração de diagramas estruturais vetoriais (SVG/DXF) e laudos de engenharia totalmente parametrizados.

---

## 💻 Tecnologias e Arquitetura (Under the Hood)

Embora o código seja fechado, a arquitetura moderna da aplicação foi construída com:

* **Core Matemático:** Python 3.11+
* **Framework API:** FastAPI / Uvicorn (Roteamento assíncrono e validações com Pydantic)
* **Banco de Dados:** SQLite3 (Sandboxed e imutável para execuções auditadas)
* **Frontend:** Servido estaticamente (HTML5, Vanilla JS, CSS) para máxima portabilidade em modo local.
* **Empacotamento:** 
  * `PyInstaller`: Compilação da engine inteira em um binário nativo.
  * `Inno Setup`: Orquestração do instalador oficial do Windows.
* **Segurança:** Proteção CSRF nativa, validação JWT de sessões, isolamento WAL/SHM de banco e proteção CSP nos artefatos.

---

## 📸 Capturas de Tela

*(Adicione imagens aqui. Para colocar imagens no GitHub, basta arrastá-las do seu computador para cá durante a edição do README).*

| Interface de Cálculo Canônico | Geração Automática do Dossiê |
| :---: | :---: |
| `<Arraste_uma_imagem_aqui.png>` | `<Arraste_outra_imagem_aqui.png>` |

---

## 📥 Como Baixar e Testar

Disponibilizamos compilações pré-construídas para Windows 64-bits:

1. Acesse a seção **[Releases](../../releases)** ao lado direito.
2. Baixe a versão mais recente desejada:
   - **`Setup_Antigravity_Engenharia.exe`** (Instalador Padrão do Windows)
   - **`Antigravity_Engenharia_Portable.zip`** (Zero-Install: Basta extrair a pasta e rodar o `.exe` sem precisar de privilégios de administrador).
3. Ao executar o binário, um servidor local imbutido será ativado silenciosamente e a interface do sistema abrirá em seu navegador padrão.

*(Nota: Como o pacote não possui assinatura EV Authenticode, o Microsoft Defender/SmartScreen poderá exibir um alerta de "Fornecedor Desconhecido". Clique em "Mais informações" > "Executar assim mesmo").*

---

## ✉️ Contato e Suporte

Para demonstrações corporativas, licenciamento ou reporte de bugs na interface, utilize a aba **Issues** deste repositório ou entre em contato pelo email de engenharia.
