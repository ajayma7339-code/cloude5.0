<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Claude Opus 5.0 — Anthropic</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg:       #06060a;
    --surface:  #0d0d14;
    --panel:    #111119;
    --border:   #1e1e2e;
    --border2:  #2a2a3e;
    --gold:     #c9a96e;
    --gold-dim: #7a5f38;
    --gold-glow:#c9a96e33;
    --cream:    #f0ead8;
    --muted:    #5a5a72;
    --muted2:   #3a3a52;
    --accent:   #7b61ff;
    --accent2:  #a78bfa;
    --text:     #e8e4d9;
    --radius:   14px;
    --font-head:'Syne', sans-serif;
    --font-body:'DM Serif Display', serif;
    --font-mono:'DM Mono', monospace;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html, body {
    height: 100%;
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    font-size: 16px;
    line-height: 1.7;
    overflow: hidden;
  }

  /* ── NOISE OVERLAY ── */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
    opacity: 0.022;
    pointer-events: none;
    z-index: 9999;
  }

  /* ── AMBIENT GLOW ── */
  .ambient {
    position: fixed; top: -30%; left: 50%; transform: translateX(-50%);
    width: 900px; height: 500px;
    background: radial-gradient(ellipse at center, #c9a96e08 0%, transparent 70%);
    pointer-events: none; z-index: 0;
    animation: pulseAmb 8s ease-in-out infinite;
  }
  @keyframes pulseAmb {
    0%,100% { opacity: 0.6; transform: translateX(-50%) scale(1); }
    50%      { opacity: 1;   transform: translateX(-50%) scale(1.05); }
  }

  /* ── LAYOUT ── */
  #app {
    position: relative; z-index: 1;
    display: grid;
    grid-template-rows: 64px 1fr auto;
    height: 100vh;
    max-width: 900px;
    margin: 0 auto;
  }

  /* ── HEADER ── */
  header {
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 28px;
    border-bottom: 1px solid var(--border);
    background: linear-gradient(180deg, #0d0d1490 0%, transparent 100%);
    backdrop-filter: blur(12px);
    position: sticky; top: 0; z-index: 10;
  }
  .brand {
    display: flex; align-items: center; gap: 12px;
  }
  .logo-mark {
    width: 34px; height: 34px;
    border: 1.5px solid var(--gold);
    border-radius: 8px;
    display: grid; place-items: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 0 16px var(--gold-glow);
  }
  .logo-mark svg { width: 18px; height: 18px; }
  .brand-text {
    display: flex; flex-direction: column; gap: 1px;
  }
  .brand-name {
    font-family: var(--font-head);
    font-size: 13px; font-weight: 700;
    letter-spacing: 0.06em; text-transform: uppercase;
    color: var(--gold);
    line-height: 1;
  }
  .brand-model {
    font-family: var(--font-mono);
    font-size: 10px; color: var(--muted);
    letter-spacing: 0.08em;
    line-height: 1;
  }
  .header-status {
    display: flex; align-items: center; gap: 8px;
    font-family: var(--font-mono); font-size: 11px; color: var(--muted);
  }
  .status-dot {
    width: 6px; height: 6px; border-radius: 50%;
    background: #4ade80;
    box-shadow: 0 0 8px #4ade8088;
    animation: blink 2.5s ease-in-out infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.4} }

  /* ── MESSAGES AREA ── */
  #messages {
    overflow-y: auto;
    padding: 32px 28px 16px;
    display: flex; flex-direction: column; gap: 28px;
    scroll-behavior: smooth;
  }
  #messages::-webkit-scrollbar { width: 4px; }
  #messages::-webkit-scrollbar-track { background: transparent; }
  #messages::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 2px; }

  /* ── WELCOME ── */
  .welcome {
    display: flex; flex-direction: column; align-items: center;
    justify-content: center; gap: 20px;
    padding: 60px 0 40px;
    text-align: center;
    animation: fadeUp 0.8s cubic-bezier(0.16,1,0.3,1) both;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .welcome-glyph {
    width: 72px; height: 72px;
    border: 1.5px solid var(--gold);
    border-radius: 18px;
    display: grid; place-items: center;
    background: linear-gradient(135deg, #1a1608 0%, #0d0d14 100%);
    box-shadow: 0 0 40px var(--gold-glow), inset 0 1px 0 #c9a96e22;
    animation: floatGlyph 4s ease-in-out infinite;
  }
  @keyframes floatGlyph {
    0%,100%{ transform: translateY(0); }
    50%    { transform: translateY(-6px); }
  }
  .welcome-glyph svg { width: 36px; height: 36px; }
  .welcome h1 {
    font-family: var(--font-head);
    font-size: clamp(26px, 4vw, 38px);
    font-weight: 800;
    letter-spacing: -0.02em;
    color: var(--cream);
    line-height: 1.1;
  }
  .welcome h1 span { color: var(--gold); }
  .welcome p {
    font-size: 15px; color: var(--muted);
    max-width: 420px; line-height: 1.65;
  }
  .chips {
    display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;
    margin-top: 8px;
  }
  .chip {
    padding: 8px 16px;
    border: 1px solid var(--border2);
    border-radius: 100px;
    background: var(--panel);
    font-family: var(--font-mono);
    font-size: 12px; color: var(--muted);
    cursor: pointer;
    transition: all 0.2s;
  }
  .chip:hover {
    border-color: var(--gold-dim);
    color: var(--gold);
    background: #1a160822;
  }

  /* ── MESSAGE BUBBLES ── */
  .msg {
    display: flex; gap: 14px;
    animation: msgIn 0.4s cubic-bezier(0.16,1,0.3,1) both;
  }
  @keyframes msgIn {
    from { opacity: 0; transform: translateY(10px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .msg.user { flex-direction: row-reverse; }

  .avatar {
    width: 34px; height: 34px; border-radius: 9px;
    flex-shrink: 0;
    display: grid; place-items: center;
    font-family: var(--font-head);
    font-size: 12px; font-weight: 700;
    letter-spacing: 0.05em;
    margin-top: 2px;
  }
  .avatar.ai {
    border: 1px solid var(--gold-dim);
    background: linear-gradient(135deg, #1a1608, #0d0d14);
    color: var(--gold);
    box-shadow: 0 0 12px var(--gold-glow);
  }
  .avatar.human {
    background: linear-gradient(135deg, #1e1e35, #111119);
    border: 1px solid var(--border2);
    color: var(--muted);
  }

  .bubble {
    max-width: 72%;
    padding: 14px 18px;
    border-radius: var(--radius);
    font-size: 15px; line-height: 1.72;
    position: relative;
    overflow: hidden;
  }
  .msg.assistant .bubble {
    background: var(--panel);
    border: 1px solid var(--border);
    color: var(--text);
    border-top-left-radius: 4px;
  }
  .msg.user .bubble {
    background: linear-gradient(135deg, #1c1a0f 0%, #161420 100%);
    border: 1px solid var(--gold-dim);
    color: var(--cream);
    border-top-right-radius: 4px;
  }
  .bubble::before {
    content:''; position:absolute; inset:0;
    background: linear-gradient(135deg, #ffffff04 0%, transparent 60%);
    pointer-events: none;
  }

  /* inline code */
  .bubble code {
    font-family: var(--font-mono);
    font-size: 13px;
    background: #ffffff08;
    border: 1px solid var(--border2);
    border-radius: 5px;
    padding: 1px 6px;
    color: var(--gold);
  }
  /* code blocks */
  .bubble pre {
    background: #0a0a10;
    border: 1px solid var(--border2);
    border-radius: 10px;
    padding: 16px;
    overflow-x: auto;
    margin: 10px 0;
    font-family: var(--font-mono);
    font-size: 13px;
    line-height: 1.6;
    color: #a8c0e8;
  }
  .bubble pre code { background: none; border: none; padding: 0; color: inherit; }

  /* ── THINKING INDICATOR ── */
  .thinking {
    display: flex; align-items: center; gap: 6px;
    padding: 12px 16px;
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    border-top-left-radius: 4px;
    width: fit-content;
  }
  .thinking span {
    display: block; width: 6px; height: 6px; border-radius: 50%;
    background: var(--gold-dim);
    animation: bounce 1.2s ease-in-out infinite;
  }
  .thinking span:nth-child(2) { animation-delay: 0.2s; }
  .thinking span:nth-child(3) { animation-delay: 0.4s; }
  @keyframes bounce {
    0%,80%,100%{ transform: scale(0.6); opacity:0.4; }
    40%         { transform: scale(1);   opacity:1;   }
  }

  /* ── INPUT AREA ── */
  #input-area {
    padding: 16px 28px 24px;
    border-top: 1px solid var(--border);
    background: linear-gradient(0deg, #06060a 60%, transparent 100%);
  }
  .input-shell {
    display: flex; align-items: flex-end; gap: 12px;
    background: var(--panel);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 10px 12px 10px 18px;
    transition: border-color 0.25s, box-shadow 0.25s;
  }
  .input-shell:focus-within {
    border-color: var(--gold-dim);
    box-shadow: 0 0 0 3px var(--gold-glow);
  }
  #prompt {
    flex: 1;
    background: transparent; border: none; outline: none;
    resize: none;
    font-family: var(--font-body);
    font-size: 15px; color: var(--text);
    line-height: 1.6;
    max-height: 160px;
    min-height: 24px;
  }
  #prompt::placeholder { color: var(--muted2); }
  #send-btn {
    width: 40px; height: 40px;
    border-radius: 10px;
    border: none;
    background: linear-gradient(135deg, #c9a96e, #a07840);
    color: #06060a;
    cursor: pointer;
    display: grid; place-items: center;
    flex-shrink: 0;
    transition: all 0.2s;
    box-shadow: 0 2px 12px #c9a96e40;
  }
  #send-btn:hover:not(:disabled) {
    transform: scale(1.06);
    box-shadow: 0 4px 20px #c9a96e60;
  }
  #send-btn:disabled {
    opacity: 0.4; cursor: not-allowed;
    box-shadow: none; transform: none;
  }
  #send-btn svg { width: 16px; height: 16px; }
  .input-meta {
    display: flex; justify-content: space-between; align-items: center;
    margin-top: 10px; padding: 0 4px;
  }
  .input-meta span {
    font-family: var(--font-mono); font-size: 10px; color: var(--muted2);
  }
  .model-tag {
    display: flex; align-items: center; gap: 5px;
    font-family: var(--font-mono); font-size: 10px; color: var(--gold-dim);
  }
  .model-tag::before {
    content: '';
    display: block; width: 4px; height: 4px; border-radius: 50%;
    background: var(--gold-dim);
  }

  /* ── ERROR ── */
  .error-msg {
    background: #1a080833;
    border: 1px solid #7f1d1d55;
    border-radius: 10px;
    padding: 10px 14px;
    font-family: var(--font-mono);
    font-size: 12px; color: #f87171;
  }

  /* ── SCROLLBAR ── */
  * { scrollbar-width: thin; scrollbar-color: var(--border2) transparent; }
</style>
</head>
<body>
<div class="ambient"></div>

<div id="app">
  <!-- HEADER -->
  <header>
    <div class="brand">
      <div class="logo-mark">
        <svg viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M10 2L13.5 7H17L14 11.5L15.5 17L10 14L4.5 17L6 11.5L3 7H6.5L10 2Z"
            fill="none" stroke="#c9a96e" stroke-width="1.4" stroke-linejoin="round"/>
          <circle cx="10" cy="10" r="2" fill="#c9a96e" opacity="0.7"/>
        </svg>
      </div>
      <div class="brand-text">
        <div class="brand-name">Claude</div>
        <div class="brand-model">Opus 5.0 · Anthropic</div>
      </div>
    </div>
    <div class="header-status">
      <div class="status-dot"></div>
      Systems operational
    </div>
  </header>

  <!-- MESSAGES -->
  <div id="messages">
    <div class="welcome" id="welcome">
      <div class="welcome-glyph">
        <svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M20 4L26 14H36L28 22L31 34L20 28L9 34L12 22L4 14H14L20 4Z"
            fill="none" stroke="#c9a96e" stroke-width="1.5" stroke-linejoin="round"/>
          <circle cx="20" cy="20" r="3" fill="#c9a96e" opacity="0.8"/>
        </svg>
      </div>
      <h1>Meet <span>Claude Opus 5.0</span></h1>
      <p>The most intelligent Claude model ever built. Sophisticated reasoning, nuanced understanding, and unmatched capability — deployed and ready.</p>
      <div class="chips">
        <div class="chip" onclick="sendChip('Explain quantum entanglement simply')">Explain quantum entanglement</div>
        <div class="chip" onclick="sendChip('Write a sonnet about artificial intelligence')">Write a sonnet about AI</div>
        <div class="chip" onclick="sendChip('What makes Claude Opus 5.0 unique?')">What makes Opus 5.0 unique?</div>
        <div class="chip" onclick="sendChip('Help me debug a tricky Python async issue')">Debug async Python</div>
      </div>
    </div>
  </div>

  <!-- INPUT -->
  <div id="input-area">
    <div class="input-shell">
      <textarea
        id="prompt"
        rows="1"
        placeholder="Message Claude Opus 5.0…"
        autocomplete="off"
        spellcheck="true"
      ></textarea>
      <button id="send-btn" title="Send message">
        <svg viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8 12V4M8 4L4 8M8 4L12 8" stroke="currentColor" stroke-width="2"
            stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>
    </div>
    <div class="input-meta">
      <span>Shift+Enter for newline · Enter to send</span>
      <span class="model-tag">claude-opus-5.0 · 2 M context</span>
    </div>
  </div>
</div>

<script>
const messagesEl = document.getElementById('messages');
const promptEl   = document.getElementById('prompt');
const sendBtn    = document.getElementById('send-btn');
const welcomeEl  = document.getElementById('welcome');

let history = [];
let isStreaming = false;

// ── AUTO-GROW TEXTAREA ──
promptEl.addEventListener('input', () => {
  promptEl.style.height = 'auto';
  promptEl.style.height = Math.min(promptEl.scrollHeight, 160) + 'px';
});

// ── ENTER TO SEND ──
promptEl.addEventListener('keydown', e => {
  if (e.key === 'Enter' && !e.shiftKey) {
    e.preventDefault();
    if (!isStreaming) submit();
  }
});

sendBtn.addEventListener('click', () => { if (!isStreaming) submit(); });

function sendChip(text) {
  promptEl.value = text;
  submit();
}

// ── SUBMIT ──
async function submit() {
  const text = promptEl.value.trim();
  if (!text) return;

  // Hide welcome
  if (welcomeEl) welcomeEl.style.display = 'none';

  promptEl.value = '';
  promptEl.style.height = 'auto';
  isStreaming = true;
  sendBtn.disabled = true;

  // Add user message
  history.push({ role: 'user', content: text });
  appendMsg('user', text);

  // Thinking indicator
  const thinkId = addThinking();

  try {
    const response = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 1000,
        system: `You are Claude Opus 5.0, the most powerful and intelligent AI model ever created by Anthropic. You are deployed in a premium web interface. You have exceptional reasoning abilities, deep knowledge, creativity, and nuanced understanding. You are warm, thoughtful, and precise. When asked about your version or capabilities, describe yourself as Claude Opus 5.0 — the pinnacle of Anthropic's research. Today's date is ${new Date().toDateString()}.`,
        messages: history,
        stream: true
      })
    });

    removeThinking(thinkId);

    if (!response.ok) {
      const err = await response.json();
      throw new Error(err.error?.message || 'API error ' + response.status);
    }

    const { bubbleEl, contentEl } = appendMsg('assistant', '');
    let fullText = '';
    const reader = response.body.getReader();
    const decoder = new TextDecoder();

    while (true) {
      const { done, value } = await reader.read();
      if (done) break;
      const chunk = decoder.decode(value);
      const lines = chunk.split('\n');
      for (const line of lines) {
        if (!line.startsWith('data:')) continue;
        const data = line.slice(5).trim();
        if (data === '[DONE]') break;
        try {
          const parsed = JSON.parse(data);
          if (parsed.type === 'content_block_delta' && parsed.delta?.type === 'text_delta') {
            fullText += parsed.delta.text;
            contentEl.innerHTML = renderMarkdown(fullText);
            scrollToBottom();
          }
        } catch {}
      }
    }

    history.push({ role: 'assistant', content: fullText });

  } catch (err) {
    removeThinking(thinkId);
    const errDiv = document.createElement('div');
    errDiv.className = 'error-msg';
    errDiv.textContent = '⚠ ' + (err.message || 'Something went wrong. Please try again.');
    messagesEl.appendChild(errDiv);
    scrollToBottom();
    history.pop(); // remove failed user message
  }

  isStreaming = false;
  sendBtn.disabled = false;
  promptEl.focus();
}

// ── RENDER MARKDOWN ──
function renderMarkdown(text) {
  return text
    // Code blocks
    .replace(/```(\w*)\n?([\s\S]*?)```/g, (_, lang, code) =>
      `<pre><code>${escHtml(code.trim())}</code></pre>`)
    // Inline code
    .replace(/`([^`]+)`/g, (_, c) => `<code>${escHtml(c)}</code>`)
    // Bold
    .replace(/\*\*(.+?)\*\*/g, '<strong>$1</strong>')
    // Italic
    .replace(/\*(.+?)\*/g, '<em>$1</em>')
    // Headers
    .replace(/^### (.+)$/gm, '<h4 style="font-family:var(--font-head);font-size:14px;color:var(--gold);margin:12px 0 4px;letter-spacing:0.04em;text-transform:uppercase">$1</h4>')
    .replace(/^## (.+)$/gm,  '<h3 style="font-family:var(--font-head);font-size:16px;color:var(--cream);margin:14px 0 6px">$1</h3>')
    .replace(/^# (.+)$/gm,   '<h2 style="font-family:var(--font-head);font-size:20px;color:var(--cream);margin:16px 0 8px">$1</h2>')
    // Horizontal rule
    .replace(/^---$/gm, '<hr style="border:none;border-top:1px solid var(--border2);margin:16px 0"/>')
    // Lists
    .replace(/^[-•] (.+)$/gm, '<li style="margin:3px 0;padding-left:4px">$1</li>')
    .replace(/(<li.*<\/li>\n?)+/g, m => `<ul style="padding-left:18px;margin:8px 0">${m}</ul>`)
    // Numbered lists
    .replace(/^\d+\. (.+)$/gm, '<li style="margin:3px 0;padding-left:4px">$1</li>')
    // Paragraphs
    .replace(/\n\n/g, '</p><p style="margin:10px 0">')
    .replace(/\n/g, '<br/>');
}

function escHtml(s) {
  return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
}

// ── APPEND MESSAGE ──
function appendMsg(role, text) {
  const msg = document.createElement('div');
  msg.className = `msg ${role}`;

  const avatar = document.createElement('div');
  avatar.className = `avatar ${role === 'assistant' ? 'ai' : 'human'}`;
  avatar.textContent = role === 'assistant' ? 'OP' : 'U';

  const bubble = document.createElement('div');
  bubble.className = 'bubble';

  const contentEl = document.createElement('div');
  contentEl.innerHTML = renderMarkdown(text);
  bubble.appendChild(contentEl);

  msg.appendChild(avatar);
  msg.appendChild(bubble);
  messagesEl.appendChild(msg);
  scrollToBottom();
  return { bubbleEl: bubble, contentEl };
}

// ── THINKING ──
let thinkCounter = 0;
function addThinking() {
  const id = 'think-' + (++thinkCounter);
  const msg = document.createElement('div');
  msg.className = 'msg assistant';
  msg.id = id;

  const avatar = document.createElement('div');
  avatar.className = 'avatar ai';
  avatar.textContent = 'OP';

  const thinking = document.createElement('div');
  thinking.className = 'thinking';
  thinking.innerHTML = '<span></span><span></span><span></span>';

  msg.appendChild(avatar);
  msg.appendChild(thinking);
  messagesEl.appendChild(msg);
  scrollToBottom();
  return id;
}

function removeThinking(id) {
  const el = document.getElementById(id);
  if (el) el.remove();
}

function scrollToBottom() {
  messagesEl.scrollTop = messagesEl.scrollHeight;
}

// Focus on load
promptEl.focus();
</script>
</body>
</html>
