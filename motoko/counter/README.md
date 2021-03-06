## Counter

[![Build Status](https://travis-ci.org/dfinity-lab/examples.svg?branch=master)](https://travis-ci.org/dfinity-lab/examples?branch=master)

This sample project create a single actor named `+Counter+` and provides a simple example of how you can verify that the variable state—that is, the value of the variable between calls—persists.

The program uses the `+counter+` variable to contain a natural number that represents the current value of the counter.
This program supports the following types of function calls:

* The `+set+` function call updates the current value to an arbitrary numeric value you specify as an argument.
* The `+inc+` function call updates the current value, incrementing by 1 (no return value).
* The `+get+` function call queries and returns the current value.

### Prerequisites

You have downloaded and installed the SDK as described in [Getting started](https://sdk.dfinity.org/developers-guide/getting-started.html).

### Demo

Start a local internet computer.

```bash
dfx start
```

Execute the following commands in another tab.

```bash
dfx build
dfx canister install --all
dfx canister call counter set '(7)'
dfx canister call counter inc
dfx canister call counter get
```

Observe the following result.

```
(8)
```
