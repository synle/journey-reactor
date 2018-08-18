# journey-reactor
A mobile app written in react native to accommodate traveling with public transit or company private shuttle services


## Setup
```
npm install -g create-react-native-app
create-react-native-app journey-reactor

npm start
```


## Classes
```
Region
  id
  name
  description
  long
  lat
  =========================
  1. Bay Area
  2. NYC


Vendor
  id
  name
  ========
  1. VTA
  2. Caltrain
  3. Bart

Route
  id
  regionid
  vendorid
  name
  description
  =========================
  1. North-Bound
  2. South-Bound

Stops (Route Stops)
  id
  routeid
  name
  time
  long
  lat
  =========================
  1. San Francisco 4th King
  2. San Mateo


Attachments (pictures for the stops / additional docs)
  id
  stopid
  linkid
  order


Attachments Links (Url)
  id
  name
  link


Alerts
  id
  regionid
  message
  link
  time
  long
  lat

Users
  id
  email
  password
  salt
  
UserVendors
  id
  userid
  vendorid

UserPreferences
  id
  userid
  preference

UserRole
  id
  userid
  role
  
RebeverseGeoCoding
  long
  lat
  streetnumber: street_number
  neighborhood: neighborhood
  political: political
  locality: locality  
  administrativeAreaLevel1: administrative_area_level_1
  administrativeAreaLevel2: administrative_area_level_2
  country: country
  postalCode: postal_code
  postalCodeSuffix: postal_code_suffix
```

## Visitor Screens
### New Users
```
1. Sign in
2. Sign up
```

### Set up your route
```
Add Your Route
1. Choose region
2. Choose stop 1
3. Choose stop 2
```


### Check Your Route
#### Tab 1 - Time Table
```
Drop down - pick your route
================================================
Current Location: San Francisco, CA
Distance to Stop 1 (4th & King): 2 Miles (15 mins)
Current Time: 5PM
Next Scheduled Time for Stop 1 (4th & King):
  5:15PM (30 mins to Stop 2 (Sunnyvale))
  6:15PM (45 mins to Stop 2 (Sunnyvale))
  7:15PM (50 mins to Stop 2 (Sunnyvale))

================================================
* Tab_1 (Time Table) | Tab_2 (Map)
```


#### Tab 2 - Map Your Rotue
```
Drop down - pick your route
================================================
Distance to Stop 1 (4th & King): 2 Miles (15 mins)


    * stop 1
      ** current location
        * stop 2

================================================
Tab_1 (Time Table) | * Tab_2 (Map)
```


## Driver / Vehicle Operator
(Optional for live traffic updates) Ping server with drivers' vehicle long and lat

### Trip Progress
ETA, Map

### Current Route Information
Trip progress and potentially alerts

### Add Alert
Communicate with dispatcher regarding the locations

## Admin Screens
Manage Routes
### CRUD Your Routes
### CRUD Route Alert
### Vehicle Status
### Stats
### Settings
