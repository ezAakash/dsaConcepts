					Binary Search 


	. Binary search eliminates ranges, not values. it complexity is log(n) because of each decision halves the alive ranges.

	. use l <= r : when searching for exact value in the range.
		- reason : you want to exaust the entire search space , including final point.

	. use l < r : when searching for a boundary (first true / last true ).
		- reason : you want to converge pointers onto a singe point.

	. HIDDEN TRAPS :
		- infinite loop : mid == l
		- mid = ( l + r ) // 2 
		  if something:
			r = mid
		  else:
			l = mid
		
		- to avoid use : l = mid + 1 and r = mid - 1

	. TEMPLATES :
		while l <= r :
			mid = l + ( r - l ) // 2      # do this and ( l - r ) // 2 works the same. 
			
			if mid == target:		
				return mid 
			elif mid < target:
				l = mid + 1
			else:
				r = mid - 1 

	. 2  LOWER BOUND / FIRST TRUE         # F F F F F F F T T T T T ( pattern : min something such that a condition holds)
		while l < r:
			mid = l + (r - l ) // 2
			
			if condition(mid) == true:
				r = mid   # keep mid 
			else:
				l = mid + 1 # remove mid
		
		return l 


	. 3 UPPER BOUND / LAST TRUE          # T T T T T T F F F F F F F F ( pattern : max sometning such that a condition holds )
		while l < r :
			mid = l + ( r - l + 1) // 2 #bais toward right
			
			if condition(mid) == true:
				l = mid      # keep mid 
			else:
				r = mid - 1  # remove mid

	. PATTERN 1: Searching for a Boundary

	. BSOA : array is irrelevant .. search space conceptual .... choose a possible answer - > check if workable


	. PATTERN 2 : Searching in Monotonic Structure ( not ness.. sorted array, but monotonicity in input )
		- Peak mountain array ( inc ---> dec )
		- rotated sorted array 
		- single elemenet in sorted array 
		- search for local minima/ maxima .

		( clues : problem involve slopes, or direction change, inflection point, rotation )	




	. DIFFERECE BETWEEN BSOA and SLIDING WINDOW PROBLEMS : 
		BSOA : here , we optimize over VALUES, not position. ( here, its about feaibility for a chosen param X )
		SW : here , we optimize over a range. ( condition is about continuous elements )
	

	





	. why Peak uses l < r not l <= r cause here we are peak def exist using == adds additional loop.

	. also this l < r condition and mid = l + r // 2 gaurantees that mid = l never r so, mid + 1 <= r always inbound.






	. GOLDEN RULE:
		1. ask : "am I trying to find a value or find a position/boundary"
		 	 - value search => l < = r
			 - boundary/Peak search => l < r 
		2. "Is boundary first or Last"
			 - first -> lower mid
			 - last -> upper mid



