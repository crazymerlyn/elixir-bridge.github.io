---
layout: page
title: Lists and Tuples
date: 2016-10-1 13:38:30 -0700
---



## Lists

Here is an example of a list in Elixir: `[1, 2, 3, 4]`

This may look exactly like an array if you are familiar with Ruby or Javascript, however they're a little different in the details. We'll get into that later.

Lists in Elixir are created by surrounding a list of values with brackets `[]`. Try creating a list in the console by typing `[1, 2, 3]`.

Lists don't need to contain only one type. They can hold on to multiple different types in the same list. Create a list with multiple types by typing: `[:hello, "world"]`

```elixir
iex> [:hello, "world"]
[:hello, "world"]
```

We create the list with the brackets, and by typing _literal_ values into the items; you can also use variables in lists.

Type the following:

```
iex> foo = "bar"
"bar"
iex> [1, foo, 3]
[1, "bar", 3]
```

As you can see, Elixir replaces the variable with the literal value in the list it creates.

We have a bunch of built-in methods we can use to interact with and manipulate lists in Elixir.

Try adding and removing items from lists.

Type the following(one line at a time):

```elixir
iex> length [1, 2, 3] # 3
iex> [1] ++ [2] # [1, 2]
iex> [1, 2, 3] -- [2] # [1, 3]
```

## Tuples

Tuples in Elixir are types that store a fixed number of elements. Let's look at how to create a tuple.

Tuples are created by using the curly brackets with elements separated by commas.

Type the following into the console:

```elixir
iex> {:ok, "hello"}
```

Because these are created and stored in one block in memory, we can use the indicies to indicate which value we want to pull out of a tuple. For instance, we can get the `:ok` value in the tuple by using the `elem/2` function. This function takes 2 arguments - the tuple itself, and the index for the value we are looking for.

In this case we want to retrieve the first element in the tuple which is located at index 0.

Type the following into the console:

```elixir
iex> elem({:ok, "hello"}, 0) # :ok
```
As you can see, the function returns `:ok`.

We can check the size of a tuple using the `tuple_size/1` function:

Type the following:

```elixir
iex> tuple_size({:ok, "hello"}) # 2
```

And we can replace elements in a tuple by using the `put_elem/3` function, which takes the tuple, the argument, and the value:

Type the following:

```elixir
iex> put_elem({:ok, "hello"}, 1, "world")
```
