# Snowplow_AVL_processing

This project aims to use RAMS API to conflate the GPS location from AVL pings to LRS route ID and measure.

## Process

* Use X, Y cooridnates to query the system to get closest measure

* Route ID correction: use before and after locations to valid current location (route type and number only)

* Direction correction: use before and after measures to valid current measure (should always be increasing as time elapsed)

## Next Step

* Maintain last ping for each label, to create connection on next 15 min interval

* Update direction correction method, include threshold for measure increase

* Handle concurrent route
