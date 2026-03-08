:root{  
  --cellSize: 54px;  
  --paper1: #ead9b8;  
  --paper1: #ead9b8;  
  --paper2: #d9c39a;  
  --ink: rgba(20,16,10,0.85);  
  --line: rgba(20,16,10,0.40);  
  --line: rgba(20,16,10,0.40);  
  --shadow: rgba(0,0,0,0.16);  
}  
  
*{ box-sizing:border-box; }  
*{ box-sizing:border-box; }  
body{  
  margin:0;  
  margin:0;  
  font-family: system-ui, -apple-system, "Noto Sans TC", "PingFang TC", "Microsoft JhengHei", Arial, sans-serif;  
  font-family: system-ui, -apple-system, "Noto Sans TC", "PingFang TC", "Microsoft JhengHei", Arial, sans-serif;  
  background:#fafafa;  
  color:#222;  
  color:#222;  
}  
}  
h1,h2,h3{ margin:0 0 10px; }  
h1,h2,h3{ margin:0 0 10px; }  
p{ margin:8px 0; }  
p{ margin:8px 0; }  
  
.screen{ padding:18px; max-width:1180px; margin:0 auto; }  
.hidden{ display:none !important; }  
.hidden{ display:none !important; }  
  
.header{ text-align:center; margin:14px 0 18px; }  
.header{ text-align:center; margin:14px 0 18px; }  
.sub{ color:#666; margin-top:6px; }  
.sub{ color:#666; margin-top:6px; }  
  
.panel{  
  background:#fff;  
  border:1px solid #e8e8e8;  
  border-radius:14px;  
  padding:14px;  
  padding:14px;  
  margin:12px 0;  
  margin:12px 0;  
  box-shadow: 0 2px 12px var(--shadow);  
}  
}  
.row{ display:flex; gap:14px; align-items:center; flex-wrap:wrap; }  
.col{ display:flex; flex-direction:column; gap:8px; }  
.col{ display:flex; flex-direction:column; gap:8px; }  
.actions{ display:flex; gap:12px; justify-content:flex-end; }  
.hintText{ color:#666; font-size: 13px; }  
  
button{  
  border:1px solid #d6d6d6;  
  border:1px solid #d6d6d6;  
  background:#fff;  
  padding:10px 14px;  
  padding:10px 14px;  
  border-radius:12px;  
  cursor:pointer;  
  font-size:14px;  
}  
}  
button.primary{  
  background:#111;  
  color:#fff;  
  color:#fff;  
  border-color:#111;  
  border-color:#111;  
  font-weight:800;  
  font-weight:800;  
}  
}  
button.ghost{ background:#fff; }  
button.ghost{ background:#fff; }  
button:disabled{ opacity:0.55; cursor:not-allowed; }  
button:disabled{ opacity:0.55; cursor:not-allowed; }  
  
.footer .small{ font-size:12px; color:#666; }  
.footer .small{ font-size:12px; color:#666; }  
  
/* Game top */  
.gameTop{  
.gameTop{  
  position:sticky;  
  position:sticky;  
  top:0;  
  z-index:5;  
  z-index:5;  
  background:#fafafa;  
  padding:12px 0;  
  display:flex;  
  display:flex;  
  align-items:center;  
  align-items:center;  
  justify-content:space-between;  
  justify-content:space-between;  
  gap:12px;  
}  
.statusLine{ font-weight:900; }  
.statusLine{ font-weight:900; }  
.subStatusLine{ font-size:13px; color:#444; margin-top:4px; min-height:18px; }  
  
.checkWin{  
.checkWin{  
  background:#b30000;  
  color:#fff;  
  color:#fff;  
  border-color:#b30000;  
  border-color:#b30000;  
  font-weight:900;  
  font-weight:900;  
}  
}  
.checkWin.flash{ animation: flash 0.8s infinite; }  
.checkWin.flash{ animation: flash 0.8s infinite; }  
@keyframes flash{ 0%{transform:scale(1)} 50%{transform:scale(1.04)} 100%{transform:scale(1)} }  
  
.gameMain{  
  display:grid;  
  grid-template-columns: 1fr 340px;  
  grid-template-columns: 1fr 340px;  
  gap:16px;  
  align-items:start;  
  align-items:start;  
}  
}  
@media (max-width: 980px){  
  .gameMain{ grid-template-columns: 1fr; }  
  .gameMain{ grid-template-columns: 1fr; }  
}  
}  
  
.boardWrap{  
  background:#fff;  
  background:#fff;  
  border:1px solid #e8e8e8;  
  border-radius:16px;  
  border-radius:16px;  
  padding:14px;  
  padding:14px;  
  box-shadow: 0 2px 12px var(--shadow);  
}  
}  
  
/* Vintage board */  
.board.vintage{  
  --cols: 9;  
  --cols: 9;  
  --rows: 10;  
  position:relative;  
  display:grid;  
  grid-template-columns: repeat(var(--cols), var(--cellSize));  
  grid-template-rows: repeat(var(--rows), var(--cellSize));  
  border-radius:14px;  
  overflow:hidden;  
  background:  
  background:  
    radial-gradient(1200px 800px at 40% 10%, rgba(255,255,255,0.25), transparent 60%),  
    radial-gradient(900px 700px at 85% 80%, rgba(0,0,0,0.06), transparent 55%),  
    linear-gradient(135deg, var(--paper1), var(--paper2));  
    linear-gradient(135deg, var(--paper1), var(--paper2));  
  border: 2px solid rgba(20,16,10,0.75);  
  border: 2px solid rgba(20,16,10,0.75);  
  box-shadow:  
    inset 0 0 0 6px rgba(20,16,10,0.12),  
    inset 0 0 0 10px rgba(255,255,255,0.14);  
}  
}  
.board.vintage::before{  
.board.vintage::before{  
  content:"";  
  content:"";  
  position:absolute;  
  position:absolute;  
  inset: 10px;  
  border:1px solid rgba(20,16,10,0.55);  
  border-radius:10px;  
  pointer-events:none;  
  pointer-events:none;  
}  
.board.vintage::after{  
  content:"";  
  position:absolute;  
  inset: 16px;  
  inset: 16px;  
  border:1px solid rgba(20,16,10,0.25);  
  border:1px solid rgba(20,16,10,0.25);  
  border-radius:8px;  
  border-radius:8px;  
  pointer-events:none;  
}  
}  
  
/* ChuHe HanJie band: thin overlay BETWEEN rows (non-interactive, not a cell) */  
.riverBand{  
.riverBand{  
  position:absolute;  
  position:absolute;  
  left:0; right:0;  
  top: calc(var(--cellSize) * 5 - 16px);  
  top: calc(var(--cellSize) * 5 - 16px);  
  height: 32px;  
  height: 32px;  
  display:flex;  
  display:flex;  
  align-items:center;  
  align-items:center;  
  justify-content:center;  
  pointer-events:none;  
}  
}  
.riverBand .bandSplit{  
.riverBand .bandSplit{  
  position:absolute;  
  position:absolute;  
  inset:0;  
  inset:0;  
  background: rgba(255,255,255,0.18);  
  border-top:1px solid rgba(20,16,10,0.22);  
  border-bottom:1px solid rgba(20,16,10,0.22);  
  border-bottom:1px solid rgba(20,16,10,0.22);  
}  
.riverBand .riverText{  
.riverBand .riverText{  
  display:flex;  
  gap:22px;  
  gap:22px;  
  font-weight:900;  
  letter-spacing: 8px;  
  letter-spacing: 8px;  
  color: rgba(20,16,10,0.85);  
  color: rgba(20,16,10,0.85);  
  font-size: 18px;  
  font-size: 18px;  
  filter: drop-shadow(0 1px 0 rgba(255,255,255,0.35));  
  filter: drop-shadow(0 1px 0 rgba(255,255,255,0.35));  
}  
}  
  
/* Dark chess title strip */  
.darkBand{  
.darkBand{  
  position:absolute;  
  position:absolute;  
  left:0; right:0;  
  top: 10px;  
  top: 10px;  
  height: 34px;  
  height: 34px;  
  display:flex;  
  align-items:center;  
  justify-content:center;  
  pointer-events:none;  
  pointer-events:none;  
}  
}  
.darkBand .darkTitle{  
.darkBand .darkTitle{  
  font-weight:900;  
  font-weight:900;  
  letter-spacing: 10px;  
  color: rgba(20,16,10,0.85);  
  color: rgba(20,16,10,0.85);  
  font-size: 16px;  
  font-size: 16px;  
  padding: 6px 14px;  
  padding: 6px 14px;  
  border:1px solid rgba(20,16,10,0.35);  
  border:1px solid rgba(20,16,10,0.35);  
  border-radius: 999px;  
  background: rgba(255,255,255,0.12);  
}  
}  
  
/* Cells */  
/* Cells */  
.cell{  
  width: var(--cellSize);  
  width: var(--cellSize);  
  height: var(--cellSize);  
  height: var(--cellSize);  
  display:flex;  
  display:flex;  
  align-items:center;  
  justify-content:center;  
  justify-content:center;  
  position:relative;  
  user-select:none;  
  user-select:none;  
  border-right: 1px solid var(--line);  
  border-right: 1px solid var(--line);  
  border-bottom: 1px solid var(--line);  
}  
}  
.cell.edgeR{ border-right:none; }  
.cell.edgeB{ border-bottom:none; }  
.cell.edgeB{ border-bottom:none; }  
  
/* subtle L ornaments */  
.cell::before{  
.cell::before{  
  content:"";  
  position:absolute;  
  inset: 8px;  
  inset: 8px;  
  border: 1px solid transparent;  
  border: 1px solid transparent;  
  pointer-events:none;  
  pointer-events:none;  
}  
}  
.cell.cornerMark::before{  
  border-color: rgba(20,16,10,0.18);  
  border-color: rgba(20,16,10,0.18);  
  clip-path: polygon(0 0, 14px 0, 14px 2px, 2px 2px, 2px 14px, 0 14px);  
}  
}  
  
/* selection and hints */  
.cell.selected{ outline:3px solid rgba(0,0,0,0.35); z-index:2; }  
.cell.selected{ outline:3px solid rgba(0,0,0,0.35); z-index:2; }  
.hintMove{ background: rgba(40,140,255,0.14); }  
.hintCapture{ background: rgba(255,120,40,0.16); }  
.danger{ box-shadow: inset 0 0 0 4px rgba(255,0,0,0.12); }  
.danger{ box-shadow: inset 0 0 0 4px rgba(255,0,0,0.12); }  
  
/* CPU last move */  
.cpuFrom{ box-shadow: inset 0 0 0 4px rgba(20,120,255,0.22); }  
.cpuFrom{ box-shadow: inset 0 0 0 4px rgba(20,120,255,0.22); }  
.cpuTo{ box-shadow: inset 0 0 0 4px rgba(20,120,255,0.32); }  
.cpuTo{ box-shadow: inset 0 0 0 4px rgba(20,120,255,0.32); }  
.cpuFlash{ animation: cpuFlash 0.45s ease-in-out 1; }  
.cpuFlash{ animation: cpuFlash 0.45s ease-in-out 1; }  
@keyframes cpuFlash{  
  0%{ filter: brightness(1); }  
  50%{ filter: brightness(1.18); }  
  100%{ filter: brightness(1); }  
  100%{ filter: brightness(1); }  
}  
}  
  
/* Pieces 3D */  
.piece{  
.piece{  
  width:44px;  
  width:44px;  
  height:44px;  
  height:44px;  
  border-radius:999px;  
  border-radius:999px;  
  display:flex;  
  display:flex;  
  align-items:center;  
  align-items:center;  
  justify-content:center;  
  font-weight:900;  
  font-size: 20px;  
  font-size: 20px;  
  letter-spacing: 1px;  
  
  border: 2px solid rgba(20,16,10,0.65);  
  box-shadow:  
    0 6px 10px rgba(0,0,0,0.18),  
    0 6px 10px rgba(0,0,0,0.18),  
    inset 0 2px 2px rgba(255,255,255,0.35),  
    inset 0 -6px 10px rgba(0,0,0,0.10);  
    inset 0 -6px 10px rgba(0,0,0,0.10);  
  background:  
    radial-gradient(circle at 30% 25%, rgba(255,255,255,0.9), rgba(255,255,255,0.22) 45%, rgba(0,0,0,0.06) 70%),  
    radial-gradient(circle at 30% 25%, rgba(255,255,255,0.9), rgba(255,255,255,0.22) 45%, rgba(0,0,0,0.06) 70%),  
    linear-gradient(180deg, rgba(255,255,255,0.18), rgba(0,0,0,0.04));  
}  
}  
.piece.red{ color:#b30000; }  
.piece.black{ color:#111; }  
  
/* Back side: NO SYMBOL / NO TEXT (only color + shading) */  
/* Back side: NO SYMBOL / NO TEXT (only color + shading) */  
.piece.back{  
.piece.back{  
  background:  
    radial-gradient(circle at 30% 25%, rgba(255,255,255,0.55), rgba(255,255,255,0.10) 55%, rgba(0,0,0,0.12)),  
    linear-gradient(180deg, rgba(0,0,0,0.06), rgba(0,0,0,0.16));  
}  
}  
  
/* Flip */  
/* Flip */  
.flipWrap{ width:44px; height:44px; position:relative; transform-style:preserve-3d; }  
.flipInner{  
.flipInner{  
  width:44px; height:44px; position:absolute; inset:0;  
  transform-style: preserve-3d;  
  transition: transform 420ms ease;  
}  
}  
.flipInner.flipped{ transform: rotateY(180deg); }  
.flipFace{ position:absolute; inset:0; backface-visibility:hidden; }  
.flipFace{ position:absolute; inset:0; backface-visibility:hidden; }  
.flipFace.front{ transform: rotateY(180deg); }  
  
/* Capture fade */  
.fadeOut{ animation: fadeOut 260ms ease forwards; }  
.fadeOut{ animation: fadeOut 260ms ease forwards; }  
@keyframes fadeOut{ to{ opacity:0; transform: scale(0.82); } }  
  
/* Moving clone */  
.flying{  
.flying{  
  position:fixed;  
  z-index:9999;  
  z-index:9999;  
  pointer-events:none;  
  pointer-events:none;  
  will-change: transform;  
  will-change: transform;  
}  
}  
  
/* Side panel */  
/* Side panel */  
.sidePanel .history{  
.sidePanel .history{  
  font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace;  
  font-size: 12px;  
  font-size: 12px;  
  white-space: pre-wrap;  
  max-height: 360px;  
  overflow:auto;  
  overflow:auto;  
  padding: 10px;  
  padding: 10px;  
  background:#fbfbfb;  
  background:#fbfbfb;  
  border:1px solid #eee;  
  border:1px solid #eee;  
  border-radius:12px;  
}  
}  
.sidePanel .toggle{ display:flex; gap:8px; align-items:center; }  
.sidePanel .toggle{ display:flex; gap:8px; align-items:center; }  
.small{ font-size:12px; color:#444; }  
.small{ font-size:12px; color:#444; }  
  
/* Modal */  
/* Modal */  
.modalOverlay{  
  position:fixed; inset:0;  
  background: rgba(0,0,0,0.42);  
  display:flex; align-items:center; justify-content:center;  
  padding:18px; z-index:50;  
  padding:18px; z-index:50;  
}  
}  
.modal{  
  width:min(760px, 96vw);  
  background:#fff;  
  background:#fff;  
  border-radius:16px;  
  overflow:hidden;  
  overflow:hidden;  
  box-shadow: 0 16px 44px rgba(0,0,0,0.25);  
  box-shadow: 0 16px 44px rgba(0,0,0,0.25);  
}  
.modalHeader{ padding:14px 16px; border-bottom:1px solid #eee; background:#fafafa; }  
.modalHeader{ padding:14px 16px; border-bottom:1px solid #eee; background:#fafafa; }  
.modalTitle{ font-weight:900; }  
.modalTitle{ font-weight:900; }  
.modalBody{ padding:14px 16px; line-height:1.7; color:#222; }  
.modalActions{  
  padding:14px 16px;  
  padding:14px 16px;  
  border-top:1px solid #eee;  
  display:flex; gap:10px;  
  justify-content:flex-end; flex-wrap:wrap;  
  justify-content:flex-end; flex-wrap:wrap;  
}  
}  
.modalActions button{ min-width: 120px; }  
.modalActions button{ min-width: 120px; }  
  
/* Dice UI */  
/* Dice UI */  
.diceBox{ display:grid; gap:10px; margin-top:10px; }  
.diceBox{ display:grid; gap:10px; margin-top:10px; }  
.diceRow{  
.diceRow{  
  display:flex; align-items:center; justify-content:space-between;  
  gap:12px; padding:10px 12px;  
  gap:12px; padding:10px 12px;  
  border:1px solid #eee; border-radius:12px; background:#fcfcfc;  
  border:1px solid #eee; border-radius:12px; background:#fcfcfc;  
}  
}  
.diceLabel{ font-weight:900; }  
.diceLabel{ font-weight:900; }  
.diceValue{  
  width: 60px; height: 44px;  
  border-radius:12px; border:2px solid #333;  
  border-radius:12px; border:2px solid #333;  
  display:flex; align-items:center; justify-content:center;  
  font-size:24px; background:#fff;  
}  
.diceValue.red{ border-color:#b30000; color:#b30000; }  
.diceValue.red{ border-color:#b30000; color:#b30000; }  
.diceValue.black{ border-color:#111; color:#111; }  
.diceValue.black{ border-color:#111; color:#111; }  
