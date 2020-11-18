---
title: Frequently Asked Questions
slug: /faq
---

### Is it "ink" or "ink!"? What does the "!" stand for?

TODO

### Who is "Squink"?

<div class="squid-container">
    <img src="./img/ink-squid.svg" alt="Squink ‒ the ink! mascot" class="squid" />
    This is Squink
    
    <br/>
    todo
    
    <br/>
    todo
</div>

### What's the relationship of Substrate/Polkadot?

TODO

### How to do cross-contract calling?

See the [Cross-contract calling](/basics/cross-contract-calling) section.

### What is a contract's ABI or Metadata?

TODO

### Can a re-entrancy bug occur in ink! contracts?

TODO

### What are chain-extensions?

TODO

### How can I use ink! with a Substrate chain with a custom chain config?

TODO

### Overflow Safety?

Being written in Rust, ink! can provide compile-time overflow/underflow safety. Using a Rust compiler configuration, you can specify whether you want to support overflowing math, or if you want contract execution to panic when overflows occur. No need to continually import "Safe Math" libraries, although Rust also provides [integrated checked, wrapped, and saturated math functions](https://doc.rust-lang.org/std/primitive.u32.html).

>Note: There are some known issues regarding functionality of compiler level overflow checks and the resulting size of the Wasm blob. This feature may change or be iterated on in the future.

### What is the difference between memory and storage?

In ink!, memory refers to computer memory, while storage refers to the on-chain storage
used by a contract instance. Memory is temporary and only lasts until the contract
execution is done, while storage is persistent and lasts over many contract executions.
The contract storage is built on top of the runtime storage, and access is considered to be slow.