---
description: Validiert am 19.09.2024 • Zuletzt bearbeitet am 18.09.2024
---

# Schwachstellen - CVSS

Die Sicherheit in der IT-Infrastruktur ist für centron von höchster Priorität, insbesondere im Kontext unserer Cloud-Lösung **ccloud³**. Um Schwachstellen effizient und einheitlich zu bewerten, verwenden wir das **Common Vulnerability Scoring System (CVSS)**, das von der **Forum of Incident Response and Security Teams (FIRST)** entwickelt wurde. Dieses Framework ermöglicht es uns, potenzielle Sicherheitslücken präzise zu bewerten und geeignete Gegenmaßnahmen zu priorisieren.

{% embed url="https://www.first.org/cvss/" %}

### **Warum CVSS für die ccloud³ von Bedeutung ist**

1. **Standardisierte Bewertung der Sicherheit**\
   Durch die Implementierung von CVSS in die Sicherheitsstrategie der ccloud³ können wir Schwachstellen systematisch und konsistent bewerten. Dies sorgt für eine transparente Kommunikation zwischen den IT-Teams von centron und unseren Kunden.
2. **Klar definierte Risikopriorisierung**\
   CVSS unterstützt centron dabei, die Schwere einer Sicherheitslücke genau einzuschätzen und anhand der Bewertung Prioritäten für Maßnahmen zu setzen. Diese Bewertungslogik fließt in unsere ccloud³-Sicherheitsprozesse ein, um sicherzustellen, dass die gravierendsten Schwachstellen sofort adressiert werden.
3. **Verbesserung der Sicherheitsstrategie**\
   Die ccloud³ ist darauf ausgelegt, höchstmögliche Sicherheitsstandards zu gewährleisten. CVSS ermöglicht uns, die Effektivität von Sicherheitsmaßnahmen zu überwachen und kontinuierlich zu verbessern. Dies trägt dazu bei, die Datenintegrität und den Schutz der sensiblen Daten unserer Kunden zu gewährleisten.

### **Wie CVSS in der ccloud³ angewendet wird**

#### **1. Schwachstellenbewertung**

In der ccloud³ wird jede entdeckte Sicherheitslücke anhand des CVSS-Frameworks bewertet. Diese Bewertung umfasst drei Kernkomponenten:

* **Basiswert:** Dieser bestimmt den Schweregrad der Schwachstelle selbst.
* **Zeitlicher Wert:** Berücksichtigt, wie sich die Bedrohung im Laufe der Zeit entwickelt.
* **Umgebungswert:** Bestimmt, wie stark die Schwachstelle auf die spezifische Umgebung der ccloud³ und unserer Kunden wirkt.

#### **2. Priorisierung und Maßnahmen**

Nach der CVSS-Bewertung leiten wir Maßnahmen zur Schwachstellenbehebung ein. Hierbei wird anhand des CVSS-Scores entschieden, wie dringend die Schwachstelle adressiert werden muss:

* **Hochkritische Schwachstellen** (CVSS Score 9.0-10.0) erhalten höchste Priorität.
* **Mittel bis kritische Schwachstellen** (CVSS Score 4.0-8.9) werden ebenfalls zeitnah bearbeitet, jedoch nach Dringlichkeit gestaffelt.
* **Niedrige Risiken** (CVSS Score 0.1-3.9) werden beobachtet und bei Bedarf in zukünftigen Updates behoben.

Durch die Integration des CVSS in die Sicherheitsprozesse der **centron ccloud³** gewährleisten wir, dass Schwachstellen nicht nur entdeckt, sondern auch objektiv und priorisiert bewertet werden. Dies ermöglicht es centron, unseren Kunden eine zuverlässige und hochsichere Cloud-Plattform bereitzustellen, die den aktuellen Bedrohungen in der IT-Welt standhält.

