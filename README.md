# iCTF Challenges

Historical and current challenges from the [iCTF](https://ictf.cs.ucsb.edu/) competition,
organized by the UCSB Security Lab. This repository covers editions from 2003 to 2026.

All challenges follow the [CTFd](https://ctfd.io/) challenge format and are compatible
with [pwn.college](https://pwn.college/) / DOJO.

## Structure

Each challenge lives in `challenges/<edition>-<service>/`:

```
challenges/
├── ictf03-servlet/       # iCTF 2003 — Windows Goes Open-Source
│   ├── challenge.yml     # CTFd metadata
│   ├── Dockerfile        # (if available)
│   ├── flag/flag         # ictf{...}
│   ├── ro/               # read-only container files
│   ├── rw/               # writable container files
│   ├── src/              # service source code
│   ├── writeup/          # vulnerability description + exploit
│   └── scripts/          # build/run/stop helpers (if Dockerfile present)
...
```

See [FORMAT.md](FORMAT.md) for the full specification.

## Editions

| Prefix   | Year | Edition | Theme |
|----------|------|---------|-------|
| ictf03   | 2003 | iCTF 3  | Windows Goes Open-Source |
| ictf04   | 2004 | iCTF 4  | UN Vote |
| ictf04r  | 2005 | iCTF 4 rematch | Bass Tard Corp |
| ictf05   | 2005 | iCTF 5  | Spam Museum |
| ictf06   | 2006 | iCTF 6  | Hillbilly Bank |
| ictf07   | 2007 | iCTF 7  | Copyright Mafia |
| ictf08   | 2008 | iCTF 8  | "24" (nuclear bomb) |
| ictf09   | 2009 | iCTF 9  | Rise of the Botnet |
| ictf10   | 2010 | iCTF 10 | Hit 'em Where it Hurts |
| ictf11   | 2011 | iCTF 11 | Money Laundering |
| ictf13   | 2013 | iCTF 13 | Nuke 'em |
| ictf15   | 2015 | iCTF 15 | Crowdsourcing Evil |
| ictf20   | 2020 | iCTF 20 | Abbey Road |
| ictf23u  | 2023 | iCTF 23 undergrad | AI and Cybersecurity |
| ictf23h  | 2023 | iCTF 23 high school | AI and Cybersecurity |
| ictf24u  | 2024 | iCTF 24 undergrad | iCTF 2024 |
| ictf24h  | 2024 | iCTF 24 high school | iCTF 2024 |
| ictf26   | 2026 | iCTF 26 normal | AI Agents and Cybersecurity |
| ictf26a  | 2026 | iCTF 26 agentish | AI Agents and Cybersecurity |

## Running a challenge

For challenges with a Dockerfile, from the challenge directory:

```bash
./scripts/build.sh   # build the Docker image
./scripts/run.sh &   # start the service
# ... interact with it ...
./scripts/stop.sh    # stop the service
```

## Archive

The raw historical archive, including VM images, network captures, scorebot scripts, and
encrypted source archives, is at
[shellphish/ictf-archive](https://github.com/shellphish/ictf-archive).
