
# Release Update – December 7th, 2022

See what's new in AIMvision and what we are gradually roling out.
This is a general maintenance release that contains enhancements, bug fixes and some new features. 

## Bug Fixes

### Merchant Level Analysis CSV download issue
The order in which the attribute columns come out seems to be random with each individual download. 
Fixed:Now the output repesents the correct order.

### Querybuilder CSV download issue
Query builder CSV download prioritizes the attributes over the date when it orders the data.
Fixed: The output now prioritizes the date followed by the attributes based on TSG internal orders.

### Report page error
The Report page in some cases were failing to load and edit properly. The issue happens when in old chart no filter value for Household/Standalone was selected or when an Attrition and Growth metric is selected with household filter value. 
Note: With the new enhancement, The default for Standalone / Household attribute is changed to `household` from `standalone`.

Fixed: The issue is fixed. All chart which were defaulted to `standalone` filter value is now using `all_merchants` filter values.

#### Definition:
    `Standalone` – When this option is selected, the metrics calculated at individual store level and 
                   only the MIDs that are not part of chain are used in calculations.
    `All Merchants` - When this option is selected, the metrics are calculated at individual store level 
                    and both chained MIDs and non-chained MIDs are used in calculations.
    `Household (default option)`  - When household is selected, the metrics are calculated at Household level,
                    i.e. standalone stores are considered as a household with one store and chained stores 
                    within a chain are combined together and considered as one single Household.  

## Enhancement

### Merchant Level Analysis

MLA output will now use household level data instead of individual store (standalone) level data.


<footer><p style='text-align:center'>© The Strawhecker Group. All Rights Reserved.</p></footer>
