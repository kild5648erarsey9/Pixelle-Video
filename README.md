# Pixelle-Video

A fork of [AIDC-AI/Ovis](https://github.com/AIDC-AI/Pixelle-Video) focused on video understanding and generation with multimodal large language models.

## Features

- Video understanding with multimodal LLMs
- Frame-level visual tokenization
- Efficient video encoding pipeline
- Support for long-form video inputs

## Installation

### From Source

```bash
git clone https://github.com/your-org/Pixelle-Video.git
cd Pixelle-Video
pip install -e .
```

### With Docker

```bash
docker build -t pixelle-video .
docker run --gpus all -it pixelle-video
```

### Dev Container

Open in VS Code and select **Reopen in Container** when prompted.

## Quick Start

```python
from pixelle_video import PixelleVideoModel

model = PixelleVideoModel.from_pretrained("pixelle-video-7b")

result = model.chat(
    video="path/to/video.mp4",
    query="Describe what is happening in this video."
)
print(result)
```

## Requirements

- Python >= 3.10
- PyTorch >= 2.0
- CUDA >= 11.8 (for GPU support)

See `pyproject.toml` for full dependency list.

## Development

```bash
# Install with dev dependencies
pip install -e ".[dev]"

# Run tests
pytest tests/

# Format code
black pixelle_video/
isort pixelle_video/
```

## Documentation

Full documentation is available at [https://your-org.github.io/Pixelle-Video](https://your-org.github.io/Pixelle-Video).

## License

This project is licensed under the Apache 2.0 License — see [LICENSE](LICENSE) for details.

## Acknowledgements

This project is a fork of [AIDC-AI/Pixelle-Video](https://github.com/AIDC-AI/Pixelle-Video). We thank the original authors for their work.
