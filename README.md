# VALIS Environment using `uv` and `conda`/`mamba`

<https://valis.readthedocs.io/en/latest/installation.html>

## Conda Environment

> Note: We use conda/mamba for two types of dependencies:
>
> 1. **pyvips**: Requires libvips which is not a Python package but a system library. Using conda helps install this in a controlled environment when you don't have root access or to avoid conflicts with other packages.
> 2. **tesseract**: Required as a dependency for Python OCR functionality, but tesseract itself is not a Python package.
>
> If your base environment already has usable libvips installed, or if you don't need OCR functionality with tesseract, you can skip creating this conda environment.

```bash
mamba create -n uv_valis pyvips tesseract 
```

## Python Environment

```bash
uv add valis-wsi==1.1.0
uv add imagecodecs zarr pytesseract pydantic ipykernel
uv add numpy==1.26.4 
uv add geopandas rasterio
```
