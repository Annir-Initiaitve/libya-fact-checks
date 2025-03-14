# Fact-Checks on Libya (2020 - September 2024)

## Overview

This dataset contains annotated fact-checks on Libya from seven fact-checking platforms, including five local and two regional platforms. The fact-checks cover misinformation content relevant to Libya that has been fact-checked by the platforms from 2020 until late September 2024.

## Sources and Fact-Check Count

The dataset aggregates fact-checks from the following platforms:

| Platform                              | Fact-Check Count |
| ------------------------------------- | ---------------- |
| [Falso](https://falso.ly/) | 434               |
| [Annir](https://annir.ly/) | 298               |
| [Fatabyyano](https://fatabyyano.net/) | 87               |
| [Misbar](https://misbar.com/) | 384               |
| [Nawerny](https://nawerny.ly/) | 418               |
| [She Checks](https://she-checks.org/) | 143               |
| [TSC](https://tsc.ly/) | 278               |

## Dataset Structure

The dataset consists of structured fact-check information with the following columns. Most columns are common across all platforms; however, some columns may be unique to specific platforms due to the nature of their content.

- **blog\_links**: URLs to original fact-check articles.
- **title**: Title of the fact-check.
- **date**: Date of publication.
- **label**: Classification of the claim as assigned by the platform (e.g., false, misleading, true, unverified).
- **text\_content**: Contains the body of the article.
- **brief**: Short summary of the fact-checking article.
- **claim**: The statement or claim being evaluated as part of the fact-checking article.
- **fact\_check**: The part of the article where the platform’s evaluation and reasoning for the fact-check are provided.
- **fact\_check\_references**: URLs to sources mentioned in the fact-check section of the article.
- **claim\_references**: URLs to sources mentioned in the claim section of the article.
- **tags**: Keywords related to the fact-check topic, as labeled by Arabi Facts Hub.

### Entities Extracted from Text:

- **claim\_name\_entity**: Names mentioned in the claim section.
- **claim\_organisation\_entity**: Organizations mentioned in the claim.
- **claim\_location\_entity**: Geographic locations in the claim.
- **claim\_misc\_entity**: Other significant entities in the claim.
- **fact\_check\_name\_entity**: Names mentioned in the fact-check section.
- **fact\_check\_organisation\_entity**: Organizations referenced in the fact-check.
- **fact\_check\_location\_entity**: Locations referenced in the fact-check.
- **fact\_check\_misc\_entity**: Other significant entities in the fact-check.
- **all\_text\_name\_entity**: Names found across all text fields.
- **all\_text\_organisation\_entity**: Organizations found across all text fields.
- **all\_text\_location\_entity**: Locations found across all text fields.
- **all\_text\_misc\_entity**: Miscellaneous entities found across all text fields.

## Methodology

Web scraping was conducted using Selenium, BeautifulSoup, and the Requests library for all platforms, except for Nawerny, whose data was provided by [Arabi Facts Hub](https://arabifactshub.com/) through researcher access.

Entities were extracted from the content using the [CAMeL-Lab Arabic Named Entity Recognition Model](https://huggingface.co/CAMeL-Lab/bert-base-arabic-camelbert-msa-ner).

## Applications and Usage

This dataset is useful for researchers, journalists, fact-checking initiatives, and policymakers interested in:

- Analyzing misinformation trends in Libya, including relevant topics, key entities, and gaps in coverage.
- Examining sources used to refute claims and identifying entities frequently targeted by misinformation.
- Analyzing methods of evidence evaluation and types of sources cited.
- Developing tools to support automated fact-checking pipelines.

## Attribution and Ethical Considerations

- **Ownership and Attribution**: All fact-checks in this dataset remain attributed to their original authors and platforms. Users are encouraged to cite the respective sources when utilizing this data.
- **No Content Text**: To encourage dataset users to visit the fact-checking platforms, we have opted **not to include the full text of fact-checks** except for our content at Annir.
- **Data Editing and Deletion Requests**: Fact-check authors or platforms may reach out to request modifications or removal of their data.

## License

This dataset is licensed under **CC BY-NC-SA** (Creative Commons Attribution-NonCommercial-ShareAlike). This license allows reusers to distribute, remix, adapt, and build upon the material in any medium or format for noncommercial purposes only, provided that attribution is given to the original creator. If you remix, adapt, or build upon the material, you must license the modified material under the same terms.

- **BY**: Credit must be given to the creator.
- **NC**: Only noncommercial uses of the work are permitted.
- **SA**: Adaptations must be shared under the same terms.

## Contact

**Credits:** Individuals who contributed to this work are [Eiad Oumer](eiadoumer14@gmail.com) and [Jehad Oumer](j.oumer@annir.ly).

For questions, requests, or collaboration opportunities with Annir, please contact us at [salam@annir.ly](mailto\:salam@annir.ly).

---

**Note:** The dataset will be periodically updated to reflect new fact-checks and adjustments requested by contributing platforms.

