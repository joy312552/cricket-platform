# Cricket platform: build progress

## Done
- [x] Pure TypeScript scoring engine (`src/engine/engine.ts`): extras, free hit, wickets and bowler credit, strike rules, over end, maidens, milestones, hat-trick, innings end, targets, results, penalties, retire.
- [x] Command log is the source of truth. Undo and edit rebuild state from the log and emit no celebration events.
- [x] 30 passing tests including a randomized invariant test (`npm run test:engine`, Node 22+).

## Not started (needs a machine with npm access)
- [ ] Next.js app, Supabase schema/RLS/migrations, auth, dashboard
- [ ] Realtime, overlay tokens, ARENA/PULSE themes, broadcast control room, public pages
- [ ] Playwright e2e, Vercel deployment (nothing deployed)

## Engine notes
- Event `seq` is assigned by the database transaction, not the engine.
- Out-batter for a run out is named relative to ends at delivery start; `runsBat` = runs completed.
- Not yet modelled: powerplay stats, super over orchestration, DLS, mid-over injury maiden edge cases, Test-match multi-innings.
