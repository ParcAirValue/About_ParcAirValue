A little help, already on the way

The best delivery route may be one someone’s taking anyway.
Communal connects people who need something delivered with neighbors already traveling that way. One shared trip can make getting an item across town a little more human.

    <div class="actions">
      <a class="btn primary lg" href="/post">
        I need something delivered
      </a>
      <a class="btn lg" href="/trips/new">
        I’m already going somewhere
      </a>
    </div>

    <p class="note">Deliveries are free during launch. No payment is collected.</p>
  </div>

  <section class="demo card pad" data-idea-demo aria-labelledby="demo-title">
    <div class="demo-heading">
      <div>
        <p class="eyebrow">Two sides, one shared trip</p>
        <h2 id="demo-title">Which sounds like you?</h2>
      </div>
      <span class="badge outline">A simple example</span>
    </div>

    <div class="switcher" role="group" aria-label="Choose your perspective">
      <button
        class="btn sm"
        type="button"
        data-idea-choice="requester"
        aria-pressed="true"
      >
        I need a delivery
      </button>
      <button
        class="btn sm"
        type="button"
        data-idea-choice="traveler"
        aria-pressed="false"
      >
        I’m already traveling
      </button>
    </div>

    <section class="story" data-idea-story="requester" aria-live="polite">
      <div class="route" aria-label="From Maple Street to Oak Street">
        <span class="stop"><span class="dot"></span>Maple Street</span>
        <span class="route-line" aria-hidden="true"></span>
        <span class="stop"><span class="dot destination"></span>Oak Street</span>
      </div>
      <h3>A box of books needs a new home.</h3>
      <p>
        Post what needs to go and where. A neighbor heading that way can
        offer to bring it along. You decide whether to accept.
      </p>
      <ol class="steps">
        <li><span>1</span>Post a request</li>
        <li><span>2</span>Choose an offer</li>
        <li><span>3</span>Confirm it arrived</li>
      </ol>
      <a class="btn primary" href="/post">Post a request</a>
    </section>

    <section
      class="story"
      data-idea-story="traveler"
      aria-live="polite"
      hidden
    >
      <div class="route" aria-label="From Maple Street to Oak Street">
        <span class="stop"><span class="dot"></span>Maple Street</span>
        <span class="route-line" aria-hidden="true"></span>
        <span class="stop"><span class="dot destination"></span>Oak Street</span>
      </div>
      <h3>You’re heading across town already.</h3>
      <p>
        Share your route and when you’re going. If someone’s request fits
        your trip, you can offer to carry it and coordinate directly.
      </p>
      <ol class="steps">
        <li><span>1</span>Share your trip</li>
        <li><span>2</span>Find a request</li>
        <li><span>3</span>Deliver together</li>
      </ol>
      <a class="btn primary" href="/trips/new">Share your trip</a>
    </section>
  </section>
</section>

<section class="why card pad" aria-labelledby="why-title">
  <div>
    <p class="eyebrow">A practical kind of community</p>
    <h2 id="why-title">Make use of journeys already happening.</h2>
    <p class="muted">
      Not another delivery fleet. Just a place for people with a need to
      meet people with a route—and work out the handoff together.
    </p>
  </div>

  <div class="facts">
    <div>
      <strong>People set the plan</strong>
      <p class="muted">The requester and traveler coordinate each handoff.</p>
    </div>
    <div>
      <strong>Privacy comes first</strong>
      <p class="muted">Exact addresses aren’t shown on the public board.</p>
    </div>
    <div>
      <strong>Free during launch</strong>
      <p class="muted">There’s no payment processing or charge to use Communal.</p>
    </div>
  </div>
</section>

<footer class="page-footer">
  <p>
    Communal is a community marketplace, not a courier service. Learn about
    handoffs, item restrictions, and what the service does—and doesn’t—provide.
  </p>
  <a class="btn" href="/guidelines">Read how it works and stay safe</a>
</footer>
<script> document.addEventListener("click", (event) => { const target = event.target; if (!(target instanceof Element)) return; const choice = target.closest("[data-idea-choice]"); const demo = choice?.closest("[data-idea-demo]"); if (!choice || !demo) return; for (const button of demo.querySelectorAll( "[data-idea-choice]", )) { button.setAttribute("aria-pressed", String(button === choice)); } for (const story of demo.querySelectorAll( "[data-idea-story]", )) { story.hidden = story.dataset.ideaStory !== choice.dataset.ideaChoice; } }); </script> <style> .idea-page { display: grid; gap: 28px; } .hero { display: grid; grid-template-columns: minmax(0, 1.1fr) minmax(360px, 0.9fr); align-items: center; gap: clamp(24px, 5vw, 64px); padding-block: clamp(24px, 5vw, 64px); } .intro { display: grid; justify-items: start; gap: 18px; max-width: 620px; } .eyebrow { margin: 0; color: var(--muted-foreground); font-size: 0.75rem; font-weight: 650; letter-spacing: 0.09em; text-transform: uppercase; } .intro h1 { max-width: 12ch; font-size: clamp(2.5rem, 5.4vw, 4.75rem); font-weight: 650; letter-spacing: -0.065em; line-height: 1.02; } .lede { max-width: 50ch; color: var(--muted-foreground); font-size: clamp(1rem, 1.3vw, 1.125rem); line-height: 1.7; } .actions { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 4px; } .note { color: var(--muted-foreground); font-size: 0.8125rem; } .demo { display: grid; gap: 20px; padding: clamp(18px, 3vw, 28px); box-shadow: var(--shadow-md); } .demo-heading { display: flex; align-items: start; justify-content: space-between; gap: 12px; } .demo-heading h2 { margin-top: 6px; font-size: 1.25rem; letter-spacing: -0.03em; } .switcher { display: flex; flex-wrap: wrap; gap: 6px; padding: 4px; border-radius: var(--radius-lg); background: var(--muted); } .switcher .btn { flex: 1; border-color: transparent; background: transparent; box-shadow: none; color: var(--muted-foreground); } .switcher .btn[aria-pressed="true"] { background: var(--background); box-shadow: var(--shadow-sm); color: var(--foreground); } .story { display: grid; justify-items: start; gap: 14px; animation: reveal 180ms var(--ease-out) both; } .story[hidden] { display: none; } .story h3 { font-size: 1.125rem; letter-spacing: -0.025em; } .story > p { color: var(--muted-foreground); line-height: 1.6; } .route { display: grid; grid-template-columns: auto minmax(40px, 1fr) auto; align-items: center; gap: 12px; width: 100%; padding: 18px 16px; border-radius: var(--radius-lg); background: var(--muted); color: var(--muted-foreground); font-size: 0.75rem; font-weight: 550; } .stop { display: flex; align-items: center; gap: 8px; white-space: nowrap; } .dot { flex: none; width: 10px; height: 10px; border: 2px solid var(--foreground); border-radius: var(--radius-full); background: var(--background); } .dot.destination { background: var(--foreground); } .route-line { position: relative; height: 2px; background: var(--border); } .route-line::after { position: absolute; top: -3px; left: 42%; width: 8px; height: 8px; border-radius: var(--radius-full); background: var(--foreground); content: ""; } .steps { display: flex; flex-wrap: wrap; gap: 8px 16px; width: 100%; margin: 0; padding: 0; list-style: none; color: var(--muted-foreground); font-size: 0.75rem; } .steps li { display: flex; align-items: center; gap: 6px; } .steps li span { display: grid; place-items: center; width: 20px; height: 20px; border: 1px solid var(--border); border-radius: var(--radius-full); color: var(--foreground); font-size: 0.6875rem; font-weight: 600; } .why { display: grid; grid-template-columns: minmax(0, 0.8fr) minmax(0, 1.2fr); align-items: start; gap: 32px; } .why h2 { max-width: 18ch; margin-block: 8px 10px; font-size: clamp(1.5rem, 3vw, 2rem); letter-spacing: -0.045em; } .why > div:first-child > p:last-child { max-width: 46ch; line-height: 1.6; } .facts { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 20px; } .facts > div { display: grid; align-content: start; gap: 8px; } .facts strong { font-size: 0.875rem; } .facts p, .page-footer p { font-size: 0.8125rem; line-height: 1.6; } .page-footer { display: flex; align-items: center; justify-content: space-between; gap: 16px; padding: 0 4px 16px; } .page-footer p { max-width: 70ch; color: var(--muted-foreground); } @keyframes reveal { from { opacity: 0; transform: translateY(4px); } } @media (max-width: 900px) { .hero, .why { grid-template-columns: minmax(0, 1fr); } .intro { max-width: 720px; } } @media (max-width: 560px) { .hero { padding-block: 12px 24px; } .demo-heading { display: grid; } .route { grid-template-columns: minmax(0, 1fr); gap: 10px; } .route-line { width: 2px; height: 18px; margin-left: 4px; } .route-line::after { top: 6px; left: -3px; } .facts { grid-template-columns: minmax(0, 1fr); gap: 16px; } .page-footer { align-items: start; flex-direction: column; } } @media (prefers-reduced-motion: reduce) { .story { animation: none; } } </style> ```
