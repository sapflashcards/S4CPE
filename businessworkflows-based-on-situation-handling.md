```mermaid
<svg viewBox="0 0 800 600" xmlns="http://www.w3.org/2000/svg">
  <!-- Background -->
  <rect width="800" height="600" fill="#f5f5f5"/>
  
  <!-- Main Platform -->
  <rect x="50" y="50" width="700" height="500" rx="10" ry="10" fill="#e6e6e6" stroke="#333" stroke-width="2"/>
  <text x="400" y="30" font-family="Arial" font-size="24" text-anchor="middle" font-weight="bold">SAP S/4HANA Cloud Architecture</text>
  
  <!-- SAP Business Technology Platform -->
  <rect x="100" y="420" width="600" height="100" rx="5" ry="5" fill="#0066cc" stroke="#333" stroke-width="2"/>
  <text x="400" y="475" font-family="Arial" font-size="18" text-anchor="middle" fill="white">SAP Business Technology Platform</text>
  
  <!-- Intelligent Situation Automation -->
  <rect x="130" y="440" width="250" height="60" rx="5" ry="5" fill="#4285F4" stroke="#333" stroke-width="1"/>
  <text x="255" y="475" font-family="Arial" font-size="14" text-anchor="middle" fill="white">Intelligent Situation Automation</text>
  
  <!-- SAP Build Process Automation -->
  <rect x="420" y="440" width="250" height="60" rx="5" ry="5" fill="#4285F4" stroke="#333" stroke-width="1"/>
  <text x="545" y="475" font-family="Arial" font-size="14" text-anchor="middle" fill="white">SAP Build Process Automation</text>
  
  <!-- SAP S/4HANA Cloud -->
  <rect x="100" y="100" width="600" height="300" rx="5" ry="5" fill="#f0f0f0" stroke="#333" stroke-width="2"/>
  <text x="400" y="125" font-family="Arial" font-size="18" text-anchor="middle">SAP S/4HANA Cloud</text>
  
  <!-- Responsibility Management -->
  <rect x="130" y="150" width="250" height="100" rx="5" ry="5" fill="#34A853" stroke="#333" stroke-width="1"/>
  <text x="255" y="175" font-family="Arial" font-size="16" text-anchor="middle" fill="white">Responsibility Management (1NJ)</text>
  
  <!-- Responsibility Management Components -->
  <rect x="150" y="190" width="70" height="40" rx="5" ry="5" fill="#81C995" stroke="#333" stroke-width="1"/>
  <text x="185" y="215" font-family="Arial" font-size="12" text-anchor="middle">Teams</text>
  
  <rect x="230" y="190" width="70" height="40" rx="5" ry="5" fill="#81C995" stroke="#333" stroke-width="1"/>
  <text x="265" y="215" font-family="Arial" font-size="12" text-anchor="middle">Functions</text>
  
  <rect x="310" y="190" width="50" height="40" rx="5" ry="5" fill="#81C995" stroke="#333" stroke-width="1"/>
  <text x="335" y="215" font-family="Arial" font-size="12" text-anchor="middle">Tasks</text>
  
  <!-- Situation Handling -->
  <rect x="420" y="150" width="250" height="100" rx="5" ry="5" fill="#EA4335" stroke="#333" stroke-width="1"/>
  <text x="545" y="175" font-family="Arial" font-size="16" text-anchor="middle" fill="white">Situation Handling (31N)</text>
  
  <!-- Situation Handling Components -->
  <rect x="440" y="190" width="100" height="40" rx="5" ry="5" fill="#F28B82" stroke="#333" stroke-width="1"/>
  <text x="490" y="215" font-family="Arial" font-size="12" text-anchor="middle">Standard Framework</text>
  
  <rect x="550" y="190" width="100" height="40" rx="5" ry="5" fill="#F28B82" stroke="#333" stroke-width="1"/>
  <text x="600" y="215" font-family="Arial" font-size="12" text-anchor="middle">Extended Framework</text>
  
  <!-- Flexible Business Workflows -->
  <rect x="130" y="270" width="540" height="100" rx="5" ry="5" fill="#FBBC05" stroke="#333" stroke-width="1"/>
  <text x="400" y="295" font-family="Arial" font-size="16" text-anchor="middle">Flexible Business Workflows</text>
  
  <!-- Workflow Components -->
  <rect x="150" y="310" width="230" height="40" rx="5" ry="5" fill="#FDE293" stroke="#333" stroke-width="1"/>
  <text x="265" y="335" font-family="Arial" font-size="12" text-anchor="middle">SAP Business Workflow</text>
  
  <rect x="420" y="310" width="230" height="40" rx="5" ry="5" fill="#FDE293" stroke="#333" stroke-width="1"/>
  <text x="535" y="335" font-family="Arial" font-size="12" text-anchor="middle">Custom Workflow Templates</text>
  
  <!-- Connecting Lines -->
  <!-- Responsibility to Situation -->
  <path d="M380 200 L420 200" stroke="#333" stroke-width="2"/>
  
  <!-- Both to Workflows -->
  <path d="M255 250 L255 270" stroke="#333" stroke-width="2"/>
  <path d="M545 250 L545 270" stroke="#333" stroke-width="2"/>
  
  <!-- To BTP -->
  <path d="M400 370 L400 420" stroke="#333" stroke-width="2"/>
  
  <!-- Add Icons -->
  <!-- Team Icon -->
  <circle cx="185" y="170" r="5" fill="#333"/>
  <circle cx="178" y="170" r="5" fill="#333"/>
  <circle cx="192" y="170" r="5" fill="#333"/>
  
  <!-- Alert Icon -->
  <polygon points="545,160 535,170 555,170" fill="#333"/>
  <rect x="540" y="170" width="10" height="10" fill="#333"/>
  
  <!-- Workflow Icon -->
  <polyline points="390,285 400,275 410,285 420,275 430,285" stroke="#333" stroke-width="2" fill="none"/>
  
  <!-- Legend -->
  <rect x="600" y="80" width="20" height="10" fill="#34A853"/>
  <text x="625" y="90" font-family="Arial" font-size="12" text-anchor="start">Responsibility Management</text>
  
  <rect x="600" y="100" width="20" height="10" fill="#EA4335"/>
  <text x="625" y="110" font-family="Arial" font-size="12" text-anchor="start">Situation Handling</text>
  
  <rect x="600" y="120" width="20" height="10" fill="#FBBC05"/>
  <text x="625" y="130" font-family="Arial" font-size="12" text-anchor="start">Business Workflows</text>
  
  <rect x="600" y="140" width="20" height="10" fill="#4285F4"/>
  <text x="625" y="150" font-family="Arial" font-size="12" text-anchor="start">SAP BTP Services</text>
</svg>
```
