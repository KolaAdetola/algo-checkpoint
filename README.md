# Insertion Sort Implementation in JavaScript

A simple implementation of the insertion sort algorithm in JavaScript. Insertion sort is a straightforward sorting algorithm that mimics the way we sort playing cards in our hands. Each time we take a new card, we insert it into the right place in our hand.

## Table of Contents

- [Description](#description)
- [Instructions](#instructions)
- [Code](#code)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Description

This project provides a JavaScript implementation of the insertion sort algorithm. Insertion sort works by taking elements from an unsorted array and inserting them into their correct position within a sorted subset of the array.

## Instructions

1. Each time, work only with the first `i-1` elements of the array.
2. Pick the element `arr[i]` and insert it into the sorted sequence in the array from `0` to `i-1`.

## Code

Here is the JavaScript implementation of the insertion sort function:

```javascript
function insertionSort(arr) {
    const n = arr.length;
    for (let i = 1; i < n; i++) {
        let current = arr[i];
        let j = i - 1;
        while (j >= 0 && arr[j] > current) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = current;
    }
    return arr;
}
