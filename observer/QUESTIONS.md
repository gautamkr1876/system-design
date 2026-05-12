# Observer Pattern in JavaScript — Question Bank

## Mental Model

**Observer = YouTube channel.** The **subject** is the channel; it keeps the list of subscribers itself. When it uploads (state change), it pings every subscriber on the list directly — no middleman. Subscribers can hit `unsubscribe` (`.off` / `removeEventListener`) anytime. This is exactly what `addEventListener` does in the browser.

**Why it's not Pub/Sub:** in Pub/Sub, a broker (event bus) sits between publisher and subscriber, and neither knows the other exists. In Observer, the subject *owns* the subscriber list — direct, usually synchronous communication.

---

## 1. Conceptual *(tests: definition, mental model, when to use)*

1. What is the Observer pattern? Name the two roles.
2. What problem does it solve? Why not just call methods directly?
3. Observer vs Pub/Sub vs Mediator — what's the difference in one sentence each?
4. Is Observer push-based or pull-based? Can it be both?
5. Where does the Observer pattern show up natively in the browser and in Node?

## 2. Implementation *(tests: code from memory)*

6. Implement `Subject` with `subscribe`, `unsubscribe`, `notify`. The unsubscribe function should be returned from `subscribe`.
7. Build a tiny `EventEmitter` with `on`, `off`, `once`, `emit`. (FAANG favorite.)
8. Convert your `EventEmitter` to support wildcards or namespaces (`user:*`).
9. Implement Observer in TypeScript with generics so observers are typed to a payload shape.
10. Implement a `Signal` / `Observable` primitive (Solid/Preact-style) using the Observer pattern under the hood.

## 3. Tricky / Gotchas *(tests: senior-level edge cases)*

11. **Dangling subscriptions / memory leaks** — what causes them and how do you prevent them?
12. What happens if an observer throws inside `notify`? Should one bad observer break the rest?
13. What happens if an observer subscribes or unsubscribes *during* a notification loop? How do you handle "mutation during iteration"?
14. Subjects can become a re-entrancy nightmare — observer A's callback triggers another emit, which calls A again. How do you guard?
15. Sync vs async notify — which is the default? When would you debounce or microtask the notify?
16. Why are `WeakRef`/`WeakMap` sometimes used in observer implementations? What's the trade-off?
17. Identity gotcha: why does `subject.off(() => {...})` never work?

## 4. Real-World Scenarios *(tests: applied design)*

18. Design a state store (mini Redux/Zustand) using Observer. Where does `useSyncExternalStore` plug in?
19. Build a typed cross-component event bus for a React app — Observer or Pub/Sub? Why?
20. Implement a `ResizeObserver`-style wrapper that batches notifications into one `requestAnimationFrame`.
21. Design an autosave system: editor (subject) notifies network-save observer + local-storage observer + UI-status observer. How do you handle failures in one observer without blocking others?
22. Real-time stock ticker — Observer for the UI layer, WebSocket below. Sketch the data flow.

## 5. Follow-ups *(what they ask after your first answer)*

23. "Now make it async." How does the pattern change?
24. "Now scale to 10,000 observers." What breaks first?
25. "How do you test a subject?"
26. "How would you add priorities so some observers are notified first?"
27. "Could RxJS replace this? When would you NOT reach for RxJS?"

## 6. Anti-patterns *(tests: judgment)*

28. Why is making *every* DOM event into an app-wide observer a bad idea?
29. Why is hand-rolling an EventEmitter inside React usually wrong — what should you reach for instead?
30. Why can Observer become an anti-pattern when subjects observe other subjects (chains)?
