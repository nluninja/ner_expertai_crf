# End-of-Life Notice: expert.ai Edge NL API

## Deprecation Status

The **expert.ai Edge NL API** was officially **retired in 2023**. This means:

- The Edge NL API runtime is no longer available for download
- The `expertai.nlapi.edge` Python module is deprecated
- New installations and deployments are not supported
- Technical support for the Edge API has ended

## Impact on This Project

This repository contains code that was developed using the Edge NL API. As a result:

- The notebook (`edgeapi_crf.ipynb`) **cannot be executed** without access to the legacy Edge API runtime
- The code is preserved for **educational and archival purposes only**
- Results shown in the notebook outputs represent historical execution

## What Was the Edge NL API?

The Edge NL API was a locally-deployable version of expert.ai's Natural Language Processing engine that provided:

- Part-of-speech tagging
- Dependency parsing
- Named entity recognition
- Semantic analysis via syncons (semantic concepts)
- Knowledge graph integration
- Sentiment analysis

It was designed for on-premise deployment where data privacy requirements prevented cloud API usage.

## Current expert.ai Solutions

**All the NL API features have been included in the NL Flow product.** See the documentation at [https://docs.expert.ai](https://docs.expert.ai).

expert.ai continues to offer enterprise NLP solutions. For information about currently available products and APIs, please contact:

- **Email**: info@expert.ai
- **Website**: [https://www.expert.ai](https://www.expert.ai)
- **Developer Portal**: [https://developer.expert.ai](https://developer.expert.ai)

## Technical Reference

For historical reference about the Edge NL API architecture:

- [A Technical Breakdown of expert.ai Studio and Edge NL API](https://content.expert.ai/blog/a-technical-breakdown-of-expertai-studio-and-edge-nl-api/)

## Questions?

If you have questions about migrating from the Edge NL API to current solutions, or about expert.ai's NLP capabilities, please reach out to:

**info@expert.ai**
