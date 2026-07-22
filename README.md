# Development Environment Setup
<p align="center">
  <img src ="https://github.com/amrangry/dev_macOS_environment_setup/blob/main/GFX_ASSETS/dev_tools.jpg?raw=true"/>
</p>

- [x] **Package manager for macOS**
  - [x] [Homebrew](https://brew.sh/)
  - [x] Ruby version manager [rbenv](https://github.com/rbenv/rbenv)
  - [ ] [macports](https://www.macports.org/install.php)

- [x] **General**
  - [x] [Z Shell via Oh My Zsh](Oh%20My%20Zsh.md)
  - [x] Modern Terminal
   - [x] [WezTerm](https://wezterm.org)
   - [x] [Ghostty](https://ghostty.org/)
  - [x] [How to use macOS Recovery!](macos-tips.md#How-to-use-macOS-Recovery%21)
  - [x] [The Quickest Way to Show/Hide Hidden Files](macos-tips.md#The-Quickest-Way-to-Show%2FHide-Hidden-Files)
  - [x] [Prevent Future .DS_Store Files (Optional)](macos-tips.md#Prevent-Future-.DS_Store-Files-(Optional))
  - [x] [Modify text files via terminal](macos-tips.md#Modify-text-files-via-terminal)
  - [x] [Modify-text-files-via-Nano](macos-tips.md#Modify-text-files-via-Nano)

- [x] **🛠 XCode Setup **
  - [x] [xcode setup](Xcode-setup.md)
  - [ ] [MacSpaceCleaner](https://github.com/sanketk2020/MacSpaceCleaner)
        
- [x] **🛠 CLI shortcuts Setup on Mac -command line interface - ** 
>> Standardized terminal configuration for React Native, PHP, WordPress, AI Development Tools, and IDE Launchers
  - [x] [CLI Standardized Configuration](cli-configuration.md)
  - [x] [PhpStorm CLI Setup on macOS](PhpStorm-setup.md)

- [x] **Text Editors**
  - [x] [Sublime Download](https://www.sublimetext.com/download_thanks?target=mac)

- [x] **GitHub - SSH Access**      
  - [x] [SSH Setup for Business GitHub vs Personal Account](SSH%20Setup%20for%20Business%20GitHub%20vs%20Personal%20Account.md)

- [x] **Package Managers for Programming Languages**
  - [x] [CocoaPods](https://guides.cocoapods.org/using/getting-started.html)
  - [ ] NPM
  - [x] [Composer][PhpStorm CLI Setup on macOS](PhpStorm-setup.md)
  - [ ] etc...

<details>
<summary>🤖 AI Tools</summary>

	
<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;📦 OpenCode</summary>
	
  - [x] [OpenCode](https://opencode.ai/) - Open source AI coding agent available as a terminal app, desktop app, and IDE extension.
  - [x] Docs: [OpenCode Documentation](https://opencode.ai/docs)
  - [x] Run OpenCode
    ```bash
    opencode
    ```
  - [x] Initialize the project
    ```bash
    /init
    ```
  - [x] Open model picker
    ```text
    /models
    ```
  - [x] Configure default model in `opencode.json`

    ```json
    {
      "model": "provider/model-id"
    }
    ``` 
</details>
</details>

<details>
<summary>🦙 Ollama -Local LLM-</summary>

 - [x] [ollama](https://ollama.com/) Run local AI models on your machine.
 - [X] [Ollama Models list](https://ollama.com/search?c=tools) or [models library](https://ollama.com/library)

<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;<strong>⚙️ Ollama Configuration (One-Time Setup)</strong></summary>

### Create Configuration File

```bash
mkdir -p ~/.ollama
nano ~/.ollama/config.yaml
```

### Content

```yaml
api:
  enabled: true
  address: 0.0.0.0:11434
```

### Test Configuration

```bash
curl http://localhost:11434/v1/models
```

If JSON containing your models is returned, the OpenAI-compatible API is enabled successfully.

</details>

<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;<strong>⌨️ Useful Ollama Commands</strong></summary>

### Check Running Processes

```bash
ps aux | grep ollama
```

### Start Server

```bash
ollama serve
```

### Download Model

```bash
ollama pull <model-name>
```

Example:

```bash
ollama pull qwen3:latest
```

### Run Model

```bash
ollama run <model-name>
```

Example:

```bash
ollama run qwen3:latest
```

### List Installed Models

```bash
ollama list
```

### Show Model Details

```bash
ollama show <model-name>
```

### Create Custom Model

```bash
ollama create
```

### Remove Model

```bash
ollama rm <model-name>
```

</details>
</details>

<details>
<summary><strong>🖥️ Cursor + Local LLM</strong></summary>

### Overview

- Cursor needs **Ollama running** when you use a local model.
- Use either **Ollama.app** or **`ollama serve`** from terminal.
- Your **config.yaml is permanent** and normally only needs to be configured once.

#### Verify Ollama is running

- http://localhost:11434/v1/models
- http://localhost:11434/

  <details>
<summary><strong>&nbsp;&nbsp;&nbsp;&nbsp;🎯 Configure Cursor (One-Time)</strong></summary>

### OpenAI Settings

1. Open **Cursor → Settings → Models → OpenAI**
2. Enable **Override OpenAI Base URL**
3. Set Base URL:

```text
http://localhost:11434/v1
```

Original value:

```text
https://api.openai.com/v1
```

4. Set any non-empty API Key:

```text
ollama
```

5. Add your local models:

- `qwen3:latest`
- `gpt-oss:20b`
- `llama3.1:8b`
- `deepseek-r1:7b`
-  etc...

This only needs to be done once unless you reinstall Cursor.

</details>

</details>



<details>
<summary><strong>🏗️ Architecture Summary (My Setup)</strong></summary>

```text
macOS
│
├── Ollama (local runtime)
│     ├── deepseek-r1:7b
│     ├── mistral:7b
│     └── llama3.1:8b
│
├── CLI tools
│     ├── ollama run
│     └── groq (optional)
│
└── Cursor IDE
      ├── Local LLM (Ollama)
      └── Cloud LLM (optional)
```

</details>

<details>
<summary><strong>✔ Hardware Requirements</strong></summary>

| RAM | Recommended Models |
|------|------|
| 16 GB | Small models (7B) |
| 32 GB | Medium models (13B) |
| 64 GB+ | Large models (33B / 70B quantized) |

</details>

<details>
<summary><strong>🏆 Model Ranking (Reasoning + Coding)</strong></summary>

1. **Qwen3 (latest)** — Best balance of speed and intelligence
2. **GPT‑OSS 20B** — Strongest reasoning, but heavier
3. **Llama 3.1 (8B)** — Excellent general-purpose model
4. **DeepSeek‑R1 (7B)** — Strong for logic and math
5. **Qwen2.5 (7B)** — Good but older generation
6. **Mistral 7B** — Fastest, but weaker reasoning

</details>


<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>


## **Author**

<div align="center">
  <img src="https://avatars.githubusercontent.com/u/2900952?s=400&u=41c504ca200e2f92638fc630e8361da78296b35c&v=4" width="180" alt="Amr Ahmed Elghadban"/>

  **Amr Ahmed Elghadban (AmrAngry)**

[![Email](https://img.shields.io/badge/Email-Contact%20Me-red?logo=gmail)](mailto:amr.elghadban@gmail.com) [![WhatsApp](https://img.shields.io/badge/GitHub-Profile-blue?logo=whatsapp)](https://api.whatsapp.com/send/?phone=00971543233227&text=Hi%20&app_absent=0) [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/amrelghadban/)

[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue?logo=github)](https://github.com/amrangry) [![StackOverflow](https://img.shields.io/badge/StackOverflow-Profile-orange?logo=stackoverflow)](https://stackoverflow.com/users/1316779/amrangry)

[![Twitter (formerly Twitter)](https://img.shields.io/badge/Twitter-Profile-blue?logo=twitter)](https://x.com/intent/follow?screen_name=amr_elghadban) [![Facebook](https://img.shields.io/badge/Facebook-Profile-blue?logo=facebook)](https://facebook.com/amr.elghadban) [![Website](https://img.shields.io/badge/Website-Visit%20Me-blue?logo=globe)](https://amrangry.github.io/)
       <div align="center" >
	       <a href = "https://www.buymeacoffee.com/amrangry">
		    <img src = "https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=&slug=your-username&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"/>
                </a>
       </div>
  <!--  [![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support%20Me-yellow?logo=buymeacoffee)](https://www.buymeacoffee.com/amrangry) -->
  <!--  [Email](mailto:amr.elghadban@gmail.com?subject=I%20checked%20your%20GitHub%20repo!): [amr.elghadban@gmail.com](mailto:amr.elghadban@gmail.com) -->
  <!-- [![Linkedin](https://img.shields.io/badge/Lets%20Connect%20via-LinkedIn-blue)](https://www.linkedin.com/in/amrelghadban/) -->
  <!-- [![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/amr_elghadban)](https://x.com/intent/follow?screen_name=amr_elghadban) -->
  
</div>

## **Contributing 🤘**

All your feedback and help to improve this project is very welcome. 
Please create issues for your bugs, ideas & enhancement requests, or better yet, contribute directly by creating a PR. 😎

When reporting an issue, please add a detailed instruction, and if possible a code snippet or test that can be used as a reproducer of your problem. 💥

When creating a pull request, please adhere to the current coding style where possible, and create tests with your code so it keeps providing an awesome test coverage level 💪


## **Code of Conduct**

I’m here to share my knowledge and findings as I work every day to improve our apps/demos for the community.

This is a space where we work together, openly and safely, as kind and considerate human beings.

We grow by giving and receiving positive, constructive feedback.
 
Let’s keep learning and building, one step at a time.


## **License**

<details>
<summary>MIT License.</summary>
Distributed under MIT License.
Copyright 2025 Amr Elghadban
</details>
