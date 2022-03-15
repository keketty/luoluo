# Start Document for PostNL

Start Document of *Ruike Yuan. Student number: **5000521*.


##Problem Description

The National Soccer Association track and require a payment of the number of cards (Red card and Yellow card) given to a player of each team in the soccer club.
They also give a Fair play award to the player with the least amount of cards.
FC Emmen wants to register the number of fouls each player has committed and how much they would have to pay the association for the number of cards their players have received. 
The fine for the Yellow and Red cards are as follows: €18,32 per Yellow card and €41,60 per Red card. 

##classes
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
| maxWeightOfPackPerDay | `integer`| 0 <= `number` |

| Package               | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| packageName           | `integer`| 0 <= `number` |
| packageWeight         | `integer`| 0 <= `number` |

| Depot                 | Type     | Conditions    |
| --------------------- | -------- | ------------- |
| depotName            |`String`| Not Empty |


###Outputs: 

| Case                  | Type               |
| ----------------------| ------------------ |
| name of the postman   |`String`|
| packagesAmount        |`ArrayList<Packages>`|
| packagesTotalWeight   | 0 <= `number`|
| maximumCarryWeightOfDepot |`integer`| 0 <= `number` |
| number of packages delivered in total per man| `integer` |


### Calculations

| Case           | Calculation                                                          |
| -------------- | -------------------------------------------------------------------- |
| number of packages delivered in total per man  | Sum of all the packages delivered|
| maximumCarryWeightOfDepot | `integer`| 0 <= `number` |
| packagesTotalWeight    | `integer`| 0 <= `number` |

## Class Diagram

![ClassDiagram](https://user-images.githubusercontent.com/91316558/158166330-6c877fcf-f2a3-4660-898c-84bfd25dc406.png)

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



