Interviewing
------------

CircuitHub's current approach to assess technical ability is based on a take
home problem, specified below.

Coding Problems
===============

CircuitHub uses a service called Octopart as a source of electronic parts. When
a user uploads a project to CircuitHub, we use Octopart to find potentially
matching parts for every component used in a project, which includes information
about pricing that is used to provide an estimated quote of the cost of
fabrication. In this problem, you'll use both the CircuitHub API along with
Octopart's API to solve a similar problem.

You will be given a CSV file listing parts in an electronic project. You can
assume that every line of this CSV file can be parsed into the following data
structure:::

   data BOMLine = BOMLine { manufacturer :: String
                          , partNumber :: String
                          , quantity :: Int
                          }

Given this CSV file, your challenge is to use Octopart to provide a cost
estimate for purchasing parts for an order.

You are free to use any Haskell libraries that are available on Hackage. Your
solution should demonstrate code clarity, and discuss any potential performance
or reliability problems.
