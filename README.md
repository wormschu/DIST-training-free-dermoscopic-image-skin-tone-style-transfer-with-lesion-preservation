# DIST-training-free-dermoscopic-image-skin-tone-style-transfer-with-lesion-preservation
This repository provides the official implementation of **DIST**, a training-free diffusion-based framework designed for **skin-tone style transfer in dermoscopic imaging**.  
DIST achieves **realistic tone adaptation** while **strictly preserving diagnostic lesion structure**.

🚧 **This work is currently under submission.  
The full codebase and pretrained configurations will be released upon paper acceptance.**

Stay tuned for updates!

## Usage

### 1. Prepare the data

Prepare content and style images in separate directories.

```text
path/to/data/
├── cnt/
│   ├── content_1.jpg
│   ├── content_2.jpg
│   └── ...
└── sty/
    ├── style_1.jpg
    ├── style_2.jpg
    └── ...

cnt/: Content images
Images whose structural information should be preserved.

sty/: Style images
Images providing style information such as color and texture.

python run_dist.py --cnt data/cnt --sty data/sty --gamma 1.2

Arguments

--cnt: Path to the content image directory

--sty: Path to the style image directory

--gamma: Content Query Amplification factor
Controls the strength of content preservation in query space.

gamma > 1.0: stronger content preservation

gamma < 1.0: stronger style influence

Default: 1.0
