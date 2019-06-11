# Week 1 - Day 2

**NOTE:** Follow the instructions carefully and follow coding discipline

## FSD.W1.2.A (10 min)

- Go to your home directory `cd ~` and create a folder called `assignments`   
- Create a folder called `week1` inside `assignments` folder  
- Create a folder called `day2` inside `week1` folder  
- Navigate to the folder `assignments/week1/day2` 
- All the work should be in this folder

## FSD.W1.2.B (40 min)

**NOTE: SAVE ALL THE COMMANDS ON HOW YOU ARRIVED AT THE ANSWER YOU NEED TO SUBMIT THEM**

Download the file https://raw.githubusercontent.com/masai-school/assignments-data/master/data/junk/marks_rand_2000.csv

The files contains marks the data of 2000 students from India and Pakistan one for each line in the below format

``` 
23 India 5cf9c9be70765c6c741bd34a
43 Pakistan 5cf9c9be70765c6c741bd352
.
.

```
1. Find the total number of students from India


```
ANSWER: 1500
```

Commands on how you got the answer

```
grep India marks_rand_2000.csv > indian.txt
wc -l indian.txt
```
2. No of students from Pakistan who are in top 100 list based on the marks scored
```
ANSWER:28
```

Commands on how you got the answer

```
sort -g marks_rand_2000.csv > top100.txt
tail -n 100 top100.txt > top100a.txt 
grep Pakistan top100a.txt > top.txt
wc -l top.txt

```
3. Top 3 students from India based on the marks scored
```
ANSWER:100 India 6cf9c9be70765c6c741bd66b
100 India 6cf9c9be70765c6c741bd6b4
100 India 6cf9c9be70765c6c741bd6fa
```

Commands on how you got the answer

```
$ grep India top100a.txt > top3india.txt
$ tail -n 3 top3india.txt 
```
4. Bottom 5 students from Pakistan based on the marks scored
```
ANSWER: 0 Pakistan 5cf9c9be70765c6c741bd540
0 Pakistan 5cf9c9be70765c6c741bd566
0 Pakistan 5cf9c9be70765c6c741bd5d2
0 Pakistan 5cf9c9be70765c6c741bd62f
0 Pakistan 5cf9c9be70765c6c741bd6a5
```

Commands on how you got the answer

```
$grep Pakistan marks_rand_2000.csv > pak.txt
$ sort -g pak.txt > pakasc.txt
$ head -n 5 pakasc.txt
```

## FSD.W1.2.C (30 min)

**NOTE: SAVE ALL THE COMMANDS ON HOW YOU ARRIVED AT THE ANSWER YOU NEED TO SUBMIT THEM**

Clone the repo https://github.com/dwmkerr/hacker-laws inside `assignments/week1/day2` folder

1. Find the total number of commits done by the user with the name `Dave`

```
ANSWER:91
```

Commands on how you got the answer

```
$ git log --author="Dave" > commit.txt
$ grep Dave commit.txt > no_commit.txt
$ wc -l no_commit.txt 

```

2. Find the total no of commits done in the month of April

```
ANSWER:10
```
Commands on how you got the answer

```

git log > log.txt
grep -i apr log.txt > apr.txt
wc -l apr.txt 

```

3. Find the total no of commits done in the year 2018

```
ANSWER:33
```
Commands on how you got the answer

```
<COMMAND 1>
grep 2018 log.txt > 2018.txt
wc -l 2018.txt 

```

## FSD.W1.1.D (20 min)

- Clone the repo https://github.com/masai-school/full-stack-dev inside `~/repos` folder
- Navigate to the folder `~/repos/full-stack-dev/`
- Copy the `course/week_1/day_2/w1_day_2_assignments.md` file to the `test` repository which should be at `~/repos/test`
- Open the file `w1_day_2_assignments.md` in the text editor using GUI and fill all the answers
- Sync your `test` repo online with the solutions
