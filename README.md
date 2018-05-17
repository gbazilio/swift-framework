Universal Framework for iOS using Swift
==========

This is a demo code with the single purpose of reproducing a specific problem.

## Compatibility
This project contains a Cocoa Touch Swift code built as a framework. The swift version is set to `Swift Language Version = Swift 3.3.` 

## App
This project uses the framework built by *Compatibility* project. The swift version is set to `Swift Language Version = Swift 4.0`.

## Usage
Open *Compatibility* project and `CMD + B` it. The output will be placed in `Compatibility/`.
Open *App* and `CMD + B`. It should already be configured to consume the `.framework` from the above compilation.

## Problems found
When *Compatibility* is built using **Xcode 9.3 (9E145)** and *App* is using **Xcode 9.2 (9C40b)**, *App* throws the following error: `Module compiled with Swift 4.1 cannot be imported in Swift 4.0.3:`

![No compatibility](https://github.com/gbazilio/swift-framework/raw/master/problem1.png "No compatibility")

**Changing Swift version between all possible combinations didn't work for me. The framework had to be consumed by a project being built in the same Xcode version.**