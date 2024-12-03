1. Standard Lorenz system parameters:


Input:

```plaintext
 Enter the number of points in the block (k): 4Enter the number of points in the block (k): 4
Enter the start time (x0): 0
Enter the end time (xend): 10
Enter the initial conditions (y0, separated by spaces): 1 1 1
Enter the error tolerance: 1e-6

```

Expected output (approximate values at x = 10):

```plaintext
y[0] = -9.047283541
y[1] = -10.20387137
y[2] = 26.44450446

```

2. Short time interval:


Input:

```plaintext
 Enter the number of points in the block (k): 4Enter the number of points in the block (k): 4
Enter the start time (x0): 0
Enter the end time (xend): 1
Enter the initial conditions (y0, separated by spaces): 1 1 1
Enter the error tolerance: 1e-6

```

Expected output (approximate values at x = 1):

```plaintext
y[0] = 1.779618859
y[1] = 3.658094348
y[2] = 1.027944252

```

3. Different initial conditions:


Input:

```plaintext
 Enter the number of points in the block (k): 4Enter the number of points in the block (k): 4
Enter the start time (x0): 0
Enter the end time (xend): 5
Enter the initial conditions (y0, separated by spaces): -10 -10 25
Enter the error tolerance: 1e-6

```

Expected output (approximate values at x = 5):

```plaintext
y[0] = -6.821115987
y[1] = -6.765306292
y[2] = 25.07613114

```

4. Higher precision:


Input:

```plaintext
 Enter the number of points in the block (k): 6Enter the number of points in the block (k): 6
Enter the start time (x0): 0
Enter the end time (xend): 15
Enter the initial conditions (y0, separated by spaces): 0 1 1.05
Enter the error tolerance: 1e-8

```

Expected output (approximate values at x = 15):

```plaintext
y[0] = 10.66434716
y[1] = -5.497748848
y[2] = 42.28466665
```

5. Long time interval:


Input:

```plaintext
 Enter the number of points in the block (k): 4Enter the number of points in the block (k): 4
Enter the start time (x0): 0
Enter the end time (xend): 100
Enter the initial conditions (y0, separated by spaces): 2 3 4
Enter the error tolerance: 1e-6

```

Expected output (approximate values at x = 100):

```plaintext
y[0] = -10.84794211
y[1] = -16.1422022
y[2] = 22.48228304
```