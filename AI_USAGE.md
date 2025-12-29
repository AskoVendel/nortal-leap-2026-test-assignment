# AI Usage

I only used ChatGPT to review how Spring works and other Java syntax related things I had forgotten. I also used it to consider and reason about strategies. It was most helpful when it helped me understand how Spring essentially derives SQL queries from Repository function names and that is the part where it helped me come up with most efficient query.

# Notes and Assumptions

- There was some confusion regarding the `POST /api/return` endpoint. there was an update which made it accept `memberId` argument, so I made an assumption that `memberId` will always be provided and wrote my logic accordingly. This, however, broke the GUI when trying to return books. I tested by sending requests directly to API to verify that everything works as it should. 
- I realized that member who borrows an available book could reserve it right after as well, essentially borrowing book twice in a row. I can see how this could be an unintended behavior. Assignment specs didn't mention anything about it, so I decided to leave this as it is.
- I was somewhat confused with `ResultWithNext` class in automatic borrow on returning a book. In commit `619edd4` I made it display the `memberId` of the member who actually receives the book after It is returned. If, however, it was meant to display the id of the member next in line of who receives the book(first person in reservation queue), then this is how it is in earlier commit.

