# Generate text emojis from a description

Flask page that asks Azure OpenAI (`gpt-4`, API version `2024-02-01`) for short text emojis. It keeps up to 10 results that are under 175 characters. This does not draw image emojis.

## Run the page

Create `config.py` next to `app.py` (it is not in the repo):

```python
OPENAI_API_KEY = "your-azure-key"
ENDPOINT = "https://your-resource.openai.azure.com/"
```

```bash
pip install flask flask-cors openai
python app.py
```

Open the Flask URL (debug mode, port 5000) and submit a description. An empty description returns `Description is required`.

## License

[MIT](LICENSE)
