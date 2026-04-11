<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="theme-color" content="#08111f">
    <link rel="manifest" href="manifest.json">
    <link rel="apple-touch-icon" href="icons/icon-192.png">
    <title>Sovereign OS</title>
    <link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
        button, .check, .vault-card, .stat, .quest, .fx-icon { touch-action: manipulation; }
        body {
            background: #08111f;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            padding: 20px 16px calc(80px + env(safe-area-inset-bottom, 0px));
            font-family: "Rajdhani", sans-serif;
            font-size: 14px;
            line-height: 1.45;
            color: #fff;
            -webkit-text-size-adjust: 100%;
        }
        .sl { width: 100%; max-width: 400px; padding-left: env(safe-area-inset-left, 0px); padding-right: env(safe-area-inset-right, 0px); }
        .win { background: #0b1d3a; border: 1px solid #1e4a8a; border-radius: 3px; overflow: hidden; position: relative; margin-bottom: 16px; }
        .corn { position: absolute; width: 24px; height: 24px; opacity: 0.5; pointer-events: none; z-index: 1; }
        .corn svg { width: 100%; height: 100%; }
        .c-tl { top: 3px; left: 3px; }
        .c-tr { top: 3px; right: 3px; transform: scaleX(-1); }
        .c-bl { bottom: 3px; left: 3px; transform: scaleY(-1); }
        .c-br { bottom: 3px; right: 3px; transform: scale(-1,-1); }
        .hdr { text-align: center; padding: 14px 12px 10px; border-bottom: 1px solid #1a3d73; position: relative; }
        .hdr-title { font-size: 15px; font-weight: 700; letter-spacing: 4px; }
        .hdr-sub { font-size: 11px; color: #4a7fc1; letter-spacing: 3px; margin-top: 2px; }
        .fx-icons { position: absolute; top: 10px; right: 12px; display: flex; gap: 4px; align-items: center; flex-wrap: wrap; justify-content: flex-end; max-width: 50%; }
        .fx-icon { width: 22px; height: 22px; border-radius: 3px; display: flex; align-items: center; justify-content: center; font-size: 11px; border: 1px solid; position: relative; cursor: pointer; transition: all 0.15s; flex-shrink: 0; }
        .fx-icon:hover { transform: scale(1.1); }
        .fx-icon-empty { opacity: 0.15; pointer-events: none; }
        /* Condition tooltip */
        .fx-tooltip { position: fixed; background: #0b1d3a; border: 1px solid #1e4a8a; padding: 6px 10px; font-size: 10px; font-weight: 700; letter-spacing: 1px; color: #e0eaf5; z-index: 5000; pointer-events: none; white-space: nowrap; border-radius: 3px; display: none; }
        .fx-tooltip.visible { display: block; }
        .fx-tooltip-sub { font-size: 9px; font-weight: 400; color: #5a8fc1; margin-top: 2px; letter-spacing: 0.5px; }
        /* Buff application flair */
        @keyframes buffFlash { 0%{opacity:0;transform:translateY(-8px) scale(0.9)} 20%{opacity:1;transform:translateY(0) scale(1.02)} 80%{opacity:1;transform:translateY(0) scale(1)} 100%{opacity:0;transform:translateY(-4px)} }
        .buff-flair { position: fixed; top: 50px; right: 12px; display: flex; align-items: center; gap: 8px; padding: 8px 12px; border: 1px solid; border-radius: 3px; z-index: 3000; pointer-events: none; animation: buffFlash 2.2s ease forwards; }
        .buff-flair-icon { font-size: 14px; font-weight: 700; }
        .buff-flair-text { display: flex; flex-direction: column; }
        .buff-flair-name { font-size: 11px; font-weight: 700; letter-spacing: 1px; }
        .buff-flair-sub  { font-size: 9px; letter-spacing: 1px; margin-top: 1px; opacity: 0.7; }
        .bod { padding: 16px 16px 12px; }
        .rank-center { display: flex; flex-direction: column; align-items: center; margin-bottom: 14px; }
        .rank-ring-wrap { position: relative; width: 100px; height: 100px; margin-bottom: 6px; }
        .rank-ring-wrap canvas { position: absolute; top: 0; left: 0; }
        .rank-inner { position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); text-align: center; pointer-events: none; }
        .rank-letter { font-size: 36px; font-weight: 700; color: #e87a4d; line-height: 1; }
        .rank-plus { font-size: 18px; font-weight: 700; color: #e87a4d; }
        .rank-label { font-size: 11px; color: #4a7fc1; letter-spacing: 2px; margin-top: 2px; }
        .div { display: flex; align-items: center; gap: 6px; margin: 10px 0 14px; }
        .dl { flex: 1; height: 1px; background: #1a3d73; }
        .dd { width: 5px; height: 5px; background: #3a6fa1; transform: rotate(45deg); flex-shrink: 0; }
        .sec { font-size: 11px; font-weight: 700; color: #4de894; letter-spacing: 3px; margin-bottom: 8px; margin-top: 4px; }
        .muted { color: #5a8fc1; font-size: 13px; letter-spacing: 0.5px; }
        .hidden { display: none !important; }
        .label { font-size: 12px; font-weight: 600; color: #5a8fc1; margin-bottom: 6px; letter-spacing: 0.5px; }
        .progress { height: 8px; background: #0a1628; border: 1px solid #1a3d73; border-radius: 2px; overflow: hidden; margin-bottom: 4px; }
        .progress > div { height: 100%; background: #f0c040; transition: width 0.35s ease; }
        .stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
        .stat { background: #0a1628; border: 1px solid #1a3d73; border-radius: 3px; padding: 8px 10px; font-size: 13px; transition: border-color 0.15s; }
        .stat:hover { border-color: #4a7fc1; }
        .stat.stat-clickable { cursor: pointer; }
        .stat.stat-clickable:active { transform: scale(0.98); }
        .stat strong { font-weight: 700; letter-spacing: 1px; color: #7ab0e8; font-size: 12px; }
        .stat-detail-toolbar { margin: -4px 0 14px; }
        .stat-back-btn { font-size: 12px; letter-spacing: 2px; padding: 8px 14px; margin: 0; min-height: 40px; }
        .stat-detail-title { font-size: 18px; font-weight: 700; letter-spacing: 4px; color: #e0eaf5; margin-bottom: 6px; }
        .stat-detail-sub { font-size: 11px; color: #5a8fc1; letter-spacing: 2px; margin-bottom: 14px; }
        .stat-detail-xp { font-size: 28px; font-weight: 700; color: #f0c040; letter-spacing: 1px; margin-bottom: 8px; }
        .stat-detail-meta { font-size: 12px; color: #7ab0e8; margin-bottom: 16px; }
        .stat-detail-blurb { font-size: 12px; line-height: 1.5; color: #a8c4e8; border-left: 2px solid #1e4a8a; padding-left: 10px; }
        .stat.atrophied { border-color: #e87a4d; box-shadow: 0 0 10px rgba(232, 122, 77, 0.12); }
        .stat.atrophied strong { color: #e87a4d; }
        .notice { background: rgba(232,77,77,0.08); border: 1px solid rgba(232,77,77,0.35); padding: 8px 10px; margin-top: 12px; border-radius: 3px; font-size: 11px; color: #e8a0a0; letter-spacing: 0.3px; }
        .notice strong { display: block; font-size: 10px; font-weight: 700; color: #e84d4d; letter-spacing: 2px; margin-bottom: 4px; }
        #ui-quest-board h2 { font-size: 11px; font-weight: 700; color: #4de894; letter-spacing: 3px; margin: 16px 0 8px; display: flex; align-items: center; justify-content: space-between; }
        #ui-quest-board h2:first-child { margin-top: 0; }
        .board-timer { font-family: "Share Tech Mono", monospace; font-size: 11px; font-weight: 400; color: #4a7fc1; letter-spacing: 1px; }
        .quest { background: #0a1628; border: 1px solid #1a3d73; border-radius: 3px; padding: 10px; margin-bottom: 8px; display: flex; flex-wrap: wrap; align-items: flex-start; gap: 8px; transition: opacity 0.6s ease, border-color 0.4s ease; }
        .quest.aura-medium { border-color: rgba(240,192,64,0.45); box-shadow: 0 0 8px rgba(240,192,64,0.12); }
        .quest.aura-high { border-color: rgba(232,77,77,0.45); box-shadow: 0 0 8px rgba(232,77,77,0.12); }
        .quest.completing { border-color: rgba(77,232,148,0.6); }
        .quest.done { opacity: 0.38; pointer-events: none; border-color: rgba(77,232,148,0.2); }
        @keyframes checkPop { 0%{transform:scale(1)} 40%{transform:scale(1.4)} 70%{transform:scale(0.9)} 100%{transform:scale(1)} }
        .check.popping { animation: checkPop 0.35s ease forwards; }
        .quest-body { flex: 1; min-width: 0; }
        .quest-title { font-weight: 700; font-size: 14px; letter-spacing: 0.5px; }
        .quest-desc { font-size: 11px; color: #5a8fc1; margin-top: 2px; }
        .tag { font-size: 11px; font-weight: 600; padding: 2px 6px; border: 1px solid #1e4a8a; color: #4a7fc1; letter-spacing: 1px; }
        button { font-family: "Rajdhani", sans-serif; font-size: 11px; font-weight: 700; letter-spacing: 1px; cursor: pointer; padding: 5px 10px; border-radius: 2px; background: rgba(77,221,232,0.08); border: 1px solid #1a3d73; color: #4a7fc1; transition: all 0.15s; }
        button:hover { border-color: #4ddde8; color: #4ddde8; }
        .check { width: 20px; height: 20px; border: 1px solid #3a6fa1; border-radius: 2px; display: inline-flex; align-items: center; justify-content: center; flex-shrink: 0; cursor: pointer; font-size: 12px; color: #4de894; }
        .check:hover { border-color: #4de894; }
        .check.on { background: rgba(77,232,148,0.15); border-color: #4de894; }
        nav.nav { position: fixed; bottom: 0; left: 0; right: 0; background: #071530; border-top: 1px solid #1a3d73; padding: 8px 10px; padding-bottom: calc(8px + env(safe-area-inset-bottom, 0px)); display: flex; justify-content: space-between; gap: 4px; flex-wrap: nowrap; z-index: 100; }
        nav.nav button { flex: 1; min-width: 0; font-size: 11px; font-weight: 700; letter-spacing: 1px; padding: 8px 4px; min-height: 44px; }
        nav.nav button.current { border-color: #4ddde8; color: #4ddde8; }
        .modal-backdrop { position: fixed; inset: 0; background: rgba(0,0,0,0.82); display: none; align-items: center; justify-content: center; z-index: 3000; padding: 16px; }
        .modal-backdrop.open { display: flex; }
        .modal-box { background: #0b1d3a; border: 1px solid #e84d4d; border-radius: 3px; padding: 20px; max-width: 22rem; box-shadow: 0 0 24px rgba(232, 77, 77, 0.15); }
        .modal-box strong { color: #e84d4d; font-size: 11px; letter-spacing: 3px; }
        .modal-box #ui-modal-text { margin-top: 10px; font-size: 14px; line-height: 1.5; color: #e0eaf5; }
        .modal-actions { display: flex; gap: 10px; margin-top: 18px; }
        .modal-actions button { flex: 1; }
        #btn-accept { color: #4de894; border-color: rgba(77,232,148,0.5); }
        #btn-accept:hover { background: rgba(77,232,148,0.1); }
        #btn-decline { color: #e84d4d; border-color: rgba(232,77,77,0.45); }
        #btn-decline:hover { background: rgba(232,77,77,0.1); }
        .toast { position: fixed; left: 50%; bottom: 24px; transform: translateX(-50%); max-width: 90vw; padding: 12px 18px; background: #0b1d3a; border: 1px solid #1e4a8a; font-size: 13px; display: none; z-index: 2500; border-radius: 3px; color: #e0eaf5; }
        .toast.open { display: block; }
        .full-overlay { position: fixed; inset: 0; background: rgba(5,8,15,0.96); color: #fff; display: none; flex-direction: column; align-items: center; justify-content: center; z-index: 4000; text-align: center; padding: 16px; }
        .full-overlay.open { display: flex; }
        .full-overlay .muted { color: #4a9fe8; letter-spacing: 4px; font-size: 11px; }
        #cinematic-reward { font-size: 1.25rem; font-weight: 700; letter-spacing: 3px; color: #f0c040; text-shadow: 0 0 20px rgba(240,192,64,0.35); margin-top: 8px; transition: all 0.3s ease; }
        @keyframes rankPulse { 0%{opacity:0;transform:scale(0.6)} 50%{opacity:1;transform:scale(1.08)} 100%{transform:scale(1)} }
        .full-overlay.open #cinematic-reward { animation: rankPulse 0.5s ease forwards; }
        .dev-fab { position: fixed; top: 12px; right: 12px; z-index: 3500; font-size: 10px; font-weight: 700; letter-spacing: 2px; padding: 6px 10px; background: #0b1d3a; border: 1px solid #1e4a8a; color: #4a7fc1; }
        .dev-fab:hover { border-color: #e84d4d; color: #e84d4d; }
        .dev-panel { position: fixed; top: 0; right: 0; width: min(100%, 24rem); height: 100%; background: #08111f; border-left: 1px solid #1e4a8a; overflow: auto; padding: 14px; display: none; z-index: 3500; font-size: 12px; color: #e0eaf5; }
        .dev-panel.open { display: block; }
        .dev-panel h2 { font-size: 10px; font-weight: 700; color: #4ddde8; letter-spacing: 2px; margin: 16px 0 6px; border-bottom: 1px solid #1a3d73; padding-bottom: 4px; }
        .dev-panel h2:first-of-type { margin-top: 0; }
        .dev-panel-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; }
        .dev-panel-header strong { letter-spacing: 2px; color: #e84d4d; font-size: 12px; }
        .dev-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; margin-bottom: 8px; }
        .dev-grid button { font-size: 9px; padding: 8px 4px; }
        .dev-danger { border-color: rgba(232,77,77,0.55) !important; color: #e84d4d !important; }
        .dev-danger:hover { background: rgba(232,77,77,0.1) !important; }
        .dev-panel table { width: 100%; border-collapse: collapse; font-size: 10px; margin-bottom: 8px; color: #5a8fc1; }
        .dev-panel th, .dev-panel td { border: 1px solid #1a3d73; padding: 4px 6px; text-align: left; }
        .dev-panel th { background: #0a1628; color: #4a9fe8; font-weight: 600; }
        .color-swatch { display: inline-block; width: 8px; height: 8px; margin-right: 4px; vertical-align: middle; }
        /* Body skill tree — horizontal scroll */
        .body-tree-scroll { display: flex; gap: 0; overflow-x: auto; margin-top: 8px; padding-bottom: 8px; -webkit-overflow-scrolling: touch; scrollbar-width: none; }
        .body-tree-scroll::-webkit-scrollbar { display: none; }
        .body-tree-branch { flex: 0 0 140px; padding: 0 8px; border-right: 1px solid #1a3d73; }
        .body-tree-branch:last-child { border-right: none; }
        .body-tree-branch-title { font-size: 11px; font-weight: 700; letter-spacing: 2px; color: #4a7fc1; text-align: center; margin-bottom: 8px; padding-bottom: 6px; border-bottom: 1px solid #1a3d73; }
        .body-node { border: 1px solid #1a3d73; border-radius: 3px; padding: 8px; text-align: center; font-size: 11px; font-weight: 600; letter-spacing: 0.5px; margin-bottom: 4px; }
        .body-node-unlocked { background: rgba(77,232,148,0.08); border-color: rgba(77,232,148,0.35); color: #b8f0d0; }
        .body-node-locked { opacity: 0.35; color: #4a7fc1; }
        .body-gate { font-size: 11px; padding: 4px 0 8px; text-align: center; border-left: 1px dashed #1e4a8a; margin-left: 50%; padding-left: 6px; margin-bottom: 2px; }
        .body-gate-done { border-left-color: rgba(77,232,148,0.4); }
        .body-gate-ok { color: #4de894; font-size: 11px; letter-spacing: 1px; }
        .body-gate-btn { font-size: 11px; padding: 6px 10px; margin-top: 4px; min-height: 36px; }
        .body-placement { margin-top: 14px; padding: 10px 12px; border: 1px solid #1e4a8a; border-radius: 3px; text-align: center; font-size: 11px; font-weight: 700; letter-spacing: 2px; }
        .body-gate-req { font-size: 9px; color: #5a8fc1; line-height: 1.35; margin-top: 4px; text-align: left; }
        .body-gate-req .met { color: #4de894; }
        .body-gate-req .unmet { color: #e87a4d; }
        .btn-fail-gate { font-size: 11px; padding: 6px 10px; margin-top: 6px; border-color: rgba(232, 122, 77, 0.55); color: #e87a4d; }
        .btn-fail-gate:hover { background: rgba(232, 122, 77, 0.12); }
        .quest-stat-hint { font-size: 11px; color: #4a7fc1; margin-top: 2px; letter-spacing: 1px; }

        /* Vault */
        .vault-tabs { display: flex; gap: 4px; margin-bottom: 12px; flex-wrap: wrap; }
        .vault-tab { flex: 1; min-width: 0; font-size: 11px; font-weight: 700; letter-spacing: 1px; padding: 8px 4px; background: transparent; border: 1px solid #1a3d73; color: #4a7fc1; cursor: pointer; transition: all 0.15s; font-family: "Rajdhani", sans-serif; min-height: 40px; }
        .vault-tab.active { border-color: #4ddde8; color: #4ddde8; }
        .vault-tab:hover:not(.active) { border-color: #4a7fc1; }
        .vault-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; }
        .vault-card { background: #0a1628; border: 1px solid #1a3d73; border-radius: 3px; padding: 10px 8px; cursor: pointer; transition: border-color 0.15s; display: flex; flex-direction: column; align-items: center; gap: 6px; text-align: center; }
        .vault-card:hover { border-color: #4a7fc1; }
        .vault-card-rarity { font-size: 10px; font-weight: 700; letter-spacing: 1px; padding: 2px 6px; border: 1px solid; border-radius: 1px; }
        .vault-card-name { font-size: 11px; font-weight: 700; color: #e0eaf5; letter-spacing: 0.3px; line-height: 1.3; }
        .vault-card-qty { font-size: 12px; color: #4a7fc1; letter-spacing: 1px; }

        /* Item descriptor modal */
        .sheet-bg { position: fixed; inset: 0; background: rgba(0,0,0,0); pointer-events: none; z-index: 2000; transition: background 0.2s; display: flex; align-items: center; justify-content: center; padding: 20px; }
        .sheet-bg.open { background: rgba(0,0,0,0.72); pointer-events: all; }
        .sheet { background: #0b1d3a; border: 1px solid #1e4a8a; border-radius: 3px; padding: 20px; z-index: 2100; width: 100%; max-width: 340px; position: relative; opacity: 0; transform: scale(0.95); transition: opacity 0.2s ease, transform 0.2s ease; pointer-events: none; }
        .sheet-bg.open .sheet { opacity: 1; transform: scale(1); pointer-events: all; }
        .sheet-close { position: absolute; top: 10px; right: 10px; width: 24px; height: 24px; display: flex; align-items: center; justify-content: center; cursor: pointer; color: #4a7fc1; font-size: 16px; border: 1px solid #1a3d73; border-radius: 2px; transition: all 0.15s; line-height: 1; }
        .sheet-close:hover { border-color: #4ddde8; color: #4ddde8; }
        .sheet-handle { display: none; }
        .sheet-rarity-tag { font-size: 9px; font-weight: 700; letter-spacing: 2px; padding: 2px 8px; border: 1px solid; display: inline-block; margin-bottom: 10px; }
        .sheet-name { font-size: 20px; font-weight: 700; letter-spacing: 2px; color: #e0eaf5; margin-bottom: 4px; padding-right: 28px; }
        .sheet-archetype { font-size: 10px; color: #4a7fc1; letter-spacing: 2px; margin-bottom: 14px; }
        .sheet-desc { font-size: 13px; color: #a8c4e8; line-height: 1.6; border-left: 2px solid #1e4a8a; padding-left: 10px; }
        .sheet-qty { font-size: 11px; color: #4a7fc1; margin-top: 14px; letter-spacing: 1px; }
        .btn-use { font-family: "Rajdhani", sans-serif; font-size: 13px; font-weight: 700; letter-spacing: 3px; padding: 8px 32px; background: transparent; border: 1px solid #4de894; color: #4de894; cursor: pointer; transition: all 0.15s; border-radius: 2px; }
        .btn-use:hover { background: rgba(77,232,148,0.1); }
        .btn-use:disabled { border-color: #1a3d73; color: #2a4d7a; cursor: default; }
    </style>
</head>
<body>

<div class="sl">
<div class="win">
  <div class="corn c-tl"><svg viewBox="0 0 24 24" fill="none"><path d="M2 22L2 6Q2 2 6 2L22 2" stroke="#4a7fc1" stroke-width="1.5"/><circle cx="5" cy="5" r="1.5" fill="#4a7fc1"/></svg></div>
  <div class="corn c-tr"><svg viewBox="0 0 24 24" fill="none"><path d="M2 22L2 6Q2 2 6 2L22 2" stroke="#4a7fc1" stroke-width="1.5"/><circle cx="5" cy="5" r="1.5" fill="#4a7fc1"/></svg></div>
  <div class="corn c-bl"><svg viewBox="0 0 24 24" fill="none"><path d="M2 22L2 6Q2 2 6 2L22 2" stroke="#4a7fc1" stroke-width="1.5"/><circle cx="5" cy="5" r="1.5" fill="#4a7fc1"/></svg></div>
  <div class="corn c-br"><svg viewBox="0 0 24 24" fill="none"><path d="M2 22L2 6Q2 2 6 2L22 2" stroke="#4a7fc1" stroke-width="1.5"/><circle cx="5" cy="5" r="1.5" fill="#4a7fc1"/></svg></div>

  <div class="hdr">
    <p class="hdr-title">SOVEREIGN OS</p>
    <p class="hdr-sub">SYSTEM INTERFACE · V.1</p>
    <div class="fx-icons" id="fx-icons-row"></div>
    <div class="fx-tooltip" id="fx-tooltip">
        <div id="fx-tooltip-name"></div>
        <div class="fx-tooltip-sub" id="fx-tooltip-sub"></div>
    </div>
  </div>

  <div class="bod">
    <div id="tab-status" class="tab-pane">
      <div id="status-overview">
        <div class="rank-center">
          <div class="rank-ring-wrap">
            <canvas id="rankRing" width="100" height="100"></canvas>
            <div class="rank-inner">
              <div><span class="rank-letter">D</span><span class="rank-plus">+</span></div>
              <div class="rank-label">OVERALL</div>
            </div>
          </div>
        </div>
        <div class="div"><div class="dl"></div><div class="dd"></div><div class="dl"></div></div>
        <p class="label">OVERALL PROGRESS (WITHIN LEVEL)</p>
        <div class="progress"><div id="ui-xp-bar" style="width:0%"></div></div>
        <p class="sec">STATS</p>
        <div class="stat-grid" id="ui-stat-grid"></div>
        <div id="ui-stat-miss" class="notice hidden">
          <strong>OPPORTUNITY MISSED</strong>Critical deadline passed.
        </div>
      </div>
      <div id="status-stat-detail" class="hidden">
        <div class="stat-detail-toolbar">
          <button type="button" class="stat-back-btn" onclick="closeStatDetail()">← STATUS</button>
        </div>
        <div id="status-stat-detail-inner"></div>
      </div>
    </div>

    <div id="tab-quests" class="tab-pane hidden">
      <p class="sec">MISSION LOG</p>
      <p class="muted" style="margin-bottom:10px;">ACTIVE DIRECTIVES</p>
      <div id="ui-quest-board"></div>
    </div>

    <div id="tab-skills" class="tab-pane hidden"><p class="sec">SKILL ATLAS</p><p class="muted">LOCKED · PHASE 2</p></div>
    <div id="tab-inventory" class="tab-pane hidden">
        <div class="vault-tabs" id="vault-tabs">
            <button class="vault-tab active" data-archetype="charms">CHARMS</button>
            <button class="vault-tab" data-archetype="keys">KEYS</button>
            <button class="vault-tab" data-archetype="artifacts">ARTIFACTS</button>
            <button class="vault-tab" data-archetype="fragments">FRAGMENTS</button>
            <button class="vault-tab" data-archetype="titles">TITLES</button>
        </div>
        <div id="vault-grid"></div>
    </div>

    <!-- Item descriptor modal -->
    <div id="vault-sheet-bg" class="sheet-bg" onclick="closeItemSheet()">
        <div id="vault-sheet" class="sheet" onclick="event.stopPropagation()">
            <div class="sheet-handle"></div>
            <div id="vault-sheet-inner"></div>
        </div>
    </div>
    <div id="tab-world" class="tab-pane hidden"><p class="sec">WORLD MAP</p><p class="muted">LOCKED · PHASE 2</p></div>
  </div>

</div>
</div>

<nav class="nav">
    <button type="button" class="current" data-tab="status">STATUS</button>
    <button type="button" data-tab="quests">QUESTS</button>
    <button type="button" data-tab="skills">SKILLS</button>
    <button type="button" data-tab="inventory">VAULT</button>
    <button type="button" data-tab="world">MAP</button>
</nav>

<button type="button" class="dev-fab" onclick="toggleDebug()">DEV</button>

<div id="debug-drawer" class="dev-panel">
  <div class="dev-panel-header">
    <strong>// DEVELOPER</strong>
    <button type="button" onclick="toggleDebug()">CLOSE</button>
  </div>
  <div class="dev-grid">
    <button type="button" onclick="debugResetDay()">Reset day</button>
    <button type="button" onclick="debugForceAtrophy()">Force decay</button>
    <button type="button" onclick="debugAddXp()">+100 XP</button>
    <button type="button" onclick="debugCompleteAll()">Complete all</button>
    <button type="button" onclick="debugTriggerSysQuest()">Trigger sys quest</button>
    <button type="button" onclick="debugSimulateMiss()">Sim miss</button>
    <button type="button" onclick="debugGrantItems()">Grant items</button>
        <button type="button" class="dev-danger" style="grid-column:span 2" onclick="debugNukeSave()">Nuke save</button>
  </div>
  <div id="debug-quests-table"></div>
  <div id="debug-loot-table"></div>
  <div id="debug-cond-table"></div>
</div>

<div id="ui-modal" class="modal-backdrop">
  <div class="modal-box">
    <strong id="ui-modal-heading">Anomaly</strong>
    <p id="ui-modal-text"></p>
    <div class="modal-actions">
      <button type="button" id="btn-accept">Accept</button>
      <button type="button" id="btn-decline">Decline</button>
    </div>
  </div>
</div>

<div id="ui-toast" class="toast">
  <span id="toast-type"></span>: <span id="toast-name"></span>
</div>

<div id="ui-cinematic" class="full-overlay">
  <p class="muted">OBJECTIVE COMPLETE</p>
  <p id="cinematic-reward">Reward</p>
</div>

<script>
/* ============================================================
   DATA
   ============================================================ */

function makeBodyGateQuest(id, name, modalBody, subStat) {
    return {
        id, name,
        desc: "Complete the directive on the mission log to advance.",
        modalHeading: "System Directive",
        modalBody,
        type: "system",
        // FIX B2: gate quests tag stat as "BODY" so generateBoard routing works
        stat: "BODY",
        bodySub: subStat,   // actual sub-stat that receives XP
        stat2: null,
        difficulty: "HIGH",
        rarity: "RARE",
        skill: null,
        statLinked: true
    };
}

const BODY_SKILL_ROMAN = ["I","II","III","IV","V","VI"];
const BODY_SUB_KEYS    = ["STR","AGIL","END"];
const BRANCH_TO_SUB    = { strength:"STR", agility:"AGIL", endurance:"END" };
const STAT_ORDER       = ["BODY","MIND","POSITION","CONNECTIONS"];

const BODY_TEST_MISSION_XP = [100, 200, 300, 400, 500];
const BODY_TEST_HIDDEN_XP  = [100, 200, 300, 400, 500];

const SYS_QUESTS = [
    {
        id: "sys_01",
        name: "The First Step",
        desc: "Email a professor regarding research",
        modalHeading: "System directive",
        modalBody: "A priority directive is queued. Accept to deploy it to your mission log, or decline to postpone.",
        type: "system",
        stat: "POSITION",
        stat2: null,
        difficulty: "HIGH",
        rarity: "RARE",
        skill: null,
        statLinked: true
    }
];

// Generate 15 body gate quests (5 tiers × 3 branches)
const branchMeta = [
    { prefix:"strength", subStat:"STR",  questBase:"sys_STR_TEST" },
    { prefix:"agility",  subStat:"AGIL", questBase:"sys_AGI_TEST" },
    { prefix:"endurance",subStat:"END",  questBase:"sys_END_TEST" }
];
for (const b of branchMeta) {
    for (let t = 1; t <= 5; t++) {
        SYS_QUESTS.push(makeBodyGateQuest(
            `${b.questBase}${t}`,
            `${b.prefix.charAt(0).toUpperCase()+b.prefix.slice(1)} Test ${BODY_SKILL_ROMAN[t-1]}`,
            `Your ${b.prefix} has developed. Accept to prove yourself.`,
            b.subStat
        ));
    }
}

// FIX B2: cal_body now uses stat:"BODY" to match generateBoard atrophy lookup
const DB_QUESTS = [
    { id:"cal_body",      name:"System Calibration", desc:"Walk for 10 mins to clear decay",     type:"calibration", stat:"BODY",        stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"cal_mind",      name:"System Calibration", desc:"Read 1 page to clear decay",          type:"calibration", stat:"MIND",        stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"cal_conn",      name:"System Calibration", desc:"Text one entity to clear decay",      type:"calibration", stat:"CONNECTIONS", stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"cal_pos",       name:"System Calibration", desc:"Update resume for 5 mins",            type:"calibration", stat:"POSITION",    stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"d_body_1",      name:"The Warrior",        desc:"Complete 50 pushups",                 type:"daily",       stat:"STR",         stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"d_body_2",      name:"The Runner",         desc:"Run 2.5km without stopping",          type:"daily",       stat:"END",         stat2:null,   difficulty:"HIGH",   rarity:"UNCOMMON", skill:null,     prerequisite:null },
    { id:"d_body_3",      name:"The Mover",          desc:"Do 20 min agility drills",            type:"daily",       stat:"AGIL",        stat2:null,   difficulty:"MEDIUM", rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"d_mind_1",      name:"The Scribe",         desc:"Journal for 10 minutes",              type:"daily",       stat:"MIND",        stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"d_mind_2",      name:"The Scholar",        desc:"Study Mandarin for 15 mins",          type:"daily",       stat:"MIND",        stat2:null,   difficulty:"MEDIUM", rarity:"UNCOMMON", skill:"mandarin", prerequisite:null },
    { id:"d_conn_1",      name:"The Ping",           desc:"Text 2 friends to check in",         type:"daily",       stat:"CONNECTIONS", stat2:null,   difficulty:"LOW",    rarity:"COMMON",   skill:null,     prerequisite:null },
    { id:"d_conn_2",      name:"The Diplomat",       desc:"Start a conversation with a stranger",type:"daily",       stat:"CONNECTIONS", stat2:null,   difficulty:"HIGH",   rarity:"RARE",     skill:null,     prerequisite:null },
    { id:"d_pos_1",       name:"The Builder",        desc:"Write code for 45 mins",              type:"daily",       stat:"POSITION",    stat2:null,   difficulty:"HIGH",   rarity:"UNCOMMON", skill:"python",  prerequisite:null },
    { id:"d_pos_2",       name:"The Applicant",      desc:"Work on portfolio for 20 mins",       type:"daily",       stat:"POSITION",    stat2:null,   difficulty:"MEDIUM", rarity:"RARE",     skill:null,     prerequisite:null },
    { id:"d_compound_1",  name:"The Musician",       desc:"Practice trombone for 20 mins",       type:"daily",       stat:"AGIL",        stat2:"MIND", difficulty:"MEDIUM", rarity:"UNCOMMON", skill:"trombone", prerequisite:null },
    { id:"w_body_1",      name:"The Grinder",        desc:"Go to the gym 3 times",               type:"weekly",      stat:"STR",         stat2:null,   difficulty:"HIGH",   rarity:"RARE",     skill:null,     prerequisite:null },
    { id:"w_conn_1",      name:"The Anchor",         desc:"Call an old friend",                  type:"weekly",      stat:"CONNECTIONS", stat2:null,   difficulty:"MEDIUM", rarity:"UNCOMMON", skill:null,     prerequisite:null },
    { id:"w_pos_1",       name:"The Architect",      desc:"Ship one feature/fix",                type:"weekly",      stat:"POSITION",    stat2:null,   difficulty:"HIGH",   rarity:"RARE",     skill:null,     prerequisite:null }
];

// Item directory — all loot definitions. inventory stores { id, qty } refs to this.
const DB_ITEMS = {
    scrap_components:  { id:"scrap_components",  name:"Scrap Components",  archetype:"fragments", rarity:"COMMON",    chroma:"#6a7080", desc:"Residual material recovered from completed directives. No known use yet." },
    caffeine_surge:    { id:"caffeine_surge",     name:"Caffeine Surge",    archetype:"charms",    rarity:"UNCOMMON",  chroma:"#4de894", conditionId:"COND_PRIMED_MND", desc:"Temporarily applies [PRIMED] to Mind for 2 hours. Increases processing speed." },
    study_room_pass:   { id:"study_room_pass",    name:"Study Room Pass",   archetype:"keys",      rarity:"UNCOMMON",  chroma:"#4de894", desc:"Unlocks a high-focus study zone on the local map. Single use." },
    shield_fragment:   { id:"shield_fragment",    name:"Shield Fragment",   archetype:"artifacts", rarity:"RARE",      chroma:"#4a9fe8", desc:"A shard of something larger. Reduces POSITION atrophy decay rate by 10% permanently." },
    lab_access:        { id:"lab_access",         name:"Lab Access",        archetype:"keys",      rarity:"RARE",      chroma:"#4a9fe8", desc:"Grants access to a restricted research node. Single use." },
    refined_core:      { id:"refined_core",       name:"Refined Core",      archetype:"artifacts", rarity:"ELITE",     chroma:"#b44de8", desc:"A dense processing unit. Increases XP gain from MIND quests by 15% permanently." },
    sovereign_seal:    { id:"sovereign_seal",     name:"Sovereign Seal",    archetype:"keys",      rarity:"LEGENDARY", chroma:"#f0c040", desc:"A mark of exceptional output. Unlocks a hidden node on the world map." },
};

// Map rarity tables to item ids
const DB_LOOT = {
    COMMON:    ["scrap_components"],
    UNCOMMON:  ["caffeine_surge", "study_room_pass"],
    RARE:      ["shield_fragment", "lab_access"],
    ELITE:     ["refined_core"],
    LEGENDARY: ["sovereign_seal"]
};

const DB_CONDITIONS = [
    { id:"COND_PRIMED_MND", name:"Deep Focus",       type:"Buff",   expireOn:"TIMED",         durationMs: 2*3600*1000, mechanic:"MODIFY_WEIGHT: POSITION_EXEC +20%",  chroma:"#4de894", desc:"Mind processing weight increased. Position execution quests appear more frequently." },
    { id:"COND_PRIMED_BOD", name:"Neurogenesis",     type:"Buff",   expireOn:"TIMED",         durationMs: 4*3600*1000, mechanic:"MODIFY_WEIGHT: MIND_PROC +20%",      chroma:"#4de894", desc:"Post-exercise neural priming active. Mind processing quests boosted." },
    { id:"COND_LOAD_HIGH",  name:"Cognitive Load",   type:"Debuff", expireOn:"DAILY",         durationMs: null,        mechanic:"BLOCK_QUEST: FRICTION_HIGH",         chroma:"#e84d4d", desc:"Mental bandwidth depleted. High-friction quests temporarily unavailable." },
    { id:"COND_SOC_DRAIN",  name:"Social Battery",   type:"Debuff", expireOn:"TIMED",         durationMs:12*3600*1000, mechanic:"BLOCK_QUEST: STAT_CONNECTIONS",      chroma:"#e84d4d", desc:"Social reserves depleted. Connection quests unavailable until recharged." },
    { id:"COND_ATROPHY_BOD",name:"Physical Rust",    type:"Debuff", expireOn:"UNTIL_CLEARED", durationMs: null,        mechanic:"BLOCK_QUEST: BODY_TIER_2+",          chroma:"#e87a4d", clearedBy:"calibration_BODY", desc:"Physical systems degraded. Complete a calibration directive to restore." },
    { id:"COND_ATROPHY_MND",name:"Mind Rust",        type:"Debuff", expireOn:"UNTIL_CLEARED", durationMs: null,        mechanic:"BLOCK_QUEST: MIND_TIER_2+",          chroma:"#e87a4d", clearedBy:"calibration_MIND", desc:"Cognitive systems degraded. Complete a calibration directive to restore." },
    { id:"COND_FLOW",       name:"Flow State",       type:"Buff",   expireOn:"TIMED",         durationMs: 2*3600*1000, mechanic:"MULTIPLIER: ALL_XP x2.0",            chroma:"#f0c040", desc:"Optimal performance window. All XP gains doubled." },
    { id:"COND_OVERDRIVE",  name:"Surplus Protocol", type:"Buff",   expireOn:"DAILY",         durationMs: null,        mechanic:"MODIFY_BOARD_LIMIT: DAILY_SLOTS +3", chroma:"#f0c040", desc:"Exceptional output detected. Daily directive slots expanded." }
];

const STAT_DETAIL_BLURB = {
    BODY:        "Physical development splits into STR, AGIL, and END. Missions tagged with those keys grant visible XP and the same amount to a hidden branch pool used to unlock [[Tests]].",
    MIND:        "Focus, learning, and mental load. Reading, journaling, and study map to this stat.",
    POSITION:    "Career, craft, and outward momentum. Projects, portfolio work, and applications reinforce POSITION.",
    CONNECTIONS: "Relationships and social bandwidth. Check-ins and real-world contact strengthen this axis."
};

// Readiness
const READINESS_DECAY_PER_DAY  = 15;
const READINESS_RECOVERY_QUEST = 30;
const ATROPHY_MECHANICAL       = 40;   // calibration fires below this
const ATROPHY_VISUAL           = 55;   // visual debuff clears above this on recovery

// XP per quest difficulty
const XP_LOW    = 5;
const XP_MEDIUM = 10;
const XP_HIGH   = 20;
const XP_CALIBRATION = 5;

// Body sub-stat tier thresholds (branchXp required to become eligible for gate test)
const BODY_SUB_TIER_THRESHOLDS = { 1:0, 2:70, 3:400, 4:1800, 5:4000, 6:8000 };

const HIGH_RARITIES = ["RARE","ELITE","LEGENDARY","UNIQUE"];
const SAVE_KEY      = "sovereign_v5";

// Rank thresholds — capacity XP to letter rank
const RANK_THRESHOLDS = [
    { rank: "F", min: 0     },
    { rank: "E", min: 50    },
    { rank: "D", min: 150   },
    { rank: "C", min: 400   },
    { rank: "B", min: 900   },
    { rank: "A", min: 2000  },
    { rank: "S", min: 4500  }
];

function getRank(capacity) {
    for (let i = RANK_THRESHOLDS.length - 1; i >= 0; i--) {
        if (capacity >= RANK_THRESHOLDS[i].min) return RANK_THRESHOLDS[i].rank;
    }
    return "F";
}

function getOverallRank() {
    const avg = STAT_ORDER.reduce((sum, s) => sum + (STATE.stats[s].capacity ?? STATE.stats[s].xp ?? 0), 0) / STAT_ORDER.length;
    return getRank(avg);
}

/* ============================================================
   STATE
   ============================================================ */
let STATE = {
    version: 5,
    player: {
        name: "[PLAYER]",
        level: 1,
        globalXp: 0,
        equippedTitle: null,
        class: {
            groupId: "ENGINEER",
            stageId: "STUDENT",
            rarity:  "RARE",
            tier:    1
        }
    },
    stats: {
        BODY:        { readiness: 100, lastLog: null },
        MIND:        { capacity: 0, readiness: 100, lastLog: null },
        POSITION:    { capacity: 0, readiness: 100, lastLog: null },
        CONNECTIONS: { capacity: 0, readiness: 100, lastLog: null }
    },
    bodySub: {
        STR:  { readiness: 100, branchXp: 0, lastLog: null },
        AGIL: { readiness: 100, branchXp: 0, lastLog: null },
        END:  { readiness: 100, branchXp: 0, lastLog: null }
    },
    systemQuest: "IDLE",
    systemQuestOfferId: "sys_01",
    dailyBoard: [],
    weeklyBoard: [],
    completedToday: [],
    rerolls: { DAILY: 2, WEEKLY: 1 },
    inventory: {
        charms:    [],
        keys:      [],
        artifacts: [],
        fragments: [],
        titles:    []
    },
    bodySkillTree: { completedGates: [], unlockedNodes: ["strength_1","agility_1","endurance_1"] },
    activeConditions: [],  // [{ id, type, appliedAt, expiresAt, expireOn, clearedBy? }]
    cinematicQueue: [],    // [{ type, stat, newRank, text }] — plays in sequence on stat page visit
    lastTick: null,
    lastWeekTick: null
};

let statusDetailStat = null;

/* ============================================================
   HELPERS
   ============================================================ */
const ALL_QUESTS = [...SYS_QUESTS, ...DB_QUESTS];
function questById(id) { return ALL_QUESTS.find(q => q.id === id); }

function getOfferedSystemQuestDef() {
    const id = STATE.systemQuestOfferId;
    return id ? SYS_QUESTS.find(q => q.id === id) ?? null : null;
}

function getGlobalXp() {
    return STATE.player?.globalXp ?? STATE.globalXp ?? 0;
}

function syncSystemQuestModal() {
    const def = getOfferedSystemQuestDef();
    document.getElementById("ui-modal-heading").textContent = def?.modalHeading ?? def?.name ?? "Notice";
    document.getElementById("ui-modal-text").textContent    = def?.modalBody ?? def?.desc ?? "";
}

function openSystemQuestModal() {
    syncSystemQuestModal();
    document.getElementById("ui-modal").classList.add("open");
}

function isBodySkillGateQuest(id) { return /^sys_(STR|AGI|END)_TEST\d+$/.test(id); }

function bodyGateTierFromQuestId(id) {
    const m = String(id).match(/TEST(\d+)$/);
    return m ? parseInt(m[1]) : 0;
}

function bodyGateBranchFromQuestId(id) {
    if (/sys_STR_TEST/.test(id)) return "strength";
    if (/sys_AGI_TEST/.test(id)) return "agility";
    if (/sys_END_TEST/.test(id)) return "endurance";
    return null;
}

function bodyGateSubKeyFromQuestId(id) {
    return BRANCH_TO_SUB[bodyGateBranchFromQuestId(id)] ?? null;
}

function gateQuestIdForBranchTier(prefix, tier) {
    if (prefix === "strength") return `sys_STR_TEST${tier}`;
    if (prefix === "agility")  return `sys_AGI_TEST${tier}`;
    return `sys_END_TEST${tier}`;
}

function bodyGateEligibility(branchPrefix, tier) {
    const sub = BRANCH_TO_SUB[branchPrefix];
    ensureBodySub();
    const missionNeed = BODY_TEST_MISSION_XP[tier - 1] ?? Infinity;
    const branchNeed  = BODY_SUB_TIER_THRESHOLDS[tier]  ?? Infinity;
    const globalXp    = STATE.player.globalXp ?? 0;
    const branchXp    = sub ? (STATE.bodySub[sub].branchXp ?? 0) : 0;
    return {
        missionOk: globalXp  >= missionNeed,
        branchOk:  branchXp  >= branchNeed,
        globalXp,  missionNeed,
        branchXp,  branchNeed,
        sub
    };
}

function ensureBodySub() {
    if (!STATE.bodySub) STATE.bodySub = {
        STR:  { readiness:100, branchXp:0, lastLog:null },
        AGIL: { readiness:100, branchXp:0, lastLog:null },
        END:  { readiness:100, branchXp:0, lastLog:null }
    };
    for (const k of BODY_SUB_KEYS) {
        if (!STATE.bodySub[k])                              STATE.bodySub[k] = { readiness:100, branchXp:0, lastLog:null };
        if (typeof STATE.bodySub[k].readiness !== "number") STATE.bodySub[k].readiness = 100;
        if (typeof STATE.bodySub[k].branchXp  !== "number") STATE.bodySub[k].branchXp  = 0;
    }
}

function syncBodyLastLog() {
    ensureBodySub();
    // BODY.lastLog = most recent activity across any sub-stat
    const logs = BODY_SUB_KEYS.map(k => STATE.bodySub[k].lastLog).filter(Boolean);
    STATE.stats.BODY.lastLog = logs.length ? Math.max(...logs) : null;
}

function addBodySubXp(key, amount) {
    if (amount <= 0 || !BODY_SUB_KEYS.includes(key)) return;
    ensureBodySub();
    STATE.bodySub[key].branchXp += amount;
    // Readiness recovery on quest completion
    STATE.bodySub[key].readiness = Math.min(100,
        (STATE.bodySub[key].readiness ?? 0) + READINESS_RECOVERY_QUEST
    );
    STATE.bodySub[key].lastLog = Date.now();
}

function applyQuestStatXp(def, base) {
    const now = Date.now();
    let total = base;

    function applyOne(statKey, amt) {
        if (amt <= 0) return;
        if (BODY_SUB_KEYS.includes(statKey)) {
            // Direct sub-stat quest (STR, AGIL, END)
            addBodySubXp(statKey, amt);
            syncBodyLastLog();
        } else if (statKey === "BODY") {
            // Calibration quest — split evenly across all sub-stats
            const each = Math.floor(amt / 3);
            for (const k of BODY_SUB_KEYS) addBodySubXp(k, each);
            syncBodyLastLog();
        } else if (STAT_ORDER.includes(statKey)) {
            // MIND, POSITION, CONNECTIONS
            STATE.stats[statKey].capacity = (STATE.stats[statKey].capacity ?? 0) + amt;
            STATE.stats[statKey].readiness = Math.min(100,
                (STATE.stats[statKey].readiness ?? 0) + READINESS_RECOVERY_QUEST
            );
            STATE.stats[statKey].lastLog = now;
        }
    }

    applyOne(def.stat, base);
    if (def.stat2) {
        const sec = Math.floor(base * 0.5);
        total += sec;
        applyOne(def.stat2, sec);
    }

    STATE.player.globalXp = (STATE.player.globalXp ?? 0) + total;
}

function ensureBodySkillTree() {
    if (!STATE.bodySkillTree) {
        STATE.bodySkillTree = { completedGates:[], unlockedNodes:["strength_1","agility_1","endurance_1"] };
    }
    if (!Array.isArray(STATE.bodySkillTree.completedGates)) STATE.bodySkillTree.completedGates = [];
    if (!Array.isArray(STATE.bodySkillTree.unlockedNodes))  STATE.bodySkillTree.unlockedNodes  = ["strength_1","agility_1","endurance_1"];
    recomputeBodySkillUnlocks();
}

function recomputeBodySkillUnlocks() {
    const done = new Set(STATE.bodySkillTree.completedGates);
    const u    = new Set(["strength_1","agility_1","endurance_1"]);
    for (const b of branchMeta) {
        for (let t = 1; t <= 5; t++) {
            const fromNode = `${b.prefix}_${t}`;
            const qid      = `${b.questBase}${t}`;
            const toNode   = `${b.prefix}_${t+1}`;
            if (u.has(fromNode) && done.has(qid)) u.add(toNode);
        }
    }
    if (["strength_4","agility_4","endurance_4"].every(k => u.has(k))) u.add("body_placement");
    STATE.bodySkillTree.unlockedNodes = [...u];
}

function isBodySkillNodeUnlocked(nodeId) {
    ensureBodySkillTree();
    return STATE.bodySkillTree.unlockedNodes.includes(nodeId);
}

function offerBodySkillGate(questId) {
    if (!isBodySkillGateQuest(questId) || !questById(questId)) return;
    if (STATE.systemQuest === "ACTIVE") {
        alert("Finish the active system directive first.");
        return;
    }
    const br   = bodyGateBranchFromQuestId(questId);
    const tier = bodyGateTierFromQuestId(questId);
    const el   = bodyGateEligibility(br, tier);
    if (!el.missionOk || !el.branchOk) {
        alert(`Not eligible.\nGlobal XP: ${el.globalXp}/${el.missionNeed}\nBranch XP (${el.sub}): ${el.branchXp}/${el.branchNeed}`);
        return;
    }
    STATE.systemQuestOfferId = questId;
    STATE.systemQuest        = "IDLE";
    openSystemQuestModal();
}

function failBodySkillGateTest(questId) {
    if (!isBodySkillGateQuest(questId)) return;
    const sub = bodyGateSubKeyFromQuestId(questId);
    if (sub) { ensureBodySub(); STATE.bodySub[sub].branchXp = 0; }
    STATE.systemQuest        = "IDLE";
    STATE.systemQuestOfferId = null;
    save();
    render();
}

function escapeHtml(s) {
    return String(s).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/"/g,"&quot;").replace(/'/g,"&#39;");
}

function save() { try { localStorage.setItem(SAVE_KEY, JSON.stringify(STATE)); } catch(e){} }
function load() { try { return JSON.parse(localStorage.getItem(SAVE_KEY)); } catch(e){ return null; } }

function shuffleInPlace(arr) {
    for (let i = arr.length-1; i > 0; i--) {
        const j = Math.floor(Math.random()*(i+1));
        [arr[i],arr[j]] = [arr[j],arr[i]];
    }
}

// FIX B4: loot drop rates now scale properly by rarity tier
function lootDropChance(rarity) {
    if (rarity === "COMMON")    return 0.30;
    if (rarity === "UNCOMMON")  return 0.40;
    if (rarity === "RARE")      return 0.60;
    if (rarity === "ELITE")     return 0.75;
    if (rarity === "LEGENDARY") return 0.90;
    return 1.0; // UNIQUE always drops
}

function baseXpForQuest(def) {
    if (def.type === "calibration") return XP_CALIBRATION;
    if (def.difficulty === "LOW")   return XP_LOW;
    if (def.difficulty === "MEDIUM")return XP_MEDIUM;
    return XP_HIGH;
}

// Sub-stat tier as integer: F=0, E=1, D=2, C=3, B=4, A=5, S=6
// Tier advances each time a gate test is passed (starts at 0 = F)
function getBodySubTier(sub) {
    const questBase = sub === "STR" ? "sys_STR_TEST" : sub === "AGIL" ? "sys_AGI_TEST" : "sys_END_TEST";
    const gates     = STATE.bodySkillTree.completedGates;
    let tier = 0; // F = 0
    for (let t = 1; t <= 6; t++) {
        if (gates.includes(`${questBase}${t}`)) tier = t;
        else break;
    }
    return tier;
}

// Body rank = truncated average of sub-stat integers → letter
function getBodyRank() {
    const tiers = BODY_SUB_KEYS.map(sub => getBodySubTier(sub));
    const avg   = Math.floor(tiers.reduce((s, t) => s + t, 0) / tiers.length);
    const intToRank = ["F","E","D","C","B","A","S"];
    return intToRank[avg] ?? "F";
}

function getBodySubEligibility(sub, tier) {
    ensureBodySub();
    const branchNeed = BODY_SUB_TIER_THRESHOLDS[tier] ?? Infinity;
    const missionNeed = BODY_TEST_MISSION_XP[tier - 1] ?? Infinity;
    const branchXp   = STATE.bodySub[sub].branchXp ?? 0;
    const globalXp   = STATE.player.globalXp ?? 0;
    return {
        branchOk:  branchXp  >= branchNeed,
        missionOk: globalXp  >= missionNeed,
        branchXp,  branchNeed,
        globalXp,  missionNeed
    };
}

/* ============================================================
   TICK & BOARD
   ============================================================ */
function tick() {
    const today    = new Date().toDateString();
    const thisWeek = getWeekKey();
    const newDay   = STATE.lastTick    !== today;
    const newWeek  = STATE.lastWeekTick !== thisWeek;

    if (!newDay && !newWeek) return;

    if (newDay) {
        const prevTick = STATE.lastTick;
        STATE.lastTick       = today;
        STATE.completedToday = [];
        STATE.rerolls        = { DAILY: 2, WEEKLY: 1 };
        pruneDailyConditions();  // expire DAILY conditions on new day tick

        // Calculate days elapsed since last tick (each full day counts as one missed day)
        // e.g. lastTick = yesterday → daysMissed = 1, lastTick = 3 days ago → daysMissed = 3
        const daysMissed = prevTick
            ? Math.max(0, Math.round((new Date(today) - new Date(prevTick)) / 86400000))
            : 0;

        // Decay readiness for each main stat (MIND/POSITION/CONNECTIONS)
        // Skip only if stat has never been touched AND player has never earned XP
        for (const stat of ["MIND","POSITION","CONNECTIONS"]) {
            const row = STATE.stats[stat];
            if (row.lastLog == null && (STATE.player?.globalXp ?? 0) === 0) continue;
            const decay = daysMissed * READINESS_DECAY_PER_DAY;
            row.readiness = Math.max(0, (row.readiness ?? 100) - decay);
        }

        // Decay readiness for each body sub-stat independently
        for (const sub of BODY_SUB_KEYS) {
            ensureBodySub();
            const row = STATE.bodySub[sub];
            if (row.lastLog == null && (STATE.player?.globalXp ?? 0) === 0) continue;
            const decay = daysMissed * READINESS_DECAY_PER_DAY;
            row.readiness = Math.max(0, (row.readiness ?? 100) - decay);
        }

        // Derive BODY readiness from worst sub-stat for atrophy check
        ensureBodySub();
        const minBodyReadiness = Math.min(...BODY_SUB_KEYS.map(k => STATE.bodySub[k].readiness ?? 100));
        STATE.stats.BODY.readiness = minBodyReadiness;

        // Freeze daily board snapshot for today
        STATE.dailyBoard = generateDailySlots();
    }

    if (newWeek) {
        STATE.lastWeekTick = thisWeek;
        STATE.weeklyBoard  = generateWeeklySlots();
    }

    save();
}

/** Returns ISO week string e.g. "2025-W03" for stable weekly cycle. */
function getWeekKey() {
    const d   = new Date();
    const day = d.getDay() || 7;
    d.setDate(d.getDate() + 4 - day);
    const year  = d.getFullYear();
    const week  = Math.ceil(((d - new Date(year, 0, 1)) / 86400000 + 1) / 7);
    return `${year}-W${String(week).padStart(2, "0")}`;
}

/** Generate frozen daily slot array — called once per day. */
function generateDailySlots() {
    const exclude = new Set([...STATE.weeklyBoard]);
    const pool = DB_QUESTS.filter(q =>
        q.type === "daily" &&
        !exclude.has(q.id) &&
        questIsEligible(q) &&
        questIsAllowed(q)
    );
    shuffleInPlace(pool);
    return pool.slice(0, 3).map(q => q.id);
}

/** Generate frozen weekly slot array — called once per week. */
function generateWeeklySlots() {
    const pool = DB_QUESTS.filter(q =>
        q.type === "weekly" &&
        questIsEligible(q) &&
        questIsAllowed(q)
    );
    shuffleInPlace(pool);
    return pool.slice(0, 2).map(q => q.id);
}

/** Compute overlay quests (calibration + system) — dynamic, not frozen. */
function getOverlayQuests() {
    const overlay = [];

    // System quest — always first in overlay
    if (STATE.systemQuest === "ACTIVE" && STATE.systemQuestOfferId &&
        !STATE.completedToday.includes(STATE.systemQuestOfferId)) {
        overlay.push(STATE.systemQuestOfferId);
    }

    // Calibration quests for atrophied stats (readiness below mechanical threshold)
    for (const stat of STAT_ORDER) {
        const readiness = stat === "BODY"
            ? Math.min(...BODY_SUB_KEYS.map(k => STATE.bodySub[k]?.readiness ?? 100))
            : (STATE.stats[stat].readiness ?? 100);
        if (readiness > ATROPHY_MECHANICAL) continue;
        const cal = DB_QUESTS.find(q => q.type === "calibration" && q.stat === stat);
        if (cal && !STATE.completedToday.includes(cal.id) && !overlay.includes(cal.id)) {
            overlay.push(cal.id);
        }
    }

    return overlay;
}

/* ============================================================
   QUEST ACTIONS
   ============================================================ */
function executeQuest(id) {
    if (STATE.completedToday.includes(id)) return;
    const def = questById(id);
    if (!def) return;

    // --- Animate the card in-place before touching state ---
    const card  = document.querySelector(`[data-quest-id="${id}"]`);
    const check = card ? card.querySelector(".check") : null;

    if (check) {
        check.classList.add("popping");
        check.innerHTML = "✓";
        check.classList.add("on");
        check.addEventListener("animationend", () => check.classList.remove("popping"), { once: true });
    }
    if (card) {
        card.classList.add("completing");
        // Short delay so the green border flash is visible before fading
        setTimeout(() => card.classList.add("done"), 280);
    }

    // --- Update state ---
    STATE.completedToday.push(id);
    applyQuestStatXp(def, baseXpForQuest(def));
    // Quest stays in dailyBoard/weeklyBoard — frozen boards are immutable mid-session.
    // completedToday is used to determine done state in renderFrozenSection.

    if (def.type === "system") {
        // Non-gate system quests — standard cinematic or toast based on rarity
        if (!isBodySkillGateQuest(id)) {
            if (HIGH_RARITIES.includes(def.rarity)) {
                setTimeout(() => showCinematic("Key item acquired"), 400);
            } else {
                setTimeout(() => showToast({ type:"Modest reward", name:"Stat acknowledged" }), 400);
            }
        }
        // Body gate quest cinematics are handled inside the gate completion block below
        if (isBodySkillGateQuest(id)) {
            ensureBodySkillTree();
            const rankBefore = getBodyRank();
            if (!STATE.bodySkillTree.completedGates.includes(id)) {
                STATE.bodySkillTree.completedGates.push(id);
            }
            recomputeBodySkillUnlocks();
            const rankAfter = getBodyRank();
            STATE.systemQuest        = "IDLE";
            STATE.systemQuestOfferId = null;
            // Queue rank-up cinematic for next Body stat page visit
            if (rankAfter !== rankBefore) {
                if (!Array.isArray(STATE.activeConditions)) STATE.activeConditions = [];
        if (!Array.isArray(STATE.cinematicQueue)) STATE.cinematicQueue = [];
                STATE.cinematicQueue.push({ type: "RANK_UP", stat: "BODY", newRank: rankAfter });
            } else {
                // Branch advanced but rank unchanged — quiet toast
                const branch = bodyGateBranchFromQuestId(id);
                const sub    = BRANCH_TO_SUB[branch] ?? "";
                setTimeout(() => showToast({ type: "BRANCH CLEARED", name: `${sub} tier advanced` }), 400);
            }
        } else {
            STATE.systemQuest = "DONE";
        }
    } else {
        setTimeout(() => rollLoot(def.rarity), 400);
    }

    // Do NOT call generateBoard here — that would fill the empty slot with a new quest.
    // Board only regenerates on daily tick. Just save and update stats display.
    save();
    renderStats();
    setTimeout(() => renderQuestBoard(), 650);
}

function rollLoot(rarity) {
    const table = DB_LOOT[rarity];
    if (!table || table.length === 0) return;
    if (Math.random() > lootDropChance(rarity)) return;
    const itemId = table[Math.floor(Math.random() * table.length)];
    const itemDef = DB_ITEMS[itemId];
    if (!itemDef) return;
    // Persist to inventory
    grantItem(itemId);
    // Toast notification
    showToast({ type: itemDef.archetype.toUpperCase(), name: itemDef.name, chroma: itemDef.chroma });
}

function grantItem(itemId) {
    const def = DB_ITEMS[itemId];
    if (!def) return;
    if (!STATE.inventory) STATE.inventory = { charms:[], keys:[], artifacts:[], fragments:[], titles:[] };
    const arr = STATE.inventory[def.archetype];
    if (!arr) return;
    const existing = arr.find(i => i.id === itemId);
    if (existing) {
        existing.qty++;
    } else {
        arr.push({ id: itemId, qty: 1 });
    }
    save();
}

function triggerReroll(id) {
    const current = questById(id);
    if (!current || STATE.completedToday.includes(id)) return;

    const poolKey     = current.type === "weekly" ? "WEEKLY" : "DAILY";
    const frozenBoard = poolKey === "WEEKLY" ? STATE.weeklyBoard : STATE.dailyBoard;
    if (STATE.rerolls[poolKey] <= 0) return;

    // Exclude quests already in either frozen board
    const allBoarded = new Set([...STATE.dailyBoard, ...STATE.weeklyBoard]);
    let pool = DB_QUESTS.filter(q =>
        q.type === current.type &&
        q.difficulty === current.difficulty &&
        !allBoarded.has(q.id) &&
        !STATE.completedToday.includes(q.id) &&
        q.id !== id &&
        questIsEligible(q) &&
        questIsAllowed(q)
    );
    // Fallback: relax difficulty constraint
    if (pool.length === 0) {
        pool = DB_QUESTS.filter(q =>
            q.type === current.type &&
            !allBoarded.has(q.id) &&
            !STATE.completedToday.includes(q.id) &&
            q.id !== id &&
            questIsEligible(q) &&
            questIsAllowed(q)
        );
    }
    if (pool.length === 0) return;

    STATE.rerolls[poolKey]--;
    // Swap within the frozen slot — slot count never changes
    const idx = frozenBoard.indexOf(id);
    if (idx !== -1) frozenBoard[idx] = pool[Math.floor(Math.random() * pool.length)].id;

    save();
    renderQuestBoard();
}

function handleSystemChoice(choice) {
    document.getElementById("ui-modal").classList.remove("open");
    const sys = getOfferedSystemQuestDef();
    if (!sys) { save(); render(); return; }

    if (choice === "accept") {
        STATE.systemQuestOfferId = sys.id;
        STATE.systemQuest        = "ACTIVE";
        // No generateBoard() — frozen boards stay frozen.
        // Overlay re-renders automatically via renderQuestBoard.
    } else if (sys.statLinked) {
        STATE.systemQuest = "PENDING";
    } else {
        STATE.systemQuest = "DISMISSED";
    }
    save();
    render();
}

/* ============================================================
   RENDER
   ============================================================ */
function render() {
    renderStats();
    renderFxIcons();
    renderQuestBoard();
    if (statusDetailStat) renderStatDetailPage(statusDetailStat);
    if (document.getElementById("tab-inventory") &&
        !document.getElementById("tab-inventory").classList.contains("hidden")) renderVault();
    if (document.getElementById("debug-drawer").classList.contains("open")) renderDebugTables();
}

function openStatDetail(statName) {
    if (!STAT_ORDER.includes(statName)) return;
    statusDetailStat = statName;
    document.getElementById("status-overview").classList.add("hidden");
    document.getElementById("status-stat-detail").classList.remove("hidden");
    renderStatDetailPage(statName);
    // Drain cinematic queue for this stat page
    drainCinematicQueue(statName);
}

// FIX B6: closeStatDetail is now also called from nav tab switching
function closeStatDetail() {
    statusDetailStat = null;
    document.getElementById("status-overview").classList.remove("hidden");
    document.getElementById("status-stat-detail").classList.add("hidden");
}

function renderStatDetailPage(statName) {
    const inner = document.getElementById("status-stat-detail-inner");
    const row   = STATE.stats[statName];
    if (!inner || !row) return;

    const lastLogStr = row.lastLog != null ? new Date(row.lastLog).toLocaleString() : "Never";
    let extra = "";

    if (statName === "BODY") {
        ensureBodySub();
        ensureBodySkillTree();
        extra = `
            <div class="stat-detail-meta muted" style="margin-top:10px;">
                STR ${STATE.bodySub.STR.branchXp ?? 0} XP &nbsp;·&nbsp;
                AGIL ${STATE.bodySub.AGIL.branchXp ?? 0} XP &nbsp;·&nbsp;
                END ${STATE.bodySub.END.branchXp ?? 0} XP
            </div>
            ${buildBodySkillTreeHtml()}
        `;
    }

    const rank = statName === "BODY" ? getBodyRank() : getRank(row.capacity ?? 0);
    const rankColors = { F:"#e84d4d", E:"#e87a4d", D:"#e87a4d", C:"#f0c040", B:"#4ddde8", A:"#4de894", S:"#b44de8" };
    const rankColor  = rankColors[rank] ?? "#e87a4d";
    const ringId     = "statRing_" + statName;

    inner.innerHTML = `
        <div style="display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:12px;">
            <div>
                <div class="stat-detail-title">${escapeHtml(statName)}</div>
                <div class="stat-detail-sub">STAT BREAKDOWN</div>
                <div class="stat-detail-xp">${statName === "BODY" ? "" : (row.capacity ?? 0) + " XP"}</div>
                <div class="stat-detail-meta">${(row.readiness ?? 100) <= ATROPHY_MECHANICAL ? "STATUS: ATROPHIED — complete a calibration quest to clear." : (row.readiness ?? 100) <= ATROPHY_VISUAL ? "STATUS: DEGRADED" : "STATUS: NOMINAL"}</div>
                <div class="stat-detail-meta muted">Last activity: ${escapeHtml(lastLogStr)}</div>
            </div>
            <div style="position:relative;width:200px;height:200px;flex-shrink:0;margin-left:-60px;margin-right:-20px;margin-top:-40px;">
                <canvas id="${ringId}" width="200" height="200"></canvas>
                <div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);text-align:center;pointer-events:none;">
                    <div style="font-size:58px;font-weight:700;color:${rankColor};line-height:1;">${rank}</div>
                    <div style="font-size:11px;color:#4a7fc1;letter-spacing:2px;">RANK</div>
                </div>
            </div>
        </div>
        <div class="stat-detail-blurb">${escapeHtml(STAT_DETAIL_BLURB[statName] ?? "")}</div>
        ${extra}
    `;

    // Draw rank ring — decorative for BODY (no progress arc), XP-based for others
    requestAnimationFrame(() => {
        const canvas = document.getElementById("${ringId}");
        if (!canvas) return;
        const ctx = canvas.getContext("2d");
        const cx = 100, cy = 100, r = 90;
        ctx.clearRect(0, 0, 200, 200);
        // Track ring (always drawn)
        ctx.beginPath(); ctx.arc(cx, cy, r, 0, Math.PI * 2);
        ctx.strokeStyle = "#1a3d73"; ctx.lineWidth = 3; ctx.stroke();
        if (statName !== "BODY") {
            // XP-based progress arc for MIND/POSITION/CONNECTIONS
            const cap = row.capacity ?? 0;
            const thresholds = RANK_THRESHOLDS;
            let curIdx = 0;
            for (let i = 0; i < thresholds.length; i++) { if (cap >= thresholds[i].min) curIdx = i; }
            const curMin  = thresholds[curIdx]?.min ?? 0;
            const nextMin = thresholds[curIdx + 1]?.min ?? curMin + 1;
            const progress = Math.min(1, (cap - curMin) / (nextMin - curMin));
            const start = -Math.PI / 2;
            const end   = start + Math.PI * 2 * progress;
            ctx.beginPath(); ctx.arc(cx, cy, r, start, end);
            ctx.strokeStyle = "${rankColor}"; ctx.lineWidth = 3; ctx.lineCap = "round"; ctx.stroke();
            const dotX = cx + r * Math.cos(end);
            const dotY = cy + r * Math.sin(end);
            ctx.beginPath(); ctx.arc(dotX, dotY, 2.5, 0, Math.PI * 2);
            ctx.fillStyle = "${rankColor}"; ctx.fill();
        } else {
            // Decorative full ring for BODY — gate tests are physical, not XP
            ctx.beginPath(); ctx.arc(cx, cy, r, 0, Math.PI * 2);
            ctx.strokeStyle = "${rankColor}"; ctx.lineWidth = 3; ctx.stroke();
        }
    });
}

function buildBodySkillTreeHtml() {
    ensureBodySkillTree();
    const branches = [
        { label:"Strength",  prefix:"strength" },
        { label:"Agility",   prefix:"agility"  },
        { label:"Endurance", prefix:"endurance" }
    ];
    let html = '<p class="sec" style="margin-top:18px;">BODY SKILL TREE</p>';

    html += '<div class="body-tree-scroll">';

    for (const b of branches) {
        const sub = BRANCH_TO_SUB[b.prefix];
        html += `<div class="body-tree-branch"><div class="body-tree-branch-title">${b.label.toUpperCase()}</div>`;
        for (let tier = 1; tier <= 6; tier++) {
            const nid = `${b.prefix}_${tier}`;
            const un  = isBodySkillNodeUnlocked(nid);
            html += `<div class="body-node ${un?"body-node-unlocked":"body-node-locked"}">${escapeHtml(b.label)} ${BODY_SKILL_ROMAN[tier-1]}</div>`;

            if (tier < 6) {
                const qid      = gateQuestIdForBranchTier(b.prefix, tier);
                const gateDone = STATE.bodySkillTree.completedGates.includes(qid);
                const nextUn   = isBodySkillNodeUnlocked(`${b.prefix}_${tier+1}`);
                const el       = bodyGateEligibility(b.prefix, tier);
                const qdef     = questById(qid);
                const onBoard  = STATE.systemQuest === "ACTIVE" && STATE.systemQuestOfferId === qid;
                const mCls     = ok => ok ? "met" : "unmet";

                html += `<div class="body-gate ${gateDone?"body-gate-done":""}">`;

                if (gateDone) {
                    html += `<span class="body-gate-ok">CLEARED</span>`;
                } else if (onBoard) {
                    html += `<span class="muted">ON MISSION LOG</span>`;
                } else if (un && !nextUn) {
                    if (el.missionOk && el.branchOk) {
                        html += `<button type="button" class="body-gate-btn" onclick="offerBodySkillGate('${qid}')">Receive directive</button>`;
                    }
                }
                html += "</div>";
            }
        }
        html += "</div>";
    }
    html += "</div>";
    const pl = isBodySkillNodeUnlocked("body_placement");
    html += `<div class="body-placement ${pl?"body-node-unlocked":"body-node-locked"}">ATHLETICISM: PLACEMENT</div>`;

    return html;
}

function renderStats() {
    document.getElementById("ui-xp-bar").style.width = `${(STATE.player?.globalXp ?? STATE.globalXp ?? 0) % 100}%`;
    document.getElementById("ui-stat-miss").classList.toggle("hidden", STATE.systemQuest !== "STATMISS");

    document.getElementById("ui-stat-grid").innerHTML = STAT_ORDER.map(name => {
        const row       = STATE.stats[name];
        const readiness = row.readiness ?? 100;
        const atrophied = readiness <= ATROPHY_VISUAL;
        const cls  = `stat stat-clickable${atrophied ? " atrophied" : ""}`;
        const note = atrophied ? ` <span class='muted'>(atrophied)</span>` : "";
        const xpLabel = name === "BODY"
            ? `Rank: ${getBodyRank()}`
            : `XP: ${row.capacity ?? 0}`;
        return `<div class="${cls}" role="button" tabindex="0" onclick="openStatDetail('${name}')">
            <div><strong>${name}</strong>${note}</div>
            <div class="muted">${xpLabel}</div>
        </div>`;
    }).join("");
}

function renderQuestBoard() {
    const el = document.getElementById("ui-quest-board");
    let html = "";
    html += renderOverlaySection();
    html += renderFrozenSection("DAILY",  STATE.dailyBoard,  "Directives",  STATE.rerolls.DAILY,  2);
    html += renderFrozenSection("WEEKLY", STATE.weeklyBoard, "Operations",  STATE.rerolls.WEEKLY, 1);
    if (!html) html = `<p class="muted">All directives complete.</p>`;
    el.innerHTML = html;
    startBoardTimers();
}

/** Overlay: calibration + system — dynamic, no slot constraints, no rerolls. */
function renderOverlaySection() {
    const ids = getOverlayQuests();
    if (ids.length === 0) return "";
    return `<h2>System</h2>` + ids.map(id => questCardHtml(id, null)).join("");
}

/**
 * Frozen section: daily or weekly board snapshot.
 * Slots are fixed — only status (active/done) changes within a session.
 * Sort order: active → complete.
 */
function renderFrozenSection(poolKey, board, label, rerollsLeft, rerollMax) {
    if (board.length === 0) return "";
    const active = board.filter(id => !STATE.completedToday.includes(id));
    const done   = board.filter(id =>  STATE.completedToday.includes(id));
    const sorted = [...active, ...done];
    const timerId = `timer-${poolKey.toLowerCase()}`;
    return `<h2>
        <span>${label} <span class="muted">(rerolls ${rerollsLeft}/${rerollMax})</span></span>
        <span class="board-timer" id="${timerId}">--:--:--</span>
    </h2>` + sorted.map(id => questCardHtml(id, poolKey)).join("");
}

/* ── Board countdown timers ─────────────────────────────────────────────── */
let _timerInterval = null;

function startBoardTimers() {
    if (_timerInterval) clearInterval(_timerInterval);
    tickTimers();
    _timerInterval = setInterval(tickTimers, 1000);
}

function tickTimers() {
    const now = new Date();

    // Daily — time until next midnight
    const dailyEl = document.getElementById("timer-daily");
    if (dailyEl) {
        const midnight = new Date(now);
        midnight.setHours(24, 0, 0, 0);
        dailyEl.textContent = formatCountdown(midnight - now, false);
    }

    // Weekly — time until next Monday 00:00
    const weeklyEl = document.getElementById("timer-weekly");
    if (weeklyEl) {
        const nextMonday = new Date(now);
        const daysUntilMon = (8 - nextMonday.getDay()) % 7 || 7;
        nextMonday.setDate(nextMonday.getDate() + daysUntilMon);
        nextMonday.setHours(0, 0, 0, 0);
        weeklyEl.textContent = formatCountdown(nextMonday - now, true);
    }
}

function formatCountdown(ms, showDays) {
    if (ms <= 0) return showDays ? "0:00:00:00" : "00:00:00";
    const totalSec = Math.floor(ms / 1000);
    const s = totalSec % 60;
    const m = Math.floor(totalSec / 60) % 60;
    const h = Math.floor(totalSec / 3600) % 24;
    const d = Math.floor(totalSec / 86400);
    const pad = n => String(n).padStart(2, "0");
    if (showDays) return `${d}:${pad(h)}:${pad(m)}:${pad(s)}`;
    return `${pad(h)}:${pad(m)}:${pad(s)}`;
}

function questLabel(type) {
    if (type === "weekly")      return "Weekly";
    if (type === "system")      return "System";
    if (type === "calibration") return "Calibrate";
    return "Daily";
}

function questCardHtml(id, poolKey) {
    const q = questById(id);
    if (!q) return "";
    const done     = STATE.completedToday.includes(id);
    // poolKey passed in from renderFrozenSection; overlay quests never get rerolls
    const canReroll= !done && poolKey && (q.type === "daily" || q.type === "weekly") && STATE.rerolls[poolKey] > 0;

    const subHint = (BODY_SUB_KEYS.includes(q.stat) || (q.stat2 && BODY_SUB_KEYS.includes(q.stat2)))
        ? `<div class="quest-stat-hint">${escapeHtml([q.stat,q.stat2].filter(Boolean).join(" · "))}</div>` : "";

    const failBtn = (!done && isBodySkillGateQuest(id))
        ? `<button type="button" class="btn-fail-gate" onclick="event.stopPropagation();failBodySkillGateTest('${id}')">Fail test</button>` : "";

    const aura = !done && q.difficulty === "MEDIUM" ? " aura-medium"
                : !done && q.difficulty === "HIGH"   ? " aura-high"
                : "";
    return `<div class="quest ${done?"done":""}${aura}" data-quest-id="${id}">
        <div class="check ${done?"on":""}" onclick="executeQuest('${id}')">${done?"✓":""}</div>
        <span class="tag">${questLabel(q.type)}</span>
        <div class="quest-body">
            <div class="quest-title">${escapeHtml(q.name)}</div>
            <div class="quest-desc">${escapeHtml(q.desc)}</div>
            ${subHint}${failBtn}
        </div>
        ${q.stat2 ? `<span class="tag">Syn</span>` : ""}
        ${canReroll ? `<button type="button" onclick="triggerReroll('${id}')">Reroll</button>` : ""}
    </div>`;
}

/* ── Vault ──────────────────────────────────────────────────────────────── */
let _vaultActiveTab = "charms";

function renderVault() {
    renderVaultGrid(_vaultActiveTab);
}

function renderVaultGrid(archetype) {
    _vaultActiveTab = archetype;
    const grid = document.getElementById("vault-grid");
    if (!grid) return;

    // Update tab active state
    document.querySelectorAll(".vault-tab").forEach(t => {
        t.classList.toggle("active", t.dataset.archetype === archetype);
    });

    const items = STATE.inventory?.[archetype] ?? [];
    if (items.length === 0) {
        grid.innerHTML = "";
        return;
    }

    grid.innerHTML = `<div class="vault-grid">` + items.map(entry => {
        const def = DB_ITEMS[entry.id];
        if (!def) return "";
        return `<div class="vault-card" onclick="openItemSheet('${entry.id}', ${entry.qty})"
            style="border-color: ${def.chroma}22;">
            <span class="vault-card-rarity" style="color:${def.chroma};border-color:${def.chroma}55;">
                ${def.rarity}
            </span>
            <span class="vault-card-name">${escapeHtml(def.name)}</span>
            ${entry.qty > 1 ? `<span class="vault-card-qty">x${entry.qty}</span>` : ""}
        </div>`;
    }).join("") + `</div>`;
}

function openItemSheet(itemId, qty) {
    const def = DB_ITEMS[itemId];
    if (!def) return;
    const inner = document.getElementById("vault-sheet-inner");
    inner.innerHTML = `
        <div class="sheet-close" onclick="closeItemSheet()">✕</div>
        <span class="sheet-rarity-tag" style="color:${def.chroma};border-color:${def.chroma}66;">${def.rarity}</span>
        <div class="sheet-name">${escapeHtml(def.name)}</div>
        <div class="sheet-archetype">${def.archetype.toUpperCase()}</div>
        <div class="sheet-desc">${escapeHtml(def.desc)}</div>
        ${qty > 1 ? `<div class="sheet-qty">IN VAULT: ${qty}</div>` : ""}
        ${def.archetype === "charms" ? `<div style="text-align:center;margin-top:20px;"><button type="button" class="btn-use" onclick="useItem('${itemId}')">USE</button></div>` : ""}
    `;
    document.getElementById("vault-sheet-bg").classList.add("open");
}

function useItem(itemId) {
    const def = DB_ITEMS[itemId];
    if (!def || def.archetype !== "charms") return;
    const arr = STATE.inventory?.charms ?? [];
    const entry = arr.find(i => i.id === itemId);
    if (!entry || entry.qty <= 0) return;
    // Consume one
    entry.qty--;
    if (entry.qty === 0) STATE.inventory.charms = arr.filter(i => i.id !== itemId);
    // Apply condition if charm has one mapped
    if (def.conditionId) applyCondition(def.conditionId);
    showToast({ type: "CHARM ACTIVATED", name: def.name, chroma: def.chroma });
    save();
    closeItemSheet();
    renderVault();
    renderFxIcons();
}

function closeItemSheet() {
    document.getElementById("vault-sheet-bg").classList.remove("open");
}

/* ── Prerequisite & condition filter engine ─────────────────────────────── */

function checkRequire(req) {
    switch (req.type) {
        case "STAT_TIER": {
            // MIND/POSITION/CONNECTIONS — XP-based rank
            const rank = getRank(STATE.stats[req.stat]?.capacity ?? 0);
            const rankToInt = { F:0, E:1, D:2, C:3, B:4, A:5, S:6 };
            return (rankToInt[rank] ?? 0) >= req.tier;
        }
        case "BODY_TIER": {
            // Body sub-stat — gate-based tier
            return getBodySubTier(req.sub) >= req.tier;
        }
        case "STAT_RANK": {
            // Explicit rank letter comparison
            const rankToInt = { F:0, E:1, D:2, C:3, B:4, A:5, S:6 };
            const current = req.stat === "BODY"
                ? getBodyRank()
                : getRank(STATE.stats[req.stat]?.capacity ?? 0);
            return (rankToInt[current] ?? 0) >= (rankToInt[req.rank] ?? 0);
        }
        case "GLOBAL_XP": {
            return (STATE.player?.globalXp ?? 0) >= req.value;
        }
        default:
            return true;
    }
}

function questIsEligible(q) {
    if (!q.prerequisite) return true;
    const reqs = q.prerequisite.require ?? [];
    return reqs.every(checkRequire);
}

// Check if a condition's mechanic blocks a specific quest
function conditionBlocks(condEntry, q) {
    const def = DB_CONDITIONS.find(c => c.id === condEntry.id);
    if (!def?.mechanic) return false;
    const m = def.mechanic;
    if (m === "BLOCK_QUEST: FRICTION_HIGH"    && q.difficulty === "HIGH")          return true;
    if (m === "BLOCK_QUEST: FRICTION_MEDIUM"  && q.difficulty === "MEDIUM")        return true;
    if (m === "BLOCK_QUEST: STAT_CONNECTIONS" && q.stat === "CONNECTIONS")         return true;
    if (m === "BLOCK_QUEST: BODY_TIER_2+"     && BODY_SUB_KEYS.includes(q.stat) && getBodySubTier(q.stat) >= 2) return true;
    if (m === "BLOCK_QUEST: MIND_TIER_2+"     && q.stat === "MIND")                return true;
    return false;
}

function questIsAllowed(q) {
    const active = getActiveConditions();
    return !active.some(c => conditionBlocks(c, q));
}

/* ── Conditions engine ──────────────────────────────────────────────────── */

function applyCondition(id) {
    const def = DB_CONDITIONS.find(c => c.id === id);
    if (!def) return;
    removeCondition(id);
    const now = Date.now();
    const entry = { id, type: def.type, appliedAt: now, expiresAt: null, expireOn: def.expireOn };
    if (def.expireOn === "TIMED" && def.durationMs) {
        entry.expiresAt = now + def.durationMs;
    }
    if (def.expireOn === "UNTIL_CLEARED") {
        entry.clearedBy = def.clearedBy ?? null;
    }
    STATE.activeConditions.push(entry);
    save();
    // Show flair for buffs, update FX row for debuffs
    if (def.type === "Buff") {
        showBuffFlair(id);
    } else {
        renderFxIcons();
    }
}

function removeCondition(id) {
    STATE.activeConditions = STATE.activeConditions.filter(c => c.id !== id);
    save();
}

function clearConditionsBy(clearedBy) {
    STATE.activeConditions = STATE.activeConditions.filter(c => c.clearedBy !== clearedBy);
    save();
}

function pruneExpiredConditions() {
    const now = Date.now();
    STATE.activeConditions = STATE.activeConditions.filter(c => {
        if (c.expireOn === "TIMED") return now < (c.expiresAt ?? Infinity);
        return true; // DAILY and UNTIL_CLEARED handled elsewhere
    });
}

function pruneDailyConditions() {
    STATE.activeConditions = STATE.activeConditions.filter(c => c.expireOn !== "DAILY");
}

function hasCondition(id) {
    pruneExpiredConditions();
    return STATE.activeConditions.some(c => c.id === id);
}

function getActiveConditions() {
    pruneExpiredConditions();
    return STATE.activeConditions;
}

/* ── FX icon row ─────────────────────────────────────────────────────────── */

function renderFxIcons() {
    const row = document.getElementById("fx-icons-row");
    if (!row) return;
    // Hide the row visually when not on status tab, but keep it rendered
    const onStatus = !document.getElementById("tab-status")?.classList.contains("hidden");
    row.style.visibility = onStatus ? "visible" : "hidden";

    const active = getActiveConditions();

    // Always show atrophy conditions derived from readiness even if not in activeConditions
    const atrophyIcons = [];
    for (const stat of STAT_ORDER) {
        const readiness = stat === "BODY"
            ? Math.min(...BODY_SUB_KEYS.map(k => STATE.bodySub[k]?.readiness ?? 100))
            : (STATE.stats[stat].readiness ?? 100);
        if (readiness <= ATROPHY_VISUAL) {
            atrophyIcons.push({
                id:      `atrophy_${stat}`,
                name:    `${stat} ATROPHY`,
                symbol:  "!",
                chroma:  "#e87a4d",
                expireOn:"UNTIL_CLEARED",
                desc:    "Readiness degraded — complete a calibration quest."
            });
        }
    }

    // Only show debuffs persistently — buffs are shown via flair on application only
    const condIcons = active.map(entry => {
        const def = DB_CONDITIONS.find(c => c.id === entry.id);
        if (!def) return null;
        const symbol = def.type === "Buff" ? "↑" : "↓";
        let timeLeft = "";
        if (entry.expireOn === "TIMED" && entry.expiresAt) {
            const ms = Math.max(0, entry.expiresAt - Date.now());
            const m  = Math.floor(ms / 60000);
            const h  = Math.floor(m / 60);
            timeLeft = h > 0 ? `${h}h ${m % 60}m` : `${m}m`;
        } else if (entry.expireOn === "DAILY") {
            timeLeft = "until midnight";
        } else if (entry.expireOn === "UNTIL_CLEARED") {
            timeLeft = "until cleared";
        }
        return { id: entry.id, name: def.name, symbol, chroma: def.chroma, desc: timeLeft };
    }).filter(Boolean);

    const allIcons = [...atrophyIcons, ...condIcons];

    if (allIcons.length === 0) {
        row.innerHTML = "";
        return;
    }

    row.innerHTML = allIcons.map(ic => {
        const bg     = ic.chroma + "26";
        const border = ic.chroma + "88";
        return `<span class="fx-icon"
            style="background:${bg};border-color:${border};color:${ic.chroma};"
            data-name="${escapeHtml(ic.name)}"
            data-desc="${escapeHtml(ic.desc)}"
            onclick="showFxTooltip(event, this)"
        >${ic.symbol}</span>`;
    }).join("");
}

function showBuffFlair(condId) {
    const def = DB_CONDITIONS.find(c => c.id === condId);
    if (!def || def.type !== "Buff") return;
    // Remove any existing flair
    document.querySelectorAll(".buff-flair").forEach(el => el.remove());
    const flair = document.createElement("div");
    flair.className = "buff-flair";
    flair.style.background   = def.chroma + "18";
    flair.style.borderColor  = def.chroma + "88";
    flair.style.color        = def.chroma;
    let duration = "";
    if (def.durationMs) {
        const h = Math.floor(def.durationMs / 3600000);
        const m = Math.floor((def.durationMs % 3600000) / 60000);
        duration = h > 0 ? `${h}h ${m > 0 ? m + "m" : ""}` : `${m}m`;
    } else if (def.expireOn === "DAILY") {
        duration = "until midnight";
    }
    flair.innerHTML = `
        <span class="buff-flair-icon">↑</span>
        <div class="buff-flair-text">
            <span class="buff-flair-name">${escapeHtml(def.name)}</span>
            ${duration ? `<span class="buff-flair-sub">${duration}</span>` : ""}
        </div>
    `;
    document.body.appendChild(flair);
    setTimeout(() => flair.remove(), 2300);
}

function showFxTooltip(e, el) {
    e.stopPropagation();
    const tooltip = document.getElementById("fx-tooltip");
    document.getElementById("fx-tooltip-name").textContent = el.dataset.name ?? "";
    document.getElementById("fx-tooltip-sub").textContent  = el.dataset.desc ?? "";
    // Position near the icon
    const rect = el.getBoundingClientRect();
    tooltip.style.top  = (rect.bottom + 6) + "px";
    tooltip.style.right = (window.innerWidth - rect.right) + "px";
    tooltip.classList.add("visible");
    // Dismiss on next tap anywhere
    setTimeout(() => document.addEventListener("click", dismissFxTooltip, { once: true }), 50);
}

function dismissFxTooltip() {
    document.getElementById("fx-tooltip")?.classList.remove("visible");
}

function showToast(item) {
    const typeEl = document.getElementById("toast-type");
    const nameEl = document.getElementById("toast-name");
    typeEl.textContent = item.type ?? "";
    nameEl.textContent = item.name ?? "";
    nameEl.style.color = item.chroma ?? "var(--chroma-teal)";
    const t = document.getElementById("ui-toast");
    t.style.borderColor = item.chroma ?? "#1e4a8a";
    t.classList.add("open");
    setTimeout(() => t.classList.remove("open"), 3000);
}

/** Pull all queued cinematics for a given stat and play them in sequence. */
function drainCinematicQueue(stat) {
    if (!Array.isArray(STATE.cinematicQueue)) return;
    const forStat = STATE.cinematicQueue.filter(e => e.stat === stat);
    if (forStat.length === 0) return;
    // Remove from queue
    STATE.cinematicQueue = STATE.cinematicQueue.filter(e => e.stat !== stat);
    save();
    // Play in sequence — each waits for the previous to finish
    let delay = 300;
    for (const entry of forStat) {
        const d = delay;
        setTimeout(() => playQueuedCinematic(entry), d);
        delay += (entry.type === "RANK_UP" ? 4500 : 3500);
    }
}

function playQueuedCinematic(entry) {
    if (entry.type === "RANK_UP") {
        showRankUpCinematic(entry.stat, entry.newRank);
    } else {
        showCinematic(entry.text ?? "");
    }
}

function showCinematic(text) {
    const o = document.getElementById("ui-cinematic");
    o.querySelector(".muted").textContent  = "OBJECTIVE COMPLETE";
    document.getElementById("cinematic-reward").textContent = text;
    document.getElementById("cinematic-reward").style.color = "#f0c040";
    o.style.background = "rgba(5,8,15,0.96)";
    o.classList.add("open");
    setTimeout(() => o.classList.remove("open"), 3000);
}

function showRankUpCinematic(stat, newRank) {
    const rankColors = { F:"#e84d4d", E:"#e87a4d", D:"#e87a4d", C:"#f0c040", B:"#4ddde8", A:"#4de894", S:"#b44de8" };
    const color = rankColors[newRank] ?? "#f0c040";
    const o = document.getElementById("ui-cinematic");
    o.querySelector(".muted").textContent = stat + " RANK UP";
    const reward = document.getElementById("cinematic-reward");
    reward.textContent = newRank;
    reward.style.color = color;
    reward.style.fontSize = "5rem";
    reward.style.textShadow = `0 0 40px ${color}88`;
    o.style.background = "rgba(5,8,15,0.98)";
    o.classList.add("open");
    setTimeout(() => {
        o.classList.remove("open");
        reward.style.fontSize = "";
        reward.style.textShadow = "";
    }, 4000);
}

/* ============================================================
   DEBUG
   ============================================================ */
function toggleDebug() {
    const d = document.getElementById("debug-drawer");
    d.classList.toggle("open");
    if (d.classList.contains("open")) renderDebugTables();
}

function renderDebugTables() {
    let q = `<h2>DB_QUESTS (${DB_QUESTS.length})</h2><table><thead><tr><th>ID</th><th>Name</th><th>Stat</th><th>Diff</th><th>Type</th></tr></thead><tbody>`;
    for (const r of DB_QUESTS) {
        q += `<tr><td>${r.id}</td><td>${escapeHtml(r.name)}</td><td>${r.stat2?r.stat+"+"+r.stat2:r.stat}</td><td>${r.difficulty}</td><td>${r.type}</td></tr>`;
    }
    q += "</tbody></table>";
    document.getElementById("debug-quests-table").innerHTML = q;

    let l = `<h2>DB_LOOT</h2><table><thead><tr><th>Tier</th><th>Type</th><th>Name</th><th>Drop%</th></tr></thead><tbody>`;
    for (const tier of Object.keys(DB_LOOT)) {
        for (const item of DB_LOOT[tier]) {
            l += `<tr><td>${tier}</td><td>${item.type}</td><td>${escapeHtml(item.name)}</td><td>${Math.round(lootDropChance(tier)*100)}%</td></tr>`;
        }
    }
    l += "</tbody></table>";
    document.getElementById("debug-loot-table").innerHTML = l;

    let c = `<h2>DB_CONDITIONS (${DB_CONDITIONS.length})</h2><table><thead><tr><th>ID</th><th>Name</th><th>Type</th><th>Mechanic</th></tr></thead><tbody>`;
    for (const r of DB_CONDITIONS) {
        c += `<tr><td>${r.id}</td><td>${escapeHtml(r.name)}</td><td>${r.type}</td><td>${escapeHtml(r.mechanic)}</td></tr>`;
    }
    c += "</tbody></table>";
    document.getElementById("debug-cond-table").innerHTML = c;
}

function debugResetDay()        { STATE.lastTick = new Date(Date.now()-86400000).toDateString(); if (!STATE.player) STATE.player = {}; if (!STATE.player.globalXp) STATE.player.globalXp = 1; tick(); render(); }
function debugForceAtrophy()    { for(const s of STAT_ORDER){ STATE.stats[s].readiness=0; STATE.stats[s].lastLog=Date.now()-72*3600000; } for(const k of BODY_SUB_KEYS){ STATE.bodySub[k].readiness=0; } STATE.stats.BODY.readiness=0; save();render();renderFxIcons(); }
function debugAddXp()           { if(!STATE.player) STATE.player = {}; STATE.player.globalXp = (STATE.player.globalXp ?? 0) + 100; save(); render(); }
function debugCompleteAll()     { [...STATE.dailyBoard, ...STATE.weeklyBoard].forEach(id=>executeQuest(id)); setTimeout(()=>render(), 800); }
function debugTriggerSysQuest() { STATE.systemQuest="IDLE"; if(!STATE.systemQuestOfferId)STATE.systemQuestOfferId=SYS_QUESTS[0].id; save();render(); setTimeout(()=>openSystemQuestModal(),300); }
function debugSimulateMiss()    {
    if(STATE.systemQuest!=="ACTIVE"){alert("No active system quest.");return;}
    const sid=STATE.systemQuestOfferId;
    const sys=sid?questById(sid):null;
    STATE.systemQuest=sys?.statLinked?"STATMISS":"DONE";
    save();render();
}
function debugNukeSave()        { if(confirm("Delete save and reload?")){localStorage.removeItem(SAVE_KEY);location.reload();} }
function debugGrantItems()      { Object.keys(DB_ITEMS).forEach(id => grantItem(id)); render(); }

/* ============================================================
   INIT
   ============================================================ */
document.addEventListener("DOMContentLoaded", () => {
    const saved = load();
    if (saved && typeof saved.version === "number" && saved.version >= 2) {
        STATE = saved;
        // Migrate v2 → v3
        if (STATE.version === 2) {
            STATE.version = 3;
            if (!STATE.bodySkillTree) STATE.bodySkillTree = { completedGates:[], unlockedNodes:["strength_1","agility_1","endurance_1"] };
            if (!STATE.systemQuestOfferId && SYS_QUESTS.length) STATE.systemQuestOfferId = SYS_QUESTS[0].id;
        }
        // Migrate v3 → v4
        if (STATE.version === 3) {
            STATE.version = 4;
            // FIX B7: migration distributes old BODY xp evenly, not all to STR
            const bx = STATE.stats?.BODY?.xp ?? 0;
            const each = Math.floor(bx / 3);
            STATE.bodySub = {
                STR:  { vis:each, hid:0 },
                AGIL: { vis:each, hid:0 },
                END:  { vis:bx - each*2, hid:0 }
            };
            syncBodyStatXpFromSubs();
        }
        for (const stat of STAT_ORDER) {
            // Migrate old isAtrophied flag to readiness number
            if (STATE.stats[stat].isAtrophied !== undefined) {
                if (STATE.stats[stat].isAtrophied) STATE.stats[stat].readiness = 0;
                delete STATE.stats[stat].isAtrophied;
            }
            if (STATE.stats[stat].readiness === undefined) STATE.stats[stat].readiness = 100;
            // Migrate xp → capacity for MIND/POSITION/CONNECTIONS
            if (STATE.stats[stat].xp !== undefined && stat !== "BODY") {
                STATE.stats[stat].capacity = STATE.stats[stat].xp;
                delete STATE.stats[stat].xp;
            }
        }
        // Migrate globalXp to player.globalXp
        if (STATE.globalXp !== undefined && !STATE.player) {
            STATE.player = { name:"[PLAYER]", level:1, globalXp: STATE.globalXp, equippedTitle:null, class:{ groupId:"ENGINEER", stageId:"STUDENT", rarity:"RARE", tier:1 } };
            delete STATE.globalXp;
        }
        // Migrate bodySub vis/hid → branchXp
        for (const k of BODY_SUB_KEYS) {
            if (STATE.bodySub[k]?.vis !== undefined) {
                STATE.bodySub[k].branchXp = STATE.bodySub[k].hid ?? 0;
                delete STATE.bodySub[k].vis;
                delete STATE.bodySub[k].hid;
            }
            if (STATE.bodySub[k]?.readiness === undefined) STATE.bodySub[k].readiness = 100;
        }
        // Migrate from old activeBoard schema to frozen daily/weekly boards
        if (!Array.isArray(STATE.dailyBoard))  STATE.dailyBoard  = [];
        if (!Array.isArray(STATE.activeConditions)) STATE.activeConditions = [];
        if (!Array.isArray(STATE.cinematicQueue)) STATE.cinematicQueue = [];
        if (STATE.pendingRankUp !== undefined) { delete STATE.pendingRankUp; } // migrate old field
        if (!Array.isArray(STATE.weeklyBoard)) STATE.weeklyBoard = [];
        if (!STATE.lastWeekTick) STATE.lastWeekTick = null;
        // If old save had activeBoard, seed daily board from it (one-time migration)
        if (STATE.activeBoard && STATE.activeBoard.length > 0 && STATE.dailyBoard.length === 0) {
            STATE.dailyBoard  = STATE.activeBoard.filter(id => questById(id)?.type !== "weekly").slice(0, 3);
            STATE.weeklyBoard = STATE.activeBoard.filter(id => questById(id)?.type === "weekly").slice(0, 2);
            delete STATE.activeBoard;
        }
        ensureBodySub();
        ensureBodySkillTree();
    } else {
        save();
        ensureBodySub();
        ensureBodySkillTree();
    }

    tick();
    render();
    renderDebugTables();

    if (STATE.systemQuest === "IDLE" && STATE.systemQuestOfferId === "sys_01") {
        setTimeout(() => openSystemQuestModal(), 600);
    }

    document.querySelectorAll("nav button").forEach(btn => {
        btn.addEventListener("click", () => {
            closeStatDetail();
            closeItemSheet();
            const tab = btn.dataset.tab;
            document.querySelectorAll(".tab-pane").forEach(p => p.classList.add("hidden"));
            document.getElementById("tab-" + tab).classList.remove("hidden");
            document.querySelectorAll("nav button").forEach(b => b.classList.remove("current"));
            btn.classList.add("current");
            if (tab === "status" && STATE.systemQuest === "PENDING") {
                setTimeout(() => openSystemQuestModal(), 300);
            }
            if (tab === "status") renderFxIcons();
            if (tab === "inventory") renderVault();
        });
    });

    // Vault tab clicks
    document.getElementById("vault-tabs")?.addEventListener("click", e => {
        const btn = e.target.closest(".vault-tab");
        if (btn) renderVaultGrid(btn.dataset.archetype);
    });

    document.getElementById("btn-accept").addEventListener("click",  () => handleSystemChoice("accept"));
    document.getElementById("btn-decline").addEventListener("click", () => handleSystemChoice("decline"));

    // Swipe-down on top half of stat detail page → go back to status overview
    let _swipeStartY = null;
    let _swipeStartX = null;
    const statDetail = document.getElementById("status-stat-detail");

    statDetail.addEventListener("touchstart", e => {
        const touch = e.touches[0];
        const rect  = statDetail.getBoundingClientRect();
        // Only track if touch starts in top half of the detail panel
        if (touch.clientY < rect.top + rect.height * 0.5) {
            _swipeStartY = touch.clientY;
            _swipeStartX = touch.clientX;
        } else {
            _swipeStartY = null;
        }
    }, { passive: true });

    statDetail.addEventListener("touchend", e => {
        if (_swipeStartY === null) return;
        const touch = e.changedTouches[0];
        const dy    = touch.clientY - _swipeStartY;
        const dx    = Math.abs(touch.clientX - (_swipeStartX ?? touch.clientX));
        // Swipe down >= 60px, more vertical than horizontal → go back
        if (dy > 60 && dx < 40) closeStatDetail();
        _swipeStartY = null;
        _swipeStartX = null;
    }, { passive: true });
});

/* ============================================================
   RANK RING
   ============================================================ */
(function () {
    function drawRankRing(progress) {
        const canvas = document.getElementById("rankRing");
        if (!canvas) return;
        const ctx = canvas.getContext("2d");
        const cx=50, cy=50, r=42, color="#e87a4d";
        ctx.clearRect(0,0,100,100);
        ctx.beginPath(); ctx.arc(cx,cy,r,0,Math.PI*2); ctx.strokeStyle="#1a3d73"; ctx.lineWidth=4; ctx.stroke();
        const start=-Math.PI/2, end=start+Math.PI*2*progress;
        ctx.beginPath(); ctx.arc(cx,cy,r,start,end); ctx.strokeStyle=color; ctx.lineWidth=4; ctx.lineCap="round"; ctx.stroke();
        ctx.beginPath(); ctx.arc(cx+r*Math.cos(end),cy+r*Math.sin(end),3.5,0,Math.PI*2); ctx.fillStyle=color; ctx.fill();
    }
    function syncFromXpBar() {
        const bar=document.getElementById("ui-xp-bar");
        drawRankRing(Math.min(1,Math.max(0,(parseFloat(bar?.style.width)||0)/100)));
    }
    document.addEventListener("DOMContentLoaded",()=>{
        syncFromXpBar();
        const bar=document.getElementById("ui-xp-bar");
        if (bar && typeof MutationObserver!=="undefined") {
            new MutationObserver(syncFromXpBar).observe(bar,{attributes:true,attributeFilter:["style"]});
        }
    });
})();
</script>
<script>
if ("serviceWorker" in navigator) {
    window.addEventListener("load", () => {
        navigator.serviceWorker.register("./sw.js")
            .then(reg => console.log("SW registered:", reg.scope))
            .catch(err => console.log("SW registration failed:", err));
    });
}
</script>
</body>
</html>
