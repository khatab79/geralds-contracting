# Gerald's Contracting Application

![Gerald_Img]

## Summary

---

**_How to use this Application_**

To run a calcuclation, pass in two parameters:

* The width of one house (preceeded by the `-w` flag)

* The length of one house (preceeded by the `-l` flag)


## Example 

~~Scratch this.~~

```
node dist/index.js -w 8 -l 8
```

---



## Scenario

This application will take the width and length of a house and return the number of studs required to frame the wall inside the 4x4 beams.

* The house should be a rectangular.

* Each corner of the house has a single 4x4 beam that walls can be nailed into and the trusses for the roof come pre-assembled. 

* The only materials that needs to buy are the 2x4’s.

**_given us the following information to help you understand the calculation :_**

1. Each wall has 2x4’s flat against the floor for the length of the edge of a wall.

1. Each wall has vertical 2x4’s spaced 16 inches apart (measured from outside edge of a board to the next outside edge; the board is included in the 16 inches).

1. Each wall has 2x4’s flat against the ceiling for the length of the edge of a wall.

1. Add 10% MORE than a perfect calculation to account for waste.

1. Partial piece of lumber can’t be purchased , so we round up a decimal in the final by using Math.ceil function.

**_Given us the following Studs Stds for the calculation :_**

* 2x4’s are actually 1.5" x 3.5”
* 4x4’s are actually 3.5” x 3.5”
* Only buys 8’ 2x4’s

---

**_Given us the following example of the calculation with the expected output as well, using an 8’ by 8’ house:_**


* Each wall is the same size in this case
* Each wall has two beams, totaling 7”, so the space in between is 7’ 5”.
* Each wall required one 2x4 on the top, bottom, and sides
* The remaining space across, broken into 16” sections, is 5.56, rounded up to 6.
* Total: 10 boards per wall, 40 boards for this house.

---
## Test log 

| House Measurement | Studs Required | Aplication Returns |   Last Test Run by   |
| ----------------- | -------------- | ------------------ | -------------------- |
|       8 x 8       |       40       |                    | Khatab AL DAGHISTANI |
|      18 x 8       |       66       |                    | Khatab AL DAGHISTANI |

---



### Note to Other developers

I used the [yargs package] for the processing of command line paramters. For more information on that package go to the [yargs package] website.

[yargs package]: https://www.npmjs.com/package/yargs

[Gerald_Img]: https://www.safetyandhealthmagazine.com/ext/resources/images/2016/04-april/construction-safety.jpg?1458739490