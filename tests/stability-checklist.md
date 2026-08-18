# Stability test plan

- [ ] Cold start
- [ ] Open 10 tabs
- [ ] Switch tabs repeatedly
- [ ] Background for 5 minutes
- [ ] Return from background
- [ ] Reload heavy page
- [ ] Network disconnect/reconnect
- [ ] Enable/disable filters
- [ ] Change regional profile
- [ ] Translation flow
- [ ] Script allowlist
- [ ] Rotate activity
- [ ] Low-memory recovery
- [ ] GPU rendering smoke test
- [ ] Crash/ANR log review

Goal: no forced crashes, no intentional force-close behavior, and no known
infinite background work. CI should fail when instrumentation tests fail.
