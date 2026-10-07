@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

:root {
  --bg: #04070d;
  --panel: rgba(14, 18, 24, 0.96);
  --panel-2: rgba(18, 25, 33, 0.98);
  --border: rgba(255, 255, 255, 0.08);
  --text: #f4f6fb;
  --muted: #8d97a8;
  --green: #2dd4bf;
  --green-soft: rgba(45, 212, 191, 0.18);
  --red: #ff5a6c;
  --red-soft: rgba(255, 90, 108, 0.18);
  --orange: #fbbf24;
  --blue: #60a5fa;
  --purple: #b794f4;
  --grid: rgba(255, 255, 255, 0.07);
  --shadow: rgba(0, 0, 0, 0.35);
}

* {
  box-sizing: border-box;
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  height: 100%;
  background: radial-gradient(circle at top, #0d1320 0%, var(--bg) 55%);
  color: var(--text);
  font-family: 'Inter', sans-serif;
}

button {
  font: inherit;
}

.app-shell {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #02050a;
  padding: 20px;
}

.screen {
  width: min(100%, 900px);
  background: linear-gradient(180deg, #050910 0%, #090d14 100%);
  border: 1px solid var(--border);
  border-radius: 28px;
  box-shadow: 0 30px 80px rgba(0, 0, 0, 0.55);
  padding: 14px 16px 18px;
  overflow: hidden;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 8px 16px;
}

.time-block {
  display: flex;
  align-items: end;
  gap: 12px;
}

.time {
  font-size: clamp(2rem, 4vw, 2.8rem);
  font-weight: 700;
  letter-spacing: -0.04em;
}

.pair-name {
  font-size: 1rem;
  color: var(--muted);
  margin-bottom: 8px;
}

.status-group {
  display: flex;
  align-items: center;
  gap: 8px;
}

.badge {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 6px 9px;
  font-size: 0.72rem;
  color: var(--muted);
}

.badge.small {
  font-size: 0.61rem;
  padding: 5px 7px;
}

.icon-box {
  width: 36px;
  height: 36px;
  display: grid;
  place-items: center;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid var(--border);
  color: #fff;
}

.chart-card {
  background: rgba(9, 14, 20, 0.8);
  border: 1px solid var(--border);
  border-radius: 20px;
  overflow: hidden;
  padding: 10px 12px 8px;
}

.chart-header-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  padding: 6px 4px 12px;
}

.mode-buttons {
  display: flex;
  gap: 8px;
}

.mode-buttons button {
  border: 1px solid var(--border);
  background: rgba(255, 255, 255, 0.04);
  color: var(--muted);
  border-radius: 999px;
  padding: 6px 11px;
  cursor: pointer;
  transition: 0.2s ease;
}

.mode-buttons button.active {
  background: rgba(96, 165, 250, 0.12);
  color: white;
  border-color: rgba(96, 165, 250, 0.4);
}

.price-tag {
  color: #f9fafb;
  font-weight: 600;
  font-size: 1.05rem;
}

.chart-area {
  border-radius: 16px;
  background: linear-gradient(180deg, rgba(2, 6, 12, 0.95), rgba(6, 12, 17, 0.92));
  border: 1px solid rgba(255, 255, 255, 0.02);
  overflow: hidden;
}

.chart-svg {
  display: block;
  width: 100%;
  height: 440px;
  background: rgba(4, 8, 12, 0.95);
}

.grid-line {
  stroke: var(--grid);
  stroke-width: 1;
}

.price-label {
  fill: rgba(255, 255, 255, 0.72);
  font-size: 12px;
  font-weight: 500;
}

.zone-line {
  stroke-dasharray: 8 6;
  stroke-width: 1.2;
  opacity: 0.8;
}

.support-zone {
  stroke: var(--green);
}

.resistance-zone {
  stroke: var(--red);
}

.ema-line {
  fill: none;
  stroke: var(--orange);
  stroke-width: 2.5;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.candle {
  stroke-width: 1.4;
}

.candle.bull {
  fill: rgba(45, 212, 191, 0.92);
  stroke: rgba(45, 212, 191, 0.9);
}

.candle.bear {
  fill: rgba(255, 90, 108, 0.92);
  stroke: rgba(255, 90, 108, 0.9);
}

.wick-up {
  stroke: rgba(45, 212, 191, 0.9);
  stroke-width: 1.8;
}

.wick-down {
  stroke: rgba(255, 90, 108, 0.9);
  stroke-width: 1.8;
}

.signal-tag {
  font-size: 9px;
  font-weight: 800;
  letter-spacing: 0.04em;
  paint-order: stroke;
  stroke: rgba(0, 0, 0, 0.4);
  stroke-width: 2;
  dominant-baseline: middle;
}

.signal-tag.buy {
  fill: var(--green);
}

.signal-tag.sell {
  fill: var(--red);
}

.trend-line {
  fill: none;
  stroke: rgba(251, 191, 36, 0.9);
  stroke-width: 2.4;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.signal-dot {
  fill: rgba(255, 255, 255, 0.9);
  stroke: rgba(103, 232, 249, 1);
  stroke-width: 2;
}

.info-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 8px 4px;
}

.info-left {
  display: flex;
  align-items: center;
  gap: 10px;
}

.pair {
  font-size: 1.1rem;
  font-weight: 700;
}

.timeframe {
  color: var(--muted);
  font-size: 0.9rem;
}

.signal-state {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255,255,255,0.02);
  border: 1px solid var(--border);
  border-radius: 999px;
  padding: 7px 10px;
  font-weight: 600;
}

.pulse {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  display: inline-block;
  box-shadow: 0 0 0 rgba(0, 0, 0, 0);
}

.pulse.buy {
  background: var(--green);
  box-shadow: 0 0 12px rgba(45, 212, 191, 0.9);
}

.pulse.sell {
  background: var(--red);
  box-shadow: 0 0 12px rgba(255, 90, 108, 0.9);
}

.pulse.wait {
  background: var(--orange);
  box-shadow: 0 0 12px rgba(251, 191, 36, 0.9);
}

.bottom-panel {
  display: grid;
  grid-template-columns: 1.5fr 0.9fr;
  gap: 14px;
  margin-top: 16px;
}

.summary-card,
.controls-card {
  background: var(--panel-2);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 14px;
}

.summary-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 12px;
  font-weight: 600;
}

.tag {
  padding: 5px 9px;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
}

.tag.buy {
  background: var(--green-soft);
  color: var(--green);
}

.tag.sell {
  background: var(--red-soft);
  color: var(--red);
}

.tag.wait {
  background: rgba(251, 191, 36, 0.14);
  color: var(--orange);
}

.stat-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 10px;
}

.stat-grid > div,
.level-row > div {
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 10px 12px;
}

.stat-grid label,
.level-row label {
  color: var(--muted);
  display: block;
  font-size: 0.72rem;
  margin-bottom: 4px;
}

.stat-grid strong,
.level-row span {
  font-size: 0.96rem;
  font-weight: 700;
}

.level-row {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 10px;
  margin-top: 12px;
}

.controls-card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 12px;
}

.toggle-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  color: var(--muted);
}

.toggle {
  min-width: 70px;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.05);
  color: var(--text);
  border-radius: 999px;
  padding: 7px 10px;
  cursor: pointer;
}

.toggle.on {
  background: rgba(45, 212, 191, 0.12);
  color: var(--green);
  border-color: rgba(45, 212, 191, 0.5);
}

.refresh-button {
  border: 1px solid rgba(96, 165, 250, 0.4);
  background: rgba(96, 165, 250, 0.12);
  color: white;
  border-radius: 12px;
  padding: 11px 14px;
  cursor: pointer;
  font-weight: 600;
}

@media (max-width: 720px) {
  .screen {
    padding: 10px 10px 14px;
    border-radius: 18px;
  }

  .bottom-panel {
    grid-template-columns: 1fr;
  }

  .chart-svg {
    height: 360px;
  }

  .mode-buttons {
    flex-wrap: wrap;
  }
}
