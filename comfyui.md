# Optimized Code for ComfyUI AI Stable Diffusion

## Requirements
- Python 3.8+
- Required Libraries: `torch`, `transformers`, `PIL`, `numpy`

## Installation
```bash
pip install torch transformers Pillow numpy
```

## Code Implementation
```python
import torch
from transformers import StableDiffusionPipeline
from PIL import Image

# Load the model
model_id = "CompVis/stable-diffusion-v1-4"
pipeline = StableDiffusionPipeline.from_pretrained(model_id, torch_dtype=torch.float16)
pipeline = pipeline.to("cuda")  # Use GPU if available

# Function to generate images
def generate_image(prompt, num_images=1, guidance_scale=7.5):
    images = pipeline(prompt, num_images=num_images, guidance_scale=guidance_scale).images
    return images

# Example usage
if __name__ == '__main__':
    prompt = "A fantasy landscape with mountains and rivers"
    images = generate_image(prompt)
    for i, img in enumerate(images):
        img.save(f'output_image_{i}.png')  # Save generated images
```

## Explanation
1. **Imports**: The necessary libraries are imported at the beginning for clarity.
2. **Model Loading**: The model is loaded once and moved to GPU for faster processing.
3. **Functionality**: A function `generate_image` is created to encapsulate the image generation logic, making it reusable.
4. **Example Usage**: The example usage is placed under a `__main__` guard to prevent execution when imported as a module.
5. **Image Saving**: Generated images are saved with a clear naming convention.
