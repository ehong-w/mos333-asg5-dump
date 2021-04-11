# EKT333 Modern Operating System ![GitHub last commit](https://img.shields.io/github/last-commit/ehong-w/mos333-asg5-dump?style=for-the-badge)

In my own words,\
`Make your life easier in a blink of a Touch n Go scan!`

![forthebadge](https://forthebadge.com/images/badges/powered-by-electricity.svg)

---

### Assignment 5
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/ehong-w/mos333-asg5-dump)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/ehong-w/mos333-asg5-dump)
![GitHub all releases](https://img.shields.io/github/downloads/ehong-w/mos333-asg5-dump/total)

---

#### Question 1
Compare and contrast the difference between First In First Out (FIFO) and Least Recently Used (LRU) page replacement algorithm.

> Both FIFO and LRU are page replacement algorithm used by an operating system to decide which memory pages to swap out. Page replacement happens whenever page fault occurs, which is when the requested page is not found in the main memory. Both FIFO and LRU algorithms describe when a page fault happens, how does the respective algorithm swaps a page frame in the memory with another page frame that is in the disk.
>
> For the FIFO algorithm, the operating system keeps track of all... ...
>
> The FIFO algorithm is one of the simplest page replacement algorithm because it is easy to implement. However, by replacing an... ...

#### Question 2
A system uses 3 page frames for storing process pages in main memory. It uses the Least Recently Used (LRU) page replacement policy. Assume that all the page frames are initially empty. What is the total number of page faults, page hit, fault ratio and hit ratio that will occur while processing the page reference string given below?

```
4, 7, 6, 1, 7, 6, 1, 2, 7, 2
```

```
          +---+---+---+---+---+---+---+---+---+---+
          | 4 | 7 | 6 | 1 | 7 | 6 | 1 | 2 | 7 | 2 |
+---------+---+---+---+---+---+---+---+---+---+---+
| Frame 1 | 4 | 4 | 4 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Frame 2 |   | 7 | 7 | 7 | 7 | 7 | 7 | 2 | 2 | 2 |
| Frame 3 |   |   | 6 | 6 | 6 | 6 | 6 | 6 | 7 | 7 |
|         | F | F | F | F | H | H | H | F | F | H |
+---------+---+---+---+---+---+---+---+---+---+---+
```

> Total number of page fault = 6
>
> Total number of page hit = 4
>
> Fault ratio = 6/10 = 0.6
>
> Hit ratio = 4/10 = 0.4

#### Question 3
A process contains eight virtual pages on disk and is assigned a fixed allocation of four page frames in main memory. The following page trace occurs :

```
1, 0, 2, 2, 1, 7, 6, 7, 0, 1, 2, 0, 3, 0, 4, 5, 1, 5, 2, 4, 5, 6, 7, 6, 7, 2, 4, 2, 7, 3, 3, 2, 3
```
