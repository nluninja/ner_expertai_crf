# Named Entity Recognition with CRF and expert.ai Edge NL API

> **IMPORTANT NOTICE**: This project was developed using the expert.ai Edge NL API, which was **retired in 2023**. The code is preserved for educational and archival purposes but will not function without access to the legacy Edge NL API runtime.
>
> **Note**: All the NL API features have been included in the **NL Flow** product. See the documentation at [https://docs.expert.ai](https://docs.expert.ai).
>
> For information about current expert.ai NLP solutions, please contact **info@expert.ai** or visit [expert.ai](https://www.expert.ai).

---

## Overview

This notebook demonstrates how to improve Named Entity Recognition (NER) performance using a **Conditional Random Field (CRF)** model enhanced with linguistic features from the **expert.ai Edge NL API**.

The approach leverages expert.ai's deep linguistic analysis to extract rich features including:
- Part-of-speech tags
- Dependency parsing labels
- Semantic concepts (syncons) from the expert.ai knowledge graph
- Knowledge labels and type classes

These features significantly improve NER accuracy compared to traditional word-based features alone.

## Results

The model achieves the following F1 scores on the **CoNLL 2003** test set:

| Entity Type | Precision | Recall | F1-Score |
|-------------|-----------|--------|----------|
| LOC (Location) | 0.886 | 0.900 | 0.893 |
| PER (Person) | 0.891 | 0.873 | 0.882 |
| ORG (Organization) | 0.825 | 0.779 | 0.801 |
| MISC (Miscellaneous) | 0.775 | 0.721 | 0.747 |
| **Overall (micro avg)** | **0.857** | **0.834** | **0.845** |

## Installation (Historical Reference)

The following instructions are preserved for reference but will not work without the deprecated Edge NL API.

### Prerequisites

Create and activate the conda environment:

```bash
conda env create -f environment.yml
conda activate ner-expertai-crf
```

### Dependencies

- Python 3.7
- sklearn-crfsuite
- expertai-nlapi (Edge API - deprecated)
- seqeval
- tqdm
- pandas
- jupyter

### Running the Edge NL API (No Longer Available)

The Edge NL API required local deployment via expert.ai Studio:

1. Create your project in **expert.ai Studio**
2. Deploy the edge instance via _Studio -> Deploy_
3. Run the appropriate startup script:
   - Windows: `runmeWindows.bat`
   - Linux: `runmeLinux.sh`

## Project Structure

```
.
├── edgeapi_crf.ipynb    # Main notebook with CRF + expert.ai implementation
├── environment.yml      # Conda environment specification
├── README.md            # This file
├── EOL_NOTICE.md        # End-of-life notice for Edge API
├── ADDENDUM.md          # Additional technical reference
└── LICENSE              # License file
```

## Technical Approach

1. **Data**: CoNLL 2003 corpus with BIO-tagged named entities
2. **Feature Engineering**: Extract linguistic features via expert.ai NLP analysis
3. **Model**: Conditional Random Field with L-BFGS optimization
4. **Evaluation**: Entity-level precision, recall, and F1 using seqeval

## References

- [CoNLL 2003 Shared Task](https://www.clips.uantwerpen.be/conll2003/ner/)
- [sklearn-crfsuite Documentation](https://sklearn-crfsuite.readthedocs.io/)
- [expert.ai Technical Blog](https://content.expert.ai/blog/a-technical-breakdown-of-expertai-studio-and-edge-nl-api/)

## Contact

For questions about expert.ai's current NLP solutions, please contact:
- **Email**: info@expert.ai
- **Website**: [https://www.expert.ai](https://www.expert.ai)

## License

See [LICENSE](LICENSE) for details.
