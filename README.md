# TokenStudio: LLM Token Counter

TokenStudio is a lightweight, privacy-focused web application designed to accurately count tokens in prompts for Large Language Models (LLMs). Built with pure browser-side JavaScript and leveraging the `js-tiktoken` library, this tool ensures no data ever leaves your device, making it a secure choice for sensitive prompts.

## Features

- **Live Tokenization**: Token counts update in real time as you type or paste your prompt.
- **Multi-Model Support**: Supports tokenization for a variety of popular GPT-based models, including `gpt-4o`, `gpt-3.5-turbo`, and legacy models.
- **Encoding Details**: View token counts across multiple encodings (e.g., `cl100k_base`, `gpt2`, `r50k_base`).
- **Token Visualization**: Inspect how your input is tokenized for your selected model, with up to 512 tokens visualized.
- **Privacy First**: No data is uploaded; all processing happens in your browser.
- **Open Source**: Fully transparent and customizable for your needs.

---

## Supported Models and Encodings

TokenStudio supports the following models and their respective encodings:

| Model Name                  | Encoding ID      |
|-----------------------------|------------------|
| OpenAI · gpt-4o            | o200k_base      |
| OpenAI · gpt-4o-mini       | o200k_base      |
| OpenAI · gpt-4             | cl100k_base     |
| OpenAI · gpt-3.5-turbo     | cl100k_base     |
| Generic · GPT-2 / NeoX     | gpt2            |
| OpenAI · text-davinci-003  | p50k_base       |
| OpenAI · GPT-3 (legacy)    | r50k_base       |

---

## Installation and Usage

### Running Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/chatgptdev/TokenStudio.git
   ```

2. Navigate to the project directory:
   ```bash
   cd TokenStudio
   ```

3. Open the `index.html` file in your browser:
   ```bash
   open index.html
   ```

No build tools or dependencies are required; the app runs entirely in the browser.

### Customizing

To add support for additional models or encodings, modify the `ENCODING_CONFIGS` and `MODEL_PRESETS` arrays in the JavaScript logic section of `index.html`.

---

## How It Works

TokenStudio uses the `js-tiktoken` library, a pure-JavaScript port of OpenAI's `tiktoken` tokenizer. This ensures compatibility with the same tokenization algorithms used by major LLMs like GPT-4 and GPT-3.5-turbo. The tool dynamically tokenizes your input text, calculates token counts, and provides visualizations for up to 512 tokens.

### Tokenization Process

1. **Input**: Paste or type your prompt into the input box.
2. **Tokenization**: The app tokenizes your input based on the selected model's encoding.
3. **Statistics**: View token counts, character counts, word counts, and token visualizations.
4. **Visualization**: Inspect the tokens generated for your input, including their IDs and decoded text.

---

## Contributing

We welcome contributions to improve TokenStudio! Here’s how you can help:

- **Bug Reports**: Report issues or unexpected behavior by opening a GitHub issue.
- **Feature Requests**: Suggest new features or improvements via GitHub issues.
- **Code Contributions**: Fork the repository, make your changes, and submit a pull request.

---

## License

TokenStudio is released under the **MIT License**. Feel free to use, modify, and distribute this tool for personal or commercial purposes.

---

## Credits

- Tokenization powered by [`js-tiktoken`](https://www.npmjs.com/package/js-tiktoken).
- Inspired by tools like OpenAI's tokenizer and other LLM debugging utilities.

---

Thank you for using TokenStudio! Your contributions and feedback help make this tool better for everyone.
