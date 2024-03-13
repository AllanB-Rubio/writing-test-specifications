Unit test specifications should take the form of:

Expect [action] to be [some result]
Example: <br><br> For the prompt "A function called "addition" that returns the sum of two input integers", your tests might include: <br><br>
Expect addition(2, 3) to be a number<br>
Expect addition(2, 3) to be equal to 5<br>
Expect addition("a", 3) to be an error

Unit Tests:

1.  A function called "multiplication" that returns the product of the two input numbers.

    Expect multiplication(2,4) to be a number
    Expect multiplication(2,4) to be equal to 8
    Expect multiplication(-2,4) to be equal to -8
    Expect multiplication(0,4) to be equal to 0
    Expect multiplication(2,"a") to be an error

2.  A function called "concatOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.

        Example: concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1])
        ...should result in [-1, 1, 3, 9, 15]

Think about the following; you may need to make assumptions or decisions about the prompt and how the code should behave:
What should happen with unexpected inputs?

What kinds of unexpected inputs should we worry about?

What should happen when there are multiples of the same odd number in the arrays? (Hint: We gave you the answer to this one in the example above.)

    Expect concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1]) to return an array of numbers
    Expect concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1]) to return only odd numbers in single array
    Expect concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1]) to return odd numbers array in ascending order
    Expect concatOdds([], []) to return an empty array
    Expect concatOdds([2], [4]) to return an empty array


3. Functional Tests:
A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.
Think about the following; you may need to make assumptions or decisions about the prompt and how the feature should behave:
What should happen if the cart is empty?
What needs to be shown to the user at each step of check out?
What behaviors of this feature does the prompt miss or gloss over?

    When the cart is empty: Expect user to be informed that the cart is empty and prompted to add items before proceeding with checkout.

    When a guest checks out: Expect user to be asked if they want to create an account or log in before proceeding with guest checkout.

    When a logged-in user checks out: Expect user to be directed to the checkout process without being prompted to create an account or log in.

    At each step of checkout: Expect user to be shown relevant information such as item details, total price, shipping options, billing information, and order summary.

    Behavior not covered by the prompt:
    Error handling for invalid inputs during checkout.
    Handling of unexpected errors during checkout process.
    Confirmation message after successful checkout.