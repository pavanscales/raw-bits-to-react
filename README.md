# From First Principles to the Web Browser
**A 12-Week Frontend Engineering Curriculum**

This course takes you from hardware and browser fundamentals to advanced frontend engineering with React/Next.js, performance optimization, and deep debugging skills. Every week builds on first principles with hands-on projects.

---

## Course Outline

### Week 0.5 – Layer 0: Hardware & Browser Fundamentals
- CPU: pipelines, registers, instruction execution, stalls
- Memory hierarchy: cache, RAM, stack/heap
- How JS and DOM translate to pixels
- Optional: minimal CPU simulation to run JS & DOM
- **Exercise:** Trace JS execution and memory usage at CPU level

### Week 1 – Layer 1: Networking & Data Flow
- TCP/IP & HTTP implementation from scratch
- TLS/HTTPS handshake
- WebSocket client/server
- Simulate latency, packet loss, congestion
- Debug raw network packets
- **Exercise:** Build minimal HTTP server/client, profile network impact on UI

### Weeks 2-3 – Layer 2: Browser Engine Core
- HTML parser → DOM tree (handle quirks & edge cases)
- CSS parser → cascade, specificity, inheritance, media queries
- Layout engine: box model, flex, grid, floats, positioning
- Paint engine: pixels, text metrics, font rendering, colors
- Rendering pipeline optimization & debugging
- **Project:** Render static HTML/CSS in terminal or canvas

### Weeks 4-5 – Layer 3: JavaScript Engine
- Interpreter: expressions, loops, closures, prototypes
- Call stack, scope chain, microtask/macrotask queues
- Memory management & garbage collection
- Connect JS execution to DOM & layout
- Optional: mini JIT for performance
- **Project:** Interactive mini-browser executing JS apps

### Week 6 – Layer 4: Virtual DOM & Reactive Systems
- Component system: state, props, lifecycle
- Manual diffing & reconciliation
- Repaint/reflow optimization
- Event binding & async handling
- Stress-test: heavy DOM updates & animations
- **Project:** Reactive UI without frameworks

### Week 7 – Layer 5: Framework Principles
- React internals: JSX → React.createElement
- Fiber architecture & concurrent rendering
- Hooks: useState, useEffect, useRef
- SSR, SSG, ISR, routing, data fetching lifecycles
- Hydration, lazy loading, dynamic imports
- **Project:** Replicate mini-React framework + SSR/CSR pipeline

### Week 8 – Layer 6: Frontend Performance
- CPU/memory profiling, repaint/reflow timings
- Virtual DOM diff optimization
- Lazy loading, caching, incremental rendering
- Network-aware performance optimization
- **Project:** Benchmark & optimize React/Next.js app under high load

### Week 9 – Layer 7: Engine Debugging & Extension
- Modify JS or browser engine
- Debug DOM updates, event loops, rendering pipeline
- Integrate WebAssembly for performance-critical features
- Simulate bottlenecks and edge cases
- **Project:** Optimize bottlenecked React/Next.js app

### Weeks 10-10.5 – Layer 8: Optional Hardware / Stress Testing
- Run JS & DOM on microcontroller/FPGA simulation
- Stress-test CPU/memory limits
- Debug rendering and UI under extreme conditions
- **Project:** Benchmark browser rendering on simulated hardware

### Weeks 11-12 – Capstone Projects
- Build a complete frontend system:
  - SSR + hydration + concurrent rendering
  - Advanced React patterns + hooks + Suspense
  - Profiling, network-aware, edge-case handling
  - Stress-test animations, DOM updates, layout recalculations
- Optional: WebAssembly modules for performance
- Optional: Hardware limit simulation
