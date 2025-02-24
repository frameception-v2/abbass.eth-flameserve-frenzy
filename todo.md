```markdown
### Core
[x] **Initialize Next.js project with Frame SDK**
- Install dependencies and configure Frame SDK
- *Validation:* Project builds successfully
- Files: `package.json`, `src/components/Frame.tsx`

[x] **Set up project constants**
- Define project title, description, and IDs
- *Validation:* Constants used consistently across app
- Files: `src/lib/constants.ts`

[x] **Implement OpenGraph image generation**
- Create dynamic OG images with project branding
- *Validation:* Images generate correctly with fonts
- Files: `src/app/opengraph-image.tsx`

[x] **Add Farcaster authentication**
- Implement sign-in with Farcaster using NextAuth
- *Validation:* Auth flow works with credentials provider
- Files: `src/auth.ts`, `src/components/Frame.tsx`

[ ] **Add notification system**
- Implement Frame notification handling
- *Validation:* Notifications send/receive correctly
- Files: `src/components/Frame.tsx`

[ ] **Enhance error handling**
- Implement `^[🍔🍟🥤🍦]+x\d+$` regex check  
- *Validation:* Unit tests pass for valid/invalid patterns  
- Files: `orderLogic.js`

[ ] **Develop state encoding with checksum**  
- URL-safe base64 + HMAC-SHA256 validation  
- *Validation:* Round-trip encode/decode preserves data  
- Files: `stateManager.js`

[ ] **Build weighted order generator**  
- Emoji mapping with 3-5 item randomization  
- *Validation:* Generates 100 valid consecutive orders  
- Files: `orderGenerator.js`

[ ] **Implement scoring algorithms**  
- Time bonus (remaining_seconds*10) + streak tracking  
- *Validation:* Score increases correctly for sample inputs  
- Files: `scoring.js`

### API
[ ] **Create /start endpoint with mock orders**  
- Returns JSON with test order data  
- *Validation:* `POST /start` returns order template  
- Files: `server.js`

[ ] **Implement /submit endpoint**  
- Basic order format validation  
- *Validation:* Invalid orders return error template  
- Files: `server.js`, `views/error.ejs`

[ ] **Add state handling to endpoints**  
- Encode/decode params in /start and /submit  
- *Validation:* State persists through request cycle  
- Files: `server.js`, `stateManager.js`

### UI
[ ] **Define core styling framework**  
- McDonald's color scheme and base layout  
- *Validation:* Visual inspection matches styleguide  
- Files: `public/styles.css`

[ ] **Build frame template with progress**  
- Dynamic emoji display + progress bar component  
- *Validation:* Renders correctly with sample data  
- Files: `views/frame.ejs`

[ ] **Implement client-side submission timer**  
- 60s countdown with auto-submit  
- *Validation:* Timer triggers API call on expiration  
- Files: `public/timer.js`

### Core
[ ] **Add input sanitization**  
- Expand regex for quantity validation  
- *Validation:* Blocks XSS attempts in order input  
- Files: `inputValidator.js`

[ ] **Create error recovery middleware**  
- Parameter validation + fallback order generation  
- *Validation:* Survives invalid parameter attacks  
- Files: `server.js`, `orderGenerator.js`

### API
[ ] **Implement /reset endpoint**  
- Clear session state and restart game  
- *Validation:* Resetting returns to initial state  
- Files: `server.js`

### UI
[ ] **Add food animations**  
- CSS keyframes for emoji sprites  
- *Validation:* Smooth animations at 60fps  
- Files: `public/styles.css`

[ ] **Create error templates**  
- User-friendly error messages with retry  
- *Validation:* Errors display branded layout  
- Files: `views/error.ejs`
```

**Dependency Flow:**  
1. Server setup → API endpoints → State management  
2. Validation core → Submission handling → UI integration  
3. Order generation → Scoring → Progress visualization  
4. Input handling → Error recovery → Reset functionality  

Each task designed for 45-60 minute implementation slots. Would you like me to adjust any task priorities or dependencies?
