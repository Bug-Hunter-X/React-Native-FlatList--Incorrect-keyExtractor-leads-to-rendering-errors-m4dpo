# React Native FlatList: Incorrect keyExtractor

This repository demonstrates a common yet elusive bug in React Native's FlatList component: using a non-unique key in the `keyExtractor` function.  This leads to incorrect rendering and performance problems, often with unhelpful error messages.

## The Problem

The `keyExtractor` function in `FlatList` *must* return a unique key for each item in the data array.  If it doesn't, FlatList may not render correctly, causing issues such as:

* Incorrect item ordering
* Items disappearing or duplicating
* Poor performance

The error messages are often generic and don't explicitly point to the `keyExtractor` issue.

## The Solution

Ensure that your `keyExtractor` returns a unique string or number for every item in the data array.  This often involves using a unique ID field from your data source (e.g., a database ID).

## Setup

1. Clone this repository
2. `npm install`
3. Run the app on an emulator or physical device
