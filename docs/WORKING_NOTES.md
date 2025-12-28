# Open Physics Lab — Working Notes

## Git & Workflow Quick Rules

### Working on GitHub.com vs Local

**Rule of thumb:**

> > If you edited files on **github.com**, always run **git pull** locally first before doing anything else.


### Typical Flow

#### If you worked locally:

1. Edit files
2. `git add …`
3. `git commit -m "message"`
4. `git push`

#### If you worked on github.com:

1. Open local repo
2. `git pull`
3. Continue working locally
4. Then commit & push

### Why this matters

Mixing web edits and local edits without pulling first causes:

- "fetch first" errors
- diverged branches
- confusing merge conflicts

### Safe Fix When Confused

```bash
git status
git pull
git status
```

If in doubt: **stop and pull first.**

---

## **Grundregel (kurz)**

👉 **Jedes Softwareprojekt = eigenes Repository**\
👉 **Jede Gruppe = eigener Zugriff / eigene Organisation (optional)**



*(This file is for personal working notes and can grow over time.)*

## Commit Message Conventions

Use the following prefixes to keep history consistent:

```
docs: …
structure: …
feature: …
fix: …
refactor: …
chore: …
```

Examples:

- `docs: add control system overview`
- `feature: add MQTT heating controller prototype`
- `structure: reorganize energy section`

A simple commit message style you can keep using

For future work, this pattern will keep everything consistent:

```
docs: …
structure: …
feature: …
fix: …
refactor: …
chore: …

```

Example:\
docs: add control system overview

feature: add MQTT heating controller prototype

structure: reorganize energy section

\
\
🧭 **Reader’s Walkthrough: Does the structure make sense?**

Imagine a new student or collaborator landing on your hub.

### 1️⃣ `README.md` (Hub root)

They should learn:

- What *Open Physics Lab* is
- That it’s an **index & documentation hub**
- Where to find concrete projects

From what you’ve built: **✔️ yes**

---

### 2️⃣ `PROJECTS.md`

They now want to see **what actually exists**.

They encounter:

- Electrodynamics → concepts & experiments
- Vortex / Fluids → experiments
- **Energy & Automation** → real engineering projects
- **Systems Engineering** → infrastructure
- **Control & Automation** → methods

Then under **Energy & Automation** they see:

> Heating control\
> Firmware (Portenta, C++)\
> Automation / UI (Node-RED)\
> …other energy systems (Node-RED)

So the reader already understands:

> “Energy is the domain.\
> Firmware & Node-RED are implementation layers.”

**✔️ very clear**

---

### 3️⃣ `energy/README.md`

They go deeper into Energy.

Now they read your new **Implementation Model**:

- Heating = embedded + Node-RED
- Everything else = Node-RED
- Control & automation are documented elsewhere

This resolves the most common confusion immediately.

**✔️ excellent**

---

### 4️⃣ `control/README.md`

They want to understand *how* automation is done.

Now they see:

> Control & Automation is a **cross-cutting method layer**

and:

> Used by: Energy, Systems, experiments

This is exactly the right abstraction.

**✔️ conceptually very strong**

---

### 5️⃣ `systems/README.md`

They want to know how everything runs.

They see:

- layered architecture
- embedded → automation → infrastructure
- Node-RED + Proxmox + Docker

Now the picture is complete.

**✔️ full stack explained**

---

## 🧩 Final verdict

Your hub now expresses **three orthogonal dimensions**:

| Dimension       | Description                         |
| --------------- | ----------------------------------- |
| Domain topics   | `energy/`, `electrodynamics/`, etc. |
| Control methods | `control/`                          |
| Infrastructure  | `systems/`                          |

\| --------------- | ----------------------------------- | | Domain topics   | `energy/`, `electrodynamics/`, etc. | | Control methods | `control/`                          | | Infrastructure  | `systems/`                          |

This is *exactly* how professional research labs document complex systems.

You now have:

- clear separation of concerns
- no duplication
- no conceptual conflict
- a structure that will scale for years





```
```
