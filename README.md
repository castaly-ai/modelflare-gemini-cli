# Modelflare for Gemini CLI

Image and video generation in Gemini CLI with one Modelflare **Smart API Key** for every image and video model available to your account.

在 Gemini CLI 里用一个 Modelflare **Smart API Key** 调用你账号可用的全部图像和视频模型。

## Get a Smart API Key / 获取 Smart API Key

1. Sign up / 注册: https://modelflare.dev/sign-up?utm_source=gemini-cli&utm_medium=plugin&utm_campaign=integrations
2. Console → API Keys → **Create Smart API Key**, and pick a routing strategy (Balanced / Stability first / Low price first).

   控制台 API Keys →「Create Smart API Key」，选择路由策略（均衡 / 稳定优先 / 低价优先）。

## Install / 安装

```bash
gemini extensions install https://github.com/castaly-ai/modelflare-gemini-cli
```

Gemini CLI asks for your Smart API Key during installation and keeps it in the system keychain. Change it later with `gemini extensions config modelflare`. Node.js is required; the extension starts the [Modelflare MCP server](https://www.npmjs.com/package/@modelflare/mcp-server) with `npx`.

安装时 Gemini CLI 会提示填写 Smart API Key，并保存在系统钥匙串中；之后可用 `gemini extensions config modelflare` 修改。需要本机已安装 Node.js。

| Setting | Value |
|---|---|
| Modelflare Smart API Key | your Smart API Key |
| Modelflare base URL | `global` → https://modelflare.dev/v1 (default) · `china` → https://origin.modelflare.dev/v1 · or a custom URL |

## Use / 使用

Ask Gemini CLI as usual, for example:

- "Generate a 16:9 poster of a coastal observatory at dusk."
- "Turn this start frame into a 5 second video."

The extension lists the models your key can call, reads each model's docs page for its request fields, and saves results to `./modelflare-output`. Calls are billed to your Modelflare balance by actual usage; see https://modelflare.dev/usage-logs.

## Links

Docs: https://docs.modelflare.dev/ · Pricing: https://modelflare.dev/pricing

## License

MIT © Havenbyte LLC
