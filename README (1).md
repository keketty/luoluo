# Startdocument for Store

Startdocument of **Husarescu Rares Matei**. Student number **4868730**.

## Problem Description

Netflix wants a new simple application that allows the user to watch series. A user, that we will call customer, has: 
* Rating for episodes
* Time remaining to complete the episode 
* Time remaining to complete the season 
* Time remaining to complete the series

The customer can see the number of each series and the total time needed to see it. He can also have a look of the remaining time to complete the series, like a timer.

Each series has a number of seasons like the series has an overview of the total remaining time to complete the season.
 
The customer can see the most ranked episodes and the less ranked episodes. Like the previous has the overview of the remaining time and he can also rate the episode from *1* to *10*.

Design and program an application based on the text above.

### Input & Output

In this section the in- and output of the application will be described.

#### Input

In the table below all the input (that the user has to input in order to make the application work) are described.

|Case|Type|Conditions|
|----|----|----------|
|Series directory|`boolean`|0 <- `watch` -> 1|
|Season directory|`boolean`|0 <- `watch` -> 1|
|Episode|`boolean`|0 <- `watch` -> 1|
|Rate the episode|`int` |1 > number <= 10|

#### Output

|Case|Type|
|----|----|
|List series|`ArrayList<series>`|
|Time progress series|`time`|
|List seasons|`ArrayList<seasons>`|
|Time progress season|`time`|
|List episodes|`ArrayList<episodes>`|
|Time progress episodes|`time`|
|Less ranked episodes|`double`|
|Most ranked episodes|`double`|


#### Calculations

| Case              | Calculation                        |
| ----------------- | ---------------------------------- |
| The ranking system| An operation to calculate the most and the less ranked episode |
| Remaining series time system| Show the remaining time to complete the series|
| Remaining season time system| Show the remaining time to complete the season|
| Remaining episode time system| Show the remaining time to complete the episode|

## Class Diagram

![Class Diagram](images/classdiagram.png )

## Testplan

In this section the testcases will be described to test the application.

### Test Data

In the following table you'll find all the data that is needed for testing.

#### USER

| ID            | Input                             | Code                              |
| ------------- | --------------------------------- | --------------------------------- |
| `rating` | number: 1   | `makeRating("1")` |


#### Series

| ID        | Input                                                        | Code                                               |
| --------- | ------------------------------------------------------------ | -------------------------------------------------- |
| `seriesDuration`     | time: 10:00:00 | `seriesDuration("10:00:00")`                  |
| `completeSeriesTime`     | time: 09:00:00 | `completeSeriesTime("09:00:00")`                  |



#### Season

| ID           | Input | Code          |
| ------------ | ----- | ------------- |
| `seasonDuration`     | time: 05:00:00 | `seasonDuration("10:00:00")`                  |
| `completeSeriesTime`     | time: 00:30:00 | `completeSeasonTime("09:00:00")`                  |

#### Episodes

| ID           | Input               | Code                 |
| ------------ | ------------------- | -------------------- |
| `episodeDuration`     | time: 01:00:00 | `episodeDuration("01:00:00")`                  |
| `completeEpisodeTime`     | time: 00:45:00 | `completeEpisodeTime("09:00:00")`                  |

### Test Cases

In this section the testcases will be described. Every test case should be executed with the test data as starting point.

#### #1 Customer select a series

The customer choose a series

|Step|Input|Action|Expected output|
|----|-----|------|---------------|
|1| `1` | `nbOfSeries()` |10|

#### #2 Customer select a season

The customer choose a season

|Step|Input|Action|Expected output|
|----|-----|------|---------------|
|1| `1` | `nbOfSeasons()` |15|


#### #3 Customer select a episode

The customer choose an episode

|Step|Input|Action|Expected output|
|----|-----|------|---------------|
|1| `1` | `nbOfEpisodes()` |30|


#### #4 Get time remaining series

There will be displayed the remaining time

| Step | Input        | Action       | Expected output |
| ---- | ------------ | ------------ | --------------- |
| 1    | `seriesDuration` | `seriesDuration()` | 10:00:00            |

#### #5 Get time remaining seasons

There will be displayed the remaining time

| Step | Input        | Action       | Expected output |
| ---- | ------------ | ------------ | --------------- |
| 1    | `seasonDuration` | `seasonDuration()` | 05:00:00            |

#### #6 Get time remaining episodes

There will be displayed the remaining time

| Step | Input        | Action       | Expected output |
| ---- | ------------ | ------------ | --------------- |
| 1    | `episodesDuration` | `episodeDuration()` | 00:45:00            |
