# Mobile Article Capture → Organized Vault → Future RAG Pipeline

## 1. Capture Stage (iPhone)
**Trigger:** You find an article worth saving (e.g., on MarkTechPost).

**Action:**
1. **Print to PDF** on iPhone (`Share → Print → Pinch Out`).
2. **Share → Save to Files** → navigate to:
- Working Copy → article-vault → pdf_inbox
3. **Commit & Push** in Working Copy to send it to GitHub.

**Why this works:**
- Keeps your current habit of printing to PDF.
- The PDF lands in a structured, synced folder (`pdf_inbox`).
- Every capture is versioned in GitHub.

---

## 2. Sync Stage
**What happens:** The pushed commit goes to your private GitHub repo.

**On Desktop:**
- Run `git pull` to update your local vault with new PDFs.
- Your `/pdf_inbox` now contains everything captured from mobile.

---

## 3. Organization Stage (Desktop/Laptop)
- Review new files in `/pdf_inbox`.
- Optional quick metadata tagging:
- Rename files to:
 ```
 YYYY-MM-DD - source - title.pdf
 ```
- Add an entry in `articles_index.md` with link & quick notes.
- Move processed PDFs into `/pdf_archive` or project-specific folder.

---

## 4. Processing Stage (Later RAG Pipeline)
When ready to process:
1. **OCR** the PDF if needed (for scanned docs).
2. **Extract text** into Markdown.
3. **Chunk** the text for embedding.
4. **Add** embeddings to your local vector database.

**Outcome:** Your RAG tool (Obsidian plugin or custom script) can search and retrieve content from this knowledge base.

---

## 5. Retrieval Stage (Future Use)
From Obsidian or your RAG interface:
- Ask context-aware questions.
- Get citations linking back to the original PDF in your vault.
- Build project notes directly connected to source material.

---

## Pipeline Diagram

iPhone → Print to PDF → Save to pdf_inbox in Working Copy → Commit & Push
↓
GitHub Repo → Pull on Desktop/Laptop → Local Vault Updated
↓
Review & Organize → Rename/Tag/Index
↓
(When Ready) Process into RAG System → OCR → Extract → Embed
↓
Ask Questions / Retrieve / Build Projects
