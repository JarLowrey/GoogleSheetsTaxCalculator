# GoogleSheetsTaxCalculator
Determine your federal and state income tax amount on your Google Sheets projects.

##To Setup

1. Tools > Script editor
2. Paste in code from Taxes Calculator.js code
3. File > New > Script File
4. Name Script File "State Names". This script was copied from [here]( https://github.com/davegaeddert/google-sheets-us-states/blob/master/Code.gs)
5. Paste in code from State Names.js
6. You're good to go!

##To Use

There are 3 basic functions: `TaxAmount(income, state)`, `TaxRateFromBrackets(income, taxInfo)`, and location specific functions. 

`TaxAmount(income, state)` is a convenience function, where you can plug in your state and the proper location specific functions will be called. 

`TaxRateFromBrackets(income, taxInfo)` calculates how much your taxes will be. It actually does the calulations and work.

Location specific functions exist for Federal [ex: `FederalTaxAmt(income)`] and state [ex: `WisconsinTaxAmt(income)`] income taxes. Inside these functions are the tax bracket definitions and a call to `TaxRateFromBrackets` to figure out how much the final tax cost will be.

Supported States:

- Alaska
- Arizona
- California
- Florida
- Nevada
- Ohio
- South Dakota
- Texas
- Washington
- Wisconsin
- Wyoming


[For More info on custom functions in Google Sheets](https://developers.google.com/apps-script/guides/sheets/functions)
