Vehicle Data
=============

Vehicle Table
-------------
PRIMARYKEY vehicle_id: String
PRIMARYKEY fuel_card_num: String
description: String
type: String (short)
year: 2-digit number
num: Integer

Stations Table
--------------
PRIMARYKEY id:  Int/String
display_name: String
long: Something (Number)
lat: Something (Number)

Fuel Type Table
----------------
PRIMARYKEY id: Int/String
display_name: String

Refuel Events Table
---------------------
FOREIGNKEY station_id (Stations Table)
FOREIGNKEY fuel_card_num (Vehicles Table)
fuel_type: Ordinal4/String
fuel_volume: Number (int)
km: Number (long)
time: DateTime (Unix timestamp, ms)

(Batched) Location Data (last known location)
-----------------------------------
** NOTE: Background job for processing and aggregating LcoationData table events into minute, hour, or something, used for mapping and heatmapping in front end (for each vehicle_id) <-- indexable by type, year, num

ONLY SUPPORTED VEHICLES: 511601, 521202, 521304, 521308, 521606, A30805, A30806, A30811, A30901, A30909, A31007, A31008, A31011, A31302, A31402, A31404, A31406, A31601, 520806, 520905, 520906, 520910, 521001, 521002, 521201, 521306, 521309, 521310, 521311, A31201, A31202, A31203, A31204, A31205, A31206, A31401, A31402
**TODO Look into what 'event' is

lat: Number
long: Numbmer
window_start_time: DateTime (unix timestamp, ms)
window_end_time: DateTime (unix timestamp, ms)
FOREIGNKEY vehicle_id



*** NOTE: Would be interesting to look into patterns re: when they refuel w.r.t. fullness
*** NOTE: km is an indicator for maintenance when doing maintenance crunching and warning prediction



Notif. Type Table
----------------
PRIMARYKEY id
display_name: String

Notification Table
-------------------
PRIMARYKEY id:
FOREIGNKEY type_id: Notif. Type Table
Urgency/Why/Description...



Garage Table
-------------
PRIMARYKEY id:
name: String
lon: Num
lat: Num

Garage Events Table
-----------------------
TODO Review later
FOREIGNKEY garage_id
total_km: Number
Item, Note, RType, Num?
{
  "TSUM": 437.6,
  "ITEM": "132872",
  "RTYPE": 1,
  "NUM": 2,
  "SSUMNOVAT": 17.96,
  "BILLD": 1433980800000,
  "IMPCODE": "A30806",
  "SERVD": 1427275560000,
  "SEHIID": 2013,
  "UNITPR": 8.98,
  "NAME": "PIKALIITIN RUNKO C-23071-08"
},
