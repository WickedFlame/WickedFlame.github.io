---
title: Polaroider
layout: "default"
nav_order: 3
---
## Polaroider
Automated Snapshottesting made simple  
  
Simplify UnitTesting with snapshots.  
Polaroider is a Approval Testing Framework that creates and compares snapshots of almost anything  

[![Build Status](https://travis-ci.org/WickedFlame/Polaroider.svg?branch=master)](https://travis-ci.org/WickedFlame/Polaroider)
[![Build status](https://ci.appveyor.com/api/projects/status/3v8mpq0p35vlegda/branch/master?svg=true)](https://ci.appveyor.com/project/chriswalpen/polaroider)
[![NuGet Version](https://img.shields.io/nuget/v/polaroider.svg?style=flat)](https://www.nuget.org/packages/polaroider/)
  
### Documentation
Visit [https://wickedflame.github.io/Polaroider/](https://wickedflame.github.io/Polaroider/) for the full documentation.
  
### Common, timeconsuming assertion testing
Conventional assertion testing needs multiple assertion checks to test and verify all properties of an object
```csharp
// arrange
var repository = new PersonRepository();

// act
var person = repository.LoadTestPerson(...);

// assert
Assert.IsEqual(person.Firstname, "Chris");
Assert.IsEqual(person.Lastname, "Walpen");
Assert.IsEqual(person.Company, "WickedFlame");
Assert.IsEqual(person.Address.Street, "Teststreet");
Assert.IsEqual(person.Address.Streetnumber, 3);
```

### Fast and easy approval testing with Polaroider
Polaroider reduces all assertions to just one call. 
Snapshottesting keeps the code simple, clean and readable.
```csharp
// arrange
var repository = new PersonRepository();

// act
var person = repository.LoadTestPerson(...);

// assert
person.MatchSnapshot();
```