# solution-5.2

#prateek joshua thotlapalem

#5.2:Suppose we toss darts randomly at a square dartboard, whose bullseye is at the origin, and whose sides are 2 feet in length. Suppose also that there’s a circle inscribed in the square dartboard. The radius of the circle is 1 foot, and it’s area is π square feet. If the points that are hit by the darts are uniformly distributed (and we always hit the square), then the number of darts that hit inside the circle should approximately satisfy the equation

 number in circle/ total number of tosses = π /4 , 

since the ratio of the area of the circle to the area of the square is π/4.

 We can use this formula to estimate the value of π with a random number generator:
number in circle = 0; 
for (toss = 0; toss < number of tosses; toss++)
 {
     x = random double between −1 and 1; 
     y = random double between −1 and 1; 
     distance squared = x∗x + y∗y; 
    if (distance squared <= 1) 
     number in circle++; 
  } 
   pi estimate = 4∗number in circle/((double) number of tosses);

This is called a “MonteCarlo” method, since it uses randomness (the dart tosses). Write an OpenMP program that uses a Monte Carlo method to estimate π. Read in the total number of tosses before forking any threads. Use are duction clause to ﬁnd the total number of darts hitting inside the circle. Print the result after joining all the threads. You may want to use long long ints for the number of hits in the circle and the number of tosses, since both may have to be very large to get a reasonable estimate of π.


#program executed 

#problem5.2: tested on windows
