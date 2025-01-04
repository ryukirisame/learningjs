
# Polling

**Polling** is a technique used in computing to repeatedly check the status of a resource, event, or condition at regular intervals until a desired state is achieved. It’s commonly used in scenarios where continuous monitoring of a task or data source is required.

### How Polling Works:
- A program sends periodic requests to check if a condition is met (e.g., if data is available or a process is complete).  
- If the condition isn't met, the program waits and checks again after a set interval.  
- This cycle continues until the condition is satisfied.

---

### Examples of Polling:
1. **Frontend Polling (Web Development)**:
   A frontend app repeatedly sends HTTP requests to the backend to check for updates.
   ```typescript
   setInterval(async () => {
     const response = await fetch('/api/status');
     const data = await response.json();
     console.log(data);
   }, 5000); // Poll every 5 seconds
   ```

2. **Hardware Polling**:  
   The CPU repeatedly checks hardware devices (like a keyboard or mouse) to see if they need attention.

3. **File Watching**:  
   A program polls the filesystem to check if a file has been created, modified, or deleted.

---

### Types of Polling:
1. **Long Polling**:  
   The client sends a request, and the server holds the connection open until new data is available. It reduces unnecessary checks but can tie up server resources.  
   ```typescript
   async function longPoll() {
     const response = await fetch('/api/events');
     const data = await response.json();
     console.log(data);
     longPoll(); // Restart after receiving data
   }
   longPoll();
   ```

2. **Short Polling**:  
   The client sends frequent, simple requests at short intervals. This is easier to implement but can cause higher load on the server.

3. **Efficient Polling (Exponential Backoff)**:  
   The polling interval increases over time if no updates are detected, reducing server load while still keeping the client updated.  
   ```typescript
   let interval = 1000; // Start with 1 second
   async function pollWithBackoff() {
     const response = await fetch('/api/status');
     const data = await response.json();
     console.log(data);
     interval = data.update ? 1000 : interval * 2; // Reset or increase interval
     setTimeout(pollWithBackoff, interval);
   }
   pollWithBackoff();
   ```

---

### Polling vs. Other Techniques:
- **Polling** – Simple but potentially inefficient (wastes resources during idle periods).  
- **WebSockets** – Real-time, two-way communication (more efficient but complex).  
- **Event-Driven (Hooks/Callbacks)** – Server pushes updates when events occur (e.g., server-sent events).  

Polling is often used when WebSockets aren’t feasible or when updates are infrequent.
