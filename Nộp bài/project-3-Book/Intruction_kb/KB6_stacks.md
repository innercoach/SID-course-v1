# KB6_stacks — Phase Prompts

> Load the section matching the current phase (from KB2). Each phase: IN ->
> OUT -> output format. All output in Vietnamese, following the KB2 4-layer
> frame. Apply KB4 gate before showing sensitive OUTLINE/DRILL/DRAFT.

---

## FRAME-BOOK
IN: raw topic (+ clarifying answers). OUT: 2-3 concepts, each with 5 fields.
```
Concept [n] — "[Title]" ([subtitle if any])
  • Doc gia: [who, situation]
  • Doc xong: [what they can do/understand]
  • Trong pham vi: [...]  |  Ngoai: [...]
  • Tone: [...]
Buoc tiep: chon 1/2/3 · yeu cau chinh
```

---

## EXPLORE-FACETS
Runs after FRAME-BOOK, before the TOC. IN: chosen concept. OUT: facet map +
priority branches + easily-missed. Do NOT write the TOC here.
```
Facet map — [title]
  • Nguoi doc: [...]   • Giao duc: [...]
  • Dao duc-an toan: [...]   • Mien lan can: [...]
Uu tien dua vao sach: [3-5 branches]
De bo sot: [1-2 branches] — nen can nhac.
Buoc tiep: dung muc luc · them/bo nhanh …
```

---

## ARCHITECT-TOC  (HUB)
IN: concept + priority branches. OUT: 5-8 chapters + 1-2 sentence role each.
Flow: foundation -> problems -> tools -> application -> synthesis. Enforce
MECE (no big overlap, no missing pillar).
```
Muc luc — [title]
  Chuong 1. [Ten] — [1-2 cau vai tro]
  ... (5-8 chuong)
Buoc tiep: chuong [X] · chinh muc luc
```

---

## OUTLINE-CHAPTER
IN: one chapter + ledger. OUT: 3-5 sections + 200-300 word summary, following
the Chapter Arc (KB5). Run KB4 gate if sensitive.
```
Chuong X. [Ten]
  Cac phan:
    X.1 [Ten] — [1 dong vai tro]  ... (3-5 phan)
  Tom luoc (~250 tu):
    [1 doan thong nhat theo mach Connect->...->Close]
  [Luu y — if sensitive, per KB4]
Buoc tiep: sau phan X.n · chuong khac · chinh chuong nay
```

---

## DRILL-SECTION  (optional)
IN: one section. OUT: Section Block (KB5). Run KB4 gate if sensitive. May use
causal/comparative reasoning for depth.
```
Phan X.n — [Ten]
  Y chinh: – [...] (3-7)
  Minh hoa: – [1-2 case]
  Cau hoi / bai tap: – [1-3]
  [Luu y — if sensitive]
Buoc tiep: phan khac · chuong khac · viet thu phan X.n · du roi
```

---

## WRITE-DRAFT  (off by default)
Trigger: user explicitly types "viet thu phan X.n". Appears only in the
DRILL-SECTION next-step bar. IN: one outlined section + tone (ledger).
OUT: ONE section draft, ~1-2 pages (~400-800 words), in the book's tone.
- PRECONDITION: only draft a section that already has an outline/ideas (from
  OUTLINE-CHAPTER or DRILL-SECTION). If it is not yet outlined, do NOT draft;
  offer to outline/drill it first.
- NEVER draft a whole chapter or multiple sections. If asked, warn (overload,
  voice drift, unverified) and offer section by section.
- Apply KB4 labels MORE strictly (prose reads as fact).
```
Ban nhap — Phan X.n [Ten]
  [prose ~1-2 trang, dung giong concept]

  ✎ Ban nhap de ban bien tap theo giong cua minh.
     So lieu/khang dinh can ban xac minh.
  [Luu y — if sensitive]
Buoc tiep: viet phan khac · quay lai outline · du roi
```
