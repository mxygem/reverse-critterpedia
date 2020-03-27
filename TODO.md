# TODO

## Data files

### Source

* [fish](https://www.ign.com/wikis/animal-crossing-new-horizons/Fish_Guide:_Fish_List,_Sell_Price,_and_Fishing_Tips#Killifish)
  * Last fish entered: rainbowfish
  * Need to use [this](https://www.polygon.com/animal-crossing-new-horizons-switch-acnh-guide/2020/3/23/21190775/fish-locations-times-month-day-list-critterpedia) guide to get shadow size added to data, too
* [bugs](https://www.ign.com/wikis/animal-crossing-new-horizons/Bug_Guide:_Bugs_List,_Sell_Price,_and_Bug_Catching_Tips#Bugs_Available_By_Month)
  * Last bug entered: none


### Example Entry

```json
"snapping turtle": {
    "price": 5000,
    "location": "river",
    "time": {
        "start": "2100",
        "end": "0400"
    },
    "months": {
        "northern": [4, 5, 6, 7, 8, 9, 10],
        "southern": [10, 11, 12, 1, 2, 3, 4]
    }
}
```

#### Notes

* Prices are ints with 0 indicating no price
* Times are 24 formatted strings
* 0000 is used in both fields to indicate "all day" creatures
* Months are broken into respective hemispheres
* Months are an array and meant to be displayed in a "wrap" order if month group crosses new year. i.e. [11, 12, 1, 2] instead of [1, 2, 11, 12] (maybe not)

## Commands

* Search - Allow for searching based on various criteria. Allow for multiple criteria to be specified to narrow search more?
  * by
    * creature type
    * name/partial name
    * month/time/etc

* List - list all data?

* Add - add a particular creature to user's local tracking file
* Remove - removes a particular creatue to user's local tracking file

## Formatting

### Ordering

* Alpha - asc/desc
* Price - asc/desc
* Proximity to current system time

### Return data

* All data from source file
* User specific data
  * Is maybe available to user now?
  * Museum donation status
    * include donation date?

### Styles

* Pretty json
* Fancy output
  * Tables?
  * Color border based on possible availability?
    * Green - available
    * Yellow - maybe available (for things like weather or rocks)
    * Red - unavailable
* Include hourly display?
