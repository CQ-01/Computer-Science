```bash
Another git process seems to be running in this repository
```
- git process가 다른 곳에서 동작하고 있어서 안됨
- process를 강제종료 시키면 해결
  - `rm -f ./.git/index.lock`