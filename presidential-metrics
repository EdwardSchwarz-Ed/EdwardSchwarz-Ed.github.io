import { useState } from “react”;

const data = {
helped: [
{
title: “Real Median Income Growth”,
desc: “Did the typical family actually get richer?”,
top: [
{ name: “Harry Truman”, years: “1945–53”, note: “Post-war boom created the modern middle class; median incomes surged ~30% as wartime savings met consumer demand.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Great Society + booming economy drove broad-based wage gains; poverty fell sharply and real wages climbed across all quintiles.” },
{ name: “Bill Clinton”, years: “1993–2001”, note: “Tech boom, tight labor markets, and fiscal discipline produced the strongest median income gains since the 1960s.” },
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Steady, widely shared prosperity; the interstate highway system and GI Bill investments lifted working families.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Starting from Depression lows, New Deal programs and wartime mobilization pulled millions into the workforce and up the income ladder.” },
],
bottom: [
{ name: “Herbert Hoover”, years: “1929–33”, note: “Great Depression wiped out incomes at every level; real wages collapsed alongside employment.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Median household income was lower when he left than when he arrived — the first president since tracking began to post a net decline.” },
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First-term pre-COVID gains were modest and top-heavy; pandemic erased them. Second term: tariffs raised effective rates from 2.5% to 27%, pushing consumer prices higher. 75% of Americans say tariffs are raising prices, and only 12% believe policies help the middle class.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Stagflation began eating into real wages; oil shocks and inflation eroded purchasing power.” },
{ name: “George H.W. Bush”, years: “1989–93”, note: “Recession of 1990–91 stalled income growth; median households saw essentially flat real wages.” },
],
},
{
title: “Life Expectancy Change”,
desc: “Did Americans live longer after this president served?”,
top: [
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Life expectancy rose ~7 years across his tenure — antibiotics, public health infrastructure, and New Deal sanitation programs.” },
{ name: “Theodore Roosevelt”, years: “1901–09”, note: “Pure Food and Drug Act, meat inspection, public health reforms laid groundwork for dramatic gains in the following decades.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Medicare and Medicaid gave millions of elderly and poor Americans access to healthcare for the first time.” },
{ name: “Harry Truman”, years: “1945–53”, note: “Post-war medical advances (penicillin mass production, polio research funding) drove significant longevity gains.” },
{ name: “Barack Obama”, years: “2009–17”, note: “ACA expanded coverage to ~20 million uninsured Americans; maternal mortality and uninsured rates dropped.” },
],
bottom: [
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term saw the first sustained U.S. life expectancy decline in a century (COVID + opioids). Second term: the 2025 megabill cut Medicaid and SNAP, health insurance premiums surged on exchanges, and 2,000 EPA staff were cut — crippling environmental health enforcement.” },
{ name: “Woodrow Wilson”, years: “1913–21”, note: “1918 flu pandemic killed ~675,000 Americans; WWI casualties compounded the toll.” },
{ name: “Warren Harding”, years: “1921–23”, note: “Rolled back public health infrastructure; life expectancy gains stalled as Progressive-era programs were defunded.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Life expectancy gains flatlined; opioid prescribing accelerated dramatically under lax regulatory oversight.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Despite creating EPA, environmental and occupational health protections were slow to impact mortality; Vietnam casualties mounted.” },
],
},
{
title: “Expansion of Civil Rights & Liberties”,
desc: “Did they broaden freedoms and equal protection?”,
top: [
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Civil Rights Act, Voting Rights Act, Fair Housing Act — the most consequential civil rights legislation since Reconstruction.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Executive Order 8802 banned employment discrimination in defense industries; appointed first Black federal judge. Mixed record due to Japanese internment.” },
{ name: “Barack Obama”, years: “2009–17”, note: “Marriage equality achieved via judicial appointments; DACA protected Dreamers; Lilly Ledbetter Fair Pay Act.” },
{ name: “Harry Truman”, years: “1945–53”, note: “Desegregated the military via Executive Order 9981; established the President’s Committee on Civil Rights.” },
{ name: “Theodore Roosevelt”, years: “1901–09”, note: “First president to invite a Black American (Booker T. Washington) to dine at the White House; expanded federal civil service protections.” },
],
bottom: [
{ name: “Woodrow Wilson”, years: “1913–21”, note: “Re-segregated the federal workforce; screened ‘Birth of a Nation’ at the White House; suppressed dissent with the Sedition Act.” },
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: Muslim travel ban, family separation, transgender military ban. Second term: rescinded LBJ’s Executive Order 11246 (workplace anti-discrimination), pardoned Jan. 6 insurrectionists, ended all federal DEI programs, dismissed civil rights complaints on book banning, and DOJ Civil Rights Division was redirected away from racial discrimination cases.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “War on Drugs explicitly designed to target Black communities and anti-war activists, per aide John Ehrlichman’s later admission.” },
{ name: “George W. Bush”, years: “2001–09”, note: “PATRIOT Act mass surveillance; Guantánamo Bay indefinite detention; warrantless wiretapping programs.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Japanese American internment — 120,000 people imprisoned without due process. Appears in both top and bottom for this reason.” },
],
},
{
title: “Reduction in Poverty Rate”,
desc: “Did fewer Americans live in poverty when they left?”,
top: [
{ name: “Lyndon Johnson”, years: “1963–69”, note: “War on Poverty cut the rate from ~19% to ~12% — the single largest sustained reduction on record.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Social Security, WPA, CCC, and wartime employment pulled tens of millions out of destitution.” },
{ name: “Bill Clinton”, years: “1993–2001”, note: “Poverty rate fell from 15.1% to 11.3%; EITC expansion was the key mechanism lifting working families.” },
{ name: “Barack Obama”, years: “2009–17”, note: “Inherited crisis-level poverty from the Great Recession; ACA and recovery measures brought the rate back down to pre-crisis levels.” },
{ name: “Harry Truman”, years: “1945–53”, note: “GI Bill and post-war boom moved millions of veterans and their families into the middle class.” },
],
bottom: [
{ name: “Herbert Hoover”, years: “1929–33”, note: “Poverty exploded during the Depression; unemployment hit 25% with no federal safety net.” },
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: pre-COVID declines reversed by pandemic. Second term: the 2025 megabill slashed Medicaid and SNAP (food assistance), with EPI analysis projecting it will sharply lower incomes for the bottom half of U.S. households. Tax cuts overwhelmingly favor the wealthy.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Poverty rate rose from 11.3% to 14.3%, driven by two recessions and stagnant wages.” },
{ name: “Ronald Reagan”, years: “1981–89”, note: “Slashed safety-net programs; poverty spiked early in his term and remained elevated, especially among children.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Despite proposing a guaranteed income (FAP), it never passed; stagflation pushed more families below the line.” },
],
},
{
title: “Diplomatic Achievements & Conflict Avoidance”,
desc: “Did they strengthen alliances, avoid unnecessary wars, or negotiate durable peace?”,
top: [
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Ended the Korean War, resisted military adventurism despite pressure (Dien Bien Phu, Suez), kept Cold War from going hot.” },
{ name: “Theodore Roosevelt”, years: “1901–09”, note: “Nobel Peace Prize for mediating the Russo-Japanese War; expanded American diplomacy without major military entanglements.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Built the Allied coalition, conceived the United Nations framework, managed an unavoidable war with extraordinary coalition diplomacy.” },
{ name: “Jimmy Carter”, years: “1977–81”, note: “Camp David Accords remain the most durable Middle East peace agreement; Panama Canal Treaty avoided a long-term conflict.” },
{ name: “George H.W. Bush”, years: “1989–93”, note: “Managed the end of the Cold War and German reunification without conflict; restrained Gulf War with clear objectives and exit.” },
],
bottom: [
{ name: “George W. Bush”, years: “2001–09”, note: “Iraq War launched on false WMD premises — destabilized the Middle East for decades; ~4,500 U.S. dead, hundreds of thousands of Iraqi civilians.” },
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: withdrew from Iran deal, Paris Agreement, strained NATO. Second term: cooled relations with closest allies (Canada, Mexico, EU), shifted support from Ukraine toward Russia, launched military action against Iran, and dismantled USAID. Chief Justice Roberts described the rule of law as ‘endangered.’” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Massive Vietnam escalation based on Gulf of Tonkin; 58,000 American dead, millions of Vietnamese casualties.” },
{ name: “Woodrow Wilson”, years: “1913–21”, note: “Entered WWI after campaigning against it; Treaty of Versailles created conditions for WWII; interventions in Latin America.” },
{ name: “William McKinley”, years: “1897–1901”, note: “Spanish-American War launched an era of imperial expansion; Philippine-American War killed 200,000+ Filipino civilians.” },
],
},
],
hurt: [
{
title: “Growth in National Debt (% of GDP)”,
desc: “Did they borrow recklessly relative to the economy?”,
top: [
{ name: “Bill Clinton”, years: “1993–2001”, note: “Only modern president to run budget surpluses; debt-to-GDP ratio fell significantly. Left office with projected surpluses.” },
{ name: “Harry Truman”, years: “1945–53”, note: “Debt-to-GDP fell from its WWII peak of 112% down to ~70% through fiscal discipline and rapid economic growth.” },
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Continued reducing the debt ratio through balanced budgets and strong growth; fiscal conservative in practice, not just rhetoric.” },
{ name: “Calvin Coolidge”, years: “1923–29”, note: “Reduced the national debt in absolute terms; federal spending shrank under his watch.” },
{ name: “Jimmy Carter”, years: “1977–81”, note: “Debt-to-GDP remained relatively stable and low (~32%); restrained spending despite economic headwinds.” },
],
bottom: [
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: debt-to-GDP surged from ~76% to ~100% via 2017 tax cuts and pandemic spending. Second term: the 2025 megabill adds $4+ trillion in projected deficits. DOGE claimed $215B in savings but multiple analyses found this was overstated and miscalculated.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Inherited surpluses, left with $1T+ annual deficits; two wars and tax cuts swung the fiscal picture dramatically.” },
{ name: “Ronald Reagan”, years: “1981–89”, note: “Debt nearly tripled in nominal terms; tax cuts without corresponding spending cuts created structural deficits.” },
{ name: “Barack Obama”, years: “2009–17”, note: “Debt-to-GDP rose from ~64% to ~76%, though largely driven by inherited Great Recession and necessary stimulus spending.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Debt-to-GDP went from ~40% to 112% — but fighting the Depression and WWII were existential necessities. Context matters enormously here.” },
],
},
{
title: “Increase in Income Inequality (Gini)”,
desc: “Did the gap between richest and poorest widen?”,
top: [
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “The ‘Great Compression’ — progressive taxation, labor rights, and wage controls dramatically narrowed inequality.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “War on Poverty, Medicare/Medicaid, and education spending reduced inequality across racial and economic lines.” },
{ name: “Harry Truman”, years: “1945–53”, note: “Maintained FDR’s progressive tax structure; GI Bill created mass upward mobility; union membership peaked.” },
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Top marginal tax rate stayed at 91%; middle-class prosperity was the norm, not the exception.” },
{ name: “Bill Clinton”, years: “1993–2001”, note: “EITC expansion and tight labor markets helped the bottom quintile gain faster than in decades, though Gini still edged up.” },
],
bottom: [
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: 2017 TCJA disproportionately favored corporations and high earners. Second term: the megabill pairs tax cuts for the wealthy with Medicaid/SNAP cuts for the poor — EPI calls it the largest single upward redistribution since 1979. 65% of Americans say his policies favor the wealthy.” },
{ name: “Ronald Reagan”, years: “1981–89”, note: “Top tax rate slashed from 70% to 28%; union-busting (PATCO); deregulation. The Gini coefficient’s modern upward trajectory starts here.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Tax cuts overwhelmingly favored top earners; capital gains preferences widened the wealth gap further.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Wage stagnation began for lower-income workers while professional-class incomes kept rising; a structural divergence took root.” },
{ name: “Calvin Coolidge”, years: “1923–29”, note: “The original ‘Roaring Twenties’ inequality surge — tax cuts for the wealthy, minimal regulation, speculative boom favoring capital owners.” },
],
},
{
title: “Erosion of Institutional Trust”,
desc: “Did this president leave Americans more cynical about their own system?”,
top: [
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Trust in government exceeded 70% throughout his tenure; seen as nonpartisan, competent, honest.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “Restored faith in government during the Depression; fireside chats built a direct bond with citizens.” },
{ name: “John F. Kennedy”, years: “1961–63”, note: “Trust peaked near 77% — highest ever recorded. Inspired civic engagement across generations.” },
{ name: “Harry Truman”, years: “1945–53”, note: “Despite low approval at times, institutional trust remained high; the public trusted the system even when they disliked the president.” },
{ name: “Theodore Roosevelt”, years: “1901–09”, note: “Trust-busting paradoxically built trust in government as a protector of ordinary people against monopolies.” },
],
bottom: [
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: attacked elections, courts, media, intelligence agencies. Second term: fired the BLS commissioner over unfavorable data, attacked Fed independence, DOGE dismantled agencies. Gallup ended its presidential approval tracking entirely. Pew: 37% approval, 50% say things are worse than expected. Only 29% trust the presidency, 14% trust Congress.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Watergate is the single most corrosive event in the history of American institutional trust. Trust in government dropped from ~60% to ~36%.” },
{ name: “George W. Bush”, years: “2001–09”, note: “WMD falsehoods, Hurricane Katrina, and financial crisis each independently cratered public confidence; together they were devastating.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Credibility gap over Vietnam — the Pentagon Papers later confirmed the administration systematically misled the public.” },
{ name: “Woodrow Wilson”, years: “1913–21”, note: “Sedition Act prosecutions, secret disability, and heavy-handed propaganda (Committee on Public Information) planted seeds of government distrust.” },
],
},
{
title: “Military Casualties from Initiated/Escalated Conflicts”,
desc: “The human cost of wars they chose to start or dramatically expand.”,
top: [
{ name: “Jimmy Carter”, years: “1977–81”, note: “Zero major military engagements; only U.S. combat deaths were the 8 servicemembers in the failed Iran hostage rescue.” },
{ name: “Dwight Eisenhower”, years: “1953–61”, note: “Ended Korea, refused to enter Vietnam or intervene in multiple crises despite pressure. Remarkably restrained for a former general.” },
{ name: “Bill Clinton”, years: “1993–2001”, note: “Kosovo air campaign had zero U.S. combat deaths; interventions in Bosnia and Haiti were limited and relatively low-casualty.” },
{ name: “Gerald Ford”, years: “1974–77”, note: “Oversaw the final withdrawal from Vietnam; no new military engagements initiated.” },
{ name: “Barack Obama”, years: “2009–17”, note: “Ended Iraq combat operations; Afghan surge had costs, but avoided new large-scale ground wars. Drone program is the major criticism.” },
],
bottom: [
{ name: “Woodrow Wilson”, years: “1913–21”, note: “WWI entry cost 116,000 American lives after campaigning on neutrality.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Escalated Vietnam from ~16,000 advisors to 535,000 troops; the bulk of the war’s 58,000 U.S. deaths occurred on his watch.” },
{ name: “George W. Bush”, years: “2001–09”, note: “~4,500 U.S. dead in Iraq (a war of choice); ~500 in Afghanistan. Hundreds of thousands of civilian casualties in both theaters.” },
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term was relatively restrained militarily. Second term: launched military operations against Iran that most Americans oppose. Full casualty data is still emerging, but the conflict has spiked gas prices and drawn broad frustration.” },
{ name: “William McKinley”, years: “1897–1901”, note: “Spanish-American War and Philippine insurrection; thousands of U.S. dead, hundreds of thousands of Filipino civilians killed.” },
],
},
{
title: “Deterioration of Public Health or Environment”,
desc: “Did health outcomes worsen or environmental protections get rolled back?”,
top: [
{ name: “Theodore Roosevelt”, years: “1901–09”, note: “National parks system, Pure Food and Drug Act, forest reserves — invented federal environmental protection.” },
{ name: “Richard Nixon”, years: “1969–74”, note: “Created the EPA, signed the Clean Air and Clean Water Acts. His best legacy by far, and bipartisan at the time.” },
{ name: “Lyndon Johnson”, years: “1963–69”, note: “Clean Air Act of 1963, Wilderness Act, Medicare/Medicaid — health and environment both advanced dramatically.” },
{ name: “Barack Obama”, years: “2009–17”, note: “Paris Climate Agreement, Clean Power Plan, ACA expanded preventive care; reduced uninsured rate to historic lows.” },
{ name: “Franklin Roosevelt”, years: “1933–45”, note: “CCC planted 3 billion trees; rural electrification improved sanitation; Social Security created a health safety net for the elderly.” },
],
bottom: [
{ name: “Donald Trump”, years: “2017–21, 2025–”, note: “First term: withdrew from Paris, 100+ rollbacks, COVID response failures (400K+ dead). Second term: EPA lost 2,000 staff, moved to rescind the Endangerment Finding (basis of all climate regulation), gutted Clean Air/Water Act enforcement, cut soot and mercury protections, National Park Service lost 24% of staff, opened 59M acres of forest to logging, and the megabill cut healthcare for the poor.” },
{ name: “George W. Bush”, years: “2001–09”, note: “Weakened Clean Air Act enforcement; opioid crisis accelerated under lax FDA oversight; rejected Kyoto Protocol.” },
{ name: “Ronald Reagan”, years: “1981–89”, note: “Gutted EPA staffing and enforcement; slow AIDS response allowed an epidemic to metastasize; James Watt as Interior Secretary.” },
{ name: “Calvin Coolidge”, years: “1923–29”, note: “Laissez-faire approach meant no federal response to workplace safety, environmental contamination, or public health infrastructure.” },
{ name: “Warren Harding”, years: “1921–23”, note: “Teapot Dome scandal involved selling off public oil reserves; dismantled Progressive-era public health and conservation programs.” },
],
},
],
};

const Medal = ({ rank }) => {
const colors = [”#c9a84c”, “#8a8a8a”, “#a0613a”];
if (rank < 3) return (
<span style={{
display: “inline-flex”, alignItems: “center”, justifyContent: “center”,
width: 26, height: 26, borderRadius: “50%”,
background: colors[rank], color: “#1a1a1a”,
fontWeight: 800, fontSize: 13, marginRight: 10, flexShrink: 0,
boxShadow: `0 1px 3px ${colors[rank]}66`
}}>{rank + 1}</span>
);
return (
<span style={{
display: “inline-flex”, alignItems: “center”, justifyContent: “center”,
width: 26, height: 26, borderRadius: “50%”,
background: “#2a2a2a”, color: “#999”,
fontWeight: 700, fontSize: 13, marginRight: 10, flexShrink: 0
}}>{rank + 1}</span>
);
};

const Card = ({ entry, rank, isBad }) => (

  <div style={{
    padding: "14px 16px", marginBottom: 8,
    background: "#1e1e1e", borderRadius: 10,
    borderLeft: `3px solid ${isBad ? "#c0392b" : "#27ae60"}`,
  }}>
    <div style={{ display: "flex", alignItems: "center", marginBottom: 6 }}>
      <Medal rank={rank} />
      <div>
        <div style={{ fontWeight: 700, fontSize: 15, color: "#eee" }}>{entry.name}</div>
        {entry.years && <div style={{ fontSize: 12, color: "#888" }}>{entry.years}</div>}
      </div>
    </div>
    <div style={{ fontSize: 13.5, color: "#bbb", lineHeight: 1.55, paddingLeft: 36 }}>
      {entry.note}
    </div>
  </div>
);

export default function App() {
const [catIdx, setCatIdx] = useState(0);
const [metricIdx, setMetricIdx] = useState(0);
const cats = [“Helped”, “Hurt”];
const currentMetrics = catIdx === 0 ? data.helped : data.hurt;
const metric = currentMetrics[metricIdx];

return (
<div style={{
minHeight: “100vh”, background: “#111”, color: “#eee”,
fontFamily: “‘IBM Plex Sans’, ‘Segoe UI’, system-ui, sans-serif”,
maxWidth: 640, margin: “0 auto”
}}>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;600;700;800&display=swap" rel="stylesheet" />

```
  <div style={{ padding: "24px 16px 12px", borderBottom: "1px solid #222" }}>
    <h1 style={{ fontSize: 22, fontWeight: 800, margin: 0, letterSpacing: -0.5 }}>
      Presidential Scorecard
    </h1>
    <p style={{ fontSize: 13, color: "#777", margin: "4px 0 0" }}>
      Last 125 years · Top 5 & Bottom 5 per metric
    </p>
    <p style={{ fontSize: 11, color: "#555", margin: "4px 0 0", fontStyle: "italic" }}>
      Trump entry reflects combined terms (2017–21 & 2025–present)
    </p>
  </div>

  <div style={{ display: "flex", gap: 0, borderBottom: "1px solid #222" }}>
    {cats.map((c, i) => (
      <button key={c} onClick={() => { setCatIdx(i); setMetricIdx(0); }} style={{
        flex: 1, padding: "12px 0", border: "none", cursor: "pointer",
        background: catIdx === i ? (i === 0 ? "#1a3a1a" : "#3a1a1a") : "transparent",
        color: catIdx === i ? (i === 0 ? "#5fd068" : "#e74c3c") : "#666",
        fontWeight: 700, fontSize: 14, fontFamily: "inherit",
        borderBottom: catIdx === i ? `2px solid ${i === 0 ? "#5fd068" : "#e74c3c"}` : "2px solid transparent",
        transition: "all 0.2s"
      }}>{i === 0 ? "✦ " : "✧ "}{c} the Country</button>
    ))}
  </div>

  <div style={{
    display: "flex", gap: 6, padding: "12px 16px",
    overflowX: "auto", scrollbarWidth: "none"
  }}>
    {currentMetrics.map((m, i) => (
      <button key={i} onClick={() => setMetricIdx(i)} style={{
        padding: "8px 14px", borderRadius: 20, border: "1px solid",
        borderColor: metricIdx === i ? (catIdx === 0 ? "#5fd068" : "#e74c3c") : "#333",
        background: metricIdx === i ? (catIdx === 0 ? "#1a3a1a" : "#3a1a1a") : "#1a1a1a",
        color: metricIdx === i ? "#eee" : "#888",
        fontSize: 12, fontWeight: 600, cursor: "pointer", whiteSpace: "nowrap",
        fontFamily: "inherit", transition: "all 0.15s"
      }}>{i + 1}</button>
    ))}
  </div>

  <div style={{ padding: "4px 16px 12px" }}>
    <h2 style={{ fontSize: 17, fontWeight: 700, margin: 0, color: "#eee" }}>
      {metric.title}
    </h2>
    <p style={{ fontSize: 13, color: "#888", margin: "4px 0 0" }}>{metric.desc}</p>
  </div>

  <div style={{ padding: "0 16px" }}>
    <div style={{
      fontSize: 11, fontWeight: 700, textTransform: "uppercase", letterSpacing: 1.5,
      color: catIdx === 0 ? "#5fd068" : "#e74c3c", marginBottom: 8,
      padding: "0 4px"
    }}>
      {catIdx === 0 ? "▲ Best" : "▲ Least Damage"}
    </div>
    {metric.top.map((e, i) => <Card key={i} entry={e} rank={i} isBad={false} />)}
  </div>

  <div style={{ padding: "20px 16px 32px" }}>
    <div style={{
      fontSize: 11, fontWeight: 700, textTransform: "uppercase", letterSpacing: 1.5,
      color: "#e74c3c", marginBottom: 8,
      padding: "0 4px"
    }}>
      {catIdx === 0 ? "▼ Worst" : "▼ Most Damage"}
    </div>
    {metric.bottom.map((e, i) => <Card key={i} entry={e} rank={i} isBad={true} />)}
  </div>

  <div style={{ padding: "0 16px 24px", fontSize: 11, color: "#555", lineHeight: 1.6 }}>
    Note: Trump's second term (2025–present) is still ongoing. Rankings incorporate available data through early 2026 from Brookings, Pew, EPI, CEPR, and other sources but may shift as the term continues. Many presidents appear in both positive and negative lists across different metrics — reflecting the genuine complexity of governance.
  </div>
</div>
```

);
}
