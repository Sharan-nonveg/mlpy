# MLPy

This repository is ready for ML projects and dataset uploads.

## Recommended dataset upload workflow

If your dataset is large, use Git LFS (Git Large File Storage) instead of pushing raw files directly to GitHub.

### 1) Install Git LFS

```bash
git lfs install
```

### 2) Track large file types

```bash
git lfs track "*.csv"
git lfs track "*.parquet"
git lfs track "*.json"
git lfs track "*.zip"
git lfs track "*.gz"
git lfs track "*.npy"
git lfs track "*.pkl"
git lfs track "*.h5"
```

### 3) Add the tracked files

```bash
git add .gitattributes
```

Then add your dataset or project files:

```bash
git add upload/
git commit -m "Add dataset and project files"
git push origin main
```

## Upload folder

Use the `upload/` directory for your dataset files, scripts, or sample data.

## Large files tips

- For files bigger than 100 MB, use Git LFS.
- For very large datasets, consider using GitHub Releases or external storage like Google Drive/Kaggle/AWS S3 and keep a download script in the repo.
- Always keep your GitHub repo lightweight and clean.

## Example project flow

```bash
mkdir -p upload
# copy your dataset files here
# then add them with git add
```

## Notes

This repository starts with a basic structure so you can upload data and code without issues.
