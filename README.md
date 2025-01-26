# Unhandled AsyncStorage null value in React Native

This repository demonstrates a common, yet easily missed, error in React Native applications when working with AsyncStorage. The problem arises when attempting to retrieve data associated with a key that doesn't exist in AsyncStorage.  AsyncStorage returns `null` in this scenario, which can lead to unexpected crashes if not handled appropriately.

The `bug.js` file showcases the problematic code. The `bugSolution.js` file presents the corrected version.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`
3. Run the problematic code in `bug.js` (it will crash).
4. Run the corrected code in `bugSolution.js` (it will handle the null value gracefully).

## Solution

Always check for `null` values when retrieving data from AsyncStorage. Use a conditional statement to handle the case where a key is not found to prevent unexpected behavior or crashes.