Thanks for taking the time to apply to CircuitHub. Our approach to assessing technical 
ability is a short take-home test that should require no more than an evening or two. 
It will provide a bit of insight into the wonderful world of electronics and it's 
also a great opportunity to collaborate with an expert team using Haskell in production. 
Please feel free to keep in touch as you work on the problem, the test is designed to 
simulate a realistic collaborative working environment.


Quoting Parts
=============

CircuitHub uses an API service called Octopart_ as a source of electronic parts data. 
When a user uploads a project to CircuitHub, we use Octopart to provide pricing data 
for all the different parts on a user's circuit board. We then combine this pricing data
to provide a total price based on the batch size a user requires. In this test, we are 
looking to replicate a simplified version of this system.

Using Haskell you should write a client for the Octopart API that can be executed::

	quoteparts bom.csv 10

and provides the output::

	23.31 USD

The input bom.csv is a bill of materials. A bill of materials is a list of all the parts
required for a given project. You can find the `CSV file here`_. Every line of the CSV
can be parsed into the following data structure::

	data BOMLine = BOMLine { manufacturer :: String
	                       , partNumber :: String
	                       , quantity :: Int
	                       }

10 is the batch size we are computing the cost for.

An interactive example of how to compute the cost for this BOM at a given batch size can
be found here_.

You are free to use any Haskell libraries that are available on Hackage. Your solution
should demonstrate code clarity, and discuss any potential performance
or reliability problems.

.. _Octopart: https://octopart.com/api/home
.. _here: https://octopart.com/bom-tool/DIGdamfs
.. _CSV file here: https://github.com/circuithub/handbook/blob/interview-problem/bom.csv