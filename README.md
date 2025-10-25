# From CPU to the Browser
**The definitive low-level frontend engineering course**

Master every layer from bare metal to production React. Build browsers, engines, and frameworks from scratch.

---

## Week 0.5 – CPU & Memory Architecture

**Hardware fundamentals**
- CPU pipelines: fetch, decode, execute, writeback
- Register allocation and instruction scheduling
- Branch prediction and pipeline stalls
- Cache hierarchy: L1/L2/L3, cache lines, false sharing
- Memory addressing: virtual memory, MMU, TLB
- Stack vs heap allocation strategies

**Low-level execution**
- Assembly language basics (x86-64)
- System calls and kernel interaction
- How C/C++ compiles to machine code
- Memory layout: text, data, BSS, stack, heap
- Pointer arithmetic and memory alignment

**Project:** Write assembly that allocates memory and executes basic operations. Trace CPU pipeline execution for JS code using performance counters.

---

## Week 1 – Networking from Scratch

**Socket programming**
- Raw sockets: IP packets, TCP segments, UDP datagrams
- Three-way handshake implementation
- Sliding window protocol and flow control
- Congestion control algorithms (TCP Reno, Cubic)
- Packet fragmentation and reassembly

**Protocol implementation**
- HTTP/1.1 parser: chunked encoding, headers, keep-alive
- HTTP/2: binary framing, multiplexing, HPACK compression
- TLS handshake: cipher suites, certificate verification, key exchange
- WebSocket upgrade and frame masking

**Network debugging**
- tcpdump and Wireshark packet analysis
- strace for system call tracing
- Network simulation: latency, jitter, packet loss

**Project:** HTTP/1.1 and HTTP/2 server in C or Rust. Profile every syscall and packet. Build WebSocket chat with custom protocol.

---

## Weeks 2-3 – Browser Engine Implementation

**HTML parsing**
- Tokenization state machine (13 states, 67 transitions)
- Tree construction algorithm
- Error recovery and quirks mode
- Parser-blocking scripts and async/defer

**CSS engine**
- Tokenizer and parser (grammar implementation)
- Selector matching with specificity calculation
- Cascade resolution algorithm
- Style computation and inheritance
- Media query evaluation

**Layout engine**
- Box model calculation
- Normal flow, floats, positioning schemes
- Flexbox algorithm: main/cross axis, flex basis, grow, shrink
- Grid algorithm: track sizing, placement, spanning
- Line breaking and text shaping

**Paint and composite**
- Layer tree construction
- Paint recording and display lists
- Rasterization strategies
- GPU compositing and texture management

**Project:** Build a browser engine in C++ or Rust that renders Wikipedia. Handle fonts, images, CSS animations. Measure every phase: parse, style, layout, paint, composite.

---

## Weeks 4-5 – JavaScript Engine

**Parsing and AST**
- Lexical analysis and tokenization
- Recursive descent parser
- AST construction and validation
- Scope analysis and symbol resolution

**Interpreter implementation**
- Bytecode design and instruction set
- Stack-based VM execution
- Closure implementation with environment chains
- Prototype chain traversal
- Property lookup optimization (inline caches)

**Memory management**
- Mark-and-sweep garbage collection
- Generational collection (young/old generations)
- Incremental and concurrent GC
- WeakMap and WeakSet implementation
- Memory profiling and leak detection

**Event loop mechanics**
- Microtask queue (Promise.then)
- Macrotask queue (setTimeout, I/O)
- Animation frame callbacks
- Idle callbacks and scheduling
- Task prioritization

**Optional: JIT compilation**
- Inline caching and polymorphic inline caching
- Type feedback and speculative optimization
- Deoptimization and bailout mechanisms
- Register allocation

**Project:** JS engine executing real programs. Implement closures, prototypes, async/await, event loop. Profile GC pauses and optimize hot paths. Connect to DOM for interactive apps.

---

## Week 6 – Virtual DOM & Reconciliation

**Diffing algorithms**
- Tree diffing complexity analysis (O(n³) → O(n))
- Key-based reconciliation
- Heuristics: component type, element type, lists
- Fiber architecture preparation

**Batching and scheduling**
- Requestanimationframe-based updates
- Double buffering for UI consistency
- Priority queues for updates
- Time slicing for interruptibility

**Repaint/reflow optimization**
- Layout thrashing detection
- Read/write batching (FastDOM pattern)
- CSS containment and layer creation
- Composite-only animations

**Project:** Virtual DOM library with optimized reconciliation. Stress test with 10,000+ dynamic nodes. Profile layout/paint timings.

---

## Week 7 – React/Next.js Internals

**Fiber reconciler**
- Work loop and unit of work
- Reconciliation phases: render and commit
- Effect list construction
- Priority levels and lane model

**Hooks implementation**
- Hooks queue and cursor
- useEffect cleanup and dependency checking
- useRef mutable container
- useCallback/useMemo memoization
- Custom hook composition

**Concurrent features**
- Time slicing and work interruption
- Suspense and lazy loading
- useTransition and useDeferredValue
- Automatic batching

**Server-side rendering**
- renderToString vs renderToPipeableStream
- Progressive hydration and selective hydration
- Double pass problem and solutions
- Edge rendering vs Node rendering

**Next.js architecture**
- File-based routing implementation
- SSG: getStaticProps build-time execution
- ISR: revalidation and stale-while-revalidate
- API routes and middleware
- Module bundling and code splitting

**Project:** Clone React's core reconciler with Fiber and hooks. Build SSR framework with streaming and hydration. Implement file-based routing.

---

## Week 8 – Performance Engineering

**Profiling tools**
- Chrome DevTools: Performance tab deep dive
- React DevTools Profiler
- Lighthouse metrics: FCP, LCP, TTI, CLS, FID
- Custom performance marks and measures
- Heap snapshots and allocation timelines

**Optimization techniques**
- Component memoization strategies
- Virtualized lists and windowing
- Image optimization: formats, lazy loading, responsive images
- Font optimization: subsetting, preloading, display strategies
- Bundle analysis and tree shaking
- Code splitting strategies: route-based, component-based

**Critical rendering path**
- Eliminate render-blocking resources
- Minimize critical CSS
- Defer non-critical JavaScript
- Preload/prefetch/preconnect strategies

**Project:** Optimize real-world app from 3s to <1s LCP. Document every optimization with before/after metrics. Handle 60fps animations with heavy DOM updates.

---

## Week 9 – Engine Modification & Debugging

**JavaScript engine hacking**
- Build V8 from source with custom patches
- Add custom bytecode instructions
- Instrument GC for detailed metrics
- Profile JIT compilation decisions

**Browser engine debugging**
- Build Chromium/WebKit from source
- Add custom tracing to layout engine
- Modify rendering pipeline for instrumentation
- Debug compositor thread interactions

**WebAssembly integration**
- Compile C/C++/Rust to WASM
- Linear memory management
- JS ↔ WASM interop optimization
- SIMD and threads

**Project:** Add custom profiling to browser engine. Build WASM module for computationally intensive task (image processing, physics simulation). Optimize JS/WASM boundary.

---

## Week 10 – Hardware Simulation & Constraints

**Embedded systems**
- Run minimal browser on microcontroller simulation
- Memory-constrained rendering (64KB RAM)
- CPU-constrained JavaScript (10MHz)
- Display optimization for small screens

**Stress testing**
- Memory pressure simulation
- CPU throttling
- Network constraint testing (2G, 3G)
- GPU bottleneck analysis

**Project:** Port mini-browser to embedded environment. Optimize for extreme constraints. Document performance characteristics.

---

## Weeks 11-12 – Capstone Project

**Build a complete system:**

1. Custom browser engine with HTML/CSS/JS support
2. React-like framework with Fiber and concurrent features
3. SSR framework with streaming and hydration
4. Production-optimized Next.js application
5. Full performance profiling suite
6. WebAssembly acceleration for critical paths
7. Hardware constraint testing and optimization

**Requirements:**
- Render complex UIs at 60fps
- Handle 10,000+ concurrent DOM updates
- Sub-second initial page load
- Progressive enhancement and graceful degradation
- Comprehensive error handling and edge cases
- Full performance documentation

**Deliverable:** Production-ready system with complete understanding of every layer from CPU to pixels.

---

## Prerequisites

- Strong C/C++ or Rust
- Assembly language basics
- Computer architecture knowledge
- Operating systems fundamentals
- Data structures and algorithms mastery

## Outcome

You will understand and have built:
- CPU execution and memory management
- Network protocols and servers
- Browser engines (parsing, layout, paint, composite)
- JavaScript engines (parser, interpreter, GC, event loop)
- Virtual DOM and reconciliation
- React internals and concurrent rendering
- SSR and hydration systems
- Performance profiling and optimization

You'll debug and optimize at every level of the stack with complete confidence.
