# Implementation Plan Breakdown

### Step 1: Set Up Base Express Server Structure
```text
1. Create foundational Node.js server with Farcaster Frame support
2. Implement basic routing and parameter handling
```
- `server.js`: Initialize Express with JSON/URL encoding
- Install dependencies: `express`, `crypto`
- Create POST `/start` endpoint with mock order generation

### Step 2: Implement Order Validation Core
```text
1. Create order verification system
2. Set up submission endpoint structure
```
- `orderLogic.js`: Add validation regex (`^[🍔🍟🥤🍦]+x\d+$`)
- Create POST `/submit` endpoint with basic correctness check
- Add error response templates in `views/error.ejs`

### Step 3: URL Parameter State Management
```text
1. Develop state encoding/decoding system
2. Implement parameter checksum validation
```
- `stateManager.js`: Create encode/decode functions with URL-safe base64
- Add checksum generation using HMAC-SHA256
- Update `/start` and `/submit` to handle encoded parameters

### Step 4: Dynamic Order Generation System
```text
1. Implement item randomization logic
2. Add token expiration tracking
```
- `orderGenerator.js`: Create weighted item pool with emoji mapping
- Add generation logic for 3-5 random items
- Implement timestamp validation in order tokens

### Step 5: Score Calculation Module
```text
1. Develop scoring algorithms
2. Create level progression system
```
- `scoring.js`: Add time bonus calculation (remaining_seconds * 10)
- Implement streak counter in frame state
- Add level-up check (every 3 correct orders)

### Step 6: Frame UI Components
```text
1. Build core visual elements
2. Implement responsive layout system
```
- `public/styles.css`: Define McDonald's color scheme (#FF0000, #FFC72C)
- Create `views/frame.ejs` with animated emoji sprites
- Add progress bar component with level tracking

### Step 7: Input Handling System
```text
1. Implement text input sanitization
2. Add timeout auto-submit functionality
```
- `inputValidator.js`: Expand regex for quantity validation
- Add client-side timer in `public/timer.js`
- Create partial credit calculation for timed-out submissions

### Step 8: Error Recovery Mechanisms
```text
1. Implement state fallback system
2. Add user-facing reset controls
```
- Create session reset endpoint (`POST /reset`)
- Add parameter validation middleware in `server.js`
- Implement default order fallback in `orderGenerator.js`

### Step 9: Animation Subsystem
```text
1. Add food sprite animations
2. Implement progress transitions
```
- Enhance `styles.css` with keyframe animations
- Create plate stacking effect using CSS transforms
- Add smooth progress bar transitions

### Step 10: Final Integration Testing
```text
1. Validate full game flow
2. Implement stress testing
```
- Create end-to-end test suite in `test/gameTest.js`
- Add load testing with Artillery
- Implement chaos testing for state recovery

Each step builds on previous implementations while maintaining the 2-4 file change constraint. Would you like me to elaborate on any particular phase?