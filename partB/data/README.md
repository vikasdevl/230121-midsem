# Dataset Information

## Dataset Used: Olivetti Faces (AT&T Dataset)

- **Source:** `sklearn.datasets.fetch_olivetti_faces`
- **Acquisition:** Loaded directly via scikit-learn (no manual download needed)
- **Samples:** 400 grayscale images, 40 subjects × 10 images each
- **Features:** 4096 (64×64 pixels, flattened)
- **Pairs generated:** ~10,000+ positive and negative pairs

## Why This Dataset?

The original Brunner et al. (2012) paper uses Labeled Faces in the Wild (LFW), which has millions of image pairs and requires GPU-scale training.
The Olivetti Faces dataset is chosen here as a smaller, publicly available substitute that:
- Supports the same pairwise verification task (same-person vs different-person)
- Has sufficient diversity across identities for meaningful pair construction
- Runs comfortably on a standard laptop CPU
- Is well-understood and widely used in academic ML benchmarks

## Preprocessing

- Images are loaded as float arrays (values between 0 and 1)
- Pairs are constructed by randomly sampling same-identity and different-identity image pairs
- Features are passed as-is (raw pixel intensity vectors) to match the paper's approach of using feature representations directly

## Limitations vs. Original Paper

| Property | This Work | Brunner et al. |
|---|---|---|
| Dataset | Olivetti (400 images) | LFW (13,000+ images) |
| Features | Raw pixels | SIFT, LBP, TPLBP |
| Pairs | ~10k | 2 million |
| Hardware | CPU laptop | HPC cluster |
| Kernel | Linear / RBF | Custom pairwise kernels |
