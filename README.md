# Apostille Atlas: apostille rules by country

Apostille Convention (Hague Convention of 5 October 1961) status for 148 countries, and for 119 countries the checked details: issuing offices, fees, processing times, steps and rules. Every fact carries its primary source (HCCH, the issuing office, a government site or the law) and the date it was checked. Also includes the Apostille Price Index: published fees side by side in euros at ECB reference rates.

- Website: https://apostilleatlas.com
- Open data page: https://apostilleatlas.com/open-data/
- Licence: CC BY 4.0 (data only)
- Last check in this release: 2026-10-23

## Files

- `apostille-atlas.csv`: one row per country.
- `apostille-atlas.json`: full details with sources per country.
- `apostille-price-index-2026-10-23.csv`: Apostille Price Index snapshot of 2026-10-23 (ECB rates of 2026-10-19).

## Fields

| Column | Meaning |
|---|---|
| iso2, iso3, name | ISO 3166 codes and English country name |
| status | contracting_party, signatory_only or not_party, as in the HCCH status table |
| hcch_member | Member of the Hague Conference itself (not the same as using apostilles) |
| signature_date, instrument_type, instrument_date, entry_into_force | How and when the country joined the Convention |
| in_force_today | Convention in force for the country on the build date |
| acceptance_procedure | Joined by accession where other parties may object |
| hcch_authority_url | HCCH page listing the country's issuing offices |
| basics_checked_at | Last comparison with the HCCH status table |
| details_checked, details_checked_at | Whether and when a person checked the details |
| authorities, fees, processing_time, e_apostille, e_register_url | Checked details (fees in the office's own currency) |
| page_url, status_source_url | Country page on apostilleatlas.com and source of the status |

The JSON adds a `sources` list per country; every fact points to one with `source_id`.

## Sources and method

Status and dates come from the HCCH status table of the Apostille Convention. Details come from the issuing office's own website or other primary sources and are published only after a person has checked them. No values are estimated or averaged. Method: https://apostilleatlas.com/methodology/

## Licence and attribution

Creative Commons Attribution 4.0 International (CC BY 4.0). Please credit:

> Source: Apostille Atlas (https://apostilleatlas.com), data checked 2026-10-20, CC BY 4.0.

## Citation

DOI: [10.5281/zenodo.23494658](https://doi.org/10.5281/zenodo.23494658). Copies: [Zenodo](https://zenodo.org/records/23494658), [Hugging Face](https://huggingface.co/datasets/apostilleatlas/apostille-atlas), [apostilleatlas.com/open-data](https://apostilleatlas.com/open-data/).

```bibtex
@misc{apostille_atlas_2026,
  title        = {Apostille Atlas: apostille rules by country},
  author       = {{Apostille Atlas}},
  year         = {2026},
  doi          = {10.5281/zenodo.23494658},
  howpublished = {\url{https://doi.org/10.5281/zenodo.23494658}},
  note         = {Data checked 2026-10-20. CC BY 4.0}
}
```

## Caveats

This is general information, not legal advice. Fees and rules change: check with the issuing office before you apply. Apostille Atlas is independent and not affiliated with the HCCH or any government.

## Updates

The data is rebuilt from the live site and committed here once a week, and sooner when the HCCH status table changes. Each commit message gives the check date. To update by hand, download the files from https://apostilleatlas.com/open-data/ into `data/` and commit.

## Issues

Found an error? Use https://apostilleatlas.com/corrections/ or email apostilleatlas@gmail.com.
