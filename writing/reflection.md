# Intersection Algorithms

## Evelyn Griffith

## Program Output

### Use eight fenced code blocks to provide output from eight different runs of `intersection` with different inputs

`Summary of the runs for the List-based algorithms:`

#### Two outputs from running the `ListSingle` algorithm with different inputs

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:23:52  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.000     CPU time: 0.000
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach ListSingle

0.001 intersection  intersection\main.py:114
└─ 0.001 compute_intersection_list_single  intersection\main.py:77
```

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:35:13  Samples:  1698
 /_//_/// /_\ / //_// / //_'/ //     Duration: 1.826     CPU time: 1.750
/   _/                      v4.0.3

Program: intersection --number 1000000 --maximum 25 --profile --approach ListSingle

1.828 intersection  intersection\main.py:114
├─ 1.800 compute_intersection_list_single  intersection\main.py:77
│  ├─ 1.504 [self]
│  └─ 0.296 list.append  <built-in>:0
│        [2 frames hidden]  <built-in>
└─ 0.029 [self]
```

#### Two outputs from running the `ListDouble` algorithm with different inputs

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:37:15  Samples:  73
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.081     CPU time: 0.078
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach ListDouble

0.073 intersection  intersection\main.py:114
├─ 0.072 compute_intersection_list_double  intersection\main.py:61
│  ├─ 0.068 [self]
│  └─ 0.004 list.append  <built-in>:0
│        [2 frames hidden]  <built-in>
└─ 0.001 stop  pyinstrument\profiler.py:136
      [3 frames hidden]  pyinstrument
```

```
🔬 Here's profiling data from computing an intersection with random data containers of 10000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:47:43  Samples:  8973
 /_//_/// /_\ / //_// / //_'/ //     Duration: 9.321     CPU time: 8.969
/   _/                      v4.0.3

Program: intersection --number 10000 --maximum 25 --profile --approach ListDouble

9.311 intersection  intersection\main.py:114
└─ 9.311 compute_intersection_list_double  intersection\main.py:61
   ├─ 8.495 [self]
   └─ 0.816 list.append  <built-in>:0
         [2 frames hidden]  <built-in>
```

#### Two outputs from running the `TupleSingle` algorithm with different inputs

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:50:32  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.010     CPU time: 0.016
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach TupleSingle

0.008 intersection  intersection\main.py:114
└─ 0.008 compute_intersection_tuple_single  intersection\main.py:103
```

```
🔬 Here's profiling data from computing an intersection with random data containers of 10000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 17:02:17  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.139     CPU time: 0.141
/   _/                      v4.0.3

Program: intersection --number 10000 --maximum 25 --profile --approach TupleSingle

0.144 intersection  intersection\main.py:114
└─ 0.144 compute_intersection_tuple_single  intersection\main.py:103
```

#### Two outputs from running the `TupleDouble` algorithm with different inputs

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 17:05:17  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 5.105     CPU time: 5.031
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach TupleDouble

5.095 intersection  intersection\main.py:114
└─ 5.095 compute_intersection_tuple_double  intersection\main.py:91
```

```
🔬 Here's profiling data from computing an intersection with random data containers of 1500!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 17:24:59  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 30.206    CPU time: 29.484
/   _/                      v4.0.3

Program: intersection --number 1500 --maximum 25 --profile --approach TupleDouble

30.216 intersection  intersection\main.py:114
└─ 30.216 compute_intersection_tuple_double  intersection\main.py:91
```

In this assignment I decided that the number in particular needed to be dependent on each individual input. What I mean by this is that the input number should depend on whether or not that function can run a number that large. For example, if I tried to run a number over 1500 for the TupleDouble approach then it would take a really long time for the program to complete it. However, if i ran 1000000 on the ListSingle approach it took less than 20 seconds to complete. So, in saying all of this I am justifying the use of these differing numbers for data collection because in order to collect data I needed to use numbers that were large or small enough for an output to be found based on the function command.

## Performance Analysis

Throughout this project, I learned that an intersection is much much faster with a list. In class I chose to say that a Tuple would be faster but this was False. A tuple is much slower than a list in this instance because a tuple is immutable whereas a list is mutable. This essentially means that one cannot be changes whereas the other one can. A list is mutable and this means that it can be changed, but the significance of that with respect to this project is that when given the code for a tuple, there is a section in the code that says `result += something`, this is critically important because this line of code is actually telling the tuple, that it needs to rebuild itself with that new "something" added in. Lists are different because they DO NOT require that they be completely rebuilt in order to add new data to the list. A tuple, because it is immutable, requires that all of the data within the container be changed in order for it to change the data. That is why a list is faster. This is also further exacerbated by the fact that when a tuple is given a really large number it may have hundreds, if not thousands, of numbers that would need to be added to its container so it would need to take itself apart and rebuild hundreds of times before it could produce a suitable output. A list, however, will just adjust itself based on the new data given without rebuilding.

On a different note, the for loops and sometimes nested for loops within the function can also help to determine whether or not a function will be faster. When a function uses a nested double for loop, it has to iterate over everything and see if each aspect of the list meets the condition. However, when using an if statement, the condition that the two things on the seperate data holders are the same is already set before the computer starts iterating so the computer just has to look through the list and see if anything matches as opposed to iterating through everything and then deciding on a case by case basis if they match. So to conclude, this means that the for-if statements will be faster because they set a preexisting condition before the iteration starts.

The fastest approach for computing overall is the ListSingle approach, not only is this approach able to handle things much faster, but it is also able to operate with much much larger numbers than any of the other functions. You will notice that in my data, the ListSingle approach is handling 1000000 whereas the others are only handling about 10000. Also, the data above shows that the ListSingle approach operates faster than the others even when handling a number this large. This is because this approach uses botht he for-if and List approaches that were spoken of in the above paragraphs.

## Source Code

### Describe in detail how the completed source code works

#### A class that defines the four algorithmic options for running the experiment

```
class IntersectionApproach(str, Enum):
    """Define the name for the approach for performing intersection of structured types."""

    list_single = "ListSingle"
    tuple_single = "TupleSingle"
    list_double = "ListDouble"
    tuple_double = "TupleDouble"
```

What this source code does is it defines the approach names for the different structured types. This means that it will give us the different names that we can use to specify which function we are trying to run a number with.

#### A function signature that defines the command-line interface for `intersection`

TODO: Use a fenced code block to provide the requested source code
TODO: Write at least one paragraph to explain the request source code
TODO: Explain each of the command-line arguments for this program

#### A function that can generate a data container with random values in it

TODO: Use a fenced code block to provide the requested source code
TODO: Write at least one paragraph to explain the request source code
TODO: Explain each line of source code in this function

### What was the greatest challenge that you faced when completing this assignment?

TODO: Provide a one-paragraph response that answers this question in your own words.

### Leveraging your response to the previous question, how did you overcome the challenge?

TODO: Provide a one-paragraph response that answers this question in your own words.
