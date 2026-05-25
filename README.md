# CLAUSTRO DO MUNDO

Aplicativo desktop católico desenvolvido em Python com interface Tkinter.

O sistema reúne:

* regra diária;
* liturgia diária;
* salmos;
* notícias católicas;
* coleta RSS automática;
* modo silêncio;
* modo cela;
* métricas espirituais;
* música ambiente;
* SQLite persistente;
* atualização automática;
* instalador profissional.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# COMANDOS PRINCIPAIS (USO DIÁRIO)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# EXECUTAR EM DESENVOLVIMENTO

```cmd
python main.py
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# LIMPAR BUILDS ANTIGOS

```cmd
rmdir /s /q build
rmdir /s /q dist
if exist claustro.spec del /q claustro.spec
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# GERAR EXECUTÁVEL

```cmd
pyinstaller ^
--onefile ^
--windowed ^
--icon=favicon.ico ^
--name="claustro" ^
--add-data "content;content" ^
main.py
```

Executável gerado em:

```text
/dist/claustro.exe
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# GERAR INSTALADOR

Abra:

```text
installer/setup.iss
```

Depois:

```text
Build → Compile
```

Resultado:

```text
installer/output/ClaustroSetup.exe
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# PUBLICAR NOVA VERSÃO

1. alterar version.py;
2. gerar novo exe;
3. compilar instalador;
4. criar release no GitHub;
5. atualizar update.json;
6. publicar na Vercel.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# PUBLICAR SITE

```cmd
vercel --prod
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# ESTRUTURA DO PROJETO

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

```text
ClaustroDoMundo/
│
├── main.py
├── updater.py
├── version.py
├── favicon.ico
│
├── assets/
├── build/
├── dist/
├── installer/
│   ├── setup.iss
│   └── output/
│
├── content/
│   ├── regra_diaria.json
│   ├── salmos.json
│   ├── music/
│   └── feeddata.json
│
├── core/
│   ├── database.py
│   ├── regra.py
│   ├── salmos.py
│   └── static_text.py
│
├── services/
│   ├── music_service.py
│   └── liturgia_service.py
│
├── ui/
│   ├── app.py
│   └── frames/
│
└── utils/
    └── content_loader.py
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# TECNOLOGIAS UTILIZADAS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

* Python
* Tkinter
* SQLite
* PyInstaller
* Inno Setup
* Requests
* BeautifulSoup
* Feedparser
* pygame
* ftfy
* GitHub Releases
* Vercel

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# INSTALAÇÃO DAS DEPENDÊNCIAS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

```cmd
pip install requests
pip install beautifulsoup4
pip install feedparser
pip install pygame
pip install ftfy
pip install pyinstaller
```

Ou:

```cmd
pip install -r requirements.txt
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# EXECUÇÃO EM DESENVOLVIMENTO

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

```cmd
python main.py
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# FUNCIONALIDADES PRINCIPAIS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## REGRA DIÁRIA

Sistema de horários espirituais:

* consagração da manhã;
* angelus;
* recolhimento da tarde;
* rosário;
* fechamento do dia;
* grande silêncio.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## LITURGIA DIÁRIA

Busca automática:

* evangelho;
* salmo;
* referência litúrgica.

Possui:

* cache SQLite;
* fallback offline;
* scraping automático.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## SISTEMA DE NOTÍCIAS

Coleta automática via RSS.

Feeds:

* Vatican News;
* Canção Nova;
* CNBB;
* Aleteia;
* Reuters;
* BBC;
* NPR;
* CNA;
* Crux;
* entre outros.

Características:

* coleta incremental;
* prevenção de duplicação;
* extração automática do conteúdo;
* limpeza de HTML;
* detecção de texto corrompido;
* atualização silenciosa;
* worker em segundo plano.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## MODO CELA

Modo visual minimalista focado em:

* silêncio;
* recolhimento;
* oração;
* baixa estimulação.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## MÉTRICAS ESPIRITUAIS

O sistema calcula:

* disciplina;
* streak;
* tendência espiritual;
* consistência do terço;
* média de quedas;
* melhor horário espiritual.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## SISTEMA DE MÚSICA

Reprodução de:

* músicas católicas;
* ambientação;
* oração.

Implementado com pygame.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# SQLITE E PERSISTÊNCIA

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

O banco SQLite é salvo em:

```text
C:\Users\USUARIO\AppData\Roaming\ClaustroDoMundo\
```

Isso evita:

* problemas com Program Files;
* perda de dados;
* falhas do PyInstaller;
* erros de permissão.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# SISTEMA DE ATUALIZAÇÃO

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Fluxo:

```text
Aplicativo inicia
↓
Verifica update.json
↓
Nova versão encontrada
↓
Baixa instalador
↓
Fecha aplicativo
↓
Executa atualização
↓
Nova versão instalada
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Arquivos envolvidos

### updater.py

Responsável por:

* verificar versões;
* baixar instalador;
* iniciar atualização.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### version.py

Define a versão atual.

Exemplo:

```python
APP_VERSION = "1.0.0"
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### update.json

Arquivo online usado pelo updater.

Exemplo:

```json
{
  "version": "1.0.0",
  "download_url": "https://github.com/SEUUSUARIO/claustro-app/releases/download/v1.0.0/ClaustroSetup.exe"
}
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# INNO SETUP

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Arquivo:

```text
installer/setup.iss
```

Configuração utilizada:

* fechamento automático do app;
* mutex de proteção;
* reinício automático;
* instalador moderno;
* suporte x64.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# COMANDO COMPLETO DE BUILD

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

```cmd
rmdir /s /q build
rmdir /s /q dist
if exist claustro.spec del /q claustro.spec

pyinstaller ^
--onefile ^
--windowed ^
--icon=favicon.ico ^
--name="claustro" ^
--add-data "content;content" ^
main.py
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# WORKER DE NOTÍCIAS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

O sistema possui worker daemon que:

* verifica feeds RSS;
* coleta novos artigos;
* atualiza SQLite;
* notifica a UI.

Atualização automática:

```text
20 em 20 minutos
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# PYINSTALLER

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

O projeto utiliza:

```python
sys._MEIPASS
```

para resolver caminhos corretamente no executável.

Funções importantes:

* resource_path();
* caminho_base();
* caminho_recurso();

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# CACHE E DADOS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Persistidos em:

```text
AppData/Roaming/ClaustroDoMundo
```

Inclui:

* banco SQLite;
* cache litúrgico;
* progresso;
* streak;
* dados espirituais.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# INTERFACE

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Interface construída em Tkinter.

Características:

* design clean;
* tons claros;
* cartões modernos;
* scroll customizado;
* modo cela;
* leitura confortável.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# MÓDULOS IMPORTANTES

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## core/database.py

Responsável por:

* SQLite;
* tabelas;
* persistência.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## services/music_service.py

Responsável por:

* reprodução de música;
* pygame mixer;
* controle de áudio.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## utils/content_loader.py

Responsável por:

* carregamento de JSON;
* compatibilidade PyInstaller.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## services/liturgia_service.py

Responsável por:

* scraping;
* cache;
* fallback offline.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# DEPLOY

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## SITE

Hospedado na Vercel.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## INSTALADORES

Hospedados no GitHub Releases.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# BOAS PRÁTICAS IMPORTANTES

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

* nunca salvar banco em Program Files;
* nunca remover releases antigas;
* manter mesmo nome do executável;
* manter mesmo nome do instalador;
* aumentar versão antes do build;
* atualizar update.json após release.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# PROBLEMAS JÁ RESOLVIDOS

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## SQLite

Correção:

```text
unable to open database file
```

Solução:

```text
AppData/Roaming
```

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## PyInstaller

Correção de:

* caminhos relativos;
* JSON embutido;
* músicas;
* assets.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

## Atualização

Correção de:

* app preso em memória;
* conflito de arquivos;
* erro DeleteFile code 5.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# ESTADO ATUAL DO PROJETO

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

O projeto já possui:

* arquitetura modular;
* atualização automática;
* instalador profissional;
* SQLite persistente;
* cache litúrgico;
* worker de notícias;
* feeds RSS;
* scraping;
* interface desktop moderna;
* compatibilidade com PyInstaller;
* deploy web;
* GitHub Releases.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# AUTOR

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Projeto Claustro do Mundo.

Aplicativo desktop espiritual focado em:

* disciplina;
* oração;
* recolhimento;
* vida sacramental;
* ascese;
* rotina cristã.
