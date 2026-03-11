<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>StableTrack — Marketing Command Center</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.2/babel.min.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,500;9..144,700&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html, body { background: #FDFBF7; font-family: 'Manrope', sans-serif; color: #2A1A0E; }
  input[type=number]:focus, textarea:focus { border-color: #C6761E !important; outline: none; }
  input[type=number] {
    font-family: 'Manrope', sans-serif; font-size: 13px;
    border: 1.5px solid rgba(126,74,23,0.14); border-radius: 7px;
    padding: 6px 10px; background: #F0E8DC; color: #2A1A0E;
    outline: none; width: 100%;
  }
  textarea {
    font-family: 'Manrope', sans-serif; font-size: 12px; line-height: 1.6;
    border: 1.5px solid rgba(126,74,23,0.14); border-radius: 8px;
    padding: 10px 14px; background: #F0E8DC; color: #2A1A0E;
    outline: none; resize: vertical; width: 100%;
  }
  table { width: 100%; border-collapse: collapse; }
  th {
    font-size: 9px; font-weight: 800; letter-spacing: 0.12em;
    text-transform: uppercase; color: #9B7B5A;
    padding: 8px 10px; border-bottom: 1.5px solid rgba(126,74,23,0.14);
    text-align: left;
  }
  td {
    font-size: 12px; padding: 9px 10px;
    border-bottom: 1px solid #F0E8DC; vertical-align: top;
  }
  tr:last-child td { border-bottom: none; }
  tr:hover td { background: #F0E8DC; }
  .g2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .g3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 14px; }
  .g4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; }
  @media (max-width: 900px) { .g4 { grid-template-columns: 1fr 1fr; } }
  @media (max-width: 640px) { .g3, .g2 { grid-template-columns: 1fr; } .g4 { grid-template-columns: 1fr 1fr; } }
</style>
</head>
<body>
<div id="root"></div>
<script type="text/babel">

const { useState } = React;

// ── DATA ──────────────────────────────────────────────────────────────────────
const HUBSPOT = {
  contacts: { total: 805, customers: 411, subscribers: 339, leads: 41 },
  deals: [
    { name: "Lauren Alderman",     pms: "ImproMed",    amount: 2400, requestedContact: true },
    { name: "Lu Ann Groves",       pms: "Antech",      amount: 2400, requestedContact: true },
    { name: "Rebecca Gervin",      pms: "Ezyvet",      amount: 2400, requestedContact: true },
    { name: "Kenneth Allison",     pms: "DVM Manager", amount: 2400, requestedContact: true },
    { name: "Leah Martin",         pms: "Shepherd",    amount: 2400, requestedContact: true },
    { name: "Lara Stephens-Brown", pms: "DSV",         amount: 2400, requestedContact: true },
    { name: "Michelle Clarke",     pms: "None",        amount: 2400, requestedContact: true },
    { name: "Teagan MacDonald",    pms: "None",        amount: 2400, requestedContact: true },
    { name: "Mallorie Humble",     pms: "HVMS",        amount: 2400, requestedContact: true },
    { name: "Maria Sequeira",      pms: "None",        amount: 2400, requestedContact: true },
    { name: "Natalia Cortes",      pms: "None",        amount: 2400, requestedContact: true },
    { name: "Amy Fitzgerald",      pms: "Ezyvet",      amount: 2400, requestedContact: true },
    { name: "Sara Wefel",          pms: "Vet View",    amount: 2400, requestedContact: true },
    { name: "Reagan Hart",         pms: "HVMS",        amount: 2400, requestedContact: true },
  ],
  sources: [
    { source: "AAEP Conference 2025",     count: 930, notes: "Full attendee list — 928 practising members" },
    { source: "AAEP Survey Respondents",  count: 49,  notes: "14 requested follow-up contact" },
    { source: "Salesforce / Keystone",    count: 425, notes: "Existing KS archiving customers" },
    { source: "StableTrack Users",        count: 43,  notes: "Active and past platform users" },
  ],
  stUsers: { active: 1, atRisk: 1, inactive: 41 },
};

const SEQUENCE_TEMPLATES = {
  reactivation: {
    name: "User Reactivation",
    audience: "Inactive StableTrack users — 41 contacts",
    goal: "Re-engage inactive users and move back to active",
    channel: "Email via HubSpot",
    emails: [
      { day: 1,  subject: "Still thinking about StableTrack?",           type: "Soft re-intro",   goal: "Re-open the door, acknowledge they haven't been active" },
      { day: 4,  subject: "What's changed since you last logged in",      type: "Product update",  goal: "Showcase improvements; reduce objection 'it wasn't ready'" },
      { day: 8,  subject: "How a practice like yours cut admin time by 40%", type: "Social proof", goal: "Peer proof from an active user champion (Aletha / Annie)" },
      { day: 14, subject: "Can I ask you something directly?",            type: "Feedback ask",    goal: "Personal ask: What stopped you? Gather insight and re-qualify" },
    ],
  },
  aaepSurvey: {
    name: "AAEP Survey Follow-Up",
    audience: "14 survey respondents who requested contact",
    goal: "Convert warm interest into a booked demo",
    channel: "Email + phone follow-up",
    emails: [
      { day: 1,  subject: "Great meeting you at AAEP — as promised",        type: "Warm intro",     goal: "Fulfil the promise made at the booth. Personalise by PMS." },
      { day: 3,  subject: "One question about your current workflow",        type: "Qualification",  goal: "Ask about biggest admin pain point to qualify deeper" },
      { day: 7,  subject: "15 minutes to show you something specific",       type: "Demo invite",    goal: "Demo ask — low-pressure, specific to their workflow" },
      { day: 12, subject: "Sharing something you might find useful",         type: "Value nurture",  goal: "Value drop — relevant guide, comparison, or case study" },
      { day: 18, subject: "Last note from me",                               type: "Breakup",        goal: "Final email. Clean close or last-chance response." },
    ],
  },
  aaepGeneral: {
    name: "AAEP Conference Nurture",
    audience: "All 930 AAEP Conference attendees (non-survey)",
    goal: "Top-of-funnel awareness; move to subscriber or MQL",
    channel: "Email via HubSpot",
    emails: [
      { day: 1,  subject: "For equine vets who still write notes in the truck", type: "Brand intro",   goal: "Brand awareness; speak to ambulatory vet identity" },
      { day: 6,  subject: "What 49 equine vets told us about their PMS",         type: "Insight email", goal: "AAEP survey data as content; builds credibility" },
      { day: 14, subject: "The equine practice management software guide",        type: "Lead magnet",  goal: "Deliver buyer's guide to qualify intent" },
      { day: 21, subject: "Is StableTrack right for your practice?",             type: "Self-qualify", goal: "Self-qualification. Soft CTA." },
      { day: 30, subject: "One more thing before we leave you be",               type: "Final value",  goal: "Final value email — product update or case study" },
    ],
  },
  keystoneXsell: {
    name: "Keystone Cross-Sell",
    audience: "425 Keystone customers in Salesforce — equine practices",
    goal: "Introduce StableTrack to existing KS customers",
    channel: "Email via HubSpot",
    emails: [
      { day: 1,  subject: "You already use Keystone — now meet StableTrack",      type: "Trust intro",       goal: "Leverage existing Asteris relationship and trust" },
      { day: 5,  subject: "How the two work together for equine practices",        type: "Integration story", goal: "Show the PACS + PMS integration story concretely" },
      { day: 10, subject: "What KS customers said after adding StableTrack",       type: "Social proof",      goal: "Proof from combined users: Aletha, Monadnock" },
      { day: 16, subject: "Add StableTrack to your Keystone plan",                 type: "Offer",             goal: "Direct offer — bundled pricing or trial. Clear CTA." },
    ],
  },
};

// ── COLOURS ───────────────────────────────────────────────────────────────────
const C = {
  amber:"#C6761E", brown:"#7E4A17", espresso:"#3E2723",
  cream:"#FDFBF7", creamDk:"#F0E8DC", border:"rgba(126,74,23,0.14)",
  muted:"#9B7B5A", text:"#2A1A0E",
  green:"#3D8B37", yellow:"#B07A00", red:"#C0392B", blue:"#2563EB",
};

const $m = n => "$" + new Intl.NumberFormat().format(n);
const $n = n => new Intl.NumberFormat().format(n);

// ── COMPONENTS ────────────────────────────────────────────────────────────────
function Card({ children, style={}, topAccent }) {
  return (
    <div style={{
      background:"#fff", border:`1.5px solid ${C.border}`, borderRadius:10,
      padding:"18px 22px", borderTop: topAccent ? `3px solid ${topAccent}` : undefined, ...style,
    }}>{children}</div>
  );
}

function Lbl({ children, style={} }) {
  return <div style={{
    fontFamily:"Manrope,sans-serif", fontSize:9, fontWeight:800,
    letterSpacing:"0.16em", textTransform:"uppercase", color:C.muted, marginBottom:10, ...style,
  }}>{children}</div>;
}

function Badge({ children, color=C.amber }) {
  return <span style={{
    display:"inline-block", fontFamily:"Manrope,sans-serif", fontSize:9,
    fontWeight:800, letterSpacing:"0.08em", textTransform:"uppercase",
    padding:"2px 8px", borderRadius:4, background:color+"1A", color,
  }}>{children}</span>;
}

function Stat({ val, label, sub, accent=C.amber }) {
  return (
    <div style={{
      background:"#fff", border:`1.5px solid ${C.border}`,
      borderLeft:`4px solid ${accent}`, borderRadius:10, padding:"16px 18px",
    }}>
      <div style={{fontFamily:"Fraunces,serif", fontSize:26, fontWeight:700, color:C.espresso, lineHeight:1}}>{val}</div>
      <div style={{fontFamily:"Manrope,sans-serif", fontSize:12, fontWeight:600, marginTop:5}}>{label}</div>
      {sub && <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginTop:2}}>{sub}</div>}
    </div>
  );
}

function Bar({ pct, color=C.amber, h=6 }) {
  return (
    <div style={{height:h, background:C.creamDk, borderRadius:3, overflow:"hidden"}}>
      <div style={{height:"100%", width:`${Math.min(100,pct)}%`, background:color, borderRadius:3, transition:"width 0.4s"}} />
    </div>
  );
}

function Notice({ children, color=C.red }) {
  return (
    <div style={{
      background:color+"0D", border:`1px solid ${color}22`, borderRadius:7,
      padding:"9px 13px", marginTop:10,
      fontFamily:"Manrope,sans-serif", fontSize:11.5, color:C.text, lineHeight:1.5,
    }}>{children}</div>
  );
}

function FieldInput({ label, value, onChange, prefix, suffix }) {
  return (
    <div>
      <div style={{fontFamily:"Manrope,sans-serif", fontSize:10, fontWeight:700, color:C.muted, letterSpacing:"0.1em", textTransform:"uppercase", marginBottom:4}}>{label}</div>
      <div style={{display:"flex", alignItems:"center", gap:5}}>
        {prefix && <span style={{fontFamily:"Manrope,sans-serif", fontSize:12, color:C.muted}}>{prefix}</span>}
        <input type="number" value={value} onChange={e => onChange(+e.target.value)} />
        {suffix && <span style={{fontFamily:"Manrope,sans-serif", fontSize:12, color:C.muted}}>{suffix}</span>}
      </div>
    </div>
  );
}

// ── SEQUENCE PLANNER ──────────────────────────────────────────────────────────
function SequencePlanner() {
  const [activeSeq, setActiveSeq] = useState("reactivation");
  const [extras, setExtras] = useState({});
  const [adding, setAdding] = useState(false);
  const [draft, setDraft] = useState({ day:"", subject:"", goal:"", type:"Custom" });
  const [notes, setNotes] = useState({});

  const seq = SEQUENCE_TEMPLATES[activeSeq];
  const all = [...seq.emails, ...(extras[activeSeq]||[])].sort((a,b)=>a.day-b.day);

  function addEmail() {
    if (!draft.day || !draft.subject) return;
    setExtras(p => ({ ...p, [activeSeq]: [...(p[activeSeq]||[]), {...draft, day:+draft.day, custom:true}] }));
    setDraft({ day:"", subject:"", goal:"", type:"Custom" });
    setAdding(false);
  }

  return (
    <div style={{display:"flex", flexDirection:"column", gap:20}}>
      <Card>
        <Lbl>Select Sequence</Lbl>
        <div style={{display:"flex", gap:8, flexWrap:"wrap"}}>
          {Object.entries(SEQUENCE_TEMPLATES).map(([key, s]) => (
            <button key={key} onClick={() => setActiveSeq(key)} style={{
              fontFamily:"Manrope,sans-serif", fontSize:11, fontWeight:700,
              padding:"7px 16px", borderRadius:6, cursor:"pointer",
              border:`1.5px solid ${activeSeq===key ? C.amber : C.border}`,
              background: activeSeq===key ? C.amber : "transparent",
              color: activeSeq===key ? "#fff" : C.muted, transition:"all 0.15s",
            }}>{s.name}</button>
          ))}
        </div>
      </Card>

      <div className="g3">
        <Stat val={all.length} label="Emails in sequence" sub={seq.channel} accent={C.amber} />
        <Stat val={`${all[all.length-1]?.day || 0} days`} label="Total sequence length" sub="From first send" accent={C.brown} />
        <Stat val={seq.audience.split("—")[0].trim()} label="Audience" sub={seq.audience.split("—")[1]?.trim()} accent={C.espresso} />
      </div>

      <Card>
        <div style={{display:"flex", justifyContent:"space-between", alignItems:"flex-start", marginBottom:16, flexWrap:"wrap", gap:8}}>
          <div>
            <Lbl style={{marginBottom:4}}>Sequence Plan</Lbl>
            <div style={{fontFamily:"Fraunces,serif", fontSize:18, fontWeight:600, color:C.espresso}}>{seq.name}</div>
            <div style={{fontFamily:"Manrope,sans-serif", fontSize:12, color:C.muted, marginTop:3}}>Goal: {seq.goal}</div>
          </div>
          <button onClick={() => setAdding(!adding)} style={{
            fontFamily:"Manrope,sans-serif", fontSize:11, fontWeight:700,
            padding:"7px 14px", borderRadius:6, cursor:"pointer",
            border:`1.5px solid ${C.amber}`, background:"transparent", color:C.amber,
          }}>+ Add Email</button>
        </div>

        {adding && (
          <div style={{background:C.creamDk, borderRadius:8, padding:14, marginBottom:16, display:"grid", gridTemplateColumns:"70px 1fr 1fr 100px", gap:10, alignItems:"end"}}>
            {[
              {label:"Day", key:"day", type:"number", placeholder:""},
              {label:"Subject line", key:"subject", type:"text", placeholder:"Enter subject..."},
              {label:"Email goal", key:"goal", type:"text", placeholder:"What should this achieve?"},
            ].map(f => (
              <div key={f.key}>
                <div style={{fontFamily:"Manrope,sans-serif", fontSize:9, fontWeight:800, color:C.muted, letterSpacing:"0.1em", textTransform:"uppercase", marginBottom:4}}>{f.label}</div>
                <input type={f.type} value={draft[f.key]} placeholder={f.placeholder}
                  onChange={e => setDraft(p => ({...p, [f.key]:e.target.value}))}
                  style={{width:"100%", fontFamily:"Manrope,sans-serif", fontSize:12, border:`1.5px solid ${C.border}`, borderRadius:6, padding:"6px 8px", background:"#fff", outline:"none"}} />
              </div>
            ))}
            <button onClick={addEmail} style={{
              fontFamily:"Manrope,sans-serif", fontSize:11, fontWeight:700,
              padding:"8px 14px", borderRadius:6, cursor:"pointer",
              background:C.amber, border:"none", color:"#fff",
            }}>Add</button>
          </div>
        )}

        <div style={{position:"relative"}}>
          <div style={{position:"absolute", left:36, top:12, bottom:12, width:2, background:C.border, borderRadius:2}} />
          {all.map((e, i) => (
            <div key={i} style={{display:"flex", gap:16, marginBottom:14, position:"relative"}}>
              <div style={{
                minWidth:72, height:40, borderRadius:6,
                background: e.custom ? C.espresso : C.amber,
                display:"flex", alignItems:"center", justifyContent:"center", flexDirection:"column",
                position:"relative", zIndex:1,
              }}>
                <div style={{fontFamily:"Manrope,sans-serif", fontSize:8, fontWeight:800, color:"rgba(255,255,255,0.65)", letterSpacing:"0.1em", textTransform:"uppercase"}}>Day</div>
                <div style={{fontFamily:"Fraunces,serif", fontSize:17, fontWeight:700, color:"#fff", lineHeight:1}}>{e.day}</div>
              </div>
              <div style={{flex:1, background:C.creamDk, borderRadius:8, padding:"10px 14px", border: e.custom ? `1.5px solid ${C.espresso}22` : undefined}}>
                <div style={{display:"flex", justifyContent:"space-between", alignItems:"flex-start", gap:8, flexWrap:"wrap"}}>
                  <div style={{fontFamily:"Manrope,sans-serif", fontSize:13, fontWeight:700, color:C.espresso}}>{e.subject}</div>
                  <Badge color={e.custom ? C.espresso : C.brown}>{e.type || "Custom"}</Badge>
                </div>
                {e.goal && <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginTop:4, lineHeight:1.4}}>{e.goal}</div>}
              </div>
            </div>
          ))}
        </div>
      </Card>

      <Card>
        <Lbl>Sequence Notes & Planning</Lbl>
        <textarea
          rows={6}
          value={notes[activeSeq] || ""}
          onChange={e => setNotes(p => ({...p, [activeSeq]: e.target.value}))}
          placeholder={`Notes for ${seq.name}...\n\n- Segments to include/exclude\n- A/B test ideas\n- Timing considerations\n- Landing pages needed`}
        />
      </Card>
    </div>
  );
}

// ── TABS ──────────────────────────────────────────────────────────────────────
const TABS = [
  {id:"overview",  label:"Overview"},
  {id:"icp",       label:"ICP & Market"},
  {id:"plan",      label:"Marketing Plan"},
  {id:"sequences", label:"Sequences"},
  {id:"metrics",   label:"Metrics"},
];

// ── APP ───────────────────────────────────────────────────────────────────────
function App() {
  const [tab, setTab]         = useState("overview");
  const [avgDeal, setAvgDeal] = useState(2400);
  const [churn, setChurn]     = useState(8);
  const [target, setTarget]   = useState(500000);

  const currentARR  = 1 * avgDeal;
  const progress    = Math.min(100, (currentARR/target)*100);
  const dealsNeeded = Math.ceil((target-currentARR)/avgDeal);
  const totalPipe   = HUBSPOT.deals.length * avgDeal;
  const ltv         = avgDeal / (churn/100);
  const cac         = 850;
  const ltvCac      = ltv / cac;

  return (
    <div style={{fontFamily:"Manrope,sans-serif", background:C.cream, minHeight:"100vh", color:C.text}}>

      {/* HEADER */}
      <div style={{background:C.espresso, padding:"14px 28px", display:"flex", alignItems:"center", justifyContent:"space-between", flexWrap:"wrap", gap:10}}>
        <div style={{display:"flex", alignItems:"center", gap:12}}>
          <div style={{width:6, height:36, borderRadius:3, background:C.amber}} />
          <div>
            <div style={{fontFamily:"Fraunces,serif", color:"#fff", fontSize:18, fontWeight:700, lineHeight:1.15}}>StableTrack</div>
            <div style={{color:C.muted, fontSize:9, letterSpacing:"0.16em", textTransform:"uppercase"}}>Marketing Command Center</div>
          </div>
        </div>
        <div style={{display:"flex", gap:10, alignItems:"center"}}>
          <Badge color={C.green}>HubSpot data — Mar 11 2026</Badge>
        </div>
      </div>

      {/* TABS */}
      <div style={{background:"#fff", borderBottom:`1.5px solid ${C.border}`, padding:"10px 28px", display:"flex", gap:4, flexWrap:"wrap"}}>
        {TABS.map(t => (
          <button key={t.id} onClick={() => setTab(t.id)} style={{
            fontFamily:"Manrope,sans-serif", fontSize:11, fontWeight:700,
            letterSpacing:"0.04em", padding:"7px 18px",
            border:`1.5px solid ${tab===t.id ? C.amber : C.border}`,
            borderRadius:5, cursor:"pointer",
            background: tab===t.id ? C.amber : "transparent",
            color: tab===t.id ? "#fff" : C.muted,
            transition:"all 0.15s",
          }}>{t.label}</button>
        ))}
      </div>

      {/* BODY */}
      <div style={{padding:"22px 28px", maxWidth:1160, margin:"0 auto", display:"flex", flexDirection:"column", gap:18}}>

        {/* ── OVERVIEW ── */}
        {tab==="overview" && <>
          <Card>
            <div style={{display:"flex", justifyContent:"space-between", alignItems:"flex-start", marginBottom:14, flexWrap:"wrap", gap:10}}>
              <div>
                <Lbl>2026 Revenue Progress</Lbl>
                <div style={{fontFamily:"Fraunces,serif", fontSize:32, fontWeight:700, color:C.espresso, lineHeight:1}}>
                  {$m(currentARR)}
                  <span style={{fontFamily:"Manrope,sans-serif", fontSize:14, color:C.muted, fontWeight:400}}> / {$m(target)}</span>
                </div>
              </div>
              <FieldInput label="ARR Target" value={target} onChange={setTarget} prefix="$" />
            </div>
            <Bar pct={progress} h={8} />
            <div style={{display:"flex", justifyContent:"space-between", marginTop:7}}>
              <span style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted}}>{progress.toFixed(1)}% to target</span>
              <span style={{fontFamily:"Manrope,sans-serif", fontSize:11, fontWeight:700, color:C.amber}}>{$n(dealsNeeded)} more accounts needed</span>
            </div>
          </Card>

          <div className="g4">
            <Stat val={$n(HUBSPOT.contacts.total)} label="Total contacts" sub="805 in HubSpot — 528 to re-import" />
            <Stat val="14" label="Requested follow-up" sub="AAEP survey respondents" accent={C.brown} />
            <Stat val="1" label="Active paid users" sub="41 inactive · 1 at-risk" accent={C.green} />
            <Stat val="14" label="Open pipeline deals" sub={`${$m(totalPipe)} total value`} accent={C.espresso} />
          </div>

          <div className="g2">
            <Card>
              <Lbl>Contact Lifecycle Funnel (Live)</Lbl>
              {[
                {label:"All Contacts",            n:805, pct:100,           color:C.amber},
                {label:"Customers (KS accounts)", n:411, pct:(411/805)*100, color:C.brown},
                {label:"Subscribers",             n:339, pct:(339/805)*100, color:"#8B6914"},
                {label:"Leads",                   n:41,  pct:(41/805)*100,  color:C.blue},
              ].map((r,i) => (
                <div key={i} style={{marginBottom:11}}>
                  <div style={{display:"flex", justifyContent:"space-between", marginBottom:4}}>
                    <span style={{fontFamily:"Manrope,sans-serif", fontSize:12}}>{r.label}</span>
                    <span style={{fontFamily:"Manrope,sans-serif", fontSize:12, fontWeight:700, color:r.color}}>{$n(r.n)}</span>
                  </div>
                  <Bar pct={r.pct} color={r.color} />
                </div>
              ))}
              <Notice color={C.red}><strong>528 contacts missing from HubSpot.</strong> Check Import History and re-upload the AAEP Conference CSV. HubSpot will deduplicate on email.</Notice>
            </Card>

            <Card>
              <Lbl>StableTrack User Health (43 total)</Lbl>
              <div style={{display:"flex", gap:12, marginBottom:14}}>
                {[
                  {label:"Active", n:5, color:C.green},
                  {label:"At Risk", n:1, color:C.yellow},
                  {label:"Inactive", n:37, color:C.red},
                ].map((u,i) => (
                  <div key={i} style={{flex:1, textAlign:"center", padding:"12px 8px", borderRadius:8, background:u.color+"12", border:`1.5px solid ${u.color}28`}}>
                    <div style={{fontFamily:"Fraunces,serif", fontSize:28, fontWeight:700, color:u.color}}>{u.n}</div>
                    <div style={{fontFamily:"Manrope,sans-serif", fontSize:10, fontWeight:700, color:u.color, marginTop:3, letterSpacing:"0.06em", textTransform:"uppercase"}}>{u.label}</div>
                  </div>
                ))}
              </div>
              <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginBottom:6}}>Trial to paid conversion</div>
              <Bar pct={(1/43)*100} h={7} color={C.amber} />
              <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginTop:5}}>1 of 43 trialling users converted — <strong style={{color:C.espresso}}>2.3%</strong>. Target: 40%.</div>
              <Notice color={C.red}><strong>Reactivation is the highest-leverage marketing action right now.</strong> 37 inactive users already know the product. Launch the reactivation sequence this week.</Notice>
            </Card>
          </div>

          <Card>
            <Lbl>Contact Database — All Sources</Lbl>
            <table>
              <thead><tr><th>Source</th><th>Contacts</th><th>Notes</th><th>Status</th></tr></thead>
              <tbody>
                {HUBSPOT.sources.map((s,i) => (
                  <tr key={i}>
                    <td><strong>{s.source}</strong></td>
                    <td style={{fontFamily:"Fraunces,serif", fontSize:16, fontWeight:600, color:C.espresso}}>{$n(s.count)}</td>
                    <td style={{color:C.muted}}>{s.notes}</td>
                    <td><Badge color={C.green}>Imported</Badge></td>
                  </tr>
                ))}
                <tr style={{background:C.creamDk}}>
                  <td><strong>Total unique (deduped by email)</strong></td>
                  <td style={{fontFamily:"Fraunces,serif", fontSize:16, fontWeight:600, color:C.espresso}}>1,333</td>
                  <td style={{color:C.red, fontWeight:600}}>HubSpot shows 805 — 528 missing</td>
                  <td><Badge color={C.red}>Needs re-import</Badge></td>
                </tr>
              </tbody>
            </table>
          </Card>
        </>}

        {/* ── ICP & MARKET ── */}
        {tab==="icp" && <>
          <Card style={{background:C.espresso}}>
            <Lbl style={{color:C.muted}}>Pillar 1 — Target Audience & Market Definition</Lbl>
            <div style={{fontFamily:"Fraunces,serif", fontSize:20, color:"#fff", fontWeight:600}}>ICP Personas · Segmentation · Competitive Landscape</div>
          </Card>

          <div className="g3">
            {[
              {title:"Ambulatory Equine Vet", tag:"Primary ICP", color:C.amber,
               items:["Solo or 1–3 vet mobile practice","50–300 active patient horses","On HVMS, Ezyvet, or paper","Pain: admin burden on the road","Decision maker: sole owner/vet"], urgency:"High"},
              {title:"Equine-Only Clinic", tag:"Secondary ICP", color:C.brown,
               items:["2–8 vet practice","300–1,000 active patients","Frustrated with HVMS cost/support","Pain: multi-vet record coordination","Decision: practice manager + lead vet"], urgency:"Medium"},
              {title:"Teaching Hospital / University", tag:"Tertiary", color:C.blue,
               items:["University-affiliated equine programs","Resident training + complex caseload","Currently on VetView or Cornerstone","Pain: teaching + clinical workflow mix","Decision: dept head + IT committee"], urgency:"Low"},
            ].map((p,i) => (
              <Card key={i} topAccent={p.color}>
                <Badge color={p.color}>{p.tag}</Badge>
                <div style={{fontFamily:"Fraunces,serif", fontSize:15, fontWeight:600, margin:"10px 0"}}>{p.title}</div>
                {p.items.map((it,j) => (
                  <div key={j} style={{fontFamily:"Manrope,sans-serif", fontSize:12, marginBottom:5, paddingLeft:12, position:"relative", lineHeight:1.4}}>
                    <span style={{position:"absolute", left:0, color:p.color, fontWeight:700}}>–</span>{it}
                  </div>
                ))}
                <div style={{marginTop:12, display:"flex", justifyContent:"space-between", alignItems:"center"}}>
                  <span style={{fontFamily:"Manrope,sans-serif", fontSize:10, color:C.muted}}>Conversion urgency</span>
                  <Badge color={p.urgency==="High"?C.green:p.urgency==="Medium"?C.yellow:C.blue}>{p.urgency}</Badge>
                </div>
              </Card>
            ))}
          </div>

          <Card>
            <Lbl>TAM · SAM · SOM — N. America</Lbl>
            <div style={{display:"flex", gap:16, flexWrap:"wrap"}}>
              {[
                {tier:"TAM", val:"~6,800", desc:"All AAEP-member equine practices in North America", color:C.amber},
                {tier:"SAM", val:"~2,400", desc:"Ambulatory + equine-only clinics, English-speaking markets", color:C.brown},
                {tier:"SOM", val:"~200",   desc:"Year 1 realistic target: 200 paying practices by Dec 2026", color:C.espresso},
              ].map((m,i) => (
                <div key={i} style={{flex:1, minWidth:160, textAlign:"center", padding:"18px 16px", borderRadius:10, background:m.color+"0E", border:`2px solid ${m.color}22`}}>
                  <div style={{fontFamily:"Fraunces,serif", fontSize:26, fontWeight:700, color:m.color}}>{m.tier}</div>
                  <div style={{fontFamily:"Fraunces,serif", fontSize:22, fontWeight:600, color:C.espresso, marginTop:4}}>{m.val}</div>
                  <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginTop:6, lineHeight:1.4}}>{m.desc}</div>
                </div>
              ))}
            </div>
          </Card>

          <Card>
            <Lbl>PMS Competitive Landscape — AAEP Survey Data (49 respondents)</Lbl>
            <table>
              <thead><tr><th>Current PMS</th><th>Respondents</th><th>Displacement Opportunity</th><th>Messaging Angle</th></tr></thead>
              <tbody>
                {[
                  {pms:"None / Paper",        n:7, opp:"Highest", angle:"Zero switching cost. First digital home for their records."},
                  {pms:"HVMS",                n:8, opp:"High",    angle:"Modern, mobile-first, at lower cost. Built for how they actually work."},
                  {pms:"Ezyvet",              n:5, opp:"Medium",  angle:"Not equine-specific. StableTrack speaks their language."},
                  {pms:"Shepherd",            n:3, opp:"Medium",  angle:"Newer but still mixed-species. Equine vets deserve their own."},
                  {pms:"DVM Manager",         n:2, opp:"High",    angle:"Legacy, clunky, desktop-only. Replace with something built for mobile."},
                  {pms:"Cornerstone/Avimark", n:2, opp:"High",    angle:"Desktop-only in a mobile-first world. Make the switch."},
                  {pms:"ImproMed / Antech",   n:2, opp:"Medium",  angle:"Mixed-species generic. StableTrack is built exclusively for equine."},
                ].map((r,i) => {
                  const col = r.opp==="Highest"?C.green:r.opp==="High"?C.yellow:C.muted;
                  return (
                    <tr key={i}>
                      <td><strong>{r.pms}</strong></td>
                      <td style={{fontFamily:"Fraunces,serif", fontSize:16, fontWeight:600, color:C.espresso}}>{r.n}</td>
                      <td><Badge color={col}>{r.opp}</Badge></td>
                      <td style={{color:C.muted, fontSize:11}}>{r.angle}</td>
                    </tr>
                  );
                })}
              </tbody>
            </table>
          </Card>
        </>}

        {/* ── MARKETING PLAN ── */}
        {tab==="plan" && <>
          <Card style={{background:C.espresso}}>
            <Lbl style={{color:C.muted}}>2026 StableTrack Marketing Plan</Lbl>
            <div style={{fontFamily:"Fraunces,serif", fontSize:20, color:"#fff", fontWeight:600}}>Messaging · Channels · Content · 90-Day Roadmap</div>
          </Card>

          <Card>
            <Lbl>Core Value Proposition</Lbl>
            <div style={{fontFamily:"Fraunces,serif", fontSize:20, fontWeight:600, color:C.espresso, lineHeight:1.3, marginBottom:14}}>
              "The only practice management platform built exclusively for equine vets on the move."
            </div>
            <div style={{display:"flex", gap:8, flexWrap:"wrap"}}>
              {["Mobile-first","Equine-only workflows","AI SOAP notes","No desktop required","Built by equine vets"].map((t,i) => (
                <Badge key={i}>{t}</Badge>
              ))}
            </div>
          </Card>

          <Card>
            <Lbl>Messaging Matrix — By ICP Segment</Lbl>
            <table>
              <thead><tr><th>Segment</th><th>Core Pain</th><th>Lead Message</th><th>Proof Point</th></tr></thead>
              <tbody>
                {[
                  {seg:"Ambulatory Vet",          pain:"Writing SOAP notes after hours, alone in the truck",          msg:"Record notes hands-free from the field. Cut admin time in half.",     proof:"Annie Schwartz — records between calls, on the road."},
                  {seg:"Clinic Practice Manager", pain:"Vets using different systems; patient records scattered",      msg:"One platform for your whole equine team. Real-time, everywhere.",    proof:"Monadnock Equine — 3 vets, one record, no duplication."},
                  {seg:"HVMS User",               pain:"Expensive, outdated software that doesn't work on mobile",    msg:"Switch in a weekend. Half the cost. Built for horse vets.",          proof:"Kenneth Allison — migrated 8 years of patient history."},
                  {seg:"Paper / No PMS",          pain:"Lost records, no audit trail, liability exposure",            msg:"Your first digital record system. Set up in under an hour.",         proof:"Michelle Clarke — first digital record same day as sign-up."},
                ].map((r,i) => (
                  <tr key={i}>
                    <td><strong>{r.seg}</strong></td>
                    <td style={{color:C.red, fontSize:11, lineHeight:1.4}}>{r.pain}</td>
                    <td style={{fontStyle:"italic", fontSize:12, lineHeight:1.4}}>"{r.msg}"</td>
                    <td style={{color:C.muted, fontSize:11, lineHeight:1.4}}>{r.proof}</td>
                  </tr>
                ))}
              </tbody>
            </table>
          </Card>

          <div className="g2">
            {[
              {name:"Email Marketing",         priority:"P1 — Launch Now", color:C.amber,
               desc:"4 sequences ready to deploy. Total addressable list: 1,333 contacts across AAEP, survey, Salesforce, and user cohorts.",
               actions:["Deploy reactivation sequence to 37 inactive users this week","Deploy AAEP survey follow-up to 14 requested-contact respondents","Deploy AAEP general nurture to 930 conference attendees","Deploy Keystone cross-sell to 425 existing KS accounts"]},
              {name:"SEO & Content",           priority:"P1 — Build Now",  color:C.amber,
               desc:"StableTrack.ai has ~20 indexed pages. Niche market means fast ranking is achievable with focused execution.",
               actions:["Publish: StableTrack vs ThoroVet comparison (high commercial intent)","Publish: Equine practice management software buyer's guide","Publish: Ambulatory equine vet workflows — pillar page","Internal linking strategy across all existing pages"]},
              {name:"LinkedIn & Social",       priority:"P2 — Build",      color:C.brown,
               desc:"Equine vet community is tight-knit and trust-driven. Peer content and day-in-the-life stories outperform product posts significantly.",
               actions:["3 posts/week: ambulatory vet identity-led content","Repurpose AAEP survey findings as data-driven posts","Feature active users — practitioner spotlights","LinkedIn newsletter: The Equine Practice"]},
              {name:"Referral & Community",    priority:"P2 — Plan",       color:C.brown,
               desc:"1 paying user and growing brand advocates. An AAEP-connected equine vet recommending a product carries more weight than any paid channel.",
               actions:["Brief 3 brand champions: Aletha, Annie, Monadnock","Referral programme: 1 free month per referred practice that activates","AAEP speaker outreach — product partnership or demo slot","Equine vet Facebook groups and forums — organic seeding"]},
              {name:"Paid Acquisition",        priority:"P3 — Hold",       color:C.muted,
               desc:"Hold paid spend until organic + email channels are validated and trial-to-paid conversion is above 25%.",
               actions:["Monitor: Google Search for 'equine practice management software'","Plan: Google Ads campaign brief ready for Q3 activation","Evaluate: AAEP digital advertising partnerships","Re-assess trigger: once organic conversion exceeds 25%"]},
              {name:"Partner & Integration",   priority:"P3 — Plan",       color:C.muted,
               desc:"Asteris Keystone integration is a built-in unfair advantage. No other equine PMS has a native PACS connection.",
               actions:["Co-marketing with Asteris: joint email to shared KS list","IDEXX and Zoetis connector development — announce when live","PMS migration guide for HVMS users (content + product)","Affiliate or revenue-share with equine vet consultants"]},
            ].map((ch,i) => (
              <Card key={i}>
                <div style={{display:"flex", justifyContent:"space-between", marginBottom:10}}>
                  <div>
                    <div style={{fontFamily:"Fraunces,serif", fontSize:15, fontWeight:600}}>{ch.name}</div>
                    <div style={{fontFamily:"Manrope,sans-serif", fontSize:11, color:C.muted, marginTop:3, lineHeight:1.4}}>{ch.desc}</div>
                  </div>
                  <Badge color={ch.color} style={{whiteSpace:"nowrap", marginLeft:10}}>{ch.priority}</Badge>
                </div>
                {ch.actions.map((a,j) => (
                  <div key={j} style={{fontFamily:"Manrope,sans-serif", fontSize:12, marginBottom:5, paddingLeft:12, position:"relative", lineHeight:1.4}}>
                    <span style={{position:"absolute", left:0, color:ch.color, fontWeight:800}}>–</span>{a}
                  </div>
                ))}
              </Card>
            ))}
          </div>

          <Card>
            <Lbl>90-Day Marketing Roadmap</Lbl>
            {[
              {period:"Days 1–14",  title:"Foundation & Quick Wins",
               tasks:["Re-import 528 missing AAEP contacts into HubSpot","Deploy reactivation email sequence — 37 inactive users","Deploy AAEP survey follow-up — 14 requested-contact respondents","Update all 14 pipeline deal stages in HubSpot","Brief 3 potential brand champions (Annie, Aletha, Monadnock)"]},
              {period:"Days 15–30", title:"Nurture & Content Launch",
               tasks:["Launch AAEP general nurture sequence — 930 conference attendees","Launch Keystone cross-sell sequence — 425 Salesforce accounts","Publish StableTrack vs ThoroVet comparison page","Begin LinkedIn content cadence — 3x/week","First NPS / feedback survey to the 1 paying user + near-active users"]},
              {period:"Days 31–60", title:"Scale What's Working",
               tasks:["Review email sequence performance — open rate, reply rate, unsubscribes","Publish equine practice management buyer's guide","First practitioner spotlight post with a brand champion","Internal linking audit across all existing site pages","Case study brief from at least 1 active user"]},
              {period:"Days 61–90", title:"Optimise & Expand",
               tasks:["A/B test 2 subject line variants on best-performing sequence","Referral programme soft launch to active user cohort","Publish pillar page: ambulatory equine vet workflows","Evaluate paid acquisition readiness (threshold: trial-to-paid 25%+)","AAEP 2026 event strategy planning begins"]},
            ].map((p,i) => (
              <div key={i} style={{display:"flex", gap:14, marginBottom:12, padding:"12px 14px", background:C.creamDk, borderRadius:8}}>
                <div style={{minWidth:90}}>
                  <div style={{fontFamily:"Manrope,sans-serif", fontSize:9, fontWeight:800, color:C.muted, letterSpacing:"0.1em", textTransform:"uppercase"}}>{p.period}</div>
                  <div style={{fontFamily:"Fraunces,serif", fontSize:13, fontWeight:600, color:C.espresso, marginTop:3, lineHeight:1.3}}>{p.title}</div>
                </div>
                <div style={{borderLeft:`2px solid ${C.border}`, paddingLeft:14, flex:1}}>
                  {p.tasks.map((t,j) => (
                    <div key={j} style={{fontFamily:"Manrope,sans-serif", fontSize:12, marginBottom:4, lineHeight:1.4}}>{t}</div>
                  ))}
                </div>
              </div>
            ))}
          </Card>
        </>}

        {/* ── SEQUENCES ── */}
        {tab==="sequences" && <SequencePlanner />}

        {/* ── METRICS ── */}
        {tab==="metrics" && <>
          <Card style={{background:C.espresso}}>
            <Lbl style={{color:C.muted}}>Pillar 5 — Metrics & Optimization</Lbl>
            <div style={{fontFamily:"Fraunces,serif", fontSize:20, color:"#fff", fontWeight:600}}>KPIs · Unit Economics · Feedback Loops</div>
          </Card>

          <Card>
            <Lbl>Assumptions (Edit to update all calculations)</Lbl>
            <div className="g3">
              <FieldInput label="Avg Deal Size (ARR / yr)" value={avgDeal} onChange={setAvgDeal} prefix="$" />
              <FieldInput label="Annual Churn Rate" value={churn} onChange={setChurn} suffix="%" />
              <FieldInput label="2026 ARR Target" value={target} onChange={setTarget} prefix="$" />
            </div>
          </Card>

          <div className="g4">
            <Stat val={$m(ltv)} label="Customer LTV" sub={`At ${churn}% annual churn`} accent={ltv>12000?C.green:C.red} />
            <Stat val={$m(cac)} label="Est. CAC" sub="AAEP + outreach blended" accent={C.brown} />
            <Stat val={ltvCac.toFixed(1)+"x"} label="LTV : CAC ratio" sub={ltvCac>=3?"Healthy":"Below 3x — needs work"} accent={ltvCac>=3?C.green:C.red} />
            <Stat val={Math.round(cac/(avgDeal/12))+" mo"} label="CAC payback" sub="Months to recover acquisition cost" accent={cac/(avgDeal/12)<12?C.green:C.red} />
          </div>

          <Card>
            <Lbl>Marketing KPI Scorecard — Week of Mar 11, 2026</Lbl>
            <table>
              <thead><tr><th>Metric</th><th>Current</th><th>Target</th><th>Status</th><th>Next Action</th></tr></thead>
              <tbody>
                {[
                  {m:"Paying Accounts",        curr:"1 paying user",       tgt:"200 by Dec 2026",  s:"red",    a:"Reactivation sequence + convert 14 AAEP follow-ups"},
                  {m:"ARR",                    curr:$m(currentARR),         tgt:$m(target),         s:"red",    a:`${dealsNeeded} more accounts needed at current pricing`},
                  {m:"Total Contacts (HubSpot)",curr:"805",                  tgt:"1,333",            s:"yellow", a:"Re-import 528 missing AAEP contacts"},
                  {m:"Email Open Rate",        curr:"Not yet deployed",     tgt:">40%",             s:"white",  a:"Launch sequences first — then measure"},
                  {m:"Email Reply Rate",       curr:"Not yet deployed",     tgt:">5%",              s:"white",  a:"AAEP survey follow-up expected highest reply rate"},
                  {m:"Trial to Paid Conv.",    curr:"2.3% (1/43)",         tgt:">40%",             s:"red",    a:"Reactivation campaign + improved onboarding flow"},
                  {m:"Churn Rate",             curr:`${churn}% assumed`,    tgt:"<8%",              s:churn<=8?"green":"red", a:"Understand churn reason via 1:1 calls with inactive users"},
                  {m:"SEO Pages Indexed",      curr:"~20 pages",            tgt:"100+ by Jun 2026", s:"red",    a:"Execute content plan — buyer's guide, comparison, pillar page"},
                  {m:"NPS",                    curr:"Not measured",         tgt:">50",              s:"white",  a:"Survey paying user + trial users this week"},
                  {m:"LinkedIn Followers",     curr:"Not measured",         tgt:"500 by Jun 2026",  s:"white",  a:"Start publishing — 3 posts/week"},
                ].map((r,i) => {
                  const dot = {green:C.green, red:C.red, yellow:C.yellow, white:C.muted}[r.s];
                  return (
                    <tr key={i}>
                      <td><strong>{r.m}</strong></td>
                      <td>{r.curr}</td>
                      <td style={{color:C.muted}}>{r.tgt}</td>
                      <td><span style={{display:"inline-block", width:8, height:8, borderRadius:"50%", background:dot}} /></td>
                      <td style={{color:C.muted, fontSize:11}}>{r.a}</td>
                    </tr>
                  );
                })}
              </tbody>
            </table>
          </Card>

          <Card>
            <Lbl>Feedback Loops — Key Marketing Signals</Lbl>
            <div className="g2">
              {[
                {title:"Signal: 86% of trial users are inactive", color:C.red,
                 items:["Root cause is unknown — this is the critical gap","Schedule 3–5 calls with inactive users this week","Ask: What stopped you? What were you expecting?","Output: identify top 1–2 barriers to fix in product + onboarding"]},
                {title:"Signal: 14 AAEP survey follow-up requests", color:C.amber,
                 items:["These explicitly requested contact — highest intent signal in the DB","Warm marketing contacts, not yet sales-qualified leads","Personalise by current PMS before first email","PMS = None (4 contacts): lowest switching friction, start here"]},
                {title:"Signal: PMS data from AAEP survey", color:C.blue,
                 items:["49 respondents shared their current PMS — a rare dataset","HVMS (8) and None/Paper (7) are the top displacement targets","Use PMS to segment all sequences — different angle per group","Build PMS-specific landing pages when SEO volume justifies it"]},
                {title:"Signal: 1 paying user — and brand advocates emerging", color:C.green,
                 items:["This is your first paying proof point — treat them as a VIP","Aletha Carson: KS + StableTrack cross-sell proof","Annie Schwartz + Monadnock: ambulatory use case","Actions: NPS survey, case study ask, referral programme invite"]},
              ].map((s,i) => (
                <div key={i} style={{padding:"14px 16px", background:s.color+"0A", border:`1.5px solid ${s.color}22`, borderRadius:9}}>
                  <div style={{fontFamily:"Fraunces,serif", fontSize:14, fontWeight:600, color:s.color, marginBottom:9}}>{s.title}</div>
                  {s.items.map((it,j) => (
                    <div key={j} style={{fontFamily:"Manrope,sans-serif", fontSize:12, marginBottom:5, lineHeight:1.4}}>{it}</div>
                  ))}
                </div>
              ))}
            </div>
          </Card>
        </>}

      </div>

      {/* FOOTER */}
      <div style={{borderTop:`1px solid ${C.border}`, padding:"12px 28px", display:"flex", justifyContent:"space-between", flexWrap:"wrap", gap:8, marginTop:12}}>
        <span style={{fontFamily:"Manrope,sans-serif", fontSize:10, color:C.muted}}>HubSpot: 805 contacts · 14 pipeline deals · 1 paying user · 41 inactive · 43 total users · Mar 11, 2026</span>
        <span style={{fontFamily:"Manrope,sans-serif", fontSize:10, color:C.muted}}>StableTrack — Marketing Command Center</span>
      </div>
    </div>
  );
}

ReactDOM.createRoot(document.getElementById("root")).render(<App />);
</script>
</body>
</html>
