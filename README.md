# Market Microstructure Analysis

Code repository for "Price Discovery in High-Frequency Markets" (Journal of Finance, 2024).

## Authors

- David Lee (Quantitative Finance Department)
- Sarah Williams (Trading Systems Lab)

## Abstract

We analyze price discovery mechanisms in high-frequency trading environments using millisecond-level order book data from major exchanges.

## Published Papers

- **Main Paper**: DOI: 10.1111/jofi.2024.12345
- **Working Paper**: arXiv:2201.67890

## Data

- `data/orderbook/` - Limit order book snapshots (10ms frequency)
- `data/trades/` - Trade and quote data
- Total size: ~50GB (available via Zenodo: 10.5281/zenodo.1234567)

## Code Structure

```
src/
  orderbook.py - Order book reconstruction
  metrics.py - Microstructure metrics
  analysis.py - Statistical analysis
notebooks/
  analysis.ipynb - Main analysis notebook
tests/
  test_orderbook.py - Unit tests
```

## Requirements

```
numpy>=1.21.0
pandas>=1.3.0
numba>=0.55.0
pytest>=6.2.0
```

## Docker

For reproducibility, we provide a Docker environment:

```bash
docker build -t market-microstructure .
docker run -v $(pwd)/data:/data market-microstructure python src/analysis.py
```

## Citation

```bibtex
@article{lee2024price,
  title={Price Discovery in High-Frequency Markets},
  author={Lee, David and Williams, Sarah},
  journal={Journal of Finance},
  year={2024},
  doi={10.1111/jofi.2024.12345}
}
```

## References

This work cites and extends:
- Hasbrouck (1991) - Measuring the information content of stock trades
- Biais et al. (1995) - An empirical analysis of the limit order book
