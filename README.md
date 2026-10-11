# Portfolio Performance compatible JSON for Achmea funds
Quotes for the following funds are updated daily using GitHub actions:

| Fund | Fund code | File |
| --- | --- | --- |
| Achmea opkomende markten aandelen fonds A | `GOA` | `AchmeaOpkomendeMarkten.json` |
| Achmea wereldwijd aandelen fonds A | `GWA` | `AchmeaWereldwijdAandelen.json` |

Quotes for the opkomende markten fund are not generally available in popular sources since it was only recently founded in May 2023.

The script pulls the API behind the rates graph at `https://www.achmeainvestmentmanagement.nl/particulier/beleggingsfondsen/koersen` and converts the rates to JSON files compatible with [Portfolio Performance](https://www.portfolio-performance.info/en/).

## How-to
In Portfolio Performance select JSON as the provider in the “Historical Quotes” tab of the security, and use the following values:

Feed URL = `https://raw.githubusercontent.com/RamonH93/process-json-achmea-funds/master/<file>` (use the file from the table above)\
Path to Date = `$.rates[*].Date`\
Path to Close = `$.rates[*].CloseQuote`
