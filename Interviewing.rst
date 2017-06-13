Interviewing
------------

CircuitHub's current approach to assess technical ability is based on a take
home problem, specified below.

Coding Problems
===============

CircuitHub uses a service called Octopart_ as a source of electronic parts data.

A bill of materials or BOM_ is a list of parts with corresponding prices and vendors.

Given a small example BOM:: 

manufacturer, partNumber, quantity
Microchip, MIC5219YM5-TR, 1
Bourns, CAT16-1000F4LF, 5
Panasonic, ERA-3AED101V, 5
Vishay Dale, TNPW0603100RBYEN, 5
Analog Devices, ADM3202ARNZ, 5

Using Haskell write a client for the Octopart API that computes the total price of the BOM 
for various batch sizes.

You are free to use any Haskell libraries that are available on Hackage. Your
solution should demonstrate code clarity, and discuss any potential performance
or reliability problems.

.. _Octopart: https://octopart.com/api/home
.. _BOM: https://octopart.com/bom-tool/DIGdamfs