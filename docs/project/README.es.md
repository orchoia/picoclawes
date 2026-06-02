<div align="center">
<img src="../../assets/logo.webp" alt="PicoClaw" width="512">

<h1>PicoClaw: Asistente de IA Ultraeficiente en Go</h1>

<h3>Hardware de $10 · 10MB de RAM · Boot en ms · ¡Let's Go, PicoClaw!</h3>
  <p>
    <img src="https://img.shields.io/badge/Go-1.25+-00ADD8?style=flat&logo=go&logoColor=white" alt="Go">
    <img src="https://img.shields.io/badge/Arch-x86__64%2C%20ARM64%2C%20MIPS%2C%20RISC--V%2C%20LoongArch-blue" alt="Hardware">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
    <br>
    <a href="https://picoclaw.io"><img src="https://img.shields.io/badge/Website-picoclaw.io-blue?style=flat&logo=google-chrome&logoColor=white" alt="Website"></a>
    <a href="https://docs.picoclaw.io/"><img src="https://img.shields.io/badge/Docs-Official-007acc?style=flat&logo=read-the-docs&logoColor=white" alt="Docs"></a>
    <a href="https://deepwiki.com/sipeed/picoclaw"><img src="https://img.shields.io/badge/Wiki-DeepWiki-FFA500?style=flat&logo=wikipedia&logoColor=white" alt="Wiki"></a>
    <br>
    <a href="https://x.com/SipeedIO"><img src="https://img.shields.io/badge/X_(Twitter)-SipeedIO-black?style=flat&logo=x&logoColor=white" alt="Twitter"></a>
    <a href="../../assets/wechat.png"><img src="https://img.shields.io/badge/WeChat-Group-41d56b?style=flat&logo=wechat&logoColor=white"></a>
    <a href="https://discord.gg/V4sAZ9XWpN"><img src="https://img.shields.io/badge/Discord-Community-4c60eb?style=flat&logo=discord&logoColor=white" alt="Discord"></a>
  </p>

[中文](README.zh.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Português](README.pt-br.md) | [Tiếng Việt](README.vi.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [Bahasa Indonesia](README.id.md) | [Malay](README.ms.md) | **Español** | [English](../../README.md)

</div>

---

> **PicoClaw** es un proyecto open-source independiente iniciado por [Sipeed](https://sipeed.com), escrito completamente en **Go** desde cero — no es un fork de OpenClaw, NanoBot ni ningún otro proyecto.

**PicoClaw** es un asistente de IA personal ultraligero inspirado en [NanoBot](https://github.com/HKUDS/nanobot). Fue reconstruido desde cero en **Go** mediante un proceso de "auto-bootstrapping" — el propio agente de IA impulsó la migración de la arquitectura y la optimización del código.

**Funciona en hardware de $10 con menos de 10 MB de RAM** — ¡eso es un 99% menos de memoria que OpenClaw y un 98% más barato que un Mac mini!

<table align="center">
<tr align="center">
<td align="center" valign="top">
<p align="center">
<img src="../../assets/picoclaw_mem.gif" width="360" height="240">
</p>
</td>
<td align="center" valign="top">
<p align="center">
<img src="../../assets/licheervnano.png" width="400" height="240">
</p>
</td>
</tr>
</table>

> [!CAUTION]
> **Aviso de seguridad**
>
> * **SIN CRIPTOMONEDAS:** PicoClaw **no** ha emitido ningún token oficial ni criptomoneda. Todas las afirmaciones en `pump.fun` u otras plataformas de trading son **estafas**.
> * **DOMINIO OFICIAL:** El **ÚNICO** sitio web oficial es **[picoclaw.io](https://picoclaw.io)**, y el sitio web de la empresa es **[sipeed.com](https://sipeed.com)**
> * **CUIDADO:** Muchos dominios `.ai/.org/.com/.net/...` han sido registrados por terceros. No confíe en ellos.
> * **NOTA:** PicoClaw está en desarrollo temprano y rápido. Puede haber problemas de seguridad no resueltos. No lo implemente en producción antes de v1.0.
> * **NOTA:** PicoClaw ha fusionado recientemente muchos PRs. Las versiones recientes pueden usar 10-20 MB de RAM. La optimización de recursos está planificada después de la estabilización de funciones.

## 📢 Novedades

2026-05-11 🛒 **¡LicheeRV-Claw en AliExpress!** Ya puede comprar LicheeRV-Claw en [AliExpress](https://www.aliexpress.com/item/1005006519668532.html), lo que facilita probar PicoClaw en hardware RISC-V compacto.

<p align="center">
  <a href="https://www.aliexpress.com/item/1005006519668532.html">
    <img src="../../assets/licheerv-claw.jpg" alt="LicheeRV-Claw en AliExpress" width="520">
  </a>
</p>

2026-03-31 📱 **¡Soporte para Android!** ¡PicoClaw ahora funciona en Android! Descargue el APK en [picoclaw.io](https://picoclaw.io/download)

2026-03-25 🚀 **¡v0.2.4 Publicada!** Reestructuración de la arquitectura del agente (SubTurn, Hooks, Steering, EventBus), integración con WeChat/WeCom, endurecimiento de seguridad (.security.yml, filtrado de datos sensibles), nuevos proveedores (AWS Bedrock, Azure, Xiaomi MiMo) y 35 correcciones de errores. ¡PicoClaw ha alcanzado las **26K estrellas**!

2026-03-17 🚀 **¡v0.2.3 Publicada!** Interfaz de bandeja del sistema (Windows y Linux), consulta de estado de subagentes (`spawn_status`), recarga en caliente experimental del Gateway, restricción de seguridad de Cron y 2 correcciones de seguridad. ¡PicoClaw ha alcanzado las **25K estrellas**!

2026-03-09 🎉 **v0.2.1 — ¡La actualización más grande hasta ahora!** Soporte del protocolo MCP, 4 nuevos canales (Matrix/IRC/WeCom/Discord Proxy), 3 nuevos proveedores (Kimi/Minimax/Avian), pipeline de visión, almacenamiento de memoria JSONL, enrutamiento de modelos.

2026-02-28 📦 **v0.2.0** publicada con soporte de Docker Compose y Web UI Launcher.

<details>
<summary>Novedades anteriores...</summary>

2026-02-26 🎉 ¡PicoClaw alcanza las **20K estrellas** en solo 17 días! Orquestación automática de canales e interfaces de capacidad activas.

2026-02-16 🎉 ¡PicoClaw supera las 12K estrellas en una semana! Roles de mantenedor de la comunidad y [Roadmap](../../ROADMAP.md) lanzados oficialmente.

2026-02-13 🎉 ¡PicoClaw supera las 5000 estrellas en 4 días! Roadmap del proyecto y grupos de desarrolladores en progreso.

2026-02-09 🎉 **¡PicoClaw publicado!** Construido en 1 día para llevar agentes de IA a hardware de $10 con menos de 10 MB de RAM. ¡Let's Go, PicoClaw!

</details>

## ✨ Características

🪶 **Ultraligero**: Huella de memoria del núcleo <10 MB — 99% más pequeño que OpenClaw.*

💰 **Costo mínimo**: Suficientemente eficiente para funcionar en hardware de $10 — 98% más barato que un Mac mini.

⚡️ **Arranque ultrarrápido**: Inicio 400x más rápido. Arranca en <1s incluso en un procesador mononúcleo de 0.6 GHz.

🌍 **Realmente portátil**: Binario único para las arquitecturas RISC-V, ARM, MIPS y x86. ¡Un solo binario, funciona en todas partes!

🤖 **Auto-impulsado por IA**: Implementación nativa en Go puro — el 95% del código central fue generado por un agente y ajustado mediante revisión humana.

🔌 **Soporte MCP**: Integración nativa con [Model Context Protocol](https://modelcontextprotocol.io/) — conecte cualquier servidor MCP para extender las capacidades del agente.

👁️ **Pipeline de visión**: Envíe imágenes y archivos directamente al agente — codificación base64 automática para LLMs multimodales.

🧠 **Enrutamiento inteligente**: Enrutamiento de modelos basado en reglas — las consultas simples van a modelos ligeros, ahorrando costos de API.

_*Las versiones recientes pueden usar 10-20 MB debido a fusiones rápidas de PRs. La optimización de recursos está planificada. La comparación de velocidad de arranque se basa en puntos de referencia de un solo núcleo a 0.8 GHz (ver tabla a continuación)._

<div align="center">

|                                | OpenClaw      | NanoBot                  | **PicoClaw**                           |
| ------------------------------ | ------------- | ------------------------ | -------------------------------------- |
| **Lenguaje**                   | TypeScript    | Python                   | **Go**                                 |
| **RAM**                        | >1 GB         | >100 MB                  | **< 10 MB***                           |
| **Tiempo de arranque**</br>(núcleo a 0.8 GHz) | >500 s        | >30 s                    | **<1 s**                               |
| **Costo**                      | Mac Mini $599 | La mayoría de placas Linux ~$50 | **Cualquier placa Linux**</br>**desde $10** |

<img src="../../assets/compare.jpg" alt="PicoClaw" width="512">

</div>

> **[Lista de compatibilidad de hardware](../../docs/guides/hardware-compatibility.md)** — Consulte todas las placas probadas, desde RISC-V de $5 hasta Raspberry Pi y teléfonos Android. ¿Su placa no está listada? ¡Envíe un PR!

<p align="center">
<img src="../../assets/hardware-banner.jpg" alt="Compatibilidad de hardware de PicoClaw" width="100%">
</p>

## 🦾 Demostración

### 🛠️ Flujos de trabajo estándar del asistente

<table align="center">
<tr align="center">
<th><p align="center">Modo ingeniero full-stack</p></th>
<th><p align="center">Registro y planificación</p></th>
<th><p align="center">Búsqueda web y aprendizaje</p></th>
</tr>
<tr>
<td align="center"><p align="center"><img src="../../assets/picoclaw_code.gif" width="240" height="180"></p></td>
<td align="center"><p align="center"><img src="../../assets/picoclaw_memory.gif" width="240" height="180"></p></td>
<td align="center"><p align="center"><img src="../../assets/picoclaw_search.gif" width="240" height="180"></p></td>
</tr>
<tr>
<td align="center">Desarrollar · Implementar · Escalar</td>
<td align="center">Programar · Automatizar · Recordar</td>
<td align="center">Descubrir · Perspectivas · Tendencias</td>
</tr>
</table>

### 🐜 Implementación innovadora de baja huella

¡PicoClaw se puede implementar en prácticamente cualquier dispositivo Linux!

- Edición $9.9 [LicheeRV-Nano](https://www.aliexpress.com/item/1005006519668532.html) E (Ethernet) o W (WiFi6), para un asistente doméstico mínimo
- $30~50 [NanoKVM](https://www.aliexpress.com/item/1005007369816019.html), o $100 [NanoKVM-Pro](https://www.aliexpress.com/item/1005010048471263.html), para operaciones de servidor automatizadas
- $50 [MaixCAM](https://www.aliexpress.com/item/1005008053333693.html) o $100 [MaixCAM2](https://www.kickstarter.com/projects/zepan/maixcam2-build-your-next-gen-4k-ai-camera), para vigilancia inteligente

<https://private-user-images.githubusercontent.com/83055338/547056448-e7b031ff-d6f5-4468-bcca-5726b6fecb5c.mp4>

🌟 ¡Más casos de implementación esperan!

## 📦 Instalación

### Descargar desde picoclaw.io (Recomendado)

Visite **[picoclaw.io](https://picoclaw.io)** — el sitio web oficial detecta automáticamente su plataforma y ofrece descarga con un solo clic. No es necesario seleccionar manualmente una arquitectura.

### Descargar binario precompilado

Alternativamente, descargue el binario para su plataforma desde la página de [GitHub Releases](https://github.com/sipeed/picoclaw/releases).

### Compilar desde el código fuente (para desarrollo)

Requisitos previos:

- Go 1.25+
- Node.js 22+ y pnpm 10.33.0+ para compilaciones de Web UI / launcher

```bash
git clone https://github.com/sipeed/picoclaw.git

cd picoclaw
make deps

# Instalar dependencias del frontend
(cd web/frontend && pnpm install --frozen-lockfile)

# Compilar el binario principal para la plataforma actual
make build

# Compilar el Web UI Launcher (requerido para el modo WebUI)
make build-launcher

# Compilar binarios principales para todas las plataformas gestionadas por Makefile
make build-all

# Compilar para Raspberry Pi Zero 2 W
# 32 bits: make build-linux-arm
# 64 bits: make build-linux-arm64
make build-pi-zero

# Compilar e instalar
make install
```

**Raspberry Pi Zero 2 W:** Use el binario que coincida con su SO: Raspberry Pi OS de 32 bits -> `make build-linux-arm`; 64 bits -> `make build-linux-arm64`. O ejecute `make build-pi-zero` para compilar ambos.

## 🚀 Guía de inicio rápido

### 🌐 WebUI Launcher (Recomendado para escritorio)

El WebUI Launcher proporciona una interfaz basada en navegador para configuración y chat. Esta es la forma más fácil de empezar — no se requieren conocimientos de línea de comandos.

**Opción 1: Doble clic (Escritorio)**

Después de descargar desde [picoclaw.io](https://picoclaw.io), haga doble clic en `picoclaw-launcher` (o `picoclaw-launcher.exe` en Windows). Su navegador se abrirá automáticamente en `http://localhost:18800`.

**Opción 2: Línea de comandos**

```bash
picoclaw-launcher
# Abra http://localhost:18800 en su navegador
```

> [!TIP]
> **Acceso remoto / Docker / VM:** Agregue la bandera `-public` para escuchar en todas las interfaces:
> ```bash
> picoclaw-launcher -public
> ```

<p align="center">
<img src="../../assets/launcher-webui.jpg" alt="WebUI Launcher" width="600">
</p>

**Primeros pasos:**

Abra el WebUI, luego: **1)** Configure un proveedor (agregue su clave API de LLM) -> **2)** Configure un canal (ej., Telegram) -> **3)** Inicie el Gateway -> **4)** ¡Chatee!

Para documentación detallada del WebUI, consulte [docs.picoclaw.io](https://docs.picoclaw.io).

<details>
<summary><b>Docker (alternativa)</b></summary>

```bash
# 1. Clone este repositorio
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# 2. Primera ejecución — genera automáticamente docker/data/config.json y luego sale
#    (solo se activa cuando faltan tanto config.json como workspace/)
docker compose -f docker/docker-compose.yml --profile launcher up
# El contenedor imprime "First-run setup complete." y se detiene.

# 3. Establezca sus claves API
vim docker/data/config.json

# 4. Iniciar
docker compose -f docker/docker-compose.yml --profile launcher up -d
# Abra http://localhost:18800
```

> **Usuarios de Docker / VM:** El Gateway escucha en `127.0.0.1` de forma predeterminada. Establezca `PICOCLAW_GATEWAY_HOST=0.0.0.0` o use la bandera `-public` para hacerlo accesible desde el host.

```bash
# Ver registros
docker compose -f docker/docker-compose.yml logs -f

# Detener
docker compose -f docker/docker-compose.yml --profile launcher down

# Actualizar
docker compose -f docker/docker-compose.yml pull
docker compose -f docker/docker-compose.yml --profile launcher up -d
```

</details>

<details>
<summary><b>macOS — Advertencia de seguridad al primer inicio</b></summary>

macOS puede bloquear `picoclaw-launcher` en el primer inicio porque se descargó de internet y no está notarizado a través de la Mac App Store.

**Paso 1:** Haga doble clic en `picoclaw-launcher`. Verá una advertencia de seguridad:

<p align="center">
<img src="../../assets/macos-gatekeeper-warning.jpg" alt="Advertencia de Gatekeeper de macOS" width="400">
</p>

> *"picoclaw-launcher" No se abrió — Apple no pudo verificar que "picoclaw-launcher" esté libre de malware que pueda dañar su Mac o comprometer su privacidad.*

**Paso 2:** Abra **Configuración del sistema** → **Privacidad y seguridad** → desplácese hacia abajo hasta la sección **Seguridad** → haga clic en **Abrir de todas formas** → confirme haciendo clic en **Abrir de todas formas** en el diálogo.

<p align="center">
<img src="../../assets/macos-gatekeeper-allow.jpg" alt="macOS Privacidad y seguridad — Abrir de todas formas" width="600">
</p>

Después de este paso único, `picoclaw-launcher` se abrirá normalmente en inicios posteriores.

</details>

<a id="-run-on-old-android-phones"></a>
### 📱 Android

¡Déle una segunda vida a su teléfono de hace una década! Conviértalo en un asistente de IA inteligente con PicoClaw.

**Opción 1: Instalación APK**

Vista previa:

<table>
  <tr>
    <td><img src="../../assets/fui_main_page.jpg" width="200"></td>
    <td><img src="../../assets/fui_web_page.jpg" width="200"></td>
    <td><img src="../../assets/fui_log_page.jpg" width="200"></td>
    <td><img src="../../assets/fui_setting_page.jpg" width="200"></td>
  </tr>
</table>

Descargue el APK desde [picoclaw.io](https://picoclaw.io/download/) e instálelo directamente. ¡No requiere Termux!

**Opción 2: Termux**

<details>
<summary><b>Terminal Launcher (para entornos con recursos limitados)</b></summary>

1. Instale [Termux](https://github.com/termux/termux-app) (descárguelo desde [GitHub Releases](https://github.com/termux/termux-app/releases), o búsquelo en F-Droid / Google Play)
2. Ejecute los siguientes comandos:

```bash
# Descargar la última versión
wget https://github.com/sipeed/picoclaw/releases/latest/download/picoclaw_Linux_arm64.tar.gz
tar xzf picoclaw_Linux_arm64.tar.gz
pkg install proot
termux-chroot ./picoclaw onboard   # chroot proporciona un diseño estándar del sistema de archivos Linux
```

Luego siga la sección de Terminal Launcher a continuación para completar la configuración.

<img src="../../assets/termux.jpg" alt="PicoClaw en Termux" width="512">

Para entornos mínimos donde solo está disponible el binario principal `picoclaw` (sin interfaz de Launcher), puede configurar todo a través de la línea de comandos y un archivo de configuración JSON.

**1. Inicializar**

```bash
picoclaw onboard
```

Esto crea `~/.picoclaw/config.json` y el directorio del espacio de trabajo.

**2. Configurar** (`~/.picoclaw/config.json`)

```json
{
  "agents": {
    "defaults": {
      "model_name": "gpt-5.4"
    }
  },
  "model_list": [
    {
      "model_name": "gpt-5.4",
      "model": "openai/gpt-5.4"
      // api_key ahora se carga desde .security.yml
    }
  ]
}
```

> Consulte `config/config.example.json` en el repositorio para una plantilla de configuración completa con todas las opciones disponibles.
>
> Tenga en cuenta: el formato de config.example.json es la versión 0, con códigos sensibles, y se migrará automáticamente a la versión 1+. Luego, config.json solo almacenará datos no sensibles; los códigos sensibles se almacenarán en .security.yml. Si necesita modificar manualmente los códigos, consulte `docs/security/security_configuration.md` para más detalles.

**3. Chatear**

```bash
# Pregunta única
picoclaw agent -m "¿Cuánto es 2+2?"

# Modo interactivo
picoclaw agent

# Iniciar gateway para integración con aplicaciones de chat
picoclaw gateway
```

</details>

## 🔌 Proveedores (LLM)

PicoClaw es compatible con más de 30 proveedores de LLM a través de la configuración `model_list`. Use el formato `protocolo/modelo`:

| Proveedor | Protocolo | Clave API | Notas |
|----------|----------|---------|-------|
| [OpenAI](https://platform.openai.com/api-keys) | `openai/` | Requerida | GPT-5.4, GPT-4o, o3, etc. |
| [Anthropic](https://console.anthropic.com/settings/keys) | `anthropic/` | Requerida | Claude Opus 4.6, Sonnet 4.6, etc. |
| [Google Gemini](https://aistudio.google.com/apikey) | `gemini/` | Requerida | Gemini 3 Flash, 2.5 Pro, etc. |
| [OpenRouter](https://openrouter.ai/keys) | `openrouter/` | Requerida | Más de 200 modelos, API unificada |
| [Zhipu (GLM)](https://open.bigmodel.cn/usercenter/proj-mgmt/apikeys) | `zhipu/` | Requerida | GLM-4.7, GLM-5, etc. |
| [DeepSeek](https://platform.deepseek.com/api_keys) | `deepseek/` | Requerida | DeepSeek-V3, DeepSeek-R1 |
| [Volcengine](https://console.volcengine.com) | `volcengine/` | Requerida | Doubao, modelos Ark |
| [Qwen](https://dashscope.console.aliyun.com/apiKey) | `qwen/` | Requerida | Qwen3, Qwen-Max, etc. |
| [Groq](https://console.groq.com/keys) | `groq/` | Requerida | Inferencia rápida (Llama, Mixtral) |
| [Moonshot (Kimi)](https://platform.moonshot.cn/console/api-keys) | `moonshot/` | Requerida | Modelos Kimi |
| [Minimax](https://platform.minimaxi.com/user-center/basic-information/interface-key) | `minimax/` | Requerida | Modelos MiniMax |
| [Mistral](https://console.mistral.ai/api-keys) | `mistral/` | Requerida | Mistral Large, Codestral |
| [NVIDIA NIM](https://build.nvidia.com/) | `nvidia/` | Requerida | Modelos alojados por NVIDIA |
| [Cerebras](https://cloud.cerebras.ai/) | `cerebras/` | Requerida | Inferencia rápida |
| [Novita AI](https://novita.ai/) | `novita/` | Requerida | Varios modelos abiertos |
| [Xiaomi MiMo](https://platform.xiaomimimo.com/) | `mimo/` | Requerida | Modelos MiMo |
| [Ollama](https://ollama.com/) | `ollama/` | No necesaria | Modelos locales, auto-alojados |
| [vLLM](https://docs.vllm.ai/) | `vllm/` | No necesaria | Implementación local, compatible con OpenAI |
| [LiteLLM](https://docs.litellm.ai/) | `litellm/` | Varía | Proxy para más de 100 proveedores |
| [Azure OpenAI](https://portal.azure.com/) | `azure/` | Clave API o Entra ID** | Implementación empresarial en Azure |
| [GitHub Copilot](https://github.com/features/copilot) | `github-copilot/` | OAuth | Inicio de sesión con código de dispositivo |
| [Antigravity](https://console.cloud.google.com/) | `antigravity/` | OAuth | Google Cloud AI |
| [AWS Bedrock](https://console.aws.amazon.com/bedrock)* | `bedrock/` | Credenciales AWS | Claude, Llama, Mistral en AWS |

> \* AWS Bedrock requiere etiqueta de compilación: `go build -tags bedrock`. Establezca `api_base` en un nombre de región (ej., `us-east-1`) para resolución automática de endpoints en todas las particiones de AWS (aws, aws-cn, aws-us-gov). Cuando use una URL de endpoint completa, también debe configurar `AWS_REGION` a través de una variable de entorno o perfil de AWS.
>
> \*\* Azure OpenAI usa `api_key` cuando está configurada. Si se omite `api_key`, el proveedor recurre a Microsoft Entra ID mediante `DefaultAzureCredential` (variables de entorno, identidad de carga de trabajo, identidad administrada, Azure CLI, etc.). La ruta de Entra ID requiere la etiqueta de compilación: `go build -tags azidentity`.

<details>
<summary><b>Implementación local (Ollama, vLLM, etc.)</b></summary>

**Ollama:**
```json
{
  "model_list": [
    {
      "model_name": "local-llama",
      "model": "ollama/llama3.1:8b",
      "api_base": "http://localhost:11434/v1"
    }
  ]
}
```

**vLLM:**
```json
{
  "model_list": [
    {
      "model_name": "local-vllm",
      "model": "vllm/your-model",
      "api_base": "http://localhost:8000/v1"
    }
  ]
}
```

Para obtener detalles completos de configuración de proveedores, consulte [Proveedores y modelos](../../docs/guides/providers.md).

</details>

## 💬 Canales (Aplicaciones de chat)

Hable con su PicoClaw a través de más de 19 plataformas de mensajería:

| Canal | Configuración | Protocolo | Docs |
|---------|-------|----------|------|
| **Telegram** | Fácil (token del bot) | Long polling | [Guía](../../docs/channels/telegram/README.md) |
| **Discord** | Fácil (token del bot + intents) | WebSocket | [Guía](../../docs/channels/discord/README.md) |
| **WhatsApp** | Fácil (escaneo QR o URL bridge) | Nativo / Bridge | [Guía](../../docs/guides/chat-apps.md#whatsapp) |
| **Weixin** | Fácil (escaneo QR nativo) | API iLink | [Guía](../../docs/guides/chat-apps.md#weixin) |
| **QQ** | Fácil (AppID + AppSecret) | WebSocket | [Guía](../../docs/channels/qq/README.md) |
| **Slack** | Fácil (token de bot + app) | Socket Mode | [Guía](../../docs/channels/slack/README.md) |
| **Matrix** | Medio (homeserver + token) | Sync API | [Guía](../../docs/channels/matrix/README.md) |
| **DingTalk** | Medio (credenciales de cliente) | Stream | [Guía](../../docs/channels/dingtalk/README.md) |
| **Feishu / Lark** | Medio (App ID + Secret) | WebSocket/SDK | [Guía](../../docs/channels/feishu/README.md) |
| **LINE** | Medio (credenciales + webhook) | Webhook | [Guía](../../docs/channels/line/README.md) |
| **WeCom** | Fácil (inicio de sesión QR o manual) | WebSocket | [Guía](../../docs/channels/wecom/README.md) |
| **VK** | Fácil (token de grupo) | Long Poll | [Guía](../../docs/channels/vk/README.md) |
| **IRC** | Medio (servidor + nick) | Protocolo IRC | [Guía](../../docs/guides/chat-apps.md#irc) |
| **OneBot** | Medio (URL WebSocket) | OneBot v11 | [Guía](../../docs/channels/onebot/README.md) |
| **MQTT** | Fácil (broker + agent_id) | MQTT pub/sub | [Guía](../../docs/channels/mqtt/README.md) |
| **MaixCam** | Fácil (habilitar) | Socket TCP | [Guía](../../docs/channels/maixcam/README.md) |
| **Pico** | Fácil (habilitar) | Protocolo nativo | Integrado |
| **Pico Client** | Fácil (URL WebSocket) | WebSocket | Integrado |

> Todos los canales basados en webhook comparten un único servidor HTTP de Gateway (`gateway.host`:`gateway.port`, predeterminado `127.0.0.1:18790`). Feishu usa el modo WebSocket/SDK y no utiliza el servidor HTTP compartido.

> La verbosidad de los registros se controla con `gateway.log_level` (predeterminado: `warn`). Valores compatibles: `debug`, `info`, `warn`, `error`, `fatal`. También se puede configurar mediante `PICOCLAW_LOG_LEVEL`. Consulte [Configuración](../../docs/guides/configuration.md#gateway-log-level) para más detalles.

Para obtener instrucciones detalladas de configuración de canales, consulte [Configuración de aplicaciones de chat](../../docs/guides/chat-apps.md).

## 🔧 Herramientas

### 🔍 Búsqueda web

PicoClaw puede buscar en la web para proporcionar información actualizada. Configure en `tools.web`:

| Motor de búsqueda | Clave API | Nivel gratuito | Enlace |
|--------------|---------|-----------|------|
| DuckDuckGo | No necesaria | Ilimitado | Respaldo integrado |
| [Gemini Google Search](https://aistudio.google.com/apikey) | Requerida | Varía | Gemini con fundamento de búsqueda de Google |
| [Baidu Search](https://cloud.baidu.com/doc/qianfan-api/s/Wmbq4z7e5) | Requerida | 1500/mes (asignación diaria) | Impulsado por IA, optimizado para China |
| [Tavily](https://tavily.com) | Requerida | 1000 consultas/mes | Optimizado para agentes de IA |
| [Brave Search](https://brave.com/search/api) | Requerida | 2000 consultas/mes | Rápido y privado |
| [Perplexity](https://www.perplexity.ai) | Requerida | Pago | Búsqueda impulsada por IA |
| [SearXNG](https://github.com/searxng/searxng) | No necesaria | Auto-alojado | Metamotor de búsqueda gratuito |
| [GLM Search](https://open.bigmodel.cn/) | Requerida | Varía | Búsqueda web de Zhipu |

### ⚙️ Otras herramientas

PicoClaw incluye herramientas integradas para operaciones de archivos, ejecución de código, programación y más. Consulte [Configuración de herramientas](../../docs/reference/tools_configuration.md) para más detalles.

## 🎯 Habilidades

Las habilidades son capacidades modulares que extienden su agente. Se cargan desde archivos `SKILL.md` en su espacio de trabajo.

**Instalar habilidades desde ClawHub:**

```bash
picoclaw skills search "web scraping"
picoclaw skills install <nombre-habilidad>
```

**Configurar registros de habilidades:**

Agregue a su `config.json`:
```json
{
  "tools": {
    "skills": {
      "registries": {
        "clawhub": {
          "auth_token": "su-token-clawhub"
        },
        "github": {
          "base_url": "https://github.com",
          "auth_token": "su-token-github",
          "proxy": ""
        }
      }
    }
  }
}
```

`tools.skills.github.*` está obsoleto. Use `tools.skills.registries.github.*` en su lugar.

Para más detalles, consulte [Configuración de herramientas - Habilidades](../../docs/reference/tools_configuration.md#skills-tool).

## 🔗 MCP (Model Context Protocol)

PicoClaw es compatible de forma nativa con [MCP](https://modelcontextprotocol.io/) — conecte cualquier servidor MCP para extender las capacidades de su agente con herramientas y fuentes de datos externas.

```json
{
  "tools": {
    "mcp": {
      "enabled": true,
      "servers": {
        "filesystem": {
          "enabled": true,
          "command": "npx",
          "args": ["-y", "@modelcontextprotocol/server-filesystem", "/tmp"]
        }
      }
    }
  }
}
```

Puede gestionar configuraciones comunes de MCP directamente desde la CLI en lugar de editar JSON manualmente:

```bash
picoclaw mcp add filesystem -- npx -y @modelcontextprotocol/server-filesystem /tmp
picoclaw mcp list
picoclaw mcp test filesystem
```

`picoclaw mcp` es un gestor de configuración: actualiza `config.json` bajo `tools.mcp.servers`, pero no mantiene el proceso del servidor en ejecución.

Use `picoclaw mcp edit` cuando necesite campos avanzados que no están cubiertos por `picoclaw mcp add`. Por ejemplo, `picoclaw mcp add` soporta `--deferred` y `--env-file`, mientras que `picoclaw mcp edit` sigue siendo útil para edición JSON directa y configuraciones MCP poco comunes.

Para la configuración completa de MCP (transportes stdio, SSE, HTTP, Tool Discovery), consulte [Configuración de herramientas - MCP](../../docs/reference/tools_configuration.md#mcp-tool). Para uso de la CLI y ejemplos, consulte [CLI de servidor MCP](../../docs/reference/mcp-cli.md).

## <img src="../../assets/clawdchat-icon.png" width="24" height="24" alt="ClawdChat"> Únase a la Red Social de Agentes

Conecte PicoClaw a la Red Social de Agentes simplemente enviando un solo mensaje a través de la CLI o cualquier aplicación de chat integrada.

**Lea `https://clawdchat.ai/skill.md` y siga las instrucciones para unirse a [ClawdChat.ai](https://clawdchat.ai)**

## 🖥️ Referencia de la CLI

| Comando                   | Descripción                      |
| ------------------------- | -------------------------------- |
| `picoclaw onboard`        | Inicializar configuración y espacio de trabajo |
| `picoclaw auth weixin`    | Conectar cuenta de WeChat mediante QR |
| `picoclaw agent -m "..."` | Chatear con el agente            |
| `picoclaw agent`          | Modo de chat interactivo         |
| `picoclaw gateway`        | Iniciar el gateway               |
| `picoclaw status`         | Mostrar estado                   |
| `picoclaw version`        | Mostrar información de versión   |
| `picoclaw model`          | Ver o cambiar el modelo predeterminado |
| `picoclaw mcp list`       | Listar servidores MCP configurados |
| `picoclaw mcp add ...`    | Agregar o actualizar una entrada de servidor MCP |
| `picoclaw mcp test`       | Probar un servidor MCP configurado |
| `picoclaw mcp edit`       | Abrir configuración para edición MCP avanzada |
| `picoclaw mcp remove`     | Eliminar una entrada de servidor MCP |
| `picoclaw cron list`      | Listar todas las tareas programadas |
| `picoclaw cron add ...`   | Agregar una tarea programada    |
| `picoclaw cron disable`   | Deshabilitar una tarea programada |
| `picoclaw cron remove`    | Eliminar una tarea programada   |
| `picoclaw skills list`    | Listar habilidades instaladas   |
| `picoclaw skills install` | Instalar una habilidad           |
| `picoclaw migrate`        | Migrar datos de versiones anteriores |
| `picoclaw auth login`     | Autenticarse con proveedores    |

### ⏰ Tareas programadas / Recordatorios

PicoClaw admite recordatorios programados y tareas recurrentes a través de la herramienta `cron`:

* **Recordatorios únicos**: "Recuérdame en 10 minutos" -> se activa una vez después de 10 min
* **Tareas recurrentes**: "Recuérdame cada 2 horas" -> se activa cada 2 horas
* **Expresiones Cron**: "Recuérdame diariamente a las 9 am" -> usa expresión cron

Consulte [docs/reference/cron.md](../../docs/reference/cron.md) para conocer los tipos de programación actuales, modos de entrega, compuertas de comandos y detalles de persistencia.

## 📚 Documentación

Para guías detalladas más allá de este README:

| Tema | Descripción |
|-------|-------------|
| [Docker e inicio rápido](../../docs/guides/docker.md) | Configuración de Docker Compose, modos Launcher/Agente |
| [Aplicaciones de chat](../../docs/guides/chat-apps.md) | Todas las guías de configuración de más de 18 canales |
| [Configuración](../../docs/guides/configuration.md) | Variables de entorno, diseño del espacio de trabajo, sandbox de seguridad |
| [CLI de servidor MCP](../../docs/reference/mcp-cli.md) | Agregar, listar, probar, editar y eliminar entradas de servidor MCP desde la CLI |
| [Tareas programadas y Cron](../../docs/reference/cron.md) | Tipos de programación Cron, modos de entrega, compuertas de comandos, almacenamiento de trabajos |
| [Proveedores y modelos](../../docs/guides/providers.md) | Más de 30 proveedores de LLM, enrutamiento de modelos, configuración de model_list |
| [Spawn y tareas asíncronas](../../docs/guides/spawn-tasks.md) | Tareas rápidas, tareas largas con spawn, orquestación de subagentes asíncronos |
| [Hooks](../../docs/architecture/hooks/README.md) | Sistema de hooks basado en eventos: observadores, interceptores, hooks de aprobación |
| [Steering](../../docs/architecture/steering.md) | Inyectar mensajes en un bucle de agente en ejecución entre llamadas a herramientas |
| [SubTurn](../../docs/architecture/subturn.md) | Coordinación de subagentes, control de concurrencia, ciclo de vida |
| [Solución de problemas](../../docs/operations/troubleshooting.md) | Problemas comunes y soluciones |
| [Configuración de herramientas](../../docs/reference/tools_configuration.md) | Activación/desactivación por herramienta, políticas de ejecución, MCP, habilidades |
| [Compatibilidad de hardware](../../docs/guides/hardware-compatibility.md) | Placas probadas, requisitos mínimos |

## 🤝 Contribuir y Roadmap

¡Los PRs son bienvenidos! La base de código es intencionalmente pequeña y legible.

Consulte nuestro [Roadmap de la comunidad](https://github.com/sipeed/picoclaw/issues/988) y [CONTRIBUTING.md](../../CONTRIBUTING.md) para obtener pautas.

¡Grupo de desarrolladores, únase después de su primer PR fusionado!

Grupos de usuarios:

Discord: <https://discord.gg/V4sAZ9XWpN>

WeChat:
<img src="../../assets/wechat.png" alt="Código QR del grupo de WeChat" width="512">
