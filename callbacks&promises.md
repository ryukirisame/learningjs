
# Importance of Callback Functions
Callbacks enables asynchronous programming in JS.

# Issues with Callbacks

1. Callback Hell
2. Inversion of Control

## Callback Hell

Let's suppose we have an E-Commerce site. 
The flow is like this: Order is Created -> Payment -> Order Summary -> Update Wallet

Now, let's suppose we have different API's for each action. Now, the issue is, the API's must be called in a given sequence.
With our current knowledge of Callbacks, what we can do is like this:

```
const cart = ["jordan shoe", "titan watch", "van heusen shirt", "jeans"];

api.createOrder(cart, function () {
  api.proceedToPayment(function () {
    api.showOrderSummary(function () {
      api.updateWallet();
    });
  });
});
```

As we can see, we have multiple nested callbacks. This happened because the sequence of operations must be maintained.
This is making the code grow horizontally, rather than vertically. This kind of code will make it difficult for us to debug and is complex to read.

This multiple nesting of callbacks is called Callback Hell (Pyramid of Doom).

## Inversion of Control

Let's consider this code:
```
api.createOrder(cart, function () {
        api.proceedToPayment();
});
```
Here, we see that we are passing a callback function to createOrder API. Now, the control of calling the proceedToPayment API has been given to createOrder API, instead of us explicitly calling the payment API ourselves. This is called inversion of control, where we lose control over our code.

### Issues with Inversion of Control
- Unpredictability: We don't know how the code is written inside the createOrder API and how it will affect our proceedToPayment function.
- Execution Guarantee: Will our proceedToPayment function be called as expected? There is uncertainty about the callback's execution.
- Multiple Invocations: What if the proceedToPayment function is called multiple times due to a bug or logic error inside createOrder?
- Error Handling: We are reliant on the createOrder API to handle errors properly. If it has bugs, our callback may not execute correctly or at all.










