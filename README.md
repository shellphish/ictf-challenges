# iCTF Challenges

Historical and current challenges from the [iCTF](https://ictf.cs.ucsb.edu/) competition,
founded by Giovanni Vigna at UC Santa Barbara in 2001 and organized by
[Shellphish](https://shellphish.net) since 2005. This repository covers editions from 2001 to 2026.

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
| ictf01   | 2001 | iCTF 1  | Red Team / Blue Team |
| ictf02   | 2002 | iCTF 2  | Treasure Hunt in Cyberspace |
| ictf03   | 2003 | iCTF 3  | Windows Goes Open-Source |
| ictf04   | 2004 | iCTF 4  | The 2004 United Nations Vote |
| ictf04r  | 2005 | iCTF 4 rematch | The Bass Tard Corporation |
| ictf05   | 2005 | iCTF 5  | The Spam Museum |
| ictf06   | 2006 | iCTF 6  | The Hillbilly Bank |
| ictf07   | 2007 | iCTF 7  | The Copyright Mafia |
| ictf08   | 2008 | iCTF 8  | "24" (nuclear bomb) |
| ictf09   | 2009 | iCTF 9  | Rise of the Botnet |
| ictf10   | 2010 | iCTF 10 | Hit 'em Where it Hurts |
| ictf11   | 2011 | iCTF 11 | Money Laundering |
| ictf12   | 2013 | iCTF 12 | SCADA Breakdown |
| ictf13   | 2013 | iCTF 13 | Nuke 'em |
| ictf14   | 2015 | iCTF 14 | Large-scale Hacking |
| ictf15   | 2015 | iCTF 15 | Crowdsourcing Evil |
| ictf16   | 2017 | iCTF 16 | Shell We Play a Game? |
| ictf19   | 2019 | iCTF 19 | The Grey Hat Nation |
| ictf20   | 2020 | iCTF 20 | Abbey Road |
| ictf23u  | 2023 | iCTF 23 undergrad | AI and Cybersecurity |
| ictf23h  | 2023 | iCTF 23 high school | AI and Cybersecurity |
| ictf24u  | 2024 | iCTF 24 undergrad | iCTF 2024 |
| ictf24h  | 2024 | iCTF 24 high school | iCTF 2024 |
| ictf26   | 2026 | iCTF 26 | AI Agents and Cybersecurity (normal + agentish tracks) |

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
