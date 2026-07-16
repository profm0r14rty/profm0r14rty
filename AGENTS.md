This project is the EXISTING Lovable-built static site at docs/index.html /
docs/404.html — do not change its visual design. Keep the exact color
tokens, fonts (JetBrains Mono), layout, and existing effects (glitch text,
scanlines/scan bar, matrix-rain canvas, terminal boot-type animation, tile
hover underline/arrow, blinking caret, footer signal dot) precisely as they
are. Nothing about the current look changes in this project.

What you ARE doing:
1. Fill in the real content constants (IDENTITY / SOCIALS / STACK) — see
   data below — replacing every placeholder value.
2. Add a small set of NEW, lightweight, purely additive animations (listed
   in Phase 2) — vanilla JS/CSS only, no new libraries or CDNs beyond the
   existing Google Fonts link, GPU-cheap (transform/opacity only), gated
   behind prefers-reduced-motion so they never override anyone's OS
   setting.
3. Get the repo genuinely ready to deploy on GitHub Pages: correct docs/
   folder layout, a working favicon, correct meta/SEO tags, clean git
   history to push.

Do not touch CSS custom properties, class names, or the existing JS effects
(matrix canvas, glitch spans, typed terminal) beyond what's explicitly asked
in later phases.

CONTENT — use exactly this:

IDENTITY:
  handle:   "profm0r14rty"      -> tiny top-left header (existing slot,
                                    already wired to IDENTITY.handle — no
                                    template change needed)
  name:     "profm0r14rty"      -> the BIG glitch title (existing slot,
                                    already wired to IDENTITY.name — this is
                                    the "main highlight" you asked for)
  realName: "Pratyay Mukherjee" -> Rendered as one new small line
                                    directly under the glitch <h1>, styled
                                    consistently with the existing .role
                                    text (same muted color/size family).
  college:  "NFSU, Agartala"    -> Rendered directly under realName,
                                    slightly smaller font-size (.875rem),
                                    same muted text treatment.
  role:     "forensic science student · offensive security · CTF player · coder"
  location: "somewhere on the grid"
             (kept from the template default, deliberately vague — tell me
             if you'd rather show an actual city)
  bio:      "Forensic Science student @ NFSU · pivoting hard into cybersecurity.
             I build tools at the intersection of digital forensics, cryptography,
             and the terminal. Self-hosted. Privacy-first. Anti-bloat."
             (feeds the typed terminal boot sequence)

SOCIALS (in this order — this REPLACES the placeholder array entirely,
including removing the Discord entry):
  { label: "GitHub",    href: "https://github.com/profm0r14rty",
    user: "profm0r14rty", cmd: "git remote -v" }
  { label: "LinkedIn",  href: "https://www.linkedin.com/in/pratyay-mukherjee-734893235/",
    user: "Pratyay Mukherjee", cmd: "curl linkedin.com" }
  { label: "X",         href: "https://x.com/PratyayM_03",
    user: "@PratyayM_03", cmd: "ssh x.com" }
  { label: "Email",     href: "mailto:prof.m0r14rty@proton.me",
    user: "prof.m0r14rty@proton.me", cmd: "mail -s hi" }
  { label: "Instagram", href: "https://www.instagram.com/somehow_somewhere_existing/",
    user: "@somehow_somewhere_existing", cmd: "wget /media" }
  { label: "Tumblr",    href: "https://www.tumblr.com/profm0r14rty",
    user: "profm0r14rty", cmd: "tail -f ./blog" }

No Discord tile anywhere. No Strava link was given — skip it for now, it's
a one-line addition to this array later if you send me a URL.

STACK (replace the placeholder chip list):
  ["linux","bash","python","html","css","javascript","c","neovim",
   "full stack","php","cyber security","burp suite","nmap"]

OS_LIST (rendered as a data-driven section below ./stack):
  { context: "daily driver",        value: "CachyOS + Hyprland" }
  { context: "ctf / cybersecurity",  value: "Kali Linux + i3wm" }
  { context: "need to disappear",    value: "Tails OS" }

WORKFLOW
I'll send the rest in numbered phases. After each phase, summarize exactly
which files/lines you touched, and don't make any change outside what that
phase asks for.
