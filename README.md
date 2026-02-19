[index.html](https://github.com/user-attachments/files/25405934/index.html)
<!doctype html>
<html><head><meta charset="utf-8"><meta http-equiv="refresh" content="0; url=index_20260219040258.html"></head>
<body style="font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Arial, sans-serif;">
Redirecting to latest build… If you are not redirected, <a href="index_20260219040258.html">click here</a>.
</body></html>[form_a.html](https://github.com/user-attachments/files/25405935/form_a.html)
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>NCLEX-Style Timed Exam — Form A (Pain & Pharm)</title>
<style>
  :root {
    --bg: #0b0f17;
    --panel: #121a29;
    --panel2: #0f1624;
    --text: #e8edf7;
    --muted: #a8b3c7;
    --accent: #5dd6ff;
    --danger: #ff5d7a;
    --ok: #52ffa8;
    --border: rgba(255,255,255,.10);
  }
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Segoe UI", Roboto, Helvetica, Arial, system-ui, sans-serif;
    background: radial-gradient(1200px 700px at 15% 10%, rgba(93,214,255,.12), transparent 60%),
                radial-gradient(900px 600px at 85% 25%, rgba(82,255,168,.10), transparent 65%),
                var(--bg);
    color: var(--text);
  }
  a { color: var(--accent); }
  .wrap {
    max-width: 1200px;
    margin: 0 auto;
    padding: 18px;
  }
  .card {
    background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
    border: 1px solid var(--border);
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0,0,0,.35);
    overflow: hidden;
  }
  .topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    padding: 14px 16px;
    background: rgba(0,0,0,.18);
    border-bottom: 1px solid var(--border);
  }
  .title {
    font-weight: 700;
    letter-spacing: .2px;
  }
  .pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 12px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.7);
    color: var(--muted);
    font-size: 13px;
    white-space: nowrap;
  }
  .timer {
    font-variant-numeric: tabular-nums;
    color: var(--text);
    font-weight: 700;
  }
  .grid {
    display: grid;
    grid-template-columns: 300px 1fr;
    min-height: 72vh;
  }
  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; }
  }
  .sidebar {
    padding: 14px;
    background: rgba(18,26,41,.35);
    border-right: 1px solid var(--border);
  }
  @media (max-width: 900px) {
    .sidebar {
      border-right: 0;
      border-bottom: 1px solid var(--border);
    }
  }
  .qnav {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    gap: 8px;
  }
  .qbtn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.6);
    color: var(--text);
    border-radius: 10px;
    padding: 10px 0;
    font-weight: 700;
    cursor: pointer;
    transition: transform .05s ease, background .2s ease, border-color .2s ease;
  }
  .qbtn:hover { transform: translateY(-1px); border-color: rgba(93,214,255,.55); }
  .qbtn.active { background: rgba(93,214,255,.18); border-color: rgba(93,214,255,.65); }
  .qbtn.answered { background: rgba(82,255,168,.12); border-color: rgba(82,255,168,.35); }
  .qbtn.flagged { background: rgba(255,93,122,.14); border-color: rgba(255,93,122,.45); }
  .sidebar .meta {
    margin-top: 14px;
    display: grid;
    gap: 10px;
  }
  .metaRow {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 13px;
    color: var(--muted);
  }
  .main {
    padding: 18px;
  }
  .stem {
    font-size: 18px;
    line-height: 1.35;
    margin: 0 0 14px 0;
  }
  .tag {
    font-size: 12px;
    color: var(--muted);
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    display: inline-block;
    padding: 6px 10px;
    border-radius: 999px;
    margin-bottom: 10px;
  }
  .choices {
    display: grid;
    gap: 10px;
  }
  label.choice {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    padding: 12px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
    cursor: pointer;
  }
  label.choice:hover {
    border-color: rgba(93,214,255,.55);
    background: rgba(15,22,36,.72);
  }
  input[type="radio"], input[type="checkbox"] {
    margin-top: 2px;
    accent-color: var(--accent);
  }
  .controls {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 16px;
  }
  button.btn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    border-radius: 12px;
    padding: 10px 12px;
    font-weight: 700;
    cursor: pointer;
  }
  button.btn:hover { border-color: rgba(93,214,255,.55); }
  button.primary {
    background: rgba(93,214,255,.18);
    border-color: rgba(93,214,255,.55);
  }
  button.danger {
    background: rgba(255,93,122,.14);
    border-color: rgba(255,93,122,.55);
  }
  button.ok {
    background: rgba(82,255,168,.12);
    border-color: rgba(82,255,168,.45);
  }
  .note {
    color: var(--muted);
    font-size: 13px;
    line-height: 1.35;
  }
  .startScreen {
    max-width: 860px;
    margin: 30px auto;
    padding: 18px;
  }
  .startScreen h1 {
    margin: 0 0 6px 0;
    font-size: 28px;
  }
  .startScreen ul {
    margin: 10px 0 0 18px;
    color: var(--muted);
    line-height: 1.5;
  }
  .hidden { display: none; }
  .calcBox {
    display: grid;
    gap: 10px;
  }
  .calcBox input {
    width: 240px;
    max-width: 100%;
    padding: 12px;
    border-radius: 12px;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    color: var(--text);
    font-size: 16px;
  }
  .ordered {
    display: grid;
    gap: 10px;
  }
  .step {
    display: flex;
    gap: 10px;
    align-items: center;
    padding: 10px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
  }
  .step .handle {
    width: 26px;
    height: 26px;
    border-radius: 8px;
    border: 1px solid var(--border);
    display: grid;
    place-items: center;
    color: var(--muted);
    font-weight: 700;
  }
  .step .txt {
    flex: 1;
    line-height: 1.3;
  }
  .step .arrows button {
    margin-left: 6px;
    padding: 6px 8px;
    border-radius: 10px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    cursor: pointer;
  }
  .results h2 {
    margin: 0 0 6px 0;
  }
  .resultItem {
    padding: 12px 12px;
    border: 1px solid var(--border);
    border-radius: 14px;
    background: rgba(15,22,36,.55);
    margin: 10px 0;
  }
  .badge {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 999px;
    font-size: 12px;
    font-weight: 800;
    border: 1px solid var(--border);
    margin-right: 8px;
  }
  .badge.ok { color: var(--ok); border-color: rgba(82,255,168,.35); background: rgba(82,255,168,.12); }
  .badge.no { color: var(--danger); border-color: rgba(255,93,122,.45); background: rgba(255,93,122,.14); }
  .rationale {
    color: var(--muted);
    margin-top: 8px;
    line-height: 1.35;
  }
</style>
</head>
<body>
<div id="start" class="wrap startScreen">
  <div class="card">
    <div class="topbar">
      <div class="title">NCLEX-Style Timed Exam - Pain & Pharmacology (50 Questions)</div>
      <div class="pill"><span>Time:</span> <span class="timer">90:00</span></div>
    </div>
    <div style="padding:16px 18px;">
      <h1>NCLEX-Style Timed Exam — Form A (Pain & Pharm)</h1>
      <div class="note">
        <ul>
          <li>This exam runs fully in your browser (works well on a Mac).</li>
          <li>Question types include Multiple Choice, Select-All-That-Apply (SATA), Ordered Response, and Calculations.</li>
          <li>Use the sidebar to jump between questions. You can flag questions for review.</li>
          <li>Your progress is saved automatically in this browser.</li>
          <li>When you submit, you'll see your score plus the answer key and rationales.</li>
        </ul>
      </div>
      <div class="controls" style="margin-top:16px;">
        <button class="btn primary" id="startBtn">Start Exam</button>
        <button class="btn" id="resetBtn">Reset Saved Attempt</button>
      </div>
      <div class="note" style="margin-top:10px;">Tip: For best timing accuracy, keep this tab open during the exam.</div>
    </div>
  </div>
</div>

<div id="exam" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title" id="headerTitle">Question</div>
      <div style="display:flex; gap:10px; align-items:center;">
        <div class="pill"><span>Answered:</span> <span id="answeredCount">0</span>/50</div>
        <div class="pill"><span>Flagged:</span> <span id="flaggedCount">0</span></div>
        <div class="pill"><span>Time Left:</span> <span class="timer" id="timer">90:00</span></div>
      </div>
    </div>

    <div class="grid">
      <div class="sidebar">
        <div class="qnav" id="qnav"></div>
        <div class="meta">
          <div class="metaRow"><span>Current</span><span id="curMeta">1 / 50</span></div>
          <div class="metaRow"><span>Type</span><span id="typeMeta">MC</span></div>
          <div class="metaRow"><span>Status</span><span id="statusMeta">Not answered</span></div>
        </div>
        <div class="controls" style="margin-top:12px;">
          <button class="btn" id="flagBtn">Flag / Unflag</button>
          <button class="btn" id="clearBtn">Clear Answer</button>
          <button class="btn danger" id="submitBtn">Submit Exam</button>
        </div>
      </div>

      <div class="main">
        <div class="tag" id="qTag">Type</div>
        <p class="stem" id="stem"></p>
        <div id="interaction"></div>

        <div class="controls">
          <button class="btn" id="prevBtn">Previous</button>
          <button class="btn primary" id="nextBtn">Next</button>
        </div>
        <div class="note" style="margin-top:10px;">Exam note: Answer key and rationales appear after submission.</div>
      </div>
    </div>
  </div>
</div>

<div id="results" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title">Results</div>
      <div class="pill"><span>Score:</span> <span class="timer" id="scoreText">0/50</span></div>
    </div>
    <div class="main results" id="resultsBody"></div>
  </div>
</div>

<script>
const QUESTIONS = [{"id": 1, "type": "mc", "stem": "A client with chronic osteoarthritis asks why ibuprofen can reduce swelling but acetaminophen usually cannot. Which explanation is most accurate?", "options": ["Ibuprofen blocks prostaglandin production throughout the body; acetaminophen mainly acts in the brain and has no meaningful anti-inflammatory effect.", "Acetaminophen irreversibly inhibits platelets, so it cannot be used for inflammation.", "Ibuprofen activates opioid receptors to reduce pain and inflammation.", "Acetaminophen is a first-generation NSAID and therefore does not treat inflammation."], "answer": ["A"], "rationale": "First-generation NSAIDs (eg, ibuprofen) reduce prostaglandin production and therefore decrease inflammation, pain, and fever, while acetaminophen is very selective to the brain and provides analgesia/antipyresis without anti-inflammatory effects."}, {"id": 2, "type": "sata", "stem": "The nurse is preparing to administer a first-generation NSAID. Which patient histories are contraindications for first-generation NSAIDs? Select all that apply.", "options": ["Hypertension and heart failure", "History of GI bleed or peptic ulcer disease", "Renal impairment", "Asthma", "Migraine with aura", "Diabetes mellitus (well controlled) with no vascular disease"], "answer": ["A", "B", "C", "D"], "rationale": "First-generation NSAIDs are contraindicated in hypertension/heart failure, history of GI bleed/PUD, renal impairment, and asthma. Migraine with aura is not a contraindication to NSAIDs, and diabetes alone is not listed as a contraindication in these materials."}, {"id": 3, "type": "mc", "stem": "A client taking naproxen asks what to do to reduce stomach irritation. Which instruction should the nurse provide?", "options": ["Take the medication with food or milk each time.", "Take the medication on an empty stomach with a full glass of water.", "Take the medication only at bedtime.", "Crush the tablet and dissolve it in juice."], "answer": ["A"], "rationale": "NSAIDs can irritate the gastric lining and increase GI bleed risk. Teaching includes taking NSAIDs with food or milk to reduce GI irritation."}, {"id": 4, "type": "mc", "stem": "A client has been taking aspirin daily for cardioprotection. Which new symptom is most concerning for salicylate toxicity?", "options": ["Tinnitus", "Mild nausea after meals", "Dry mouth", "Photophobia"], "answer": ["A"], "rationale": "Aspirin has typical NSAID side effects plus signs of salicylate toxicity; tinnitus is a key finding."}, {"id": 5, "type": "mc", "stem": "A parent asks if they can give aspirin to a 6-year-old with a fever. What is the nurse's best response?", "options": ["\"Do not give aspirin to infants or children; use a different medication as directed by the provider.\"", "\"Aspirin is safest for children because it prevents clotting.\"", "\"Give aspirin only if the child is also taking ibuprofen.\"", "\"Aspirin is safe if the child takes it with food.\""], "answer": ["A"], "rationale": "Aspirin (not all NSAIDs) is contraindicated in infants and children per the provided materials."}, {"id": 6, "type": "mc", "stem": "A client with rheumatoid arthritis is scheduled to start celecoxib (a second-generation NSAID). Which assessment finding should the nurse report before administration?", "options": ["New chest pain with exertion", "Pain rating 6/10 that decreases with rest", "Mild photophobia during headaches", "Report of muscle spasms in the lower back"], "answer": ["A"], "rationale": "Second-generation NSAIDs have significant cardiovascular risk; new chest pain suggests possible cardiac disease and warrants holding and contacting the provider."}, {"id": 7, "type": "sata", "stem": "Which teaching points should the nurse include for a client prescribed a second-generation NSAID? Select all that apply.", "options": ["Watch for black, tarry stools or vomiting blood/coffee-ground emesis.", "Seek immediate care for chest pain or symptoms of a cardiovascular event.", "Continue the medication through the day of surgery to prevent inflammation.", "Do not take if pregnant.", "Combine with alcohol to decrease stomach upset."], "answer": ["A", "B", "D"], "rationale": "Second-generation NSAIDs can still cause GI ulcers/bleeds and have major cardiac risk. They should be stopped about a week prior to surgery and avoided in pregnancy (category D in these materials). Alcohol increases GI risk."}, {"id": 8, "type": "mc", "stem": "The nurse is reviewing a PRN order for pain: \"acetaminophen 650 mg PO q6h PRN mild pain.\" Which pain score is the best match for this PRN indication?", "options": ["2/10", "6/10", "8/10", "10/10"], "answer": ["A"], "rationale": "In these materials, acetaminophen is appropriate for mild pain, typically not exceeding about 3/10. Moderate to severe pain needs a different strategy."}, {"id": 9, "type": "calc", "stem": "An older adult has received acetaminophen 650 mg PO at 0800, 1400, 2000, and 0200. Based on the not-to-exceed (NTE) guidance for older adults (3 g per 24 hours), can the nurse administer another 650 mg dose at 0800? (Answer Yes or No.)", "answer": ["No"], "rationale": "Four 650 mg doses = 2600 mg. A fifth dose would total 3250 mg in 24 hours, exceeding the 3000 mg NTE for older adults."}, {"id": 10, "type": "calc", "stem": "A client with liver impairment has taken acetaminophen 650 mg PO three times in the last 24 hours. The provider orders another 650 mg now. Using the liver-impairment NTE (2 g per 24 hours), should the nurse administer the dose? (Answer Yes or No.)", "answer": ["No"], "rationale": "Three 650 mg doses = 1950 mg in 24 hours; administering another 650 mg would total 2600 mg, exceeding the 2 g (2000 mg) NTE for liver impairment. Hold and contact the provider."}, {"id": 11, "type": "mc", "stem": "A client overdoses on acetaminophen. Which medication does the nurse anticipate as a potential antidote?", "options": ["Naloxone", "Acetylcysteine", "Sumatriptan", "Celecoxib"], "answer": ["B"], "rationale": "Acetylcysteine is the potential antidote for acetaminophen overdose to help preserve liver function."}, {"id": 12, "type": "sata", "stem": "Which findings should the nurse monitor for possible acetaminophen-related hepatotoxicity? Select all that apply.", "options": ["Jaundice (yellowing of skin)", "Yellowing of sclera (scleral icterus)", "Ascites and weight gain", "Tinnitus", "Coffee-ground emesis", "Elevated AST/ALT"], "answer": ["A", "B", "C", "F"], "rationale": "Acetaminophen toxicity is associated with liver impairment. Signs include jaundice, scleral icterus, ascites/weight gain, and abnormal LFTs (AST/ALT). Tinnitus is linked to salicylate toxicity; coffee-ground emesis suggests GI bleeding."}, {"id": 13, "type": "mc", "stem": "A client is prescribed tramadol for pain. Which pain description best matches the intended indication for tramadol in these materials?", "options": ["Moderate to moderately severe pain", "Severe pain requiring high potency opioids", "Mild pain and fever only", "Abortive migraine therapy"], "answer": ["A"], "rationale": "Tramadol is described as a centrally acting non-opioid used for moderate to moderately severe pain."}, {"id": 14, "type": "sata", "stem": "The nurse is teaching a client taking tramadol. Which statements indicate the client understands the teaching? Select all that apply.", "options": ["\"I will change positions slowly because dizziness can happen.\"", "\"I can safely mix tramadol with alcohol because it's not an opioid.\"", "\"If I have not had a bowel movement in more than 3 days, I'll contact my provider.\"", "\"I should avoid taking this with other centrally acting medications unless prescribed.\"", "\"Respiratory depression is impossible with tramadol.\""], "answer": ["A", "C", "D"], "rationale": "Tramadol commonly causes dizziness/sedation and can contribute to constipation and, less commonly, respiratory depression, especially with other CNS/serotonin-influencing meds. Safety teaching includes avoiding CNS depressants/alcohol and avoiding unsafe combinations."}, {"id": 15, "type": "mc", "stem": "A nurse administers tramadol and notes that the client is also taking an SSRI. What is the priority nursing action?", "options": ["Reassess respiratory rate and level of consciousness more frequently.", "Encourage a high-protein diet to prevent hypoglycemia.", "Place the client on contact precautions.", "Administer naloxone prophylactically."], "answer": ["A"], "rationale": "Tramadol affects serotonin/norepinephrine reuptake and has weak mu activity. Combining with other serotonin-influencing meds increases risk of sedation and potential respiratory depression; close assessment is priority."}, {"id": 16, "type": "mc", "stem": "A client receives cyclobenzaprine for acute muscle spasm. Which assessment finding would most strongly suggest the medication is working too well?", "options": ["New muscle weakness affecting safe ambulation", "Pain score decreased from 7/10 to 4/10", "Mild dry mouth", "Improved range of motion"], "answer": ["A"], "rationale": "Cyclobenzaprine can cause dizziness/drowsiness and muscle weakness. New weakness that impacts safety suggests excessive effect and requires provider notification and safety measures."}, {"id": 17, "type": "sata", "stem": "Which are anticholinergic effects the nurse should assess for in a client taking cyclobenzaprine? Select all that apply.", "options": ["Dry mouth", "Urinary retention", "Blurred vision or difficulty seeing", "Increased sweating", "Constipation"], "answer": ["A", "B", "C", "E"], "rationale": "Anticholinergic effects include dry mouth, urinary retention, blurred vision, and constipation (overall drying and decreased parasympathetic activity)."}, {"id": 18, "type": "mc", "stem": "A client reports burning, pins-and-needles pain in both feet due to diabetic neuropathy. Which medication class from the materials is most appropriate?", "options": ["Anti-convulsant (gabapentin or pregabalin)", "Triptan (sumatriptan)", "First-generation NSAID (ibuprofen)", "Opioid antagonist (naloxone)"], "answer": ["A"], "rationale": "Neuropathic pain described as burning/shocking/pins and needles is treated with adjuvant anti-convulsants such as gabapentin or pregabalin."}, {"id": 19, "type": "mc", "stem": "Which statement about pregabalin is correct based on the course materials?", "options": ["It is a schedule V controlled substance and may be more sedating than gabapentin.", "It requires routine therapeutic blood levels when used for nerve pain.", "It is contraindicated in all adults older than 65 years.", "It is used only as an abortive migraine medication."], "answer": ["A"], "rationale": "Pregabalin is described as a schedule V controlled substance and can be more sedating due to its CNS calcium-channel effects; therapeutic levels are not required for pain management."}, {"id": 20, "type": "ordered", "stem": "Place the following nursing actions in the most appropriate order when a client receives IV morphine for severe pain. (1 = first, 4 = last)", "steps": ["Assess baseline pain using PQRST and obtain respiratory rate/level of consciousness.", "Administer IV morphine as ordered (per policy for rate of administration).", "Reassess pain relief and monitor for opioid side effects (RR, LOC, nausea, pruritus).", "Implement/maintain safety measures (fall precautions, call light, position changes slowly)."], "answer_order": [1, 2, 4, 3], "rationale": "First obtain baseline assessment and safety context, then give medication, ensure safety measures are in place while effects begin, and then reassess effect and side effects after administration."}, {"id": 21, "type": "mc", "stem": "A client on opioids becomes difficult to arouse and has a respiratory rate of 6/min. Which medication is most appropriate to anticipate?", "options": ["Acetylcysteine", "Naloxone", "Ibuprofen", "Sumatriptan"], "answer": ["B"], "rationale": "Naloxone is an opioid antagonist indicated for opioid overdose signs: decreased respiratory rate and decreased level of consciousness."}, {"id": 22, "type": "sata", "stem": "Which findings are common opioid side effects the nurse should monitor? Select all that apply.", "options": ["Respiratory depression", "Constipation", "Urinary retention", "Miosis", "Diarrhea", "Pruritus"], "answer": ["A", "B", "C", "D", "F"], "rationale": "Opioids can cause respiratory depression, constipation, urinary retention, miosis, and pruritus; diarrhea is not typical."}, {"id": 23, "type": "mc", "stem": "A client receiving opioids is at increased risk for aspiration pneumonia primarily because opioids can:", "options": ["Suppress the cough reflex", "Increase salivation", "Cause bronchial dilation", "Increase peristalsis"], "answer": ["A"], "rationale": "Opioids can suppress the cough reflex, reducing airway protective mechanisms and increasing aspiration risk."}, {"id": 24, "type": "mc", "stem": "A client receiving IV opioids reports itching shortly after administration. What is the nurse's best initial interpretation?", "options": ["This may be a histamine-related effect and is not necessarily a true allergy.", "This is diagnostic of anaphylaxis and requires epinephrine immediately.", "This indicates opioid withdrawal and requires naloxone.", "This indicates acetaminophen toxicity."], "answer": ["A"], "rationale": "Pruritus can occur with opioids, especially with rapid IV administration, due to histamine release; it is not automatically an allergic reaction."}, {"id": 25, "type": "mc", "stem": "The nurse is teaching a client prescribed hydrocodone/acetaminophen. Which statement by the client shows correct understanding?", "options": ["\"I need to count the acetaminophen in this medication toward my 24-hour maximum.\"", "\"Because this has acetaminophen, I can also take unlimited DayQuil.\"", "\"This medication cannot cause constipation.\"", "\"If I feel sleepy, I should drive anyway to stay alert.\""], "answer": ["A"], "rationale": "Combination products contain acetaminophen that counts toward the 24-hour NTE; also opioids can cause sedation and constipation, so safety precautions apply."}, {"id": 26, "type": "mc", "stem": "A nurse is evaluating whether naloxone is indicated. Which patient presentation best meets the indication criteria from the materials?", "options": ["Respiratory rate 10/min and mild nausea after oxycodone", "New constipation after hydrocodone", "Difficult to arouse with bradypnea after morphine", "Pruritus after fentanyl patch placement"], "answer": ["C"], "rationale": "Naloxone is given for opioid overdose signs: decreased respiratory rate and decreased level of consciousness; not for other opioid side effects."}, {"id": 27, "type": "sata", "stem": "After naloxone administration, which adverse effects should the nurse anticipate and monitor for? Select all that apply.", "options": ["Vomiting", "Hypertension", "Tachycardia", "Dysrhythmias", "Tinnitus"], "answer": ["A", "B", "C", "D"], "rationale": "Naloxone can rapidly reverse opioid effects and cause vomiting, hypertension, tachycardia, and dysrhythmias. Tinnitus is unrelated."}, {"id": 28, "type": "mc", "stem": "A nurse is explaining why a fentanyl dose is ordered in micrograms while morphine is ordered in milligrams. Which concept best explains this difference?", "options": ["Fentanyl has higher potency than morphine.", "Fentanyl has lower efficacy than morphine.", "Fentanyl has a wider therapeutic window than morphine.", "Fentanyl is an antagonist and morphine is an agonist."], "answer": ["A"], "rationale": "Potency refers to the amount of drug needed to elicit an effect. Highly potent drugs (eg, fentanyl) require smaller doses (often micrograms)."}, {"id": 29, "type": "mc", "stem": "Two analgesics produce the same maximal pain relief, but Drug A requires a much lower dose to achieve it. Drug A is more:", "options": ["Potent", "Efficacious", "Toxic", "Antagonistic"], "answer": ["A"], "rationale": "Potency refers to the dose required for an effect. If maximal effect is the same (efficacy equal) but dose is lower, the drug is more potent."}, {"id": 30, "type": "mc", "stem": "A nurse is teaching about therapeutic index. Which medication characteristic is most concerning for toxicity risk?", "options": ["Low therapeutic index", "High therapeutic index", "Long onset", "Short duration"], "answer": ["A"], "rationale": "A low therapeutic index indicates a narrow margin between therapeutic effect and toxicity, increasing risk for harm and need for close monitoring."}, {"id": 31, "type": "mc", "stem": "A medication begins to work in 15 minutes, reaches its highest effect at 60 minutes, and lasts 6 hours. The 60-minute mark represents the medication's:", "options": ["Onset", "Peak", "Duration", "Therapeutic window"], "answer": ["B"], "rationale": "Peak is the time it takes a medication to have its highest effect or concentration."}, {"id": 32, "type": "mc", "stem": "Which route of administration has 100% bioavailability and the most immediate systemic effect?", "options": ["Intravenous (IV)", "Intramuscular (IM)", "Subcutaneous (SC)", "Oral (PO)"], "answer": ["A"], "rationale": "IV medications enter directly into the bloodstream, providing 100% bioavailability and immediate effect."}, {"id": 33, "type": "mc", "stem": "Which route is intended to have low systemic absorption and is commonly used for skin testing (eg, TB test)?", "options": ["Intradermal", "Intramuscular", "Intravenous", "Intraosseous"], "answer": ["A"], "rationale": "Intradermal administration is between epidermis and dermis with limited systemic absorption; used for tests like PPD."}, {"id": 34, "type": "mc", "stem": "A nurse is caring for a client with severe peripheral arterial disease and a toe infection. Which pharmacokinetic concept best explains why antibiotics may be less effective in the toe?", "options": ["Decreased distribution due to reduced blood flow", "Increased absorption due to high bioavailability", "Increased metabolism due to CYP induction", "Increased excretion due to high GFR"], "answer": ["A"], "rationale": "Distribution depends on adequate blood flow to deliver the drug to target tissues; blocked vessels can limit delivery."}, {"id": 35, "type": "mc", "stem": "A malnourished client has a very low albumin level. Which medication effect is most likely?", "options": ["Increased free drug leading to higher risk of toxicity", "Decreased free drug leading to no therapeutic effect", "Decreased absorption of IV medications", "Faster excretion of all drugs through the kidneys"], "answer": ["A"], "rationale": "Many drugs bind plasma proteins such as albumin. Low albumin means fewer binding sites, increasing free (active) drug and toxicity risk."}, {"id": 36, "type": "calc", "stem": "A nurse administers metoprolol tartrate 50 mg. The half-life is 3 hours. How many milligrams remain after 12 hours? (Round to three decimals.)", "answer": ["3.125"], "rationale": "12 hours is four half-lives (12/3=4). 50 -> 25 -> 12.5 -> 6.25 -> 3.125 mg."}, {"id": 37, "type": "mc", "stem": "Which lab is highlighted in the materials as the gold standard indicator of kidney function for drug excretion concerns?", "options": ["Creatinine", "Blood urea nitrogen (BUN) only", "Sodium", "Hemoglobin"], "answer": ["A"], "rationale": "Creatinine is emphasized as the gold standard for kidney function; BUN can be elevated for other reasons."}, {"id": 38, "type": "mc", "stem": "A client has an eGFR of 25 mL/min. Which nursing implication is most important related to medication therapy?", "options": ["Increased risk of drug toxicity due to impaired excretion; assess and anticipate dose adjustments.", "Decreased risk of toxicity because drugs clear faster.", "Increased drug metabolism in the liver.", "Increased bioavailability of intradermal medications."], "answer": ["A"], "rationale": "Reduced GFR indicates impaired renal excretion, increasing risk for accumulation and toxicity; nurses should assess labs and advocate for dosing changes."}, {"id": 39, "type": "mc", "stem": "A client asks, \"What is pharmacodynamics?\" Which response is best?", "options": ["\"It is what the drug does to the body, including the mechanism of action.\"", "\"It is how the body absorbs, distributes, metabolizes, and excretes the drug.\"", "\"It is the study of kidney clearance of drugs.\"", "\"It is the process of writing a prescription.\""], "answer": ["A"], "rationale": "Pharmacodynamics is what the drug does to the body (mechanism of action). Pharmacokinetics is what the body does to the drug (ADME)."}, {"id": 40, "type": "mc", "stem": "A medication binds to a receptor and blocks the normal body process from occurring. The medication is a(n):", "options": ["Antagonist", "Agonist", "Prodrug", "Metabolite"], "answer": ["A"], "rationale": "An antagonist blocks a receptor responsible for an existing body process."}, {"id": 41, "type": "mc", "stem": "A client with migraine with aura describes flashing zigzag lines followed by unilateral throbbing headache and nausea. Which treatment plan aligns with the materials for abortive therapy?", "options": ["Take sumatriptan at the first sign of the migraine/aura as a PRN abortive medication.", "Take topiramate only during an active migraine attack.", "Take celecoxib daily only during migraine weeks.", "Take naloxone at the first sign of a headache."], "answer": ["A"], "rationale": "Triptans such as sumatriptan are abortive medications taken at the first sign (including aura) to stop an active migraine."}, {"id": 42, "type": "sata", "stem": "Which patients are NOT good candidates for sumatriptan (triptans) based on contraindications described in the materials? Select all that apply.", "options": ["Client with hypertension", "Client with coronary artery disease", "Client with peripheral vascular disease", "Client who is pregnant or planning pregnancy", "Client with migraine without aura and no cardiovascular history"], "answer": ["A", "B", "C", "D"], "rationale": "Triptans can cause coronary vasoconstriction and are contraindicated in cardiovascular disease including hypertension and vessel narrowing (CAD/PVD). They are also not appropriate in pregnancy/planning pregnancy due to teratogenicity in these materials."}, {"id": 43, "type": "mc", "stem": "A client takes their usual dose of sumatriptan and it fails to abort their migraine on three separate occasions. What is the best next step?", "options": ["Notify the health care provider for a new plan.", "Double the dose for the next migraine.", "Start taking sumatriptan daily to prevent migraines.", "Switch to aspirin daily."], "answer": ["A"], "rationale": "Teaching includes that if the usual triptan dose fails three times (on separate migraines), the client should notify the provider; repeat dosing per migraine is discouraged due to vasoconstriction risk."}, {"id": 44, "type": "mc", "stem": "A client is prescribed topiramate for migraine prevention. Which statement indicates the client needs further teaching?", "options": ["\"I will take it every day even if I do not have a migraine.\"", "\"If I have a migraine, I will take an abortive medication rather than extra topiramate.\"", "\"Because this is for prevention, I will only take it when an aura starts.\"", "\"I will call my provider if I need abortive meds more than once a week.\""], "answer": ["C"], "rationale": "Topiramate is a daily scheduled preventive medication, not PRN at aura onset. Abortive meds are used for active migraines."}, {"id": 45, "type": "sata", "stem": "Which are appropriate nursing priorities for a client taking topiramate for migraine prevention? Select all that apply.", "options": ["Perform neurological assessment and assess migraine frequency/need for abortive meds.", "Monitor for CNS-related side effects impacting safety (drowsiness, impaired concentration).", "Obtain routine topiramate therapeutic levels for migraine prevention.", "Reinforce safety precautions if dizziness or sedation occurs.", "Teach that taking extra doses during a migraine will abort it faster."], "answer": ["A", "B", "D"], "rationale": "Topiramate prevention focuses on neuro assessment and monitoring CNS side effects for safety. Therapeutic levels are not required for migraine prevention in these materials, and extra doses during a migraine are not recommended."}, {"id": 46, "type": "ordered", "stem": "A client with asthma is prescribed ibuprofen for fever. The client develops wheezing shortly after the first dose. Place the nursing actions in priority order. (1 = first, 4 = last)", "steps": ["Assess airway, breathing, and oxygenation; obtain vital signs and lung sounds.", "Stop further NSAID dosing and notify the provider.", "Provide or prepare prescribed respiratory support (eg, oxygen/bronchodilator per orders) based on assessment.", "Educate the client to use acetaminophen instead of NSAIDs in the future unless directed otherwise."], "answer_order": [1, 3, 2, 4], "rationale": "First assess ABCs, then intervene to support breathing, then ensure the offending medication is held and provider notified, then provide education after stabilization."}, {"id": 47, "type": "mc", "stem": "A provider writes: \"Ibuprofen 400 mg PO q6h PRN\" but no indication is listed. What is the nurse's best action?", "options": ["Clarify the order, because PRN orders require an indication.", "Administer for any complaint without additional assessment.", "Refuse to administer any PRN medications ever.", "Convert the order to acetaminophen automatically."], "answer": ["A"], "rationale": "PRN orders require an indication (eg, PRN mild pain or fever). The nurse should clarify for safe administration."}, {"id": 48, "type": "sata", "stem": "The nurse is preparing discharge teaching for a client prescribed scheduled gabapentin for nerve pain. Which points should be included? Select all that apply.", "options": ["Expect possible dizziness and drowsiness, especially when starting therapy.", "Do not drive or operate heavy machinery until you know how the medication affects you.", "Therapeutic blood levels must be checked weekly for nerve pain management.", "This medication is typically taken daily on a schedule, not only when pain flares.", "Report excessive sedation that interferes with daily activities."], "answer": ["A", "B", "D", "E"], "rationale": "Gabapentin can cause dizziness/drowsiness; safety precautions are key. For pain management, it is a scheduled daily medication and does not require therapeutic level monitoring. Excess sedation should be reported."}, {"id": 49, "type": "mc", "stem": "A nurse is differentiating acute vs chronic pain during assessment. Which statement is accurate per the materials?", "options": ["Chronic pain lasts longer than 3 months and may not have a well-defined cause.", "Acute pain lasts longer than 3 months and serves no useful purpose.", "Chronic pain always has a clear reversible cause.", "Acute pain is never severe."], "answer": ["A"], "rationale": "Chronic pain is defined as lasting longer than 3 months, often without a well-defined cause, and can significantly impact quality of life."}, {"id": 50, "type": "mc", "stem": "Which sequence best matches the stages of nociceptive pain processing described in the materials?", "options": ["Transduction -> Transmission -> Perception -> Modulation", "Absorption -> Distribution -> Metabolism -> Excretion", "Onset -> Peak -> Duration -> Toxicity", "Efficacy -> Potency -> Therapeutic index -> Bioavailability"], "answer": ["A"], "rationale": "Nociceptive pain becomes a conscious experience through transduction, transmission, perception, and modulation."}];
const STORAGE_KEY = "nclex_painpharm_attempt_v1";

function defaultState(){
  return {
    startedAt: null,
    durationSec: 90*60,
    answers: {},
    flagged: {},
    submitted: false
  };
}

function loadState(){
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if(!raw) return defaultState();
    const s = JSON.parse(raw);
    return Object.assign(defaultState(), s);
  } catch(e) {
    return defaultState();
  }
}

function saveState(){
  localStorage.setItem(STORAGE_KEY, JSON.stringify(state));
}

function resetState(){
  localStorage.removeItem(STORAGE_KEY);
  state = defaultState();
}

let state = loadState();
let currentIndex = 0;
let tickHandle = null;

function fmtTime(sec){
  sec = Math.max(0, Math.floor(sec));
  const m = Math.floor(sec/60);
  const s = sec%60;
  return String(m).padStart(2,"0")+":"+String(s).padStart(2,"0");
}

function computeTimeLeft(){
  if(!state.startedAt) return state.durationSec;
  const elapsed = (Date.now() - state.startedAt)/1000;
  return state.durationSec - elapsed;
}

function answeredCount(){
  let c=0;
  for(const q of QUESTIONS){
    const a = state.answers[q.id];
    if(a==null) continue;
    if(q.type==="mc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="calc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="sata" && Array.isArray(a) && a.length>0) c++;
    else if(q.type==="ordered" && a && Array.isArray(a.order) && a.order.length===q.steps.length) c++;
  }
  return c;
}

function flaggedCount(){
  return Object.keys(state.flagged).length;
}

function isAnswered(q){
  const a = state.answers[q.id];
  if(a==null) return false;
  if(q.type==="mc" || q.type==="calc") return String(a).trim()!=="";
  if(q.type==="sata") return Array.isArray(a) && a.length>0;
  if(q.type==="ordered") return a && Array.isArray(a.order) && a.order.length===q.steps.length;
  return false;
}

function isCorrect(q){
  const a = state.answers[q.id];
  if(q.type==="calc"){
    const want = String(q.answer[0]).trim();
    const got = String(a ?? "").trim();
    const wantNum = Number(want);
    const gotNum = Number(got);
    if(!Number.isNaN(wantNum) && !Number.isNaN(gotNum)){
      return Math.abs(wantNum - gotNum) <= 0.001;
    }
    return got.toLowerCase() === want.toLowerCase();
  }
  if(q.type==="mc"){
    return String(a) === q.answer[0];
  }
  if(q.type==="sata"){
    const got = Array.isArray(a) ? a.slice().sort() : [];
    const want = q.answer.slice().sort();
    return JSON.stringify(got) === JSON.stringify(want);
  }
  if(q.type==="ordered"){
    const got = (a && Array.isArray(a.order)) ? a.order : [];
    const want = q.answer_order;
    return JSON.stringify(got) === JSON.stringify(want);
  }
  return false;
}

function buildNav(){
  const nav = document.getElementById("qnav");
  nav.innerHTML="";
  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const b = document.createElement("button");
    b.className="qbtn";
    b.textContent = String(i+1);
    b.addEventListener("click", ()=>{ currentIndex=i; render(); });
    nav.appendChild(b);
  }
}

function updateNavStyles(){
  const buttons = Array.from(document.querySelectorAll(".qbtn"));
  buttons.forEach((b, i)=>{
    const q = QUESTIONS[i];
    b.classList.toggle("active", i===currentIndex);
    b.classList.toggle("answered", isAnswered(q));
    b.classList.toggle("flagged", !!state.flagged[q.id]);
  });
}

function render(){
  const q = QUESTIONS[currentIndex];
  document.getElementById("headerTitle").textContent = `Question ${currentIndex+1}`;
  document.getElementById("curMeta").textContent = `${currentIndex+1} / ${QUESTIONS.length}`;
  document.getElementById("typeMeta").textContent = q.type.toUpperCase();
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
  document.getElementById("qTag").textContent = ({
    mc:"Multiple Choice",
    sata:"Select all that apply (SATA)",
    ordered:"Ordered response",
    calc:"Calculation / short answer"
  })[q.type] || q.type;

  document.getElementById("stem").textContent = q.stem;

  const area = document.getElementById("interaction");
  area.innerHTML = "";

  if(q.type==="mc" || q.type==="sata"){
    const wrap = document.createElement("div");
    wrap.className="choices";
    const current = state.answers[q.id] ?? (q.type==="sata" ? [] : "");
    q.options.forEach((opt, idx)=>{
      const letter = String.fromCharCode(65+idx);
      const id = `q${q.id}_${letter}`;
      const lab = document.createElement("label");
      lab.className="choice";
      const inp = document.createElement("input");
      inp.type = (q.type==="mc") ? "radio" : "checkbox";
      inp.name = `q${q.id}`;
      inp.id = id;
      inp.value = letter;
      if(q.type==="mc"){
        inp.checked = (current === letter);
      } else {
        inp.checked = Array.isArray(current) && current.includes(letter);
      }
      inp.addEventListener("change", ()=>{
        if(q.type==="mc"){
          state.answers[q.id] = letter;
        } else {
          const arr = new Set(Array.isArray(state.answers[q.id]) ? state.answers[q.id] : []);
          if(inp.checked) arr.add(letter); else arr.delete(letter);
          state.answers[q.id] = Array.from(arr);
        }
        saveState();
        renderMeta();
        updateNavStyles();
      });

      const txt = document.createElement("div");
      txt.innerHTML = `<strong>${letter}.</strong> ${opt}`;
      lab.appendChild(inp);
      lab.appendChild(txt);
      wrap.appendChild(lab);
    });
    area.appendChild(wrap);
  }

  if(q.type==="calc"){
    const box = document.createElement("div");
    box.className="calcBox";
    const inp = document.createElement("input");
    inp.type="text";
    inp.placeholder="Type your answer (e.g., Yes, No, 3.125)";
    inp.value = state.answers[q.id] ?? "";
    inp.addEventListener("input", ()=>{
      state.answers[q.id] = inp.value;
      saveState();
      renderMeta();
      updateNavStyles();
    });
    box.appendChild(inp);
    const hint = document.createElement("div");
    hint.className="note";
    hint.textContent = "Tip: For numeric answers, enter a number (decimals allowed). For Yes/No, type Yes or No.";
    box.appendChild(hint);
    area.appendChild(box);
  }

  if(q.type==="ordered"){
    const ordWrap = document.createElement("div");
    ordWrap.className="ordered";
    let cur = state.answers[q.id]?.order;
    if(!Array.isArray(cur) || cur.length !== q.steps.length){
      cur = Array.from({length:q.steps.length}, (_,i)=> i+1);
      state.answers[q.id] = {order:cur};
      saveState();
    }
    function renderSteps(){
      ordWrap.innerHTML="";
      cur.forEach((stepNum, pos)=>{
        const row = document.createElement("div");
        row.className="step";
        const handle = document.createElement("div");
        handle.className="handle";
        handle.textContent = String(pos+1);
        const txt = document.createElement("div");
        txt.className="txt";
        txt.textContent = q.steps[stepNum-1];
        const arrows = document.createElement("div");
        arrows.className="arrows";
        const up = document.createElement("button");
        up.textContent = "▲";
        up.disabled = pos===0;
        up.addEventListener("click", ()=>{
          const t = cur[pos-1]; cur[pos-1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        const dn = document.createElement("button");
        dn.textContent = "▼";
        dn.disabled = pos===cur.length-1;
        dn.addEventListener("click", ()=>{
          const t = cur[pos+1]; cur[pos+1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        arrows.appendChild(up);
        arrows.appendChild(dn);
        row.appendChild(handle);
        row.appendChild(txt);
        row.appendChild(arrows);
        ordWrap.appendChild(row);
      });
      const note = document.createElement("div");
      note.className="note";
      note.textContent = "Use the arrows to place the actions in correct order.";
      ordWrap.appendChild(note);
    }
    renderSteps();
    area.appendChild(ordWrap);
  }

  document.getElementById("prevBtn").disabled = currentIndex===0;
  document.getElementById("nextBtn").disabled = currentIndex===QUESTIONS.length-1;

  updateNavStyles();
  renderMeta();
}

function renderMeta(){
  document.getElementById("answeredCount").textContent = answeredCount();
  document.getElementById("flaggedCount").textContent = flaggedCount();
  const q = QUESTIONS[currentIndex];
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
}

function startTimer(){
  if(tickHandle) clearInterval(tickHandle);
  tickHandle = setInterval(()=>{
    const left = computeTimeLeft();
    document.getElementById("timer").textContent = fmtTime(left);
    if(left <= 0){
      clearInterval(tickHandle);
      tickHandle = null;
      submitExam(true);
    }
  }, 250);
}

function submitExam(auto=false){
  if(state.submitted) return;
  if(!auto){
    const ok = confirm("Submit now? You will see answers and rationales.");
    if(!ok) return;
  }
  state.submitted = true;
  saveState();

  let score=0;
  for(const q of QUESTIONS){
    if(isCorrect(q)) score++;
  }

  document.getElementById("exam").classList.add("hidden");
  document.getElementById("results").classList.remove("hidden");
  document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;

  const body = document.getElementById("resultsBody");
  body.innerHTML = `<p class="note">Auto-grading note: SATA requires an exact match. Ordered response requires the exact sequence. Calculations accept a small numeric tolerance (plus case-insensitive Yes/No).</p>`;

  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const ok = isCorrect(q);
    const div = document.createElement("div");
    div.className="resultItem";
    const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
    const your = state.answers[q.id];
    let yourTxt = "";
    let correctTxt = "";

    if(q.type==="mc"){
      yourTxt = your ? your : "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="sata"){
      yourTxt = (Array.isArray(your) && your.length) ? your.slice().sort().join(", ") : "(no answer)";
      correctTxt = q.answer.slice().sort().join(", ");
    } else if(q.type==="calc"){
      yourTxt = (your ?? "").toString().trim() || "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="ordered"){
      const y = (your && Array.isArray(your.order)) ? your.order.join("-") : "(no answer)";
      const c = q.answer_order.join("-");
      yourTxt = y;
      correctTxt = c;
    }

    div.innerHTML = `
      <div style="margin-bottom:6px;">
        ${badge}<strong>Q${i+1}.</strong> ${q.stem}
      </div>
      <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
      <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>
    `;
    body.appendChild(div);
  }

  body.insertAdjacentHTML("beforeend", `
    <div class="controls" style="margin-top:16px;">
      <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
      <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
    </div>
  `);
}

document.getElementById("startBtn").addEventListener("click", ()=>{
  if(state.submitted){
    alert("This attempt is already submitted. Use 'Reset Saved Attempt' to start over.");
    return;
  }
  if(!state.startedAt){
    state.startedAt = Date.now();
    saveState();
  }
  document.getElementById("start").classList.add("hidden");
  document.getElementById("exam").classList.remove("hidden");
  buildNav();
  render();
  document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
  startTimer();
});

document.getElementById("resetBtn").addEventListener("click", ()=>{
  const ok = confirm("Reset saved attempt? This clears answers and timer for this browser.");
  if(!ok) return;
  resetState();
  location.reload();
});

document.getElementById("prevBtn").addEventListener("click", ()=>{
  if(currentIndex>0) currentIndex--;
  render();
});
document.getElementById("nextBtn").addEventListener("click", ()=>{
  if(currentIndex<QUESTIONS.length-1) currentIndex++;
  render();
});
document.getElementById("flagBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  if(state.flagged[q.id]) delete state.flagged[q.id];
  else state.flagged[q.id]=true;
  saveState();
  renderMeta();
  updateNavStyles();
});
document.getElementById("clearBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  delete state.answers[q.id];
  if(q.type==="ordered"){
    state.answers[q.id] = {order: Array.from({length:q.steps.length}, (_,i)=> i+1)};
  }
  saveState();
  render();
});
document.getElementById("submitBtn").addEventListener("click", ()=> submitExam(false));

(function init(){
  if(state.submitted){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("results").classList.remove("hidden");
    let score=0;
    for(const q of QUESTIONS) if(isCorrect(q)) score++;
    document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;
    const body = document.getElementById("resultsBody");
    body.innerHTML = `<p class="note">This attempt was already submitted on this browser.</p>`;
    for(let i=0;i<QUESTIONS.length;i++){
      const q = QUESTIONS[i];
      const ok = isCorrect(q);
      const div = document.createElement("div");
      div.className="resultItem";
      const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
      const your = state.answers[q.id];
      let yourTxt="", correctTxt="";
      if(q.type==="mc"){ yourTxt = your ? your : "(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="sata"){ yourTxt=(Array.isArray(your)&&your.length)?your.slice().sort().join(", "):"(no answer)"; correctTxt=q.answer.slice().sort().join(", "); }
      else if(q.type==="calc"){ yourTxt=(your??"").toString().trim()||"(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="ordered"){ yourTxt=(your&&Array.isArray(your.order))?your.order.join("-"):"(no answer)"; correctTxt=q.answer_order.join("-"); }
      div.innerHTML = `<div style="margin-bottom:6px;">${badge}<strong>Q${i+1}.</strong> ${q.stem}</div>
        <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
        <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>`;
      body.appendChild(div);
    }
    body.insertAdjacentHTML("beforeend", `
      <div class="controls" style="margin-top:16px;">
        <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
        <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
      </div>
    `);
    return;
  }

  if(state.startedAt){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("exam").classList.remove("hidden");
    buildNav();
    render();
    document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
    startTimer();
  }
})();
</script>
</body>
</html>
[form_b.html](https://github.com/user-attachments/files/25405942/form_b.html)
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>NCLEX-Style Timed Exam — Form B (Balanced)</title>
<style>
  :root {
    --bg: #0b0f17;
    --panel: #121a29;
    --panel2: #0f1624;
    --text: #e8edf7;
    --muted: #a8b3c7;
    --accent: #5dd6ff;
    --danger: #ff5d7a;
    --ok: #52ffa8;
    --border: rgba(255,255,255,.10);
  }
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Segoe UI", Roboto, Helvetica, Arial, system-ui, sans-serif;
    background: radial-gradient(1200px 700px at 15% 10%, rgba(93,214,255,.12), transparent 60%),
                radial-gradient(900px 600px at 85% 25%, rgba(82,255,168,.10), transparent 65%),
                var(--bg);
    color: var(--text);
  }
  a { color: var(--accent); }
  .wrap {
    max-width: 1200px;
    margin: 0 auto;
    padding: 18px;
  }
  .card {
    background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
    border: 1px solid var(--border);
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0,0,0,.35);
    overflow: hidden;
  }
  .topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    padding: 14px 16px;
    background: rgba(0,0,0,.18);
    border-bottom: 1px solid var(--border);
  }
  .title {
    font-weight: 700;
    letter-spacing: .2px;
  }
  .pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 12px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.7);
    color: var(--muted);
    font-size: 13px;
    white-space: nowrap;
  }
  .timer {
    font-variant-numeric: tabular-nums;
    color: var(--text);
    font-weight: 700;
  }
  .grid {
    display: grid;
    grid-template-columns: 300px 1fr;
    min-height: 72vh;
  }
  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; }
  }
  .sidebar {
    padding: 14px;
    background: rgba(18,26,41,.35);
    border-right: 1px solid var(--border);
  }
  @media (max-width: 900px) {
    .sidebar {
      border-right: 0;
      border-bottom: 1px solid var(--border);
    }
  }
  .qnav {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    gap: 8px;
  }
  .qbtn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.6);
    color: var(--text);
    border-radius: 10px;
    padding: 10px 0;
    font-weight: 700;
    cursor: pointer;
    transition: transform .05s ease, background .2s ease, border-color .2s ease;
  }
  .qbtn:hover { transform: translateY(-1px); border-color: rgba(93,214,255,.55); }
  .qbtn.active { background: rgba(93,214,255,.18); border-color: rgba(93,214,255,.65); }
  .qbtn.answered { background: rgba(82,255,168,.12); border-color: rgba(82,255,168,.35); }
  .qbtn.flagged { background: rgba(255,93,122,.14); border-color: rgba(255,93,122,.45); }
  .sidebar .meta {
    margin-top: 14px;
    display: grid;
    gap: 10px;
  }
  .metaRow {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 13px;
    color: var(--muted);
  }
  .main {
    padding: 18px;
  }
  .stem {
    font-size: 18px;
    line-height: 1.35;
    margin: 0 0 14px 0;
  }
  .tag {
    font-size: 12px;
    color: var(--muted);
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    display: inline-block;
    padding: 6px 10px;
    border-radius: 999px;
    margin-bottom: 10px;
  }
  .choices {
    display: grid;
    gap: 10px;
  }
  label.choice {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    padding: 12px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
    cursor: pointer;
  }
  label.choice:hover {
    border-color: rgba(93,214,255,.55);
    background: rgba(15,22,36,.72);
  }
  input[type="radio"], input[type="checkbox"] {
    margin-top: 2px;
    accent-color: var(--accent);
  }
  .controls {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 16px;
  }
  button.btn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    border-radius: 12px;
    padding: 10px 12px;
    font-weight: 700;
    cursor: pointer;
  }
  button.btn:hover { border-color: rgba(93,214,255,.55); }
  button.primary {
    background: rgba(93,214,255,.18);
    border-color: rgba(93,214,255,.55);
  }
  button.danger {
    background: rgba(255,93,122,.14);
    border-color: rgba(255,93,122,.55);
  }
  button.ok {
    background: rgba(82,255,168,.12);
    border-color: rgba(82,255,168,.45);
  }
  .note {
    color: var(--muted);
    font-size: 13px;
    line-height: 1.35;
  }
  .startScreen {
    max-width: 860px;
    margin: 30px auto;
    padding: 18px;
  }
  .startScreen h1 {
    margin: 0 0 6px 0;
    font-size: 28px;
  }
  .startScreen ul {
    margin: 10px 0 0 18px;
    color: var(--muted);
    line-height: 1.5;
  }
  .hidden { display: none; }
  .calcBox {
    display: grid;
    gap: 10px;
  }
  .calcBox input {
    width: 240px;
    max-width: 100%;
    padding: 12px;
    border-radius: 12px;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    color: var(--text);
    font-size: 16px;
  }
  .ordered {
    display: grid;
    gap: 10px;
  }
  .step {
    display: flex;
    gap: 10px;
    align-items: center;
    padding: 10px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
  }
  .step .handle {
    width: 26px;
    height: 26px;
    border-radius: 8px;
    border: 1px solid var(--border);
    display: grid;
    place-items: center;
    color: var(--muted);
    font-weight: 700;
  }
  .step .txt {
    flex: 1;
    line-height: 1.3;
  }
  .step .arrows button {
    margin-left: 6px;
    padding: 6px 8px;
    border-radius: 10px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    cursor: pointer;
  }
  .results h2 {
    margin: 0 0 6px 0;
  }
  .resultItem {
    padding: 12px 12px;
    border: 1px solid var(--border);
    border-radius: 14px;
    background: rgba(15,22,36,.55);
    margin: 10px 0;
  }
  .badge {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 999px;
    font-size: 12px;
    font-weight: 800;
    border: 1px solid var(--border);
    margin-right: 8px;
  }
  .badge.ok { color: var(--ok); border-color: rgba(82,255,168,.35); background: rgba(82,255,168,.12); }
  .badge.no { color: var(--danger); border-color: rgba(255,93,122,.45); background: rgba(255,93,122,.14); }
  .rationale {
    color: var(--muted);
    margin-top: 8px;
    line-height: 1.35;
  }
</style>
</head>
<body>
<div id="start" class="wrap startScreen">
  <div class="card">
    <div class="topbar">
      <div class="title">NCLEX-Style Timed Exam - Pain & Pharmacology (50 Questions)</div>
      <div class="pill"><span>Time:</span> <span class="timer">90:00</span></div>
    </div>
    <div style="padding:16px 18px;">
      <h1>NCLEX-Style Timed Exam — Form B (Balanced)</h1>
      <div class="note">
        <ul>
          <li>This exam runs fully in your browser (works well on a Mac).</li>
          <li>Question types include Multiple Choice, Select-All-That-Apply (SATA), Ordered Response, and Calculations.</li>
          <li>Use the sidebar to jump between questions. You can flag questions for review.</li>
          <li>Your progress is saved automatically in this browser.</li>
          <li>When you submit, you'll see your score plus the answer key and rationales.</li>
        </ul>
      </div>
      <div class="controls" style="margin-top:16px;">
        <button class="btn primary" id="startBtn">Start Exam</button>
        <button class="btn" id="resetBtn">Reset Saved Attempt</button>
      </div>
      <div class="note" style="margin-top:10px;">Tip: For best timing accuracy, keep this tab open during the exam.</div>
    </div>
  </div>
</div>

<div id="exam" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title" id="headerTitle">Question</div>
      <div style="display:flex; gap:10px; align-items:center;">
        <div class="pill"><span>Answered:</span> <span id="answeredCount">0</span>/50</div>
        <div class="pill"><span>Flagged:</span> <span id="flaggedCount">0</span></div>
        <div class="pill"><span>Time Left:</span> <span class="timer" id="timer">90:00</span></div>
      </div>
    </div>

    <div class="grid">
      <div class="sidebar">
        <div class="qnav" id="qnav"></div>
        <div class="meta">
          <div class="metaRow"><span>Current</span><span id="curMeta">1 / 50</span></div>
          <div class="metaRow"><span>Type</span><span id="typeMeta">MC</span></div>
          <div class="metaRow"><span>Status</span><span id="statusMeta">Not answered</span></div>
        </div>
        <div class="controls" style="margin-top:12px;">
          <button class="btn" id="flagBtn">Flag / Unflag</button>
          <button class="btn" id="clearBtn">Clear Answer</button>
          <button class="btn danger" id="submitBtn">Submit Exam</button>
        </div>
      </div>

      <div class="main">
        <div class="tag" id="qTag">Type</div>
        <p class="stem" id="stem"></p>
        <div id="interaction"></div>

        <div class="controls">
          <button class="btn" id="prevBtn">Previous</button>
          <button class="btn primary" id="nextBtn">Next</button>
        </div>
        <div class="note" style="margin-top:10px;">Exam note: Answer key and rationales appear after submission.</div>
      </div>
    </div>
  </div>
</div>

<div id="results" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title">Results</div>
      <div class="pill"><span>Score:</span> <span class="timer" id="scoreText">0/50</span></div>
    </div>
    <div class="main results" id="resultsBody"></div>
  </div>
</div>

<script>
const QUESTIONS = [{"id": 1, "type": "mc", "stem": "A client with chronic kidney disease (eGFR 25 mL/min) requests ibuprofen for back pain. Which provider order should the nurse question?", "options": ["Ibuprofen 600 mg PO every 6 hours PRN pain", "Acetaminophen 650 mg PO every 6 hours PRN pain (max daily dose per policy)", "Nonpharmacologic heat/ice per comfort protocol", "Topical lidocaine patch per order"], "answer": "Ibuprofen 600 mg PO every 6 hours PRN pain", "rationale": "First‑generation NSAIDs increase risk for renal impairment and can worsen kidney function; an NSAID order is most concerning in a client with significant renal impairment."}, {"id": 2, "type": "sata", "stem": "A nurse is teaching a client starting tramadol for acute pain. Which instructions should the nurse include? Select all that apply.", "options": ["Avoid driving or operating machinery until you know how the medication affects you.", "Increase fiber/fluid and consider a stool softener to prevent constipation.", "Take the medication with alcohol to enhance pain relief.", "Report slowed breathing or extreme sleepiness immediately.", "Stop the medication abruptly once pain improves to prevent dependence."], "answer": ["Avoid driving or operating machinery until you know how the medication affects you.", "Increase fiber/fluid and consider a stool softener to prevent constipation.", "Report slowed breathing or extreme sleepiness immediately."], "rationale": "Tramadol can cause sedation/dizziness, respiratory depression, and constipation. Alcohol increases CNS/respiratory depression risk. Abrupt stopping is not a teaching point for short-term PRN use; safety and adverse effect monitoring are priorities."}, {"id": 3, "type": "mc", "stem": "A client is prescribed sumatriptan for migraines. Which history finding is most important to report to the provider before administration?", "options": ["Migraine occurs 3 times per month", "Hypertension and coronary artery disease", "Photophobia during migraine attacks", "Nausea with vomiting during migraines"], "answer": "Hypertension and coronary artery disease", "rationale": "Triptans can cause coronary vasoconstriction and are contraindicated/used with extreme caution in cardiovascular disease and uncontrolled hypertension."}, {"id": 4, "type": "mc", "stem": "A client taking gabapentin for neuropathic pain says, “I don’t want this because there’s no therapeutic level drawn.” Which is the best nurse response?", "options": ["Therapeutic levels are only drawn for medications that cause kidney toxicity.", "Gabapentin used for pain does not require a therapeutic serum level; we monitor symptom relief and side effects.", "If no level is drawn, the medication is not safe to take.", "Therapeutic levels are required only for controlled substances."], "answer": "Gabapentin used for pain does not require a therapeutic serum level; we monitor symptom relief and side effects.", "rationale": "Gabapentin (for nerve pain) typically does not require therapeutic drug monitoring; nursing focuses on indication, symptom response, and CNS side effects like dizziness/drowsiness."}, {"id": 5, "type": "mc", "stem": "A postoperative client received IV hydromorphone. Which assessment finding requires the most immediate nursing action?", "options": ["Respiratory rate 8/min and difficult to arouse", "Pruritus and nausea", "Constipation for 2 days", "Pain score decreased from 9/10 to 4/10"], "answer": "Respiratory rate 8/min and difficult to arouse", "rationale": "Opioid‑induced respiratory depression and decreased LOC are life‑threatening and require immediate intervention (airway support, hold opioid, notify provider, consider naloxone per protocol)."}, {"id": 6, "type": "calc", "stem": "Half‑life calculation: A client receives metoprolol tartrate 50 mg. The half‑life is 3 hours. How many mg remain after 12 hours? (Enter a number; no rounding.)", "answer": ["3.125"], "rationale": "Every 3 hours the amount halves: 50 → 25 (3h) → 12.5 (6h) → 6.25 (9h) → 3.125 (12h)."}, {"id": 7, "type": "calc", "stem": "Half‑life calculation: Ibuprofen 200 mg has a half‑life of 2 hours. How many mg remain after 10 hours? (Enter a number; no rounding.)", "answer": ["6.25"], "rationale": "10 hours is five half‑lives (2h each): 200 → 100 → 50 → 25 → 12.5 → 6.25 mg."}, {"id": 8, "type": "mc", "stem": "A nurse is reviewing an order: “Morphine 2 mg IV now PRN severe pain.” Which additional element must be present for a safe PRN order?", "options": ["A stop date only", "An indication (e.g., PRN severe pain)", "A refill number", "A brand name medication"], "answer": "An indication (e.g., PRN severe pain)", "rationale": "PRN medication orders must include a clear indication for use to guide safe administration and evaluation."}, {"id": 9, "type": "sata", "stem": "Which client findings increase risk for drug toxicity due to altered protein binding? Select all that apply.", "options": ["Albumin 2.2 g/dL", "Poor nutrition with low protein intake", "Creatinine within expected range", "Cirrhosis with decreased albumin production", "High albumin level"], "answer": ["Albumin 2.2 g/dL", "Poor nutrition with low protein intake", "Cirrhosis with decreased albumin production"], "rationale": "Low albumin (from liver impairment or poor nutrition) reduces protein binding, increasing free drug and risk of excessive effect/toxicity."}, {"id": 10, "type": "mc", "stem": "A client takes acetaminophen for pain. Which statement by the client indicates correct understanding of a key safety risk?", "options": ["I should take it on an empty stomach for faster absorption.", "It can cause liver damage if I take too much or if I have liver disease.", "It will reduce inflammation better than ibuprofen.", "It increases bleeding risk, so I’ll avoid it with anticoagulants."], "answer": "It can cause liver damage if I take too much or if I have liver disease.", "rationale": "Acetaminophen’s major dose‑related toxicity is hepatotoxicity; it is not a meaningful anti‑inflammatory and does not have the same platelet effects as NSAIDs."}, {"id": 11, "type": "mc", "stem": "A client reports ringing in the ears after taking high doses of aspirin. Which interpretation is most accurate?", "options": ["Expected anticholinergic effect", "Sign of salicylate toxicity", "Sign of opioid withdrawal", "Indicates therapeutic effect reached"], "answer": "Sign of salicylate toxicity", "rationale": "Tinnitus can be an early sign of salicylate (aspirin) toxicity and should be reported."}, {"id": 12, "type": "mc", "stem": "A client with asthma asks for ibuprofen for a fever. Which is the best action?", "options": ["Administer ibuprofen; asthma is unrelated to NSAID use.", "Hold ibuprofen and notify the provider; NSAIDs can be contraindicated in asthma.", "Administer aspirin instead.", "Administer naproxen instead."], "answer": "Hold ibuprofen and notify the provider; NSAIDs can be contraindicated in asthma.", "rationale": "First‑generation NSAIDs can be contraindicated in clients with asthma due to risk of bronchospasm/worsening symptoms."}, {"id": 13, "type": "calc", "stem": "A client has been receiving a maintenance dose of a medication with a half‑life of 6 hours. Approximately how long will it take to reach steady state (plateau)? (Enter hours.)", "answer": ["24"], "rationale": "Steady state is reached after ~4 half‑lives. 4 × 6 hours = 24 hours."}, {"id": 14, "type": "mc", "stem": "A nurse is caring for a client with severe pain. Which opioid is typically dosed in micrograms due to high potency?", "options": ["Morphine", "Hydromorphone", "Fentanyl", "Codeine"], "answer": "Fentanyl", "rationale": "Fentanyl is highly potent and commonly ordered in micrograms, reflecting potency differences across opioids."}, {"id": 15, "type": "sata", "stem": "A nurse is preparing to administer naloxone for suspected opioid overdose. Which findings support this intervention? Select all that apply.", "options": ["Pinpoint pupils", "Respiratory rate 6/min", "Severe hypertension and agitation after recent stimulant use", "Unresponsive to verbal stimuli", "Watery eyes and yawning with normal respirations"], "answer": ["Pinpoint pupils", "Respiratory rate 6/min", "Unresponsive to verbal stimuli"], "rationale": "Opioid overdose commonly presents with miosis, respiratory depression, and decreased LOC. Watery eyes/yawning may indicate withdrawal; hypertension/agitation suggests other causes."}, {"id": 16, "type": "ordered", "stem": "Place the following actions in priority order for a client with suspected opioid overdose. (1 = first, 5 = last)", "steps": ["Assess airway and breathing; apply oxygen as needed.", "Call for help/activate rapid response per facility policy.", "Check responsiveness, pulse, and obtain vital signs.", "Prepare and administer naloxone per protocol.", "Reassess respiratory status and level of consciousness; anticipate repeat dosing and monitor for recurrence."], "answer_order": [3, 2, 1, 4, 5], "rationale": "Initial assessment of responsiveness/vitals occurs immediately, while calling for help and addressing airway/breathing are priorities; naloxone follows confirmation of opioid toxidrome, and reassessment is ongoing."}, {"id": 17, "type": "mc", "stem": "A client with peptic ulcer disease asks which OTC medication is safest for fever. Which is best?", "options": ["Ibuprofen", "Naproxen", "Acetaminophen", "Aspirin"], "answer": "Acetaminophen", "rationale": "NSAIDs increase risk for GI ulceration and bleeding; acetaminophen is preferred for pain/fever when GI bleeding risk is present (within safe dosing limits)."}, {"id": 18, "type": "calc", "stem": "Half‑life calculation: Sumatriptan 20 mg (nasal) has a half‑life of 15 minutes. How many mg remain after 60 minutes? (Enter a number; no rounding.)", "answer": ["1.25"], "rationale": "60 minutes is four half‑lives (15 min each): 20 → 10 → 5 → 2.5 → 1.25 mg."}, {"id": 19, "type": "mc", "stem": "A client has an active migraine with aura and requests the best timing for an abortive medication. Which teaching is correct?", "options": ["Take it only after the headache is at maximum intensity.", "Take it at the first sign of migraine, including aura symptoms.", "Take it daily to prevent future migraines.", "Take it only at bedtime to avoid side effects."], "answer": "Take it at the first sign of migraine, including aura symptoms.", "rationale": "Abortive therapy works best when taken early—at the first sign of migraine (including aura)."}, {"id": 20, "type": "mc", "stem": "A client reports migraines occurring 3 times per week that interfere with ADLs and are not relieved with abortive therapy. Which medication approach is most appropriate?", "options": ["Start a daily preventative medication such as topiramate.", "Increase the frequency of triptan use to daily.", "Avoid medications and use only dark rooms.", "Switch to aspirin daily."], "answer": "Start a daily preventative medication such as topiramate.", "rationale": "Frequent migraines (>2/week) that impair ADLs and are not relieved with acute therapy warrant daily preventative therapy (e.g., topiramate)."}, {"id": 21, "type": "sata", "stem": "The nurse is teaching a client about cyclobenzaprine. Which expected side effects should be included? Select all that apply.", "options": ["Drowsiness", "Muscle weakness", "Dry mouth", "Severe respiratory depression as the most common effect", "Dizziness"], "answer": ["Drowsiness", "Muscle weakness", "Dry mouth", "Dizziness"], "rationale": "Cyclobenzaprine commonly causes dizziness/drowsiness and anticholinergic effects (e.g., dry mouth) and may contribute to muscle weakness; severe respiratory depression is not the most common adverse effect."}, {"id": 22, "type": "mc", "stem": "A client with heart failure asks for naproxen sodium for joint pain. Which is the best response?", "options": ["It is safe because it is an OTC medication.", "It can worsen heart failure due to sodium and fluid retention; ask the provider about alternatives.", "It is preferred over acetaminophen for heart failure.", "Take it on an empty stomach for best effect."], "answer": "It can worsen heart failure due to sodium and fluid retention; ask the provider about alternatives.", "rationale": "Many first‑generation NSAIDs (including naproxen sodium) can worsen hypertension/heart failure due to sodium content and fluid retention; alternatives may be safer."}, {"id": 23, "type": "mc", "stem": "A client is prescribed an oral medication known to undergo significant first‑pass metabolism. Which alternative route would best bypass first‑pass effect?", "options": ["Oral tablet", "Rectal suppository", "Sublingual administration", "Enteral feeding tube"], "answer": "Sublingual administration", "rationale": "Sublingual administration bypasses the GI tract and hepatic first‑pass metabolism via absorption through oral mucosa into systemic circulation."}, {"id": 24, "type": "mc", "stem": "A nurse is evaluating medication effectiveness. Which statement best describes efficacy?", "options": ["How quickly the medication begins to work", "The largest effect a medication can produce", "The amount of medication needed to produce an effect", "How much of the medication reaches the bloodstream"], "answer": "The largest effect a medication can produce", "rationale": "Efficacy refers to the maximal effect a drug can produce (height of the dose‑response curve)."}, {"id": 25, "type": "mc", "stem": "A nurse explains potency to a client comparing morphine to hydromorphone. Which statement is best?", "options": ["Potency describes the maximum effect the drug can produce.", "A more potent drug requires a smaller dose to produce a desired effect.", "Potency means the drug has fewer side effects.", "Potency is the same as bioavailability."], "answer": "A more potent drug requires a smaller dose to produce a desired effect.", "rationale": "Potency refers to the amount of drug required to produce an effect; higher potency means less drug is needed for the same effect."}, {"id": 26, "type": "sata", "stem": "A nurse is reviewing a medication list for potential risk of excessive free drug effect. Which conditions support this concern? Select all that apply.", "options": ["Albumin 2.0 g/dL", "Severe dehydration", "Normal liver function tests", "Advanced cirrhosis", "High-protein diet with albumin 4.5 g/dL"], "answer": ["Albumin 2.0 g/dL", "Advanced cirrhosis"], "rationale": "Low albumin—often from liver impairment or malnutrition—reduces protein binding, increasing free drug and risk for toxicity."}, {"id": 27, "type": "mc", "stem": "A client has status migrainosus lasting longer than 72 hours with poor oral intake. Which complication is the nurse most concerned about?", "options": ["Hyperkalemia from excess intake", "Fluid and electrolyte imbalance from dehydration", "Hypoglycemia from insulin overdose", "Respiratory depression from triptans"], "answer": "Fluid and electrolyte imbalance from dehydration", "rationale": "Migraines lasting >72 hours can impair hydration and nutrition, raising risk for dehydration and electrolyte imbalance."}, {"id": 28, "type": "calc", "stem": "A client received acetaminophen 1,000 mg at 0800, 1,000 mg at 1400, and 1,000 mg at 2000. The provider writes: “acetaminophen 650 mg PO now at 2300.” Using an adult max of 4,000 mg/24 hr, is it safe? (Answer Yes or No.)", "answer": ["Yes"], "rationale": "Total so far = 3,000 mg. Adding 650 mg = 3,650 mg in 24 hours, which is under 4,000 mg (assuming no liver disease/other combo products)."}, {"id": 29, "type": "mc", "stem": "Which opioid adverse effect is most important to anticipate and prevent in all clients receiving around‑the‑clock opioids?", "options": ["Constipation", "Miosis", "Pruritus", "Urinary retention"], "answer": "Constipation", "rationale": "Constipation is predictable with opioid therapy; prophylaxis (bowel regimen, fluids/fiber as appropriate) is standard. Other effects may occur but are not as universal."}, {"id": 30, "type": "mc", "stem": "A client taking oxycodone/APAP for pain asks why they must avoid other acetaminophen products. Best explanation?", "options": ["Because acetaminophen causes kidney failure first.", "Because combining products can exceed the safe daily maximum and cause hepatotoxicity.", "Because acetaminophen cancels the opioid effect.", "Because acetaminophen causes severe hypertension."], "answer": "Because combining products can exceed the safe daily maximum and cause hepatotoxicity.", "rationale": "Combination opioid/APAP products increase risk of accidental acetaminophen overdose leading to liver toxicity; clients must track total daily acetaminophen."}, {"id": 31, "type": "sata", "stem": "Which nursing assessments are most appropriate before administering a PRN opioid for severe pain? Select all that apply.", "options": ["Respiratory rate and oxygen saturation", "Level of consciousness/sedation level", "Pain assessment (location, quality, intensity, timing)", "Apical pulse for 1 full minute only", "Bowel sounds only"], "answer": ["Respiratory rate and oxygen saturation", "Level of consciousness/sedation level", "Pain assessment (location, quality, intensity, timing)"], "rationale": "Before giving opioids, assess pain and baseline respiratory/mental status to reduce risk for respiratory depression and oversedation."}, {"id": 32, "type": "mc", "stem": "A nurse is caring for a client receiving multiple medications. Which statement best defines pharmacokinetics?", "options": ["What the drug does to the body", "What the body does to the drug (ADME)", "The maximum effect a drug can produce", "The safest dose range of a drug"], "answer": "What the body does to the drug (ADME)", "rationale": "Pharmacokinetics describes absorption, distribution, metabolism, and excretion—what the body does to the drug."}, {"id": 33, "type": "mc", "stem": "A client has liver impairment with elevated ALT/AST and low albumin. Why is this clinically important for medication administration?", "options": ["The client will metabolize drugs faster and need higher doses.", "The client is at increased risk for drug toxicity due to delayed metabolism and more free drug.", "The client will excrete drugs faster via kidneys.", "The client will have fewer side effects from opioids."], "answer": "The client is at increased risk for drug toxicity due to delayed metabolism and more free drug.", "rationale": "Liver impairment can delay metabolism (prolonging half‑life) and reduce albumin (increasing free drug), both raising toxicity risk."}, {"id": 34, "type": "mc", "stem": "A nurse teaches about bioavailability. Which route has 100% bioavailability?", "options": ["Oral", "Intramuscular", "Intravenous", "Transdermal"], "answer": "Intravenous", "rationale": "IV administration delivers the entire dose directly into the bloodstream, giving 100% bioavailability."}, {"id": 35, "type": "mc", "stem": "A client with peripheral arterial disease has a toe infection. Which factor may reduce the effectiveness of antibiotics?", "options": ["Increased albumin levels", "Poor blood flow limiting distribution to the toe", "Increased gastric acid", "Rapid renal excretion"], "answer": "Poor blood flow limiting distribution to the toe", "rationale": "Distribution depends on adequate blood flow. Severe PAD can limit drug delivery to distal tissues like toes, reducing antibiotic effectiveness."}, {"id": 36, "type": "mc", "stem": "A nurse is caring for an older adult on multiple meds. Which age-related change increases risk for drug toxicity?", "options": ["Increased CYP activity", "Slower hepatic enzyme activity delaying metabolism", "Increased albumin production", "Increased renal clearance"], "answer": "Slower hepatic enzyme activity delaying metabolism", "rationale": "Geriatric enzyme systems slow, delaying metabolism and increasing toxicity risk; dosing may need adjustment."}, {"id": 37, "type": "mc", "stem": "Which description best matches therapeutic index?", "options": ["Time it takes for half the drug to be eliminated", "Comparison of therapeutic dose to toxic dose (safety)", "Amount of time to reach peak effect", "Percentage of drug that reaches the bloodstream"], "answer": "Comparison of therapeutic dose to toxic dose (safety)", "rationale": "Therapeutic index measures drug safety by comparing dose required for effect to dose that causes toxicity; narrow TI = higher toxicity risk."}, {"id": 38, "type": "sata", "stem": "Which medications/classes commonly warrant therapeutic drug monitoring due to narrow therapeutic index? Select all that apply.", "options": ["Certain anti-seizure (antiepileptic) medications", "Acetaminophen at normal doses", "Vancomycin (peak/trough in some cases)", "Topical lidocaine patches", "Some anticoagulants requiring lab monitoring"], "answer": ["Certain anti-seizure (antiepileptic) medications", "Vancomycin (peak/trough in some cases)", "Some anticoagulants requiring lab monitoring"], "rationale": "Narrow therapeutic index drugs often require monitoring to avoid toxicity—antiepileptics and some IV antibiotics (e.g., vancomycin) and certain anticoagulants with lab parameters are common examples."}, {"id": 39, "type": "mc", "stem": "A nurse is teaching a client about opioid safety at home. Which instruction is most important?", "options": ["Store opioids in an unlocked bathroom cabinet for easy access.", "Do not share the medication; keep it secured and dispose of leftovers properly.", "Take an extra dose if the pain returns within 30 minutes.", "Stop breathing exercises to avoid discomfort."], "answer": "Do not share the medication; keep it secured and dispose of leftovers properly.", "rationale": "Opioids should be secured, never shared, and disposed of safely to prevent misuse/overdose; extra doses increase risk for respiratory depression."}, {"id": 40, "type": "mc", "stem": "A client receiving naloxone begins vomiting and develops tachycardia. Which is the best nurse interpretation?", "options": ["Expected effects of naloxone; continue monitoring and provide supportive care.", "Allergic reaction; stop naloxone immediately.", "Indicates acetaminophen overdose.", "Indicates the opioid dose was too low."], "answer": "Expected effects of naloxone; continue monitoring and provide supportive care.", "rationale": "Naloxone can precipitate acute withdrawal-like symptoms (vomiting, tachycardia, hypertension, dysrhythmias). Monitor and manage airway/VS."}, {"id": 41, "type": "ordered", "stem": "A client reports new chest pain 10 minutes after taking sumatriptan. Place the nurse actions in priority order. (1 = first, 4 = last)", "steps": ["Stop further doses and assess vital signs and pain characteristics.", "Activate emergency response/notify provider and prepare for ECG per protocol.", "Place the client on oxygen if indicated and maintain IV access.", "Document findings and teaching about when to seek emergency care."], "answer_order": [1, 3, 2, 4], "rationale": "New chest pain after a triptan is concerning for coronary vasoconstriction/MI: assess immediately, support oxygenation/circulation, escalate care, and document/teach."}, {"id": 42, "type": "mc", "stem": "A client with suspected opioid toxicity is breathing 8/min. Which oxygen device is most appropriate to apply immediately while preparing further interventions?", "options": ["Nasal cannula at 1 L/min", "Venturi mask", "Non‑rebreather mask", "No oxygen; wait for naloxone"], "answer": "Non‑rebreather mask", "rationale": "In a respiratory emergency, provide high‑concentration oxygen (non‑rebreather) while addressing the underlying cause."}, {"id": 43, "type": "mc", "stem": "A nurse is deciding who to see first. Which client should be prioritized?", "options": ["Client requesting acetaminophen for a mild headache", "Client 1 hour post‑opioid with new confusion and RR 10/min", "Client with constipation after 3 days of opioids", "Client asking when the next dose of ibuprofen is due"], "answer": "Client 1 hour post‑opioid with new confusion and RR 10/min", "rationale": "Priority is the client with potential airway/breathing compromise and acute change in LOC after opioids."}, {"id": 44, "type": "sata", "stem": "A client is prescribed NSAIDs. Which findings/history increase risk for serious adverse effects? Select all that apply.", "options": ["History of gastrointestinal bleeding", "Heart failure", "Renal impairment", "Asthma", "Seasonal allergies only"], "answer": ["History of gastrointestinal bleeding", "Heart failure", "Renal impairment", "Asthma"], "rationale": "First‑generation NSAIDs can cause GI bleeding, worsen HF/HTN, worsen renal impairment, and may be contraindicated in asthma."}, {"id": 45, "type": "mc", "stem": "A nurse is preparing to administer ibuprofen. Which administration instruction is best to reduce GI irritation?", "options": ["Give with food or milk.", "Give only with water on an empty stomach.", "Crush and mix with grapefruit juice.", "Administer at bedtime only."], "answer": "Give with food or milk.", "rationale": "NSAIDs should be taken with food or milk to reduce gastric irritation and ulcer risk."}, {"id": 46, "type": "mc", "stem": "A client is receiving a medication that requires a trough level. When should the nurse plan to draw the trough?", "options": ["Immediately after the dose is infused", "Just before the next scheduled dose", "One hour after the next dose", "At the midpoint between doses"], "answer": "Just before the next scheduled dose", "rationale": "A trough is the lowest concentration and is drawn just before the next dose to guide dosing safely."}, {"id": 47, "type": "calc", "stem": "A medication has a half‑life of 8 hours. About how many hours until the drug is at its lowest concentration after stopping (≈5 half‑lives)? (Enter hours.)", "answer": ["40"], "rationale": "It takes ~5 half‑lives to reach minimal concentration after stopping: 5 × 8 = 40 hours."}, {"id": 48, "type": "mc", "stem": "A nurse reviews an order for aspirin for a 10‑year‑old with a viral illness. What is the best action?", "options": ["Administer as ordered.", "Question the order because aspirin is contraindicated in children.", "Give naproxen instead without notifying the provider.", "Give half the dose."], "answer": "Question the order because aspirin is contraindicated in children.", "rationale": "Aspirin is contraindicated in infants and children (risk of serious complications); the nurse should clarify the order."}, {"id": 49, "type": "mc", "stem": "A client says, “This drug is safer because it has a wide therapeutic window.” What does that mean?", "options": ["It is absorbed faster.", "There is a larger range between effective and toxic doses.", "It has a shorter half‑life.", "It is more potent."], "answer": "There is a larger range between effective and toxic doses.", "rationale": "A wide therapeutic window indicates a larger margin of safety between effective dose and toxic dose."}, {"id": 50, "type": "mc", "stem": "A nurse is reviewing a controlled substance prescription. Which agency regulates controlled substances in the U.S.?", "options": ["CDC", "DEA", "NIH", "OSHA"], "answer": "DEA", "rationale": "The Drug Enforcement Administration (DEA) enforces controlled substances laws and regulations."}];
const STORAGE_KEY = "nclex_painpharm_attempt_v1";

function defaultState(){
  return {
    startedAt: null,
    durationSec: 90*60,
    answers: {},
    flagged: {},
    submitted: false
  };
}

function loadState(){
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if(!raw) return defaultState();
    const s = JSON.parse(raw);
    return Object.assign(defaultState(), s);
  } catch(e) {
    return defaultState();
  }
}

function saveState(){
  localStorage.setItem(STORAGE_KEY, JSON.stringify(state));
}

function resetState(){
  localStorage.removeItem(STORAGE_KEY);
  state = defaultState();
}

let state = loadState();
let currentIndex = 0;
let tickHandle = null;

function fmtTime(sec){
  sec = Math.max(0, Math.floor(sec));
  const m = Math.floor(sec/60);
  const s = sec%60;
  return String(m).padStart(2,"0")+":"+String(s).padStart(2,"0");
}

function computeTimeLeft(){
  if(!state.startedAt) return state.durationSec;
  const elapsed = (Date.now() - state.startedAt)/1000;
  return state.durationSec - elapsed;
}

function answeredCount(){
  let c=0;
  for(const q of QUESTIONS){
    const a = state.answers[q.id];
    if(a==null) continue;
    if(q.type==="mc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="calc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="sata" && Array.isArray(a) && a.length>0) c++;
    else if(q.type==="ordered" && a && Array.isArray(a.order) && a.order.length===q.steps.length) c++;
  }
  return c;
}

function flaggedCount(){
  return Object.keys(state.flagged).length;
}

function isAnswered(q){
  const a = state.answers[q.id];
  if(a==null) return false;
  if(q.type==="mc" || q.type==="calc") return String(a).trim()!=="";
  if(q.type==="sata") return Array.isArray(a) && a.length>0;
  if(q.type==="ordered") return a && Array.isArray(a.order) && a.order.length===q.steps.length;
  return false;
}

function isCorrect(q){
  const a = state.answers[q.id];
  if(q.type==="calc"){
    const want = String(q.answer[0]).trim();
    const got = String(a ?? "").trim();
    const wantNum = Number(want);
    const gotNum = Number(got);
    if(!Number.isNaN(wantNum) && !Number.isNaN(gotNum)){
      return Math.abs(wantNum - gotNum) <= 0.001;
    }
    return got.toLowerCase() === want.toLowerCase();
  }
  if(q.type==="mc"){
    return String(a) === q.answer[0];
  }
  if(q.type==="sata"){
    const got = Array.isArray(a) ? a.slice().sort() : [];
    const want = q.answer.slice().sort();
    return JSON.stringify(got) === JSON.stringify(want);
  }
  if(q.type==="ordered"){
    const got = (a && Array.isArray(a.order)) ? a.order : [];
    const want = q.answer_order;
    return JSON.stringify(got) === JSON.stringify(want);
  }
  return false;
}

function buildNav(){
  const nav = document.getElementById("qnav");
  nav.innerHTML="";
  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const b = document.createElement("button");
    b.className="qbtn";
    b.textContent = String(i+1);
    b.addEventListener("click", ()=>{ currentIndex=i; render(); });
    nav.appendChild(b);
  }
}

function updateNavStyles(){
  const buttons = Array.from(document.querySelectorAll(".qbtn"));
  buttons.forEach((b, i)=>{
    const q = QUESTIONS[i];
    b.classList.toggle("active", i===currentIndex);
    b.classList.toggle("answered", isAnswered(q));
    b.classList.toggle("flagged", !!state.flagged[q.id]);
  });
}

function render(){
  const q = QUESTIONS[currentIndex];
  document.getElementById("headerTitle").textContent = `Question ${currentIndex+1}`;
  document.getElementById("curMeta").textContent = `${currentIndex+1} / ${QUESTIONS.length}`;
  document.getElementById("typeMeta").textContent = q.type.toUpperCase();
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
  document.getElementById("qTag").textContent = ({
    mc:"Multiple Choice",
    sata:"Select all that apply (SATA)",
    ordered:"Ordered response",
    calc:"Calculation / short answer"
  })[q.type] || q.type;

  document.getElementById("stem").textContent = q.stem;

  const area = document.getElementById("interaction");
  area.innerHTML = "";

  if(q.type==="mc" || q.type==="sata"){
    const wrap = document.createElement("div");
    wrap.className="choices";
    const current = state.answers[q.id] ?? (q.type==="sata" ? [] : "");
    q.options.forEach((opt, idx)=>{
      const letter = String.fromCharCode(65+idx);
      const id = `q${q.id}_${letter}`;
      const lab = document.createElement("label");
      lab.className="choice";
      const inp = document.createElement("input");
      inp.type = (q.type==="mc") ? "radio" : "checkbox";
      inp.name = `q${q.id}`;
      inp.id = id;
      inp.value = letter;
      if(q.type==="mc"){
        inp.checked = (current === letter);
      } else {
        inp.checked = Array.isArray(current) && current.includes(letter);
      }
      inp.addEventListener("change", ()=>{
        if(q.type==="mc"){
          state.answers[q.id] = letter;
        } else {
          const arr = new Set(Array.isArray(state.answers[q.id]) ? state.answers[q.id] : []);
          if(inp.checked) arr.add(letter); else arr.delete(letter);
          state.answers[q.id] = Array.from(arr);
        }
        saveState();
        renderMeta();
        updateNavStyles();
      });

      const txt = document.createElement("div");
      txt.innerHTML = `<strong>${letter}.</strong> ${opt}`;
      lab.appendChild(inp);
      lab.appendChild(txt);
      wrap.appendChild(lab);
    });
    area.appendChild(wrap);
  }

  if(q.type==="calc"){
    const box = document.createElement("div");
    box.className="calcBox";
    const inp = document.createElement("input");
    inp.type="text";
    inp.placeholder="Type your answer (e.g., Yes, No, 3.125)";
    inp.value = state.answers[q.id] ?? "";
    inp.addEventListener("input", ()=>{
      state.answers[q.id] = inp.value;
      saveState();
      renderMeta();
      updateNavStyles();
    });
    box.appendChild(inp);
    const hint = document.createElement("div");
    hint.className="note";
    hint.textContent = "Tip: For numeric answers, enter a number (decimals allowed). For Yes/No, type Yes or No.";
    box.appendChild(hint);
    area.appendChild(box);
  }

  if(q.type==="ordered"){
    const ordWrap = document.createElement("div");
    ordWrap.className="ordered";
    let cur = state.answers[q.id]?.order;
    if(!Array.isArray(cur) || cur.length !== q.steps.length){
      cur = Array.from({length:q.steps.length}, (_,i)=> i+1);
      state.answers[q.id] = {order:cur};
      saveState();
    }
    function renderSteps(){
      ordWrap.innerHTML="";
      cur.forEach((stepNum, pos)=>{
        const row = document.createElement("div");
        row.className="step";
        const handle = document.createElement("div");
        handle.className="handle";
        handle.textContent = String(pos+1);
        const txt = document.createElement("div");
        txt.className="txt";
        txt.textContent = q.steps[stepNum-1];
        const arrows = document.createElement("div");
        arrows.className="arrows";
        const up = document.createElement("button");
        up.textContent = "▲";
        up.disabled = pos===0;
        up.addEventListener("click", ()=>{
          const t = cur[pos-1]; cur[pos-1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        const dn = document.createElement("button");
        dn.textContent = "▼";
        dn.disabled = pos===cur.length-1;
        dn.addEventListener("click", ()=>{
          const t = cur[pos+1]; cur[pos+1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        arrows.appendChild(up);
        arrows.appendChild(dn);
        row.appendChild(handle);
        row.appendChild(txt);
        row.appendChild(arrows);
        ordWrap.appendChild(row);
      });
      const note = document.createElement("div");
      note.className="note";
      note.textContent = "Use the arrows to place the actions in correct order.";
      ordWrap.appendChild(note);
    }
    renderSteps();
    area.appendChild(ordWrap);
  }

  document.getElementById("prevBtn").disabled = currentIndex===0;
  document.getElementById("nextBtn").disabled = currentIndex===QUESTIONS.length-1;

  updateNavStyles();
  renderMeta();
}

function renderMeta(){
  document.getElementById("answeredCount").textContent = answeredCount();
  document.getElementById("flaggedCount").textContent = flaggedCount();
  const q = QUESTIONS[currentIndex];
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
}

function startTimer(){
  if(tickHandle) clearInterval(tickHandle);
  tickHandle = setInterval(()=>{
    const left = computeTimeLeft();
    document.getElementById("timer").textContent = fmtTime(left);
    if(left <= 0){
      clearInterval(tickHandle);
      tickHandle = null;
      submitExam(true);
    }
  }, 250);
}

function submitExam(auto=false){
  if(state.submitted) return;
  if(!auto){
    const ok = confirm("Submit now? You will see answers and rationales.");
    if(!ok) return;
  }
  state.submitted = true;
  saveState();

  let score=0;
  for(const q of QUESTIONS){
    if(isCorrect(q)) score++;
  }

  document.getElementById("exam").classList.add("hidden");
  document.getElementById("results").classList.remove("hidden");
  document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;

  const body = document.getElementById("resultsBody");
  body.innerHTML = `<p class="note">Auto-grading note: SATA requires an exact match. Ordered response requires the exact sequence. Calculations accept a small numeric tolerance (plus case-insensitive Yes/No).</p>`;

  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const ok = isCorrect(q);
    const div = document.createElement("div");
    div.className="resultItem";
    const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
    const your = state.answers[q.id];
    let yourTxt = "";
    let correctTxt = "";

    if(q.type==="mc"){
      yourTxt = your ? your : "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="sata"){
      yourTxt = (Array.isArray(your) && your.length) ? your.slice().sort().join(", ") : "(no answer)";
      correctTxt = q.answer.slice().sort().join(", ");
    } else if(q.type==="calc"){
      yourTxt = (your ?? "").toString().trim() || "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="ordered"){
      const y = (your && Array.isArray(your.order)) ? your.order.join("-") : "(no answer)";
      const c = q.answer_order.join("-");
      yourTxt = y;
      correctTxt = c;
    }

    div.innerHTML = `
      <div style="margin-bottom:6px;">
        ${badge}<strong>Q${i+1}.</strong> ${q.stem}
      </div>
      <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
      <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>
    `;
    body.appendChild(div);
  }

  body.insertAdjacentHTML("beforeend", `
    <div class="controls" style="margin-top:16px;">
      <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
      <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
    </div>
  `);
}

document.getElementById("startBtn").addEventListener("click", ()=>{
  if(state.submitted){
    alert("This attempt is already submitted. Use 'Reset Saved Attempt' to start over.");
    return;
  }
  if(!state.startedAt){
    state.startedAt = Date.now();
    saveState();
  }
  document.getElementById("start").classList.add("hidden");
  document.getElementById("exam").classList.remove("hidden");
  buildNav();
  render();
  document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
  startTimer();
});

document.getElementById("resetBtn").addEventListener("click", ()=>{
  const ok = confirm("Reset saved attempt? This clears answers and timer for this browser.");
  if(!ok) return;
  resetState();
  location.reload();
});

document.getElementById("prevBtn").addEventListener("click", ()=>{
  if(currentIndex>0) currentIndex--;
  render();
});
document.getElementById("nextBtn").addEventListener("click", ()=>{
  if(currentIndex<QUESTIONS.length-1) currentIndex++;
  render();
});
document.getElementById("flagBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  if(state.flagged[q.id]) delete state.flagged[q.id];
  else state.flagged[q.id]=true;
  saveState();
  renderMeta();
  updateNavStyles();
});
document.getElementById("clearBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  delete state.answers[q.id];
  if(q.type==="ordered"){
    state.answers[q.id] = {order: Array.from({length:q.steps.length}, (_,i)=> i+1)};
  }
  saveState();
  render();
});
document.getElementById("submitBtn").addEventListener("click", ()=> submitExam(false));

(function init(){
  if(state.submitted){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("results").classList.remove("hidden");
    let score=0;
    for(const q of QUESTIONS) if(isCorrect(q)) score++;
    document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;
    const body = document.getElementById("resultsBody");
    body.innerHTML = `<p class="note">This attempt was already submitted on this browser.</p>`;
    for(let i=0;i<QUESTIONS.length;i++){
      const q = QUESTIONS[i];
      const ok = isCorrect(q);
      const div = document.createElement("div");
      div.className="resultItem";
      const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
      const your = state.answers[q.id];
      let yourTxt="", correctTxt="";
      if(q.type==="mc"){ yourTxt = your ? your : "(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="sata"){ yourTxt=(Array.isArray(your)&&your.length)?your.slice().sort().join(", "):"(no answer)"; correctTxt=q.answer.slice().sort().join(", "); }
      else if(q.type==="calc"){ yourTxt=(your??"").toString().trim()||"(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="ordered"){ yourTxt=(your&&Array.isArray(your.order))?your.order.join("-"):"(no answer)"; correctTxt=q.answer_order.join("-"); }
      div.innerHTML = `<div style="margin-bottom:6px;">${badge}<strong>Q${i+1}.</strong> ${q.stem}</div>
        <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
        <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>`;
      body.appendChild(div);
    }
    body.insertAdjacentHTML("beforeend", `
      <div class="controls" style="margin-top:16px;">
        <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
        <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
      </div>
    `);
    return;
  }

  if(state.startedAt){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("exam").classList.remove("hidden");
    buildNav();
    render();
    document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
    startTimer();
  }
})();
</script>
</body>
</html>
[form_c.html](https://github.com/user-attachments/files/25405953/form_c.html)
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>NCLEX-Style Timed Exam — Form C (Balanced)</title>
<style>
  :root {
    --bg: #0b0f17;
    --panel: #121a29;
    --panel2: #0f1624;
    --text: #e8edf7;
    --muted: #a8b3c7;
    --accent: #5dd6ff;
    --danger: #ff5d7a;
    --ok: #52ffa8;
    --border: rgba(255,255,255,.10);
  }
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Segoe UI", Roboto, Helvetica, Arial, system-ui, sans-serif;
    background: radial-gradient(1200px 700px at 15% 10%, rgba(93,214,255,.12), transparent 60%),
                radial-gradient(900px 600px at 85% 25%, rgba(82,255,168,.10), transparent 65%),
                var(--bg);
    color: var(--text);
  }
  a { color: var(--accent); }
  .wrap {
    max-width: 1200px;
    margin: 0 auto;
    padding: 18px;
  }
  .card {
    background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
    border: 1px solid var(--border);
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0,0,0,.35);
    overflow: hidden;
  }
  .topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    padding: 14px 16px;
    background: rgba(0,0,0,.18);
    border-bottom: 1px solid var(--border);
  }
  .title {
    font-weight: 700;
    letter-spacing: .2px;
  }
  .pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 12px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.7);
    color: var(--muted);
    font-size: 13px;
    white-space: nowrap;
  }
  .timer {
    font-variant-numeric: tabular-nums;
    color: var(--text);
    font-weight: 700;
  }
  .grid {
    display: grid;
    grid-template-columns: 300px 1fr;
    min-height: 72vh;
  }
  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; }
  }
  .sidebar {
    padding: 14px;
    background: rgba(18,26,41,.35);
    border-right: 1px solid var(--border);
  }
  @media (max-width: 900px) {
    .sidebar {
      border-right: 0;
      border-bottom: 1px solid var(--border);
    }
  }
  .qnav {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    gap: 8px;
  }
  .qbtn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.6);
    color: var(--text);
    border-radius: 10px;
    padding: 10px 0;
    font-weight: 700;
    cursor: pointer;
    transition: transform .05s ease, background .2s ease, border-color .2s ease;
  }
  .qbtn:hover { transform: translateY(-1px); border-color: rgba(93,214,255,.55); }
  .qbtn.active { background: rgba(93,214,255,.18); border-color: rgba(93,214,255,.65); }
  .qbtn.answered { background: rgba(82,255,168,.12); border-color: rgba(82,255,168,.35); }
  .qbtn.flagged { background: rgba(255,93,122,.14); border-color: rgba(255,93,122,.45); }
  .sidebar .meta {
    margin-top: 14px;
    display: grid;
    gap: 10px;
  }
  .metaRow {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 13px;
    color: var(--muted);
  }
  .main {
    padding: 18px;
  }
  .stem {
    font-size: 18px;
    line-height: 1.35;
    margin: 0 0 14px 0;
  }
  .tag {
    font-size: 12px;
    color: var(--muted);
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    display: inline-block;
    padding: 6px 10px;
    border-radius: 999px;
    margin-bottom: 10px;
  }
  .choices {
    display: grid;
    gap: 10px;
  }
  label.choice {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    padding: 12px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
    cursor: pointer;
  }
  label.choice:hover {
    border-color: rgba(93,214,255,.55);
    background: rgba(15,22,36,.72);
  }
  input[type="radio"], input[type="checkbox"] {
    margin-top: 2px;
    accent-color: var(--accent);
  }
  .controls {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 16px;
  }
  button.btn {
    appearance: none;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    border-radius: 12px;
    padding: 10px 12px;
    font-weight: 700;
    cursor: pointer;
  }
  button.btn:hover { border-color: rgba(93,214,255,.55); }
  button.primary {
    background: rgba(93,214,255,.18);
    border-color: rgba(93,214,255,.55);
  }
  button.danger {
    background: rgba(255,93,122,.14);
    border-color: rgba(255,93,122,.55);
  }
  button.ok {
    background: rgba(82,255,168,.12);
    border-color: rgba(82,255,168,.45);
  }
  .note {
    color: var(--muted);
    font-size: 13px;
    line-height: 1.35;
  }
  .startScreen {
    max-width: 860px;
    margin: 30px auto;
    padding: 18px;
  }
  .startScreen h1 {
    margin: 0 0 6px 0;
    font-size: 28px;
  }
  .startScreen ul {
    margin: 10px 0 0 18px;
    color: var(--muted);
    line-height: 1.5;
  }
  .hidden { display: none; }
  .calcBox {
    display: grid;
    gap: 10px;
  }
  .calcBox input {
    width: 240px;
    max-width: 100%;
    padding: 12px;
    border-radius: 12px;
    border: 1px solid var(--border);
    background: rgba(15,22,36,.55);
    color: var(--text);
    font-size: 16px;
  }
  .ordered {
    display: grid;
    gap: 10px;
  }
  .step {
    display: flex;
    gap: 10px;
    align-items: center;
    padding: 10px 12px;
    background: rgba(15,22,36,.55);
    border: 1px solid var(--border);
    border-radius: 12px;
  }
  .step .handle {
    width: 26px;
    height: 26px;
    border-radius: 8px;
    border: 1px solid var(--border);
    display: grid;
    place-items: center;
    color: var(--muted);
    font-weight: 700;
  }
  .step .txt {
    flex: 1;
    line-height: 1.3;
  }
  .step .arrows button {
    margin-left: 6px;
    padding: 6px 8px;
    border-radius: 10px;
    border: 1px solid var(--border);
    background: rgba(18,26,41,.65);
    color: var(--text);
    cursor: pointer;
  }
  .results h2 {
    margin: 0 0 6px 0;
  }
  .resultItem {
    padding: 12px 12px;
    border: 1px solid var(--border);
    border-radius: 14px;
    background: rgba(15,22,36,.55);
    margin: 10px 0;
  }
  .badge {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 999px;
    font-size: 12px;
    font-weight: 800;
    border: 1px solid var(--border);
    margin-right: 8px;
  }
  .badge.ok { color: var(--ok); border-color: rgba(82,255,168,.35); background: rgba(82,255,168,.12); }
  .badge.no { color: var(--danger); border-color: rgba(255,93,122,.45); background: rgba(255,93,122,.14); }
  .rationale {
    color: var(--muted);
    margin-top: 8px;
    line-height: 1.35;
  }
</style>
</head>
<body>
<div id="start" class="wrap startScreen">
  <div class="card">
    <div class="topbar">
      <div class="title">NCLEX-Style Timed Exam - Pain & Pharmacology (50 Questions)</div>
      <div class="pill"><span>Time:</span> <span class="timer">90:00</span></div>
    </div>
    <div style="padding:16px 18px;">
      <h1>NCLEX-Style Timed Exam — Form C (Balanced)</h1>
      <div class="note">
        <ul>
          <li>This exam runs fully in your browser (works well on a Mac).</li>
          <li>Question types include Multiple Choice, Select-All-That-Apply (SATA), Ordered Response, and Calculations.</li>
          <li>Use the sidebar to jump between questions. You can flag questions for review.</li>
          <li>Your progress is saved automatically in this browser.</li>
          <li>When you submit, you'll see your score plus the answer key and rationales.</li>
        </ul>
      </div>
      <div class="controls" style="margin-top:16px;">
        <button class="btn primary" id="startBtn">Start Exam</button>
        <button class="btn" id="resetBtn">Reset Saved Attempt</button>
      </div>
      <div class="note" style="margin-top:10px;">Tip: For best timing accuracy, keep this tab open during the exam.</div>
    </div>
  </div>
</div>

<div id="exam" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title" id="headerTitle">Question</div>
      <div style="display:flex; gap:10px; align-items:center;">
        <div class="pill"><span>Answered:</span> <span id="answeredCount">0</span>/50</div>
        <div class="pill"><span>Flagged:</span> <span id="flaggedCount">0</span></div>
        <div class="pill"><span>Time Left:</span> <span class="timer" id="timer">90:00</span></div>
      </div>
    </div>

    <div class="grid">
      <div class="sidebar">
        <div class="qnav" id="qnav"></div>
        <div class="meta">
          <div class="metaRow"><span>Current</span><span id="curMeta">1 / 50</span></div>
          <div class="metaRow"><span>Type</span><span id="typeMeta">MC</span></div>
          <div class="metaRow"><span>Status</span><span id="statusMeta">Not answered</span></div>
        </div>
        <div class="controls" style="margin-top:12px;">
          <button class="btn" id="flagBtn">Flag / Unflag</button>
          <button class="btn" id="clearBtn">Clear Answer</button>
          <button class="btn danger" id="submitBtn">Submit Exam</button>
        </div>
      </div>

      <div class="main">
        <div class="tag" id="qTag">Type</div>
        <p class="stem" id="stem"></p>
        <div id="interaction"></div>

        <div class="controls">
          <button class="btn" id="prevBtn">Previous</button>
          <button class="btn primary" id="nextBtn">Next</button>
        </div>
        <div class="note" style="margin-top:10px;">Exam note: Answer key and rationales appear after submission.</div>
      </div>
    </div>
  </div>
</div>

<div id="results" class="wrap hidden">
  <div class="card">
    <div class="topbar">
      <div class="title">Results</div>
      <div class="pill"><span>Score:</span> <span class="timer" id="scoreText">0/50</span></div>
    </div>
    <div class="main results" id="resultsBody"></div>
  </div>
</div>

<script>
const QUESTIONS = [{"id": 1, "type": "mc", "stem": "A client with chronic hypertension is prescribed celecoxib for arthritis. Which teaching is most appropriate?", "options": ["This NSAID has no cardiovascular risks.", "Monitor for signs of cardiovascular complications and report chest pain or shortness of breath.", "Take it with alcohol to improve absorption.", "Because it is COX‑2 selective, it can be used safely with any anticoagulant without risk."], "answer": "Monitor for signs of cardiovascular complications and report chest pain or shortness of breath.", "rationale": "Second‑generation (COX‑2 selective) NSAIDs may still carry cardiovascular risk; clients should be taught to monitor/report concerning symptoms."}, {"id": 2, "type": "mc", "stem": "Which assessment finding would make the nurse question administering an NSAID first‑generation medication?", "options": ["BP 168/94 with history of heart failure", "Temperature 101.2°F with no chronic disease", "Mild seasonal allergic rhinitis", "Migraine headache with nausea"], "answer": "BP 168/94 with history of heart failure", "rationale": "First‑generation NSAIDs are contraindicated in hypertension and heart failure due to fluid retention/worsening cardiovascular status."}, {"id": 3, "type": "calc", "stem": "Half‑life calculation: A medication dose is 160 mg with a half‑life of 4 hours. How many mg remain after 16 hours? (Enter a number; no rounding.)", "answer": ["10"], "rationale": "16 hours is four half‑lives (4h each): 160 → 80 → 40 → 20 → 10 mg."}, {"id": 4, "type": "mc", "stem": "A nurse is educating a client on why nitroglycerin is given sublingually rather than swallowed. Which concept explains this?", "options": ["Protein binding", "First‑pass effect", "Therapeutic index", "Half‑life"], "answer": "First‑pass effect", "rationale": "Swallowed nitroglycerin undergoes significant first‑pass metabolism. Sublingual administration bypasses the GI tract and first‑pass effect for rapid action."}, {"id": 5, "type": "sata", "stem": "A client on opioids is at risk for falls. Which nursing actions reduce this risk? Select all that apply.", "options": ["Implement fall precautions and keep call light within reach.", "Teach the client to change positions slowly.", "Encourage the client to ambulate alone to build confidence.", "Assess sedation level before assisting to the bathroom.", "Administer an extra opioid dose before ambulation to prevent pain."], "answer": ["Implement fall precautions and keep call light within reach.", "Teach the client to change positions slowly.", "Assess sedation level before assisting to the bathroom."], "rationale": "Opioids can cause sedation, dizziness, and hypotension; fall precautions, slow position changes, and assessing sedation before mobility reduce risk."}, {"id": 6, "type": "mc", "stem": "A client is prescribed pregabalin for neuropathic pain. Which consideration is most important?", "options": ["It requires routine therapeutic levels for pain control.", "It can cause dizziness/drowsiness; reinforce safety precautions.", "It is contraindicated because it is a controlled substance.", "It has no CNS side effects."], "answer": "It can cause dizziness/drowsiness; reinforce safety precautions.", "rationale": "Pregabalin can cause dizziness and drowsiness; safety teaching is essential. It does not require routine therapeutic drug levels for pain."}, {"id": 7, "type": "calc", "stem": "Steady state: A medication has a half‑life of 5 hours. Approximately how many hours to reach plateau with a maintenance dose? (Enter hours.)", "answer": ["20"], "rationale": "Plateau occurs after ~4 half‑lives: 4 × 5 = 20 hours."}, {"id": 8, "type": "mc", "stem": "A client taking hydrocodone/APAP reports taking additional OTC cold medicine “with acetaminophen.” What is the priority nursing concern?", "options": ["Increased risk of renal stones", "Increased risk of hepatotoxicity from total acetaminophen dose", "Increased risk of serotonin syndrome", "Decreased pain control due to antagonism"], "answer": "Increased risk of hepatotoxicity from total acetaminophen dose", "rationale": "Combining multiple acetaminophen-containing products can exceed safe daily maximum and cause liver injury."}, {"id": 9, "type": "mc", "stem": "A nurse is administering opioids. Which expected physiologic effect is associated with opioids?", "options": ["Mydriasis", "Miosis", "Bronchodilation", "Hyperactive bowel sounds"], "answer": "Miosis", "rationale": "Opioids commonly cause miosis (pinpoint pupils)."}, {"id": 10, "type": "sata", "stem": "Which findings indicate a client may be experiencing acetaminophen toxicity? Select all that apply.", "options": ["Right upper quadrant abdominal pain", "Jaundice", "Elevated liver enzymes (ALT/AST)", "Tinnitus", "Severe diarrhea immediately after one dose"], "answer": ["Right upper quadrant abdominal pain", "Jaundice", "Elevated liver enzymes (ALT/AST)"], "rationale": "Acetaminophen toxicity primarily affects the liver; RUQ pain, jaundice, and elevated ALT/AST are concerning. Tinnitus is more consistent with salicylate toxicity."}, {"id": 11, "type": "mc", "stem": "A client received naloxone for opioid overdose. Which nursing plan is most important after the initial response?", "options": ["Discontinue monitoring once respirations improve.", "Continue close monitoring because naloxone may wear off before the opioid.", "Administer another opioid to prevent pain rebound.", "Encourage the client to ambulate immediately."], "answer": "Continue close monitoring because naloxone may wear off before the opioid.", "rationale": "Naloxone duration may be shorter than many opioids; recurrence of respiratory depression is possible, so ongoing monitoring and repeat dosing may be needed."}, {"id": 12, "type": "calc", "stem": "Half‑life calculation: A client receives 64 mg of a drug with a half‑life of 6 hours. How many mg remain after 18 hours? (Enter a number.)", "answer": ["8"], "rationale": "18 hours is three half‑lives: 64 → 32 → 16 → 8 mg."}, {"id": 13, "type": "mc", "stem": "A nurse evaluates a medication’s onset, peak, and duration. Which statement is correct?", "options": ["Peak is when the medication first begins to work.", "Duration is the length of time the medication has desired effect.", "Onset is the time it takes to be completely eliminated.", "Duration is the highest concentration achieved."], "answer": "Duration is the length of time the medication has desired effect.", "rationale": "Duration refers to how long the medication produces the desired effect."}, {"id": 14, "type": "mc", "stem": "A nurse sees an order for an enteral (swallowed) nitroglycerin tablet for acute chest pain. What should the nurse do first?", "options": ["Administer immediately for rapid relief.", "Hold and clarify the order; oral nitroglycerin undergoes first‑pass effect and is not appropriate for rapid relief.", "Crush the tablet and give via feeding tube.", "Give with food to reduce side effects."], "answer": "Hold and clarify the order; oral nitroglycerin undergoes first‑pass effect and is not appropriate for rapid relief.", "rationale": "Nitroglycerin should be given via routes that bypass first‑pass metabolism (e.g., sublingual) for acute chest pain; clarify inappropriate oral order."}, {"id": 15, "type": "sata", "stem": "A nurse is reviewing contraindications for first‑generation NSAIDs. Which client histories are contraindications? Select all that apply.", "options": ["Asthma", "History of peptic ulcer disease", "Chronic kidney disease", "Heart failure", "Seasonal migraines"], "answer": ["Asthma", "History of peptic ulcer disease", "Chronic kidney disease", "Heart failure"], "rationale": "First‑generation NSAIDs are contraindicated in asthma, GI bleed/PUD, renal impairment, and hypertension/heart failure."}, {"id": 16, "type": "ordered", "stem": "A client with severe pain is prescribed IV morphine. Order the nurse’s actions. (1 = first, 4 = last)", "steps": ["Verify indication, allergies, and last opioid dose; assess baseline RR/LOC and pain.", "Administer IV morphine per policy and monitor during administration.", "Implement safety measures (bed low, call light, assist with ambulation).", "Reassess pain and monitor for adverse effects (RR, LOC, hypotension, nausea)."], "answer_order": [1, 2, 3, 4], "rationale": "Assess first, administer safely, ensure safety due to sedation/hypotension risk, then reassess for effectiveness and adverse effects."}, {"id": 17, "type": "calc", "stem": "A client has taken aspirin 650 mg every 6 hours for 2 days and now reports tinnitus. What is the best nurse action? (Answer: Hold, Continue, or Notify.)", "answer": ["Notify"], "rationale": "Tinnitus is a sign of salicylate toxicity; the nurse should hold further doses and notify the provider. (For this item, ‘Notify’ reflects escalation.)"}, {"id": 18, "type": "mc", "stem": "A client with migraine without aura reports unilateral pulsating pain with photophobia. Which nonpharmacologic intervention is most appropriate?", "options": ["Brightly lit room to improve alertness", "Dark, quiet environment", "High‑intensity exercise", "Large meal with caffeine"], "answer": "Dark, quiet environment", "rationale": "A dark, quiet space can reduce sensory stimulation and help during acute migraine."}, {"id": 19, "type": "mc", "stem": "A nurse is selecting a medication for nerve pain described as burning and shooting. Which class is commonly used?", "options": ["Anticonvulsants such as gabapentin", "Loop diuretics", "Beta blockers", "Antibiotics"], "answer": "Anticonvulsants such as gabapentin", "rationale": "Neuropathic pain (burning/shocking/pins and needles) is often managed with anticonvulsants such as gabapentin or pregabalin."}, {"id": 20, "type": "calc", "stem": "Drug clearance estimate: A drug is stopped. About what percent remains after 5 half‑lives? (Enter percent.)", "answer": ["3.125"], "rationale": "After 5 half‑lives: (1/2)^5 = 1/32 = 3.125% remaining."}, {"id": 21, "type": "mc", "stem": "Which finding best reflects decreased renal excretion increasing drug toxicity risk?", "options": ["Creatinine elevated above baseline", "Albumin elevated", "Hemoglobin elevated", "Sodium slightly low after IV fluids"], "answer": "Creatinine elevated above baseline", "rationale": "Creatinine is a key indicator of kidney function; elevated creatinine suggests impaired excretion and increased toxicity risk."}, {"id": 22, "type": "mc", "stem": "A client taking cyclobenzaprine reports dry mouth and drowsiness. Which category explains dry mouth?", "options": ["Serotonergic effect", "Anticholinergic effect", "Cholinergic effect", "Opioid receptor activation"], "answer": "Anticholinergic effect", "rationale": "Cyclobenzaprine can cause anticholinergic effects such as dry mouth."}, {"id": 23, "type": "sata", "stem": "Which statements about therapeutic window are accurate? Select all that apply.", "options": ["Below the window the drug may be ineffective.", "Within the window the drug is expected to be effective with acceptable risk.", "Above the window the drug may cause harm/toxicity.", "Therapeutic window and therapeutic index are identical terms.", "A narrow window often requires closer monitoring."], "answer": ["Below the window the drug may be ineffective.", "Within the window the drug is expected to be effective with acceptable risk.", "Above the window the drug may cause harm/toxicity.", "A narrow window often requires closer monitoring."], "rationale": "Therapeutic window is the effective range; narrow windows require closer monitoring. Therapeutic index relates to safety ratio and is not identical."}, {"id": 24, "type": "mc", "stem": "A nurse suspects opioid‑induced hypotension. Which assessment supports this?", "options": ["BP 86/48 with dizziness on standing", "Temp 100.9°F", "HR 58 with athletic history", "RR 18 with normal LOC"], "answer": "BP 86/48 with dizziness on standing", "rationale": "Opioids can cause hypotension/orthostatic changes; low BP with dizziness suggests this effect."}, {"id": 25, "type": "calc", "stem": "Safe dosing: An older adult has received acetaminophen 650 mg at 0600, 1200, 1800, and 0000. Using an older-adult max of 3,000 mg/24 hr, can another 650 mg dose be given at 0600? (Answer Yes or No.)", "answer": ["No"], "rationale": "Four doses = 2,600 mg. Another 650 mg would total 3,250 mg in 24 hours, exceeding 3,000 mg."}, {"id": 26, "type": "mc", "stem": "A client with migraine is prescribed topiramate daily. Which is the best evaluation question to assess “working too well”?", "options": ["Are you having fewer migraines per week?", "Are you feeling excessively drowsy or cognitively slowed?", "Do you have tinnitus?", "Are you bleeding when you brush your teeth?"], "answer": "Are you feeling excessively drowsy or cognitively slowed?", "rationale": "Topiramate side effects are CNS related; excessive drowsiness/cognitive slowing suggests the drug may be causing problematic effects."}, {"id": 27, "type": "mc", "stem": "Which nursing action best reflects understanding of drug potency differences among opioids?", "options": ["Administer equal milligram doses of all opioids for similar pain relief.", "Verify dosing units carefully, especially for highly potent opioids ordered in micrograms.", "Assume fentanyl is safest because it is a small dose.", "Avoid reassessment because opioids have predictable effects."], "answer": "Verify dosing units carefully, especially for highly potent opioids ordered in micrograms.", "rationale": "Potency varies; dosing units and amounts differ. Fentanyl is potent and often ordered in micrograms—verification is critical."}, {"id": 28, "type": "mc", "stem": "A client is prescribed an IV antibiotic that is nephrotoxic. Which lab is most important to monitor for toxicity risk?", "options": ["ALT", "Creatinine", "Albumin", "WBC"], "answer": "Creatinine", "rationale": "Creatinine is the key marker for kidney function, which affects drug excretion and nephrotoxic risk."}, {"id": 29, "type": "mc", "stem": "A client with opioid therapy reports urinary retention. What is the nurse’s best first action?", "options": ["Administer a diuretic immediately.", "Assess bladder distention and last void; implement toileting measures and notify provider if needed.", "Ignore; urinary retention is unrelated to opioids.", "Give another opioid to relax the client."], "answer": "Assess bladder distention and last void; implement toileting measures and notify provider if needed.", "rationale": "Urinary retention is a known opioid side effect; assess and manage safely, escalating per protocol if inability to void persists."}, {"id": 30, "type": "sata", "stem": "A client presents with migraine with aura. Which symptoms are consistent with aura? Select all that apply.", "options": ["Flashing lights or zigzag lines", "Numbness/tingling of lips or tongue", "Unilateral weakness", "Diarrhea", "Acute confusion or aphasia"], "answer": ["Flashing lights or zigzag lines", "Numbness/tingling of lips or tongue", "Unilateral weakness", "Acute confusion or aphasia"], "rationale": "Aura can include visual disturbances, sensory changes, aphasia/confusion, and unilateral weakness."}, {"id": 31, "type": "calc", "stem": "Dose stacking: A medication peaks at 1 hour and has a duration of 6 hours. It is scheduled every 4 hours. What is the major concern? (Answer: Under-dose or Overlap.)", "answer": ["Overlap"], "rationale": "Scheduling doses before duration ends can cause overlapping effects (‘stacking’) and increases risk of excessive drug effect/toxicity."}, {"id": 32, "type": "mc", "stem": "A client with low albumin is prescribed a highly protein‑bound drug. What nursing implication is most accurate?", "options": ["Expect decreased drug effect because more drug is bound.", "Expect increased drug effect/toxicity because more free drug is available.", "No change; albumin does not affect drug action.", "Expect only delayed excretion."], "answer": "Expect increased drug effect/toxicity because more free drug is available.", "rationale": "Low albumin reduces binding, increasing free (active) drug and risk for excessive effect/toxicity."}, {"id": 33, "type": "mc", "stem": "Which statement best differentiates side effects from adverse effects?", "options": ["Side effects are rare and always require hospitalization.", "Adverse effects are rare, serious, and always negative; side effects are known and explainable.", "Adverse effects are positive; side effects are negative.", "There is no difference."], "answer": "Adverse effects are rare, serious, and always negative; side effects are known and explainable.", "rationale": "Adverse effects are rare, serious, and negative; side effects are expected/known effects that may be less serious."}, {"id": 34, "type": "mc", "stem": "A nurse is deciding whether to use a Venturi mask or non‑rebreather for a client with respiratory distress. Which is correct?", "options": ["Venturi mask is first‑line for emergency severe hypoxia.", "Non‑rebreather provides high concentration oxygen for emergencies.", "Nasal cannula provides the most precise oxygen delivery.", "Simple mask can be used at any flow rate including 2 L/min."], "answer": "Non‑rebreather provides high concentration oxygen for emergencies.", "rationale": "Non‑rebreather delivers high concentration oxygen and is appropriate in emergencies; Venturi provides precise FiO2 often used when controlled oxygen is needed."}, {"id": 35, "type": "ordered", "stem": "A client with suspected NSAID‑related GI bleed reports black, tarry stools. Order the nurse actions. (1 = first, 4 = last)", "steps": ["Assess vital signs and symptoms of hypovolemia.", "Hold NSAID and notify provider of suspected GI bleeding.", "Prepare for potential labs/IV access as ordered and monitor for worsening.", "Provide client teaching to avoid NSAIDs and report bleeding symptoms."], "answer_order": [1, 2, 3, 4], "rationale": "Assess and stabilize first, then stop the offending medication and notify provider; anticipate orders/monitor, then teach prevention."}, {"id": 36, "type": "calc", "stem": "Half‑life calculation: A client receives 20 mg of a drug with a half‑life of 1 hour. How many mg remain after 6 hours? (Enter a number; no rounding.)", "answer": ["0.3125"], "rationale": "6 hours is six half‑lives: 20 → 10 → 5 → 2.5 → 1.25 → 0.625 → 0.3125 mg."}, {"id": 37, "type": "mc", "stem": "Which client is at highest risk for opioid neurotoxicity and oversedation?", "options": ["Young adult with normal liver/kidney function", "Older adult with renal impairment receiving repeated opioid doses", "Client with seasonal allergies", "Client receiving topical NSAIDs only"], "answer": "Older adult with renal impairment receiving repeated opioid doses", "rationale": "Renal impairment and older age can reduce clearance and increase sensitivity, raising risk for accumulation and neurotoxicity/sedation."}, {"id": 38, "type": "mc", "stem": "A nurse is calculating what remains after half‑lives. Why does prolonged half‑life matter clinically?", "options": ["It always increases drug potency.", "It increases risk for toxicity and may require dose or frequency reduction.", "It means the drug is ineffective.", "It guarantees fewer side effects."], "answer": "It increases risk for toxicity and may require dose or frequency reduction.", "rationale": "Delayed metabolism/excretion prolongs half‑life, increasing accumulation and toxicity risk—dosing adjustments may be needed."}, {"id": 39, "type": "sata", "stem": "A client is discharged with a new opioid prescription. Which education points are essential? Select all that apply.", "options": ["Do not mix with alcohol or other sedatives unless prescribed.", "Use the lowest effective dose and avoid extra doses.", "Expect constipation and start prevention measures.", "Share leftovers with a family member who has pain.", "Store medication locked and dispose of unused tablets properly."], "answer": ["Do not mix with alcohol or other sedatives unless prescribed.", "Use the lowest effective dose and avoid extra doses.", "Expect constipation and start prevention measures.", "Store medication locked and dispose of unused tablets properly."], "rationale": "Key opioid safety: avoid CNS depressants, prevent overdose, prevent constipation, secure storage and safe disposal; never share medications."}, {"id": 40, "type": "mc", "stem": "Which pain description most strongly suggests neuropathic pain rather than nociceptive pain?", "options": ["Dull ache after exercise", "Burning, shooting, pins-and-needles sensation", "Throbbing pain with swelling", "Cramping pain after eating"], "answer": "Burning, shooting, pins-and-needles sensation", "rationale": "Neuropathic pain is often described as burning, shooting, or pins-and-needles."}, {"id": 41, "type": "calc", "stem": "Loading dose concept: A medication would take 30 hours to reach plateau (steady state). Approximately what is the drug’s half‑life? (Enter hours.)", "answer": ["7.5"], "rationale": "Plateau ≈ 4 half‑lives. 30 ÷ 4 = 7.5 hours per half‑life."}, {"id": 42, "type": "mc", "stem": "A client with renal impairment is prescribed a medication primarily excreted by kidneys. Which provider action is most likely?", "options": ["Increase the dose to overcome reduced excretion.", "Decrease dose or extend dosing interval to prevent toxicity.", "Switch to oral route to improve excretion.", "No changes are needed."], "answer": "Decrease dose or extend dosing interval to prevent toxicity.", "rationale": "Impaired renal excretion increases toxicity risk; providers often reduce dose or extend dosing interval."}, {"id": 43, "type": "mc", "stem": "A nurse notes that a medication has a narrow therapeutic index. What is the priority nursing implication?", "options": ["No monitoring is needed because dosing is standardized.", "Monitor closely for toxicity and ensure appropriate lab/parameter monitoring.", "Administer extra doses if not effective immediately.", "Avoid documenting assessments."], "answer": "Monitor closely for toxicity and ensure appropriate lab/parameter monitoring.", "rationale": "Narrow TI drugs have small margin of safety; close monitoring and timely labs/parameters are essential."}, {"id": 44, "type": "calc", "stem": "A drug’s half‑life is 2 hours. Starting with 128 mg, how many mg remain after 10 hours? (Enter a number.)", "answer": ["4"], "rationale": "10 hours is five half‑lives: 128 → 64 → 32 → 16 → 8 → 4 mg."}, {"id": 45, "type": "mc", "stem": "A client reports nausea after morphine. Which nursing intervention is most appropriate?", "options": ["Stop morphine permanently without provider notification.", "Assess severity and request/implement antiemetic as ordered while monitoring for respiratory depression.", "Give alcohol to settle the stomach.", "Encourage driving to distract from nausea."], "answer": "Assess severity and request/implement antiemetic as ordered while monitoring for respiratory depression.", "rationale": "Nausea/vomiting are common opioid side effects; manage symptoms while continuing safety monitoring for more serious effects."}, {"id": 46, "type": "mc", "stem": "Which statement best reflects the nurse’s responsibility regarding CYP450 enzyme specifics?", "options": ["Nurses must memorize which CYP enzyme metabolizes every drug.", "Nurses focus on assessing effectiveness and adverse effects, and report concerns; detailed CYP mapping is pharmacist-level.", "CYP enzymes are only relevant in pediatrics.", "CYP enzymes are found in the kidneys."], "answer": "Nurses focus on assessing effectiveness and adverse effects, and report concerns; detailed CYP mapping is pharmacist-level.", "rationale": "Detailed CYP enzyme mapping is beyond typical nursing scope; nurses monitor response/safety and communicate concerns."}, {"id": 47, "type": "calc", "stem": "Clinical math: A client’s opioid order is morphine 4 mg IV every 2 hours PRN. The vial is 10 mg/mL. How many mL will the nurse draw up for one dose? (Enter mL.)", "answer": ["0.4"], "rationale": "mL = dose ÷ concentration = 4 mg ÷ 10 mg/mL = 0.4 mL."}, {"id": 48, "type": "mc", "stem": "A client’s migraine medication “is not working enough.” What is the nurse’s best first step?", "options": ["Immediately double the dose without provider input.", "Assess timing of administration and whether it was taken at first sign of migraine; evaluate need to notify provider.", "Tell the client to stop all migraine medications.", "Assume the diagnosis is wrong and ignore the complaint."], "answer": "Assess timing of administration and whether it was taken at first sign of migraine; evaluate need to notify provider.", "rationale": "Abortive therapy is most effective when taken early. Assess timing/response and communicate to provider for safe adjustments."}, {"id": 49, "type": "mc", "stem": "Which client statement about NSAIDs indicates a need for further teaching?", "options": ["I’ll watch for black stools or vomiting blood and report it.", "I can take NSAIDs even if I have kidney disease because they are OTC.", "I’ll take it with food to reduce stomach upset.", "I’ll avoid taking more than one NSAID at a time."], "answer": "I can take NSAIDs even if I have kidney disease because they are OTC.", "rationale": "NSAIDs can worsen renal impairment; OTC status does not equal safety in all clients."}, {"id": 50, "type": "mc", "stem": "A nurse is prioritizing client education. Which topic is most important for a client newly prescribed opioids?", "options": ["How to request brand name refills", "Recognition of respiratory depression and when to call 911", "How to increase caffeine intake", "How to avoid sunlight exposure"], "answer": "Recognition of respiratory depression and when to call 911", "rationale": "Respiratory depression is the most dangerous opioid adverse effect; clients must know warning signs and emergency actions."}];
const STORAGE_KEY = "nclex_painpharm_attempt_v1";

function defaultState(){
  return {
    startedAt: null,
    durationSec: 90*60,
    answers: {},
    flagged: {},
    submitted: false
  };
}

function loadState(){
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if(!raw) return defaultState();
    const s = JSON.parse(raw);
    return Object.assign(defaultState(), s);
  } catch(e) {
    return defaultState();
  }
}

function saveState(){
  localStorage.setItem(STORAGE_KEY, JSON.stringify(state));
}

function resetState(){
  localStorage.removeItem(STORAGE_KEY);
  state = defaultState();
}

let state = loadState();
let currentIndex = 0;
let tickHandle = null;

function fmtTime(sec){
  sec = Math.max(0, Math.floor(sec));
  const m = Math.floor(sec/60);
  const s = sec%60;
  return String(m).padStart(2,"0")+":"+String(s).padStart(2,"0");
}

function computeTimeLeft(){
  if(!state.startedAt) return state.durationSec;
  const elapsed = (Date.now() - state.startedAt)/1000;
  return state.durationSec - elapsed;
}

function answeredCount(){
  let c=0;
  for(const q of QUESTIONS){
    const a = state.answers[q.id];
    if(a==null) continue;
    if(q.type==="mc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="calc" && typeof a==="string" && a.trim()!=="") c++;
    else if(q.type==="sata" && Array.isArray(a) && a.length>0) c++;
    else if(q.type==="ordered" && a && Array.isArray(a.order) && a.order.length===q.steps.length) c++;
  }
  return c;
}

function flaggedCount(){
  return Object.keys(state.flagged).length;
}

function isAnswered(q){
  const a = state.answers[q.id];
  if(a==null) return false;
  if(q.type==="mc" || q.type==="calc") return String(a).trim()!=="";
  if(q.type==="sata") return Array.isArray(a) && a.length>0;
  if(q.type==="ordered") return a && Array.isArray(a.order) && a.order.length===q.steps.length;
  return false;
}

function isCorrect(q){
  const a = state.answers[q.id];
  if(q.type==="calc"){
    const want = String(q.answer[0]).trim();
    const got = String(a ?? "").trim();
    const wantNum = Number(want);
    const gotNum = Number(got);
    if(!Number.isNaN(wantNum) && !Number.isNaN(gotNum)){
      return Math.abs(wantNum - gotNum) <= 0.001;
    }
    return got.toLowerCase() === want.toLowerCase();
  }
  if(q.type==="mc"){
    return String(a) === q.answer[0];
  }
  if(q.type==="sata"){
    const got = Array.isArray(a) ? a.slice().sort() : [];
    const want = q.answer.slice().sort();
    return JSON.stringify(got) === JSON.stringify(want);
  }
  if(q.type==="ordered"){
    const got = (a && Array.isArray(a.order)) ? a.order : [];
    const want = q.answer_order;
    return JSON.stringify(got) === JSON.stringify(want);
  }
  return false;
}

function buildNav(){
  const nav = document.getElementById("qnav");
  nav.innerHTML="";
  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const b = document.createElement("button");
    b.className="qbtn";
    b.textContent = String(i+1);
    b.addEventListener("click", ()=>{ currentIndex=i; render(); });
    nav.appendChild(b);
  }
}

function updateNavStyles(){
  const buttons = Array.from(document.querySelectorAll(".qbtn"));
  buttons.forEach((b, i)=>{
    const q = QUESTIONS[i];
    b.classList.toggle("active", i===currentIndex);
    b.classList.toggle("answered", isAnswered(q));
    b.classList.toggle("flagged", !!state.flagged[q.id]);
  });
}

function render(){
  const q = QUESTIONS[currentIndex];
  document.getElementById("headerTitle").textContent = `Question ${currentIndex+1}`;
  document.getElementById("curMeta").textContent = `${currentIndex+1} / ${QUESTIONS.length}`;
  document.getElementById("typeMeta").textContent = q.type.toUpperCase();
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
  document.getElementById("qTag").textContent = ({
    mc:"Multiple Choice",
    sata:"Select all that apply (SATA)",
    ordered:"Ordered response",
    calc:"Calculation / short answer"
  })[q.type] || q.type;

  document.getElementById("stem").textContent = q.stem;

  const area = document.getElementById("interaction");
  area.innerHTML = "";

  if(q.type==="mc" || q.type==="sata"){
    const wrap = document.createElement("div");
    wrap.className="choices";
    const current = state.answers[q.id] ?? (q.type==="sata" ? [] : "");
    q.options.forEach((opt, idx)=>{
      const letter = String.fromCharCode(65+idx);
      const id = `q${q.id}_${letter}`;
      const lab = document.createElement("label");
      lab.className="choice";
      const inp = document.createElement("input");
      inp.type = (q.type==="mc") ? "radio" : "checkbox";
      inp.name = `q${q.id}`;
      inp.id = id;
      inp.value = letter;
      if(q.type==="mc"){
        inp.checked = (current === letter);
      } else {
        inp.checked = Array.isArray(current) && current.includes(letter);
      }
      inp.addEventListener("change", ()=>{
        if(q.type==="mc"){
          state.answers[q.id] = letter;
        } else {
          const arr = new Set(Array.isArray(state.answers[q.id]) ? state.answers[q.id] : []);
          if(inp.checked) arr.add(letter); else arr.delete(letter);
          state.answers[q.id] = Array.from(arr);
        }
        saveState();
        renderMeta();
        updateNavStyles();
      });

      const txt = document.createElement("div");
      txt.innerHTML = `<strong>${letter}.</strong> ${opt}`;
      lab.appendChild(inp);
      lab.appendChild(txt);
      wrap.appendChild(lab);
    });
    area.appendChild(wrap);
  }

  if(q.type==="calc"){
    const box = document.createElement("div");
    box.className="calcBox";
    const inp = document.createElement("input");
    inp.type="text";
    inp.placeholder="Type your answer (e.g., Yes, No, 3.125)";
    inp.value = state.answers[q.id] ?? "";
    inp.addEventListener("input", ()=>{
      state.answers[q.id] = inp.value;
      saveState();
      renderMeta();
      updateNavStyles();
    });
    box.appendChild(inp);
    const hint = document.createElement("div");
    hint.className="note";
    hint.textContent = "Tip: For numeric answers, enter a number (decimals allowed). For Yes/No, type Yes or No.";
    box.appendChild(hint);
    area.appendChild(box);
  }

  if(q.type==="ordered"){
    const ordWrap = document.createElement("div");
    ordWrap.className="ordered";
    let cur = state.answers[q.id]?.order;
    if(!Array.isArray(cur) || cur.length !== q.steps.length){
      cur = Array.from({length:q.steps.length}, (_,i)=> i+1);
      state.answers[q.id] = {order:cur};
      saveState();
    }
    function renderSteps(){
      ordWrap.innerHTML="";
      cur.forEach((stepNum, pos)=>{
        const row = document.createElement("div");
        row.className="step";
        const handle = document.createElement("div");
        handle.className="handle";
        handle.textContent = String(pos+1);
        const txt = document.createElement("div");
        txt.className="txt";
        txt.textContent = q.steps[stepNum-1];
        const arrows = document.createElement("div");
        arrows.className="arrows";
        const up = document.createElement("button");
        up.textContent = "▲";
        up.disabled = pos===0;
        up.addEventListener("click", ()=>{
          const t = cur[pos-1]; cur[pos-1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        const dn = document.createElement("button");
        dn.textContent = "▼";
        dn.disabled = pos===cur.length-1;
        dn.addEventListener("click", ()=>{
          const t = cur[pos+1]; cur[pos+1]=cur[pos]; cur[pos]=t;
          state.answers[q.id] = {order:cur};
          saveState();
          renderSteps();
          renderMeta();
          updateNavStyles();
        });
        arrows.appendChild(up);
        arrows.appendChild(dn);
        row.appendChild(handle);
        row.appendChild(txt);
        row.appendChild(arrows);
        ordWrap.appendChild(row);
      });
      const note = document.createElement("div");
      note.className="note";
      note.textContent = "Use the arrows to place the actions in correct order.";
      ordWrap.appendChild(note);
    }
    renderSteps();
    area.appendChild(ordWrap);
  }

  document.getElementById("prevBtn").disabled = currentIndex===0;
  document.getElementById("nextBtn").disabled = currentIndex===QUESTIONS.length-1;

  updateNavStyles();
  renderMeta();
}

function renderMeta(){
  document.getElementById("answeredCount").textContent = answeredCount();
  document.getElementById("flaggedCount").textContent = flaggedCount();
  const q = QUESTIONS[currentIndex];
  document.getElementById("statusMeta").textContent = isAnswered(q) ? "Answered" : "Not answered";
}

function startTimer(){
  if(tickHandle) clearInterval(tickHandle);
  tickHandle = setInterval(()=>{
    const left = computeTimeLeft();
    document.getElementById("timer").textContent = fmtTime(left);
    if(left <= 0){
      clearInterval(tickHandle);
      tickHandle = null;
      submitExam(true);
    }
  }, 250);
}

function submitExam(auto=false){
  if(state.submitted) return;
  if(!auto){
    const ok = confirm("Submit now? You will see answers and rationales.");
    if(!ok) return;
  }
  state.submitted = true;
  saveState();

  let score=0;
  for(const q of QUESTIONS){
    if(isCorrect(q)) score++;
  }

  document.getElementById("exam").classList.add("hidden");
  document.getElementById("results").classList.remove("hidden");
  document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;

  const body = document.getElementById("resultsBody");
  body.innerHTML = `<p class="note">Auto-grading note: SATA requires an exact match. Ordered response requires the exact sequence. Calculations accept a small numeric tolerance (plus case-insensitive Yes/No).</p>`;

  for(let i=0;i<QUESTIONS.length;i++){
    const q = QUESTIONS[i];
    const ok = isCorrect(q);
    const div = document.createElement("div");
    div.className="resultItem";
    const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
    const your = state.answers[q.id];
    let yourTxt = "";
    let correctTxt = "";

    if(q.type==="mc"){
      yourTxt = your ? your : "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="sata"){
      yourTxt = (Array.isArray(your) && your.length) ? your.slice().sort().join(", ") : "(no answer)";
      correctTxt = q.answer.slice().sort().join(", ");
    } else if(q.type==="calc"){
      yourTxt = (your ?? "").toString().trim() || "(no answer)";
      correctTxt = q.answer[0];
    } else if(q.type==="ordered"){
      const y = (your && Array.isArray(your.order)) ? your.order.join("-") : "(no answer)";
      const c = q.answer_order.join("-");
      yourTxt = y;
      correctTxt = c;
    }

    div.innerHTML = `
      <div style="margin-bottom:6px;">
        ${badge}<strong>Q${i+1}.</strong> ${q.stem}
      </div>
      <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
      <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>
    `;
    body.appendChild(div);
  }

  body.insertAdjacentHTML("beforeend", `
    <div class="controls" style="margin-top:16px;">
      <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
      <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
    </div>
  `);
}

document.getElementById("startBtn").addEventListener("click", ()=>{
  if(state.submitted){
    alert("This attempt is already submitted. Use 'Reset Saved Attempt' to start over.");
    return;
  }
  if(!state.startedAt){
    state.startedAt = Date.now();
    saveState();
  }
  document.getElementById("start").classList.add("hidden");
  document.getElementById("exam").classList.remove("hidden");
  buildNav();
  render();
  document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
  startTimer();
});

document.getElementById("resetBtn").addEventListener("click", ()=>{
  const ok = confirm("Reset saved attempt? This clears answers and timer for this browser.");
  if(!ok) return;
  resetState();
  location.reload();
});

document.getElementById("prevBtn").addEventListener("click", ()=>{
  if(currentIndex>0) currentIndex--;
  render();
});
document.getElementById("nextBtn").addEventListener("click", ()=>{
  if(currentIndex<QUESTIONS.length-1) currentIndex++;
  render();
});
document.getElementById("flagBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  if(state.flagged[q.id]) delete state.flagged[q.id];
  else state.flagged[q.id]=true;
  saveState();
  renderMeta();
  updateNavStyles();
});
document.getElementById("clearBtn").addEventListener("click", ()=>{
  const q = QUESTIONS[currentIndex];
  delete state.answers[q.id];
  if(q.type==="ordered"){
    state.answers[q.id] = {order: Array.from({length:q.steps.length}, (_,i)=> i+1)};
  }
  saveState();
  render();
});
document.getElementById("submitBtn").addEventListener("click", ()=> submitExam(false));

(function init(){
  if(state.submitted){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("results").classList.remove("hidden");
    let score=0;
    for(const q of QUESTIONS) if(isCorrect(q)) score++;
    document.getElementById("scoreText").textContent = `${score}/${QUESTIONS.length}`;
    const body = document.getElementById("resultsBody");
    body.innerHTML = `<p class="note">This attempt was already submitted on this browser.</p>`;
    for(let i=0;i<QUESTIONS.length;i++){
      const q = QUESTIONS[i];
      const ok = isCorrect(q);
      const div = document.createElement("div");
      div.className="resultItem";
      const badge = `<span class="badge ${ok ? "ok":"no"}">${ok ? "Correct":"Incorrect"}</span>`;
      const your = state.answers[q.id];
      let yourTxt="", correctTxt="";
      if(q.type==="mc"){ yourTxt = your ? your : "(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="sata"){ yourTxt=(Array.isArray(your)&&your.length)?your.slice().sort().join(", "):"(no answer)"; correctTxt=q.answer.slice().sort().join(", "); }
      else if(q.type==="calc"){ yourTxt=(your??"").toString().trim()||"(no answer)"; correctTxt=q.answer[0]; }
      else if(q.type==="ordered"){ yourTxt=(your&&Array.isArray(your.order))?your.order.join("-"):"(no answer)"; correctTxt=q.answer_order.join("-"); }
      div.innerHTML = `<div style="margin-bottom:6px;">${badge}<strong>Q${i+1}.</strong> ${q.stem}</div>
        <div class="note"><strong>Your answer:</strong> ${yourTxt} &nbsp;&nbsp; <strong>Correct:</strong> ${correctTxt}</div>
        <div class="rationale"><strong>Rationale:</strong> ${q.rationale}</div>`;
      body.appendChild(div);
    }
    body.insertAdjacentHTML("beforeend", `
      <div class="controls" style="margin-top:16px;">
        <button class="btn ok" onclick="window.print()">Print / Save as PDF</button>
        <button class="btn" onclick="resetState(); location.reload();">Start New Attempt</button>
      </div>
    `);
    return;
  }

  if(state.startedAt){
    document.getElementById("start").classList.add("hidden");
    document.getElementById("exam").classList.remove("hidden");
    buildNav();
    render();
    document.getElementById("timer").textContent = fmtTime(computeTimeLeft());
    startTimer();
  }
})();
</script>
</body>
</html>

