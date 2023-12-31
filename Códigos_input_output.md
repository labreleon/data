

## 1 telemedicina4

-   **input**:

    -   `"./Planos Estaduais de Saude/regioes_saude_sage.csv"`
    -   `"./Resultados/municipios_idh_localidades_18102022.xlsx"`
    -   `"./Resultados/Implantações AMET 25042023.xlsx"`
    -   `"./Dados/IBGE/estimativa_dou_2018_20181019.xls"`

-   **output**

    -   `"./DiD/base_inicial.csv"`

## 2 parse_sia_int

-   **input**:

    -   `"./Dados/SIA"`

-   **output**

    -   `"Dados/SIA/sia_proc.csv"`

## analise_dados

### Para

-   **input**:

    -   `"./Portal Governo Transparente/"`
    -   `""./Portal Fenix/"`

-   **output**

    -   `"../gastos_para.csv"`

### Tocantins

-   **input**:

    -   `"./Portal Megasoft/"`
    -   `"./Portal Fenix/"`
    -   `./Portal SIG/"`
    -   `"./Portal 7focus/"`

-   **output**

    -   `"../gastos_tocantins.csv"`

### Rondônia

-   **input**:

    -   `"./Portal Oxy/"`

-   **output**

    -   `"../gastos_rondonia.csv"`

### Acre

-   **input**:

    -   `"./Portal BethaCloud/"`
    -   `"./Portal Fly/"`

-   **output**

    -   `"../gastos_acre.csv"`

## analise_tfd_transparência

-   **input**:

    -   `"./DiD/base_inicial.csv"`
    -   `"./Dados/Portais da Transparência/gastos_acre.csv"`
    -   `"./Dados/Portais da Transparência/gastos_para.csv"`
    -   `"./Dados/Portais da Transparência/gastos_rondonia.csv"`
    -   `"./Dados/Portais da Transparência/gastos_tocantins.csv"`

-   **output/Figure**

    -   `"./Figuras/Gráficos Staggered TFD/gasto_nivel_tri.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_cap_tri.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_empenhos_tri.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_empenhos_cap_tri.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_nivel_sem.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_cap_sem.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_ln_gasto1_sem.png"`

## analise_tfd_sia

-   **input**:

    -   `"Dados/SIA/sia_proc.csv"`
    -   `"./DiD/base_inicial.csv"`

-   **output/Figure**

    -   `"./Figuras/Gráficos Staggered TFD/gasto_nivel_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_medio_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_tfd_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_tfd_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_con_espec_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_con_espec_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_telcon_espec_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_telcon_espec_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_con_gen_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_con_gen_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_ter_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_ter_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_ter_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_ter_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_desloc_ter_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_med_desloc_ter_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_flu_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_flu_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_flu_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_flu_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_desloc_flu_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_med_desloc_flu_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_aer_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_aer_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_aer_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_aer_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_desloc_aer_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_med_desloc_aer_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_desloc_intest_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggere TFD/gasto_desloc_intest_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_intest_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_desloc_intest_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_desloc_intest_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_med_desloc_intest_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_alim_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_alim_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_alim_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/n_alim_cap_tri_SIA.png"`
    -   `./Figuras/Gráficos Staggered TFD/qnt_alim_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/qnt_med_alim_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_nivel_sem_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_cap_sem_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_ln_gasto1_sem_SIA.png"`
    -   `"./Dados/SIA/muns_selecionados_norte.csv"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_nivel_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_cap_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_ln_gasto1_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_medio_tri_SIA.png"`
    -   `"./Figuras/Gráficos Staggered TFD/gasto_medio_qnt_tri_SIA.png"`

## mapas_implementacao

-   **input**:

    -   `"./DiD/base_inicial.csv"`
    -   `"./Dados/Portais da Transparência/gastos_acre.csv"`
    -   `"./Dados/Portais da Transparência/gastos_para.csv"`
    -   `"./Dados/Portais da Transparência/gastos_rondonia.csv"`
    -   `"./Dados/Portais da Transparência/gastos_tocantins.csv"`

-   **output/Figure**

    -   `"./Figuras/implementacao_mes.png"`
    -   `"./Figuras/evolucao_implementacao.png"`
    -   `"./Figuras/Situação Municípios.png"`

## descritivas_sia_transparência

-   **input**:

    -   `"./DiD/base_inicial.csv"`
    -   `"Dados/SIA/sia_proc.csv"`
    -   `"./Dados/Portais da Transparência/gastos_acre.csv"`
    -   `"./Dados/Portais da Transparência/gastos_para.csv"`
    -   `"./Dados/Portais da Transparência/gastos_rondonia.csv"`
    -   `"./Dados/Portais da Transparência/gastos_tocantins.csv"`

-   **output/Tabelas**

    -   `"./Tabelas/gasto_municipio_2019.csv"`
    -   `"./Tabelas/gasto_municipio_2020.csv"`
    -   `"./Tabelas/gasto_municipio_2022.csv"`
