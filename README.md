# ResumoCamada

Plugin para QGIS que gera um resumo da camada ativa, exibindo informações como quantidade de feições, tipo de geometria, área total e comparação entre áreas, com opção de exportação em CSV e PDF.

## Visão geral

O **ResumoCamada** foi desenvolvido para facilitar a visualização rápida de métricas de uma camada vetorial no QGIS.  
A proposta do plugin é oferecer uma interface simples e organizada para consultar dados da camada selecionada e gerar relatórios de apoio.

### Funcionalidades

- Exibe o nome da camada ativa.
- Mostra a quantidade de feições.
- Identifica o tipo de geometria da camada.
- Calcula a área total em:
  - metros quadrados (m²)
  - hectares (ha)
  - quilômetros quadrados (km²)
- Compara áreas quando houver múltiplas feições.
- Exporta os resultados em **CSV**.
- Gera relatório em **PDF** com resumo e mapa da área.

## Interface

O plugin possui uma interface gráfica no QGIS com:

- Cabeçalho com informações gerais da camada.
- Bloco de resumo com métricas principais.
- Bloco de comparação entre áreas.
- Botões de ação para:
  - Exportar CSV
  - Exportar PDF
  - Fechar

## Demonstração

### Tela inicial
![Tela inicial](./assets/captura.png)


## Tecnologias utilizadas

- Python 3
- PyQt
- QGIS API

## Estrutura do projeto

```bash
RESUMO_CAMADA/
├── help/
├── i18n/
├── scripts/
├── test/
├── __init__.py
├── camada.qlr
├── icon.png
├── Makefile
├── metadata.txt
├── pb_tool.cfg
├── plugin_upload.py
├── pylintrc
├── README.html
├── README.txt
├── resources.py
├── resources.qrc
├── resumo_camada_dialog_base.ui
├── resumo_camada_dialog.py
└── resumo_camada.py
```

## Instalação

### Opção 1: instalar manualmente no QGIS

1. Clone ou baixe este repositório:
   ```bash
   git clone https://github.com/seu-usuario/resumo-camada.git
   ```
2. Copie a pasta do plugin para o diretório de plugins do QGIS.

No Windows, normalmente:
```bash
C:\Users\SEU_USUARIO\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins
```

No Linux, normalmente:
```bash
~/.local/share/QGIS/QGIS3/profiles/default/python/plugins
```

3. Abra o QGIS.
4. Vá em **Complementos > Gerenciar e Instalar Complementos**.
5. Procure por **ResumoCamada** na lista de plugins instalados localmente.
6. Ative o plugin.

## Como usar

1. Abra o QGIS.
2. Carregue uma camada vetorial.
3. Selecione a camada desejada.
4. Execute o plugin **ResumoCamada**.
5. Visualize os dados resumidos na janela principal.
6. Use os botões para exportar:
   - **CSV**, para dados tabulares;
   - **PDF**, para relatório visual com mapa.

## Exportações

### CSV
O arquivo CSV contém os principais dados resumidos da camada, facilitando análise externa ou integração com outras ferramentas.

### PDF
O relatório PDF reúne:
- informações gerais da camada;
- métricas calculadas;
- comparação entre áreas;
- mapa da região analisada.

## Objetivo do projeto

Este plugin foi criado como projeto prático para estudo de desenvolvimento de plugins no QGIS com Python e PyQt, com foco em automação de análises simples e geração de relatórios.

## Melhorias futuras

- Melhorar o layout do PDF.
- Adicionar suporte a mais tipos de análise.
- Permitir seleção de feições específicas.
- Incluir pré-visualização do mapa antes da exportação.
- Melhorar o tratamento para camadas com muitas feições.
- Adicionar internacionalização completa.

## Desenvolvimento

Caso queira editar ou evoluir o plugin:

1. Abra a pasta do projeto no VS Code ou outro editor.
2. Edite os arquivos principais:
   - `resumo_camada.py` → lógica do plugin
   - `resumo_camada_dialog.py` → comportamento da interface
   - `resumo_camada_dialog_base.ui` → layout visual da interface
3. Recarregue o plugin no QGIS para testar as alterações.

## Autor

**Leandro Eloi**

- Email: leandroodev001@gmail.com

