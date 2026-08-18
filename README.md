# The-Algorithm-
Students spend significant time scrolling short-form content. Much of it may be harmless entertainment but provide little educational or career value.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Algorithm Knows You Too Well | AI Recommendation Engine</title>
  <meta name="description" content="AI-Powered Recommendation Agent that analyzes student Reel interactions, infers underlying technical interests beyond keyword matching, and recommends engaging educational tech content.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
/* ==========================================================================
   THE ALGORITHM KNOWS YOU TOO WELL - DESIGN SYSTEM
   Modern, Precision-Crafted Technical UI
   ========================================================================== */

:root {
  --bg-main: #090d16;
  --bg-card: #111827;
  --bg-card-hover: #162032;
  --bg-card-elevated: #1e293b;
  --bg-input: #0f172a;
  
  --border-subtle: #1e293b;
  --border-medium: #334155;
  --border-active: #38bdf8;

  --text-primary: #f8fafc;
  --text-secondary: #94a3b8;
  --text-muted: #64748b;
  --text-highlight: #38bdf8;

  --color-cyan: #38bdf8;
  --color-emerald: #10b981;
  --color-amber: #f59e0b;
  --color-rose: #f43f5e;
  --color-blue: #3b82f6;

  --font-sans: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', Consolas, monospace;

  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.4);
  --shadow-md: 0 4px 12px -2px rgba(0, 0, 0, 0.5);
  --shadow-lg: 0 12px 28px -4px rgba(0, 0, 0, 0.6);
  --transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-sans);
  background-color: var(--bg-main);
  color: var(--text-primary);
  min-height: 100vh;
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}

/* ==========================================================================
   Header & Navigation
   ========================================================================== */

.app-header {
  background-color: rgba(17, 24, 39, 0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-subtle);
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 12px 24px;
}

.header-container {
  max-width: 1440px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 16px;
}

.brand-group {
  display: flex;
  align-items: center;
  gap: 14px;
}

.brand-badge {
  background: linear-gradient(135deg, #0284c7, #0369a1);
  color: #fff;
  font-size: 0.72rem;
  font-weight: 800;
  letter-spacing: 0.08em;
  padding: 4px 8px;
  border-radius: var(--radius-sm);
  box-shadow: 0 2px 4px rgba(0,0,0,0.3);
}

.brand-title {
  font-size: 1.15rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color: var(--text-primary);
}

.brand-subtitle {
  font-size: 0.78rem;
  color: var(--text-secondary);
  font-weight: 500;
}

.header-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.nav-tabs {
  display: flex;
  background-color: var(--bg-input);
  padding: 4px;
  border-radius: var(--radius-md);
  border: 1px solid var(--border-subtle);
  gap: 4px;
}

.tab-btn {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: none;
  background: transparent;
  color: var(--text-secondary);
  font-family: var(--font-sans);
  font-size: 0.82rem;
  font-weight: 600;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: var(--transition);
}

.tab-btn:hover {
  color: var(--text-primary);
  background-color: rgba(255, 255, 255, 0.04);
}

.tab-btn.active {
  background-color: var(--bg-card-elevated);
  color: var(--color-cyan);
  box-shadow: var(--shadow-sm);
}

.tab-icon {
  width: 16px;
  height: 16px;
}

.btn-icon-toggle {
  position: relative;
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  color: var(--text-primary);
  width: 38px;
  height: 38px;
  border-radius: var(--radius-md);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
}

.btn-icon-toggle:hover {
  border-color: var(--color-cyan);
  color: var(--color-cyan);
}

.badge-count {
  position: absolute;
  top: -4px;
  right: -4px;
  background-color: var(--color-cyan);
  color: #030712;
  font-size: 0.65rem;
  font-weight: 800;
  width: 18px;
  height: 18px;
  border-radius: var(--radius-full);
  display: flex;
  align-items: center;
  justify-content: center;
}

/* ==========================================================================
   Main Layout & Panels
   ========================================================================== */

.main-layout {
  max-width: 1440px;
  margin: 0 auto;
  padding: 24px;
}

.tab-pane {
  display: none;
}

.tab-pane.active {
  display: block;
}

.panel {
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: 20px;
  box-shadow: var(--shadow-md);
}

.panel-header {
  margin-bottom: 16px;
}

.panel-header h2 {
  font-size: 1.15rem;
  font-weight: 700;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  margin-top: 4px;
}

.panel-tag {
  display: inline-block;
  font-size: 0.68rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text-secondary);
  background-color: var(--bg-card-elevated);
  padding: 2px 8px;
  border-radius: var(--radius-sm);
}

.tag-primary {
  color: var(--color-cyan);
  background-color: rgba(56, 189, 248, 0.1);
  border: 1px solid rgba(56, 189, 248, 0.2);
}

.tag-success {
  color: var(--color-emerald);
  background-color: rgba(16, 185, 129, 0.1);
  border: 1px solid rgba(16, 185, 129, 0.2);
}

.phone-top-controls {
  display: flex;
  gap: 8px;
}

/* ==========================================================================
   Feed Simulator Grid (3 Columns)
   ========================================================================== */

.feed-grid {
  display: grid;
  grid-template-columns: 380px 1fr 340px;
  gap: 20px;
  align-items: start;
}

@media (max-width: 1200px) {
  .feed-grid {
    grid-template-columns: 360px 1fr;
  }
  .right-column {
    grid-column: span 2;
  }
}

@media (max-width: 860px) {
  .feed-grid {
    grid-template-columns: 1fr;
  }
  .right-column {
    grid-column: span 1;
  }
}

/* ==========================================================================
   Phone Mockup Simulator
   ========================================================================== */

.phone-frame {
  background-color: #030712;
  border: 3px solid #1f2937;
  border-radius: 36px;
  padding: 12px;
  position: relative;
  box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.8);
}

.phone-speaker {
  width: 50px;
  height: 4px;
  background-color: #374151;
  border-radius: 2px;
  margin: 4px auto 10px;
}

.phone-screen {
  background-color: #0b0f19;
  border-radius: 24px;
  overflow: hidden;
  position: relative;
  height: 490px;
  border: 1px solid #1f2937;
}

.reel-media-viewport {
  width: 100%;
  height: 100%;
  position: relative;
  background-color: #020617;
}

#media-canvas {
  width: 100%;
  height: 100%;
  display: block;
}

.media-overlay-badge {
  position: absolute;
  top: 14px;
  left: 14px;
  background: rgba(15, 23, 42, 0.85);
  backdrop-filter: blur(8px);
  color: var(--color-cyan);
  font-size: 0.72rem;
  font-weight: 700;
  padding: 4px 10px;
  border-radius: var(--radius-full);
  border: 1px solid rgba(56, 189, 248, 0.3);
}

.play-indicator-pill {
  position: absolute;
  top: 14px;
  right: 14px;
  background: rgba(16, 185, 129, 0.85);
  color: #fff;
  font-size: 0.65rem;
  font-weight: 800;
  padding: 3px 8px;
  border-radius: var(--radius-full);
}

.screen-nav-btn {
  position: absolute;
  right: 14px;
  width: 28px;
  height: 28px;
  background: rgba(15, 23, 42, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.15);
  color: #fff;
  border-radius: var(--radius-full);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.7rem;
  transition: var(--transition);
  z-index: 10;
}

.prev-btn { top: 60px; }
.next-btn { top: 96px; }

.screen-nav-btn:hover {
  background: rgba(56, 189, 248, 0.4);
  transform: scale(1.1);
}

.reel-info-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 54px;
  padding: 16px 14px;
  background: linear-gradient(to top, rgba(3, 7, 18, 0.95) 0%, rgba(3, 7, 18, 0.7) 70%, transparent 100%);
  pointer-events: none;
}

.reel-creator-row {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 6px;
  pointer-events: auto;
}

.avatar-circle {
  width: 28px;
  height: 28px;
  border-radius: var(--radius-full);
  background-color: #0284c7;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.75rem;
  font-weight: 700;
}

.creator-handle {
  font-size: 0.82rem;
  font-weight: 700;
  color: #fff;
}

.creator-follow-btn {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-cyan);
  background: transparent;
  border: 1px solid rgba(56, 189, 248, 0.4);
  padding: 1px 8px;
  border-radius: var(--radius-sm);
  margin-left: 4px;
  cursor: pointer;
  transition: var(--transition);
}

.creator-follow-btn:hover {
  background: rgba(56, 189, 248, 0.2);
}

.creator-follow-btn.following {
  background: rgba(16, 185, 129, 0.2);
  color: var(--color-emerald);
  border-color: var(--color-emerald);
}

.reel-caption {
  font-size: 0.8rem;
  color: #f1f5f9;
  line-height: 1.35;
  margin-bottom: 6px;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.reel-tags-row {
  display: flex;
  flex-wrap: wrap;
  gap: 4px;
  margin-bottom: 6px;
}

.reel-pill {
  font-size: 0.68rem;
  color: var(--color-cyan);
  font-weight: 600;
}

.audio-ticker {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 0.7rem;
  color: var(--text-secondary);
}

/* Floating Actions on Phone */
.reel-actions-rail {
  position: absolute;
  right: 8px;
  bottom: 24px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: center;
}

.action-circle-btn {
  background: rgba(30, 41, 59, 0.7);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  width: 38px;
  height: 38px;
  border-radius: var(--radius-full);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #fff;
  cursor: pointer;
  transition: var(--transition);
}

.action-circle-btn:hover {
  background: rgba(56, 189, 248, 0.3);
  transform: scale(1.08);
}

.action-circle-btn.liked {
  color: var(--color-rose);
}

.action-circle-btn.saved {
  color: var(--color-amber);
}

.action-icon {
  width: 17px;
  height: 17px;
}

.action-count {
  font-size: 0.6rem;
  font-weight: 700;
  margin-top: 1px;
}

/* Phone Controls */
.phone-controls {
  margin-top: 14px;
  padding: 6px;
}

.control-row {
  display: flex;
  justify-content: space-between;
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-bottom: 4px;
}

.slider-val {
  color: var(--color-cyan);
  font-weight: 700;
  font-family: var(--font-mono);
}

.slider-input {
  width: 100%;
  accent-color: var(--color-cyan);
  cursor: pointer;
  margin-bottom: 12px;
}

.preset-reels-selector label {
  font-size: 0.75rem;
  font-weight: 700;
  color: var(--text-secondary);
  display: block;
}

.category-indicator {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-cyan);
}

.reel-thumbnails-bar {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 6px;
}

.thumb-item {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-sm);
  padding: 6px 4px;
  text-align: center;
  cursor: pointer;
  transition: var(--transition);
}

.thumb-item:hover {
  background-color: var(--bg-card-hover);
  border-color: var(--border-medium);
}

.thumb-item.active {
  border-color: var(--color-cyan);
  background-color: rgba(56, 189, 248, 0.12);
}

.thumb-num {
  font-size: 0.65rem;
  font-weight: 800;
  color: var(--text-muted);
}

.thumb-item.active .thumb-num {
  color: var(--color-cyan);
}

.thumb-label {
  font-size: 0.68rem;
  font-weight: 600;
  color: var(--text-primary);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

/* ==========================================================================
   Center Column & SPEC OUTPUT CARD (Problem Statement Compliance)
   ========================================================================== */

.flex-between {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.copy-actions {
  display: flex;
  gap: 6px;
}

.spec-output-card {
  background-color: #0b0f19;
  border: 1px solid #1e293b;
  border-left: 4px solid var(--color-cyan);
  border-radius: var(--radius-md);
  padding: 18px;
  font-family: var(--font-mono);
  box-shadow: inset 0 0 20px rgba(0,0,0,0.4);
  margin-bottom: 20px;
}

.spec-card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 14px;
  padding-bottom: 8px;
  border-bottom: 1px solid #1e293b;
}

.spec-badge {
  font-size: 0.72rem;
  font-weight: 800;
  color: var(--color-cyan);
  letter-spacing: 0.05em;
}

.spec-status-pill {
  font-size: 0.68rem;
  font-weight: 700;
  background-color: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
  padding: 2px 8px;
  border-radius: var(--radius-full);
}

.spec-field-group {
  margin-bottom: 12px;
}

.spec-label {
  font-size: 0.72rem;
  font-weight: 700;
  color: #64748b;
  letter-spacing: 0.04em;
  margin-bottom: 2px;
}

.spec-value {
  font-size: 0.88rem;
  line-height: 1.45;
  color: #e2e8f0;
}

.highlight-cyan {
  color: #38bdf8;
  font-weight: 600;
}

.highlight-amber {
  color: #fbbf24;
  font-weight: 600;
}

.highlight-emerald {
  color: #34d399;
  font-weight: 600;
}

.text-subtle {
  color: #94a3b8;
  font-family: var(--font-sans);
  font-size: 0.84rem;
}

.spec-divider {
  height: 1px;
  background: #1e293b;
  margin: 14px 0;
}

.spec-meta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  margin: 12px 0;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 6px;
}

.meta-pill {
  font-size: 0.72rem;
  font-weight: 700;
  padding: 2px 8px;
  border-radius: var(--radius-sm);
  background-color: #1e293b;
  color: #f1f5f9;
}

.category-pill {
  background-color: rgba(56, 189, 248, 0.15);
  color: var(--color-cyan);
  border: 1px solid rgba(56, 189, 248, 0.3);
}

.diff-pill {
  background-color: rgba(245, 158, 11, 0.15);
  color: var(--color-amber);
  border: 1px solid rgba(245, 158, 11, 0.3);
}

.conf-pill {
  background-color: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.rec-action-bar {
  margin-top: 14px;
  padding-top: 10px;
  border-top: 1px solid #1e293b;
}

.btn-preview-rec {
  width: 100%;
  background: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
  padding: 8px 14px;
  border-radius: var(--radius-sm);
  font-family: var(--font-sans);
  font-size: 0.82rem;
  font-weight: 700;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.btn-preview-rec:hover {
  background: rgba(16, 185, 129, 0.25);
  border-color: var(--color-emerald);
}

/* ==========================================================================
   Reasoning Pipeline Steps
   ========================================================================== */

.reasoning-pipeline {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 16px;
}

.section-title {
  font-size: 0.88rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: 12px;
}

.pipeline-steps {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.step-card {
  display: flex;
  gap: 12px;
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-sm);
  padding: 10px 12px;
  align-items: flex-start;
}

.step-num {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  color: var(--color-cyan);
  background: rgba(56, 189, 248, 0.1);
  padding: 2px 6px;
  border-radius: var(--radius-sm);
}

.step-body h4 {
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--text-primary);
}

.step-body p {
  font-size: 0.76rem;
  color: var(--text-secondary);
  margin-top: 2px;
}

.substance-score-tag {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-emerald);
}

/* ==========================================================================
   Right Column: Profile & Vector Radar
   ========================================================================== */

.profile-card {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 16px;
  margin-bottom: 16px;
}

.profile-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 14px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border-subtle);
}

.student-avatar {
  width: 36px;
  height: 36px;
  border-radius: var(--radius-full);
  background: linear-gradient(135deg, #10b981, #047857);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 0.85rem;
}

.student-info h4 {
  font-size: 0.85rem;
  font-weight: 700;
}

.student-info p {
  font-size: 0.74rem;
  color: var(--text-secondary);
}

.text-emerald {
  color: var(--color-emerald);
}

.vector-breakdown {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.vector-row {
  display: grid;
  grid-template-columns: 130px 1fr 34px;
  align-items: center;
  gap: 8px;
}

.vector-name {
  font-size: 0.74rem;
  color: var(--text-secondary);
  font-weight: 600;
}

.progress-track {
  height: 6px;
  background-color: var(--bg-card-elevated);
  border-radius: var(--radius-full);
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  border-radius: var(--radius-full);
  transition: width 0.4s ease;
}

.fill-java { background-color: #f59e0b; }
.fill-hld { background-color: #38bdf8; }
.fill-dsa { background-color: #10b981; }
.fill-hw { background-color: #a855f7; }
.fill-sec { background-color: #f43f5e; }
.fill-ai { background-color: #06b6d4; }

.vector-pct {
  font-size: 0.72rem;
  font-family: var(--font-mono);
  color: var(--text-muted);
  text-align: right;
}

.conversion-widget {
  background: linear-gradient(135deg, rgba(16, 185, 129, 0.08), rgba(56, 189, 248, 0.05));
  border: 1px solid rgba(16, 185, 129, 0.2);
  border-radius: var(--radius-md);
  padding: 14px;
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 16px;
}

.metric-circle {
  width: 58px;
  height: 58px;
  border-radius: var(--radius-full);
  background-color: rgba(16, 185, 129, 0.15);
  border: 2px solid var(--color-emerald);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.metric-val {
  font-size: 0.95rem;
  font-weight: 800;
  color: var(--color-emerald);
  line-height: 1;
}

.metric-lbl {
  font-size: 0.52rem;
  text-transform: uppercase;
  color: var(--text-secondary);
  font-weight: 700;
}

.metric-info h4 {
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--text-primary);
}

.metric-info p {
  font-size: 0.72rem;
  color: var(--text-secondary);
  margin-top: 2px;
}

.trap-shortcut-box {
  background-color: var(-
