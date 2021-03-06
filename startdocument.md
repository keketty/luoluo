# Start Document for PostNL

Start Document of *Ruike Yuan. Student number: **5000521*.


##Problem Description

Nowadays everybody shops online. PostNL is THE company to get the packages to the customers. PostNL wants healthy postmen so they want an application to measure the max amount of packages the postman can carry(per day). Every postman may carry a maximum weight of packages. Each postman can carry a different weight. But with a maximum of 5 times the weight, they can carry per day.
The Depot should know if they need to hire extra postmen so they can deliver all of the packages. The Depot tracks the number of packages delivered per postman per day and shows the name of the postman and the number of packages that he has delivered.

Notice




  + Everyday the depot sets a new package amount.
  + The capacity of postman is depentent on the amounts of packages he/she can carry per day, whether there is a need to hire extra postman is based on the amount of packages that all the postman in the depot can carry per day.

## classes
| Postmen               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| postManId             | `integer`| 0 <= `number` |
| postManName           | `String` | Not Empty     |
| maxAmountPackage      | `integer`| 0 <= `number` |
| maxWeightOfPack       | `integer`| 0 <= `number` |
| maxWeightOfPackPerDay | `integer`| 0 <= `number` |
| PackagesDelivered| `ArrayList<DPackage>`| Not Empty |

| Package               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| packageNumber           | `integer`| 0 <= `number` |
| packageWeight         | `integer` | 0 <= `number` |

| Depot                 | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| depotId               |`integer`| 0 <= `number` |
| packagesAmount        |`ArrayList<TPackage>`| Not Empty |
| needMoreMen |`boolean`| true/false |

## Inputs, Outputs & Calculations 

### Inputs: 

| Postmen               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| postManName           | `String` | Not Empty     |
| maxAmountPackage      | `integer`| 0 <= `number` |
| maxWeightOfPack       | `integer`| 0 <= `number` |


| Package               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| packageNumber          | `integer`| 0 <= `number` |
| packageWeight         | `integer`| 0 <= `number` |

| Depot                 | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| depotName            |`String`| Not Empty |


### Outputs: 

| Case                  | Type               |
| ----------------------| ------------------ |
| name of the postman   |`String`|
| number of packages delivered in total per man| `integer` |
| needMoreMen |`boolean`|



### Calculations

| Case           | Calculation                                                          |
| -------------- | -------------------------------------------------------------------- |
| number of packages delivered in total per man  | 0 <= `number`|
| maxWeightOfPackPerDayPerPerson |`integer`| 0 <= `number` |
| packagesTotalAmount   | 0 <= `number`|

## Class Diagram

![ClassDiagram](https://github.com/keketty/luoluo/blob/main/Class%20Diagram%20PostNL.png?raw=true)

## Test Plan 

### Test Data

#### Depot

| ID        | Input                                                        | Code                                               |
| --------- | ------------------------------------------------------------ | -------------------------------------------------- |
| `timeSquare`| name: timeSquare | `new Depot("timeSquare")`      |
| `summerPalace` | name: summerPalace| `new Depot("summerPalace")` |


####  Postmen

| ID            | Input                                                                             | Code                                       |
| ------------- | --------------------------------------------------------------------------------- | ------------------------------------------ |
| `Rick`        | postManName: `Rick` <br/> maxAmountPackage : `20`| `new  Postmen("Rick", "20")` |

####  Package  

| ID            | Input                                                                             | Code                                       |
| ------------- | --------------------------------------------------------------------------------- | ------------------------------------------ |
| `packageOne`       | PackageName: `packageOne` <br/> PackageWeight : `300` | `new  Package("packageOne", "300")` |

### Test Cases

#1 get number of packages.

| Step | Input | Code                     | Expected Output           |
| ---- |-------| ------------------------ | ------------------------- |
| `1`  | `timeSquare`|`getDailyPackageAmount()` | `PackageAmount`     |

#1 getPackageDeliveredToday.

| Step | Input | Code                     | Expected Output           |
| ---- | ------|------------------------ | ------------------------- |
| `1`  | `Rick`| `getNumOfPackageDeliveredToday()` | `NumOfPackageDelivered` |

#2 addPackagesDelivered.

| Step | Input       | Code                 | Expected Output           |
| ---- | ----------- | -------------------- | ------------------------- |
| `1`  | `packageOne`| `addPackagesDelivered("packageOne")`|`NoOutput`|

#3 getNeedMoreMen.

| Step | Input       | Code                 | Expected Output           |
| ---- | ----------- | -------------------- | ------------------------- |
| `2` | `depotOne`  | `getNeedMoreMen()` | `true/false`  |

#4 getPostManName.

| Step | Input       | Expected Output           |
| ---- | ----------- | ------------------------- |
| `2` | `Rick` | `PostManName` |



