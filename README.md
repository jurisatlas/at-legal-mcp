# Austria Legal Research MCP Server (`at-legal-mcp`)

**[Deutsch](#lang-de) | [English Documentation](#english-documentation)**

---

<a id="lang-de"></a>
## Rechts- und Rechtsprechungs-MCP-Server (`at-legal-mcp`) — Deutsch

### Über dieses Repository

Dieses Repository stellt einen Model Context Protocol (MCP) Server bereit, der Ihre KI-Anwendung (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline, Continue.dev oder Antigravity) direkt mit den amtlichen Gesetzesportalen und den mehrstufigen Rechtsprechungsdatenbanken für **Austria** (1. Instanz, Berufungs-/Kantons-/Oberlandesgerichte sowie Höchst- und Verfassungsgerichte) verbindet.

### Installation (Auswahl Ihrer KI-Anwendung)

1. **Herunterladen:** Klicken Sie oben rechts auf **`<> Code` -> `Download ZIP`** und entpacken Sie das Archiv auf Ihrem Computer.
2. **Installationsassistent starten:** Doppelklicken Sie auf **`Click_Here_To_Install_Windows.bat`** (Windows) oder **`Click_Here_To_Install_Mac.command`** (macOS).
3. **KI-Programm auswählen:** Wählen Sie im Fenster die von Ihnen genutzten KI-Programme aus (Claude, Cursor, Windsurf, VS Code, Antigravity), klicken Sie auf Installieren und starten Sie Ihre KI-Anwendung neu.

**Sicherheitshinweis:** Das Installationsprogramm arbeitet vollständig im Nur-Lese-Modus (Read-Only) und greift auf keinerlei persönliche Dateien auf Ihrem System zu.

### Gerichtsinstanzen und amtliche Datenquellen

| Instanz | Abgedeckte Gerichte |
|:---|:---|
| **1. Instanz (Eingangsgerichte)** | Bezirksgerichte (BG), Landesgerichte (LG), Handelsgericht Wien & Arbeits- und Sozialgericht Wien |
| **2. Instanz (Kantons-, Ober- und Berufungsgerichte)** | 4 Oberlandesgerichte (OLG Wien, Graz, Linz, Innsbruck), 9 Landesverwaltungsgerichte (LVwG), Bundesverwaltungsgericht (BVwG) & Bundesfinanzgericht (BFG) |
| **3. Instanz (Höchst- und Verfassungsgerichte)** | Oberster Gerichtshof (OGH), Verfassungsgerichtshof (VfGH) & Verwaltungsgerichtshof (VwGH) |

- **RIS Open Government Data API (data.bka.gv.at - Bundesrecht & Landesrecht):** [https://www.ris.bka.gv.at](https://www.ris.bka.gv.at) (`ris.bka.gv.at`, `parlament.gv.at`)
- **RIS BKA Judikatur API v2.6 (Justiz, VfGH, VwGH, BVwG, LVwG, BFG — data.bka.gv.at):** [https://www.ris.bka.gv.at/Judikatur](https://www.ris.bka.gv.at/Judikatur) (`ris.bka.gv.at`, `ogh.gv.at`, `vfgh.gv.at`, `vwgh.gv.at`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Austria (AT)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Austria**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Bezirksgerichte (BG), Landesgerichte (LG), Handelsgericht Wien & Arbeits- und Sozialgericht Wien |
| **Tier 2 — Regional / Cantonal / Appellate** | 4 Oberlandesgerichte (OLG Wien, Graz, Linz, Innsbruck), 9 Landesverwaltungsgerichte (LVwG), Bundesverwaltungsgericht (BVwG) & Bundesfinanzgericht (BFG) |
| **Tier 3 — Supreme & Constitutional** | Oberster Gerichtshof (OGH), Verfassungsgerichtshof (VfGH) & Verwaltungsgerichtshof (VwGH) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** RIS Open Government Data API (data.bka.gv.at - Bundesrecht & Landesrecht) — [https://www.ris.bka.gv.at](https://www.ris.bka.gv.at)
  - *Indexed Legislation Domains:* `ris.bka.gv.at`, `parlament.gv.at`
- **Court Decisions & Jurisprudence Archives:** RIS BKA Judikatur API v2.6 (Justiz, VfGH, VwGH, BVwG, LVwG, BFG — data.bka.gv.at) — [https://www.ris.bka.gv.at/Judikatur](https://www.ris.bka.gv.at/Judikatur)
  - *Indexed Judicial & Open Case Law Domains:* `ris.bka.gv.at`, `ogh.gv.at`, `vfgh.gv.at`, `vwgh.gv.at`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Austria. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Austria. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Austria. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "at-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/at-legal-mcp/archive/refs/heads/main.zip",
        "at-legal-mcp"
      ]
    }
  }
}
```
</details>
