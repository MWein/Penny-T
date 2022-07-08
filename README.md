# Penny-T

## Purpose

Penny Tracker. This project will not be an auto-trading bot like other versions of Penny. This app will allow me to keep track of manually entered option trades and possibly suggest trades in the future. The Penny trading bots previously written frequently entered trades that I would have vetoed, and writing in new rules to account for every possible situation is not viable since the markets just don't behave the same day-to-day. Some of Penny's functionality will be carried over, but the final decision will be made by me.

The connection to Tradier will remain only for data purposes (which is free unlike ORATS and others). This app will be broker-independant considering the time and effort it took to write the code specific to Tradier in the first place. And the fact that I found a broker with much, much looser margin requirements that I will be using going forward. And they approved me for tier 5 (for some reason) while Tradier wanted a whole dissertation on why I should get approved for just tier 3. Sadly, my new broker does not have an API so all trades and inputs must be done manually.

There is specific information that I want to see using this app. In particular, real-time income tax calculations, visualization of how my trades are going, current theta decay rate, etc. This is information that I want displayed all in one place without logging into the broker. The broker provides this information as well, but it's not in one place. And, of course, this is resume candy.

The other upside of this approach is that it no longer needs to be hosted in the cloud. It's not making real trades, only providing information, so my shitty Spectrum internet is of less concern.

I also want to try making a mobile app with React Native so I can see how much money I'm losing on the go. Of course, this would require a cloud-based DB. We'll see where things go.

## MVP

Entering a trade: Once a trade is entered with the broker, information about the option legs will be entered.

UI: The UI will display cards with each active strategy. The cards will show the P/L graph with a dot indicating the current underlying price. It will show the max potential gain and loss, and show the current P/L if the play were closed now. There will be some indication that the trade is in danger or losing, as well as trades that are winning.

Closing a trade: When the trade is closed, the closing price of each leg will be collected. This will then be saved for tax calculation purposes. Maybe a nice graph view. This will be displayed on a dedicated monitor.

When closing a trade, there should be some mechanism where I can tell the app the trade is closed, but not yet enter the closing prices. There would be a todo list or something where I can enter that information at a later date.

## Additional features

Tax calculation. I have a tendancy to spend it as I make it. In my first year of actual success in the stock market, I kinda forgot about the whole tax thing. At first I'll just use my highest tax bracket based on my other incomes. Later, I'd like to be able to input info from my paychecks including taxes withheld so I can see a better estimate of my tax bill from all sources.

Suggestions. This app could sift through the entire stock market each morning and suggest trades to me like the trading bots did.

Full financial management. I may want to use this app to keep track of credit lines and bills so I can finally ditch the spreadsheet. I wrote an app for this before which was really useful... but my god I designed it very poorly looking back. I think I wrote that after just 3 months of web dev experience. Round 2?
