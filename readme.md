# Currency Converter
**Laravel wrapper for [fixer.io](https://fixer.io)**

[![Travis](https://img.shields.io/travis/byte5digital/currency-converter.svg?style=flat-square)]()

## Install
`composer require naoray/currency-converter`

*optional*
`php artisan vendor:publish --provider="Naoray\CurrencyConverter\CurrencyConverterServiceProvider"`

## Usage

```
// Converting currencies
Currency::convert(100, 'EUR')->into('USD');

// get currency rates
Currency::getLatestRates();

// get rates for different base (default: EUR)
Currency::setBase('USD')->getLatestRates();

// get specific currency rates
Currency::getLatestRates(['USD', 'GBP']);
Currency::getLatestRates('USD');

// get historical currency rates
Currency::getHistoricalRates('2000-01-03');
Currency::getHistoricalRates(Carbon::yesterday());
Currency::getHistoricalRates('2000-01-03', ['USD', 'GBP']);
```