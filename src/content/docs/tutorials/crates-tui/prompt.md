---
title: Prompt
---

The state of the search prompt is represented by this struct:

```rust
{{#include @code/crates-tui-tutorial-app/src/widgets/search_prompt.rs:state}}
```

Here is the search prompt widget:

```rust
{{#include @code/crates-tui-tutorial-app/src/widgets/search_prompt.rs:widget}}
```

To render the prompt, you can

1. render a border
2. split the horizontal space into 2
   - render the prompt text into the first part
   - render the sort by text into the second part

Finally you have to update the cursor state so that the `app` chooses to show the cursor
appropriately.

```rust
{{#include @code/crates-tui-tutorial-app/src/widgets/search_prompt.rs:render}}
```

Here's the full code for reference:

<details>

<summary>Copy the following into <code>src/widgets/search_prompt.rs</code></summary>

```rust
{{#include @code/crates-tui-tutorial-app/src/widgets/search_prompt.rs}}
```

</details>