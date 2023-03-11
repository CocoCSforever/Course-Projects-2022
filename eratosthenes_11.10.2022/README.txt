Summary:
    The idea behind the Sieve of Eratosthenes is that finding composite numbers (non primes) is a lot easier than finding primes, so we can follow a process of elimination where we exclude composites to quickly winnow down our collection of candidate numbers.
    We do this by iteratively identifying as composite the multiples of values, starting at 2. We then exclude in our subsequent search anything that has been identified as a composite previously. Each time we hit a prime we add that to our list of primes and then mark all multiples of the prime as composites.

list_primes.py
    import prime generator module, and contain a main function that call a method defined in that module that returns the list of primes, and finally it should print them out.
prime_generator.py
    will define the class PrimeGenerator that contains a method primes_to_max() that takes an integer argument and returns a list of all primes from 2 to the argument value. It should employ the Sieve of Eratosthenes algorithm, which can be expected to compile a list for the argument 1000000 in about a second (this may vary somewhat, but you should expect to be in this ballpark).
prime_generator_test.py
    will be PyTest test suite. It will import the PrimeGenerator class and define a single test function called test_primes_to_max(). 
    Although it's not straightforward to test the output of our primes generator with absolute certainty, we can create a unit test that will test to ensure that some known primes are showing up in the appropriate places in the list when the method is called on smaller numbers.

Run list_primes.py