
# Importance of Callback Functions
Callbacks enables asynchronous programming in JS.

# Issues with Callbacks

1. Callback Hell
2. Inversion of Control

# Callback Hell

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








