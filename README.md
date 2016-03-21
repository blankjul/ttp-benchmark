-------------------------------------------------------
Traveling Thief Problem Benchmark
-------------------------------------------------------

1. Format:
We provide two different formats of our benchmark. 

First, the old format which was used for the larged scaled benchmark, which allows reusability 
for source code developed for the old benchmark.

Second, a JSON format which allows to use JSON parser to read the problem data easily.
One example format looks like the following:

{

	// could be either SingleObjective, MultiObjective or ProfitConstraint
	"problemType" : %problem_type%, 
	
	// maximal weight of the knapsack
	"maxWeight" : 748,

	// rent rate - note: only if problemType is equal to SingleObjective
	"R" : 1.55,

	// minimal speed of the thief
	"minSpeed" : 0.1,

	// maximal speed of the thief
	"maxSpeed" : 1.0,

	// NO_DROPPING, EXPONTENTIAL, INDIVIDUAL
	"profitEvaluator" : %profit_evaluator%, 

	// only STANDARD so far
	"timeEvaluator" : %time_evaluator%, 

	// XY_COORDINATES, FULL_MATRIX
	"cityType" : %city_type%,

	"cities" : [
	    [
	      X,
	      Y
	    ],
	    ....
	  ],
	"items" : [
	    {
	      "city" : $assigned_to_city$,
	      "weight" : 99.0,
	      "value" : 388.0
	    },
	    ......
	 ]
}

If the cities are listed coordinate wise the distance is caclulated by:

NEAREST_INT_ROUNDING(EUCL_2D(C1, C2))

which is nothing else than calculating the euclidean distance and rounding to the nearest integer.




-------------------------------------------------------
2. Parameter





-------------------------------------------------------
3. 

