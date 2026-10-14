# Modelflare image and video tools

The `modelflare` MCP server generates images and videos with the user's Modelflare Smart API Key.

- Call `list_models` first. It returns the image and video models this key can call, each with a docs page.
- Read the model's docs page before building a request: field names and nesting differ by model family. Put those fields in `parameters` for `generate_image` or in `request` for `create_video`; they are sent unchanged.
- Videos are asynchronous: `create_video`, then `get_video_status`, then `download_video` (it can wait up to 300 seconds).
- Results are saved to the output directory right away because result URLs expire. Tell the user the saved file paths.
- Calls are billed to the user's Modelflare balance. Confirm the model and the main parameters with the user before starting expensive jobs such as long or high-resolution videos.
- If a tool reports that the key cannot call a model, show the message as is; it explains when a Smart API Key helps.
