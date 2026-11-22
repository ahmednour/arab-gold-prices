# Monthly gold price per gram in eight Arab countries since 1960

**سعر جرام الذهب الشهري في ثماني دول عربية منذ 1960**

Monthly average price of one gram of gold (24, 22, 21 and 18 karat) in **Saudi Arabia, Egypt, the United Arab Emirates, Kuwait, Qatar, Bahrain, Oman and Jordan**, in each country's own currency, from January 1960 (1966 for the UAE, Qatar and Bahrain) to October 2026.

- File: [`arab-gold-prices-monthly.csv`](arab-gold-prices-monthly.csv) (6,190 rows, UTF-8)
- Page, updates and Arabic documentation: https://www.zahabtoday.com/data
- Licence: our compilation and the computed prices are [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); the `usd_rate` column is IMF data and stays under the [IMF terms](https://www.imf.org/en/about/copyright-and-terms) (see below)

## Columns

| column | meaning |
|---|---|
| `month` | `YYYY-MM` |
| `country_code` | ISO 3166 alpha-2: SA, EG, AE, KW, QA, BH, OM, JO |
| `country` | English name |
| `currency` | ISO 4217 |
| `gold_usd_per_oz` | monthly average gold price, US$ per troy ounce (World Bank) |
| `usd_rate` | monthly average exchange rate, local currency per US$ (IMF) |
| `price_24k_per_gram` … `price_18k_per_gram` | price of one gram, local currency |
| `note` | `egp_official_rate_parallel_market` for Egypt, March 2023 – February 2024; otherwise empty |

## Method

```
price_24k_per_gram = gold_usd_per_oz / 31.1035 * usd_rate
price_Nk_per_gram  = price_24k_per_gram * N / 24
```

Raw metal value: no making charge, VAT or shop margin. Exchange rates are official rates. From March 2023 to February 2024 Egypt had a parallel dollar market well above the official rate, and shops priced gold off it, so actual shop prices in those months were higher than these figures (the rows are flagged in `note`).

## Sources

- Gold: World Bank, *Commodity Price Data (The Pink Sheet)*, monthly average of daily prices. https://www.worldbank.org/en/research/commodity-markets (CC BY 4.0)
- Exchange rates: International Monetary Fund, *Exchange Rates (ER)*, period average, monthly. https://data.imf.org/en/datasets/IMF.STA:ER

## Licence

- **Our work** (the compilation of this file and the per-gram prices computed from the sources): CC BY 4.0. The prices are derived, not copied: they are computed from the two sources with the formula above.
- **`usd_rate` column**: data of the International Monetary Fund, reproduced as published. It, and figures computed from it, remain subject to the [IMF's terms for data](https://www.imf.org/en/about/copyright-and-terms): credit the IMF as *Source: International Monetary Fund, Exchange Rates (ER), https://data.imf.org/en/datasets/IMF.STA:ER*; do not alter the data in a way that affects its accuracy; commercial reuse of IMF data needs the IMF's permission (copyright@imf.org).
- **Gold price**: World Bank Commodity Price Data, CC BY 4.0.
- Neither the World Bank nor the IMF endorses this dataset or zahabtoday.com.

## How to cite

> Zahab Today (zahabtoday.com), "Monthly gold price per gram in eight Arab countries since 1960", computed from World Bank Pink Sheet and IMF exchange-rate data. https://www.zahabtoday.com/data — Source: International Monetary Fund, Exchange Rates (ER), https://data.imf.org/en/datasets/IMF.STA:ER

> ذهب اليوم (zahabtoday.com)، «سعر جرام الذهب الشهري في الدول العربية منذ 1960»، محسوب من بيانات البنك الدولي وصندوق النقد الدولي. https://www.zahabtoday.com/data — Source: International Monetary Fund, Exchange Rates (ER), https://data.imf.org/en/datasets/IMF.STA:ER

For today's prices see https://www.zahabtoday.com (live, every 5 minutes) or the free JSON API at https://www.zahabtoday.com/api-docs.

The figures are indicative, not official prices of any shop or exchange.
