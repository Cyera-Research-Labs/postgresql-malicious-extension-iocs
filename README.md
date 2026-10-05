# Malicious PostgreSQL Extension IOCs

IOCs for trojanized PostgreSQL extensions delivering XMRigCC across Windows and Linux, attributed to Tor2Mine.

All indicators are in [`iocs.md`](iocs.md). Last verified 2026-09-27.

## Contents

| Section | Description |
|-------|-------------|
| `gc_manager Campaign` | The PostgreSQL extension chain: C2 domains and IPs, 16 Windows `gc_manager.dll` and 4 Linux `gcmanager-1.so` extension samples, embedded Stage 2 downloaders, XMRigCC payloads, and mining pools |
| `patch.exe Campaign` | A parallel operation by the same actor using a different initial access vector against the same C2 infrastructure, dropping the AZORult stealer |
