# Orders page

*Note: The API always returns only 10 orders, doesn't support sorting, filtering, pagination.*

Here will be 3 main features: list of orders, sorting and filter.

## List of orders

First of all, you need to implement a redux module to fetch and store orders.
Basicly, it's a table with 5 columns:

Ref | Patient | Clinic | Lab | Created at
--- | ------- | ------ | --- | ----------

Each row mush be clickable, and on click a user must be redirected to the order page (`/orders/:orderId`).

Don't forget to render loader while a loading of the list. Don't implement pagination.

## Sorting

Implement a dropdown with 4 options somewhere above the orders list:

1. Lab (ASC)
2. Lab (DESC)
3. Created at (ASC)
4. Created at (DESC)

Obviously, list should be sorted properly.

## Filter

There must be 2 item: the first one - dropdown with types (e.g filter by clinic, lab, etc), the second one is input with value that'll be used for filtering. Filter the list after each typed letter.

Filter should implement "includes" logic, so for "foo" query "beforefoo", "fooafter", "inthefoomiddle" are the possible values. Transform values to lower case.

"Filter by" dropdown options:
1. Clinic 
2. Lab
3. Patient
4. Created at (Please, use "YYYY-MM-DD" format for comparison)

There shouldn't be any filters by default.

## UX

Think about UX, display all the items as you want, make it easy to use.