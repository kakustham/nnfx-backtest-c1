# nnfx-backtest
Expert Advisor to backtest confirmation indicators in NNFX way

## How to Use:
* Put the NNFX_Backtest.mq4 in MQL4/Experts folder
* Open NNFX_backtest.mq4 in MetaEditor
* Go to getSignal() function
* Uncomment only the indParams and the line of indicator to test. Make sure that if we call getIndicator* function, the first parameter is the name of compiled indicator relative to the root indicators directory (MQL4/Indicators/). If the indicator is located in subdirectory, for example, in MQL4/Indicators/Examples, its name must be specified as "Examples\\\\indicator_name".
![configure indicator](./config_ea.png)
* Save the file
* Compile
* Open MetaTrader4 and open Strategy Tester, select Expert Advisor NNFX_Backtest
* Configure like below image and start. If the indicator is not shown in chart, check if the journal tab is it has errors
![run ea](./run_ea.png)

## Test Other Indicators:
Beyond the examples in getSignal() function, we can test specific indicators, through one of three functions:
* getIndicatorMASignal: return LONG signal when Moving Avarage starts to rise; return SHORT signal when Moving Avarage starts to go down.
* getIndicatorZerocrossSignal: return LONG signal when the indicator cross 0 line to up; return SHORT signal when the indicator cross 0 line to down.
* getIndicatorCrossoverSignal: return LONG or SHORT signal when two lines crosses.