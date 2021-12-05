# SecureReview

[`SecureReview`](https://github.com/thesecurereview/securereview/) is  a security mechanism that can be applied on top of a
Git-based code review system to ensure the integrity of the code review process
and provide verifiable guarantees that the code review process followed the
intended review policy.
To achieve this goal, `SecureReview` provides three main features:
- __Sing Code Review Policy__: `SecureReview` allows the project owner to compute
a digital signature over the code review policy and store it on the code review server
so it can be later retrieved from the server to verify the integrity of the code review policy.
In order to store the signature, a check status and a code review label
are defined on Github and Gerrit, respectively.
- __Sing Code Reviews__: `SecureReview` encapsulates each review in a review unit
and embeds it in a Git commit message.
Each review unit contains the relevant information in the review, such as
the reviewer’s rating, reviewer's comment and a signature over the entire review unit.
- __Create a Verifable Chain of Reviews per Code Change__: Each review unit depends on
the prior review unit (i.e., includes the signature field of the previous review).
This property prevents unauthorized changes in the middle of the chain.

## About

This project is managed by Prof. Reza Curtmola and other members of the
[NJIT Cybersecurity Research Center](https://centers.njit.edu/cybersecurity)
at NJIT and the [Secure Systems Lab](https://ssl.engineering.nyu.edu/) at NYU.


Contact: <hammad.afzali@gmail.com>
