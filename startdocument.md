# Start Document for PostNL

Start Document of *Ruike Yuan. Student number: **5000521*.


##Problem Description

Nowadays everybody shops online. PostNL is THE company to get the packages to the customers. PostNL wants healthy postmen so they want an application to measure the max amount of packages the postman can carry. Every postman may carry a maximum weight of packages. Each postman can carry a different weight. But with a maximum of 5 times the weight, they can carry per day.
The Depot should know if they need to hire extra postmen so they can deliver all of the packages. The Depot tracks the number of packages delivered per postman per day and shows the name of the postman and the number of packages that he has delivered.

## classes
| Postmen               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| postManId             | `integer`| 0 <= `number` |
| postManName           | `String` | Not Empty     |
| maxAmountPackage      | `integer`| 0 <= `number` |
| maxWeightOfPack       | `integer`| 0 <= `number` |
| maxWeightOfPackPerDay | `integer`| 0 <= `number` |

| Package               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| packageName           | `integer`| 0 <= `number` |
| packageWeight         | `integer` | 0 <= `number` |
| packageId             | `integer`| 0 <= `number` |

| Depot                 | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| depotId     | `integer`| 0 <= `number` |
| packagesAmount        |`ArrayList<Package>`| Not Empty |
| packagesTotalWeight   | `integer`| 0 <= `number` |
| maximumCarryWeight    | `integer`| 0 <= `number` |
| needMoreMen | `boolean`| true/false |

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
| needMoreMen | `boolean`|



### Calculations

| Case           | Calculation                                                          |
| -------------- | -------------------------------------------------------------------- |
| number of packages delivered in total per man  | 0 <= `number`|
| maxWeightOfPackPerDayPerPerson |`integer`| 0 <= `number` |
| packagesTotalAmount   | 0 <= `number`|

## Class Diagram

![ClassDiagram](https://)

## Test Plan 

### Test Data

#### Depot

| ID        | Input                                                        | Code                                               |
| --------- | ------------------------------------------------------------ | -------------------------------------------------- |
| `timeSquare`| number: 1<br />name: timeSquare | `new Depot(1, " timeSquare")`      |
| `summerPalace` | number: 2<br />name: summerPalace| `new Depot(2, "summerPalace")` |


####  Postmen

| ID            | Input                                                                             | Code                                       |
| ------------- | --------------------------------------------------------------------------------- | ------------------------------------------ |
| `Rick`        | postManName: `Rick` <br/> maxAmountPackage : `200` <br/> maxWeightOfPack : `200` | `new  Postmen("Rick", "200", "200")` |

####  Package  

| ID            | Input                                                                             | Code                                       |
| ------------- | --------------------------------------------------------------------------------- | ------------------------------------------ |
| `packageOne`       | Package  Name: `packageOne` <br/> PackageWeight : `300` | `new  Package("packageOne", "300")` |

### Test Cases

#1 get number of packages.

| Step | Code                     | Expected Output           |
| ---- | ------------------------ | ------------------------- |
| `1`  | `getNumberOfPackages()`  | `NumofPackages`           |

#2 AddPackagesDelivered.

| Step | Input       | Code                 | Expected Output           |
| ---- | ----------- | -------------------- | ------------------------- |
| `packageOne`  | `packageOne`     | `AddPackagesDelivered("packageOne")` | `NoOutput`  |



