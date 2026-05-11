# Cat Facts Dataset

A merged and deduplicated dataset of 509 cat facts in JSON format.

## Goal

This dataset is the data source for the [Cat Facts HACS integration](https://github.com/bglnelissen/hacs-cat-facts) for Home Assistant. The integration shows a new cat fact every configurable number of hours.

## Dataset

The file `cat_facts.json` contains 509 unique cat facts in English.

### Structure

```json
{
  "meta": {
    "total": 509,
    "sources": [...]
  },
  "facts": [
    "A cat has 32 muscles in each ear.",
    "..."
  ]
}
```

## Sources

All sources use permissive open source licenses (MIT / Apache-2.0) which allow redistribution and combination.

| Source | License | URL |
|--------|---------|-----|
| alexwohlbruck/cat-facts (catfact.ninja) | Apache-2.0 | https://github.com/alexwohlbruck/cat-facts |
| vadimdemedes/cat-facts | MIT | https://github.com/vadimdemedes/cat-facts |
| wh-iterabb-it/meowfacts | MIT | https://github.com/wh-iterabb-it/meowfacts |

## Fact length

Home Assistant limits sensor state values to 255 characters. To ensure every fact displays correctly without truncation, all 17 facts from the original sources that exceeded this limit have been manually rewritten. The core information of each fact is preserved; only the wording was shortened to fit within the limit.

## License

This dataset is released under the [MIT License](LICENSE).
