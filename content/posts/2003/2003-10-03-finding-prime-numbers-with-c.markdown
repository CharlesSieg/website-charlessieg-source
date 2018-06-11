---
date: '2003-10-03 19:04:00'
layout: post
slug: finding-prime-numbers-with-c
status: publish
title: Finding Prime Numbers with C#
wordpress_id: '12'
tags:
- Tips and Tricks
---

This class, PrimeFinder, has two methods. The Find method takes the piMax parameter and finds all prime numbers between 0 and piMax. The Print method dumps the list of prime numbers from piStart to piMax, for example, between 1,000 and 100,000. With the int type, this class works well for primes up to approximately 14,000,000.

The Find method uses the algorithm known as the Sieve of Eratosthenes to identify prime numbers. It is an effective algorithm for “small” primes, i.e. numbers less than 10 billion. In fact, any Pentium class computer running at 1 GHz or faster can compute all small primes in less than a second.

Surprisingly, the .NET framework is very efficient in managing boolean arrays. The total increase in system memory usage is only a few kilobytes, depending on value of piMax.

This routine is a trivial programming exercise and does not do much to demonstrate features of C# but I present it as a C# implementation of the Sieve and to serve as a basis for other programming examples on this site which demonstrate delegate usage and multithreading.

Prime number research continues and many articles can be found at the Prime Pages at [http://www.utm.edu/research/primes/](http://www.utm.edu/research/primes/).

The source code to this class is available here:

`
using System;`

`namespace RenkaraTutorials
{
public class PrimeFinder
{
bool[] moNumberArray;

public void Find( int piMax )
{
// Create array and set all values to true
moNumberArray = new bool[ piMax ];
for ( int i = 2; i < piMax; i++ )
{
moNumberArray[ i ] = true;
}

// mark out all multiples of 2 first
int j = 2;
for ( int i = j + j; i < piMax; i = i + j ) // start with 2j as j is prime
{
moNumberArray[ i ] = false;
}

// Find square root of n and calculate up to n
double ldLimit = Math.Sqrt( piMax );
for ( j = 3; j <= ldLimit; j = j + 2 )
{
// only do if j is a prime
if ( moNumberArray[ j ] )
{
for ( int i = j + j; i < piMax; i = i + j ) // start with 2j as j is prime
{
moNumberArray[ i ] = false; // set all multiples to false
}
}
}
} // end method Find

public void Print( int piStart, int piMax)
{
Console.WriteLine( "Prime Numbers from " + piStart + " to " + piMax + ":" );
for ( int i = piStart; i < piMax; i++ )
{
if ( moNumberArray[ i ] )
{
Console.Write( i + " " );
}
}
} // end method Print

`

`} // end class PrimeFinder
} // end namespace RenkaraTutorials
`
