# 🗳️ All-Hands Vote — Monthly Runbook

## Every Month: 2 URLs, Zero Code Changes

### Step 1 — Reset votes before the meeting
Open this once right before the all-hands. Green toast confirms it worked.
```
https://cyrusmansoor.github.io/cyrus/vote.html?reset=spark-reset
```

### Step 2 — Open the session URL during the meeting
Swap the month. Project this on screen. QR code auto-updates to match.
Attendees scan it and land on the right session (fresh vote lock each month).

```
https://cyrusmansoor.github.io/cyrus/vote.html?session=apr-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=may-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=jun-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=jul-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=aug-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=sep-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=oct-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=nov-2026
https://cyrusmansoor.github.io/cyrus/vote.html?session=dec-2026
```

---

## How It All Works

| Thing | How |
|---|---|
| **Vote lock** | Tied to `?session=`. New month = new session = everyone can vote again. |
| **QR code** | Auto-generates from whatever URL you have open. No manual updates ever. |
| **Real-time sync** | Firebase updates all browsers live. |
| **Reset** | `?reset=spark-reset` wipes Firebase vote counts. No session needed. |

---

## Quick Copy — April 2026 (this Thursday!)

Reset:
```
https://cyrusmansoor.github.io/cyrus/vote.html?reset=spark-reset
```
Live voting page:
```
https://cyrusmansoor.github.io/cyrus/vote.html?session=apr-2026
```

---

## One-Time Security Setup (if not done yet)

Restrict your Firebase API key to your domain so it can't be used anywhere else:

1. Go to **https://console.cloud.google.com**
2. Select your Firebase project from the top dropdown
3. **APIs & Services → Credentials**
4. Click your **Browser API key**
5. Under **Application restrictions** → select **HTTP referrers (websites)**
6. Add: `https://cyrusmansoor.github.io/*`
7. Click **Save**
