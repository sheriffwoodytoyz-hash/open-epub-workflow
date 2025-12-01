# open-epub-workflow
Open-source EPUB/XHTML/CSS templates for scalable publishing workflows


# EPUB template for Copilot-assisted publishing

- [日本語 / Japanese]
- [English]
- [Français]

> This repository uses a split README strategy to improve maintainability and community translations over time. For small projects, a single multi-language README can suffice; with wider translation needs, separate files per language are commonly used. See community discussions for rationale.
> 
> [日本語 / Japanese]
# Copilot ワークフローテンプレート

このリポジトリは、スケーラブルな EPUB/XHTML/CSS ワークフロー用テンプレートを提供します。  
自動化・再現性・コミュニティ共有を重視して設計されており、**Microsoft Copilot** をドキュメント作成や最適化、知識共有のパートナーとして活用できます。

## 特徴
- 📚 出版ワークフロー向けのオープンソーステンプレート
- ⚙️ 正規表現の安全性を考慮した自動化対応設計
- 🔗 サブモジュールを用いたマルチリポジトリ GitHub 構成
- 🤝 コミュニティ主導の改善

## 使い方
1. リポジトリをクローンします。
2. `/templates` ディレクトリで EPUB/XHTML/CSS の例を確認します。
3. Copilot を活用してカスタマイズやドキュメント化を行います。
4. 改善提案はプルリクエストで貢献してください。

## ライセンス
オープンソースライセンスの下で配布されています。詳細は `LICENSE.md` をご確認ください。

 [English]
# EPUB template optimized for Copilot assistance

**Overview:**  
A public template that enables reproducible EPUB production with AI (Copilot) support, while keeping original manuscripts private. It balances community reuse with ongoing personal extension and publishing/journalism support.

**Goals and orientation:**  
- **Reuse:** Provide minimal semantic XHTML tags, CSS themes, OPF/nav templates for immediate adoption.  
- **Scale:** Systematize ID conventions and extraction design to withstand large-scale production (1000+ chapters).  
- **Public value:** Support education and journalism with standardized styles and verification tasks.  
- **Boundary:** Public = templates, settings, tools, dummy examples. Private = manuscripts, images, contract-bound assets.

**Repository layout (example):**  
- **template/:**  
  - **xhtml/** minimal semantic set (chapter, section, figure, note)  
  - **css/** reader-difference-absorbing base + overlay themes (light/dark/serif/sans)  
  - **opf/** EPUB 3.2 package skeleton (metadata placeholders)  
  - **nav.xhtml** accessibility-conscious TOC template  
- **tools/:** VS Code settings/tasks/launch; snippets for JP input; regex safe patterns  
- **examples/:** license-safe dummy text & CC0 images; ID naming sample for 1000+ chapters  
- **docs/:** README/CONTRIBUTING/SECURITY/CHANGELOG; copilot-prompts.md (semantics, IDs, CSS vars)

> Sources: 

**VS Code workflow and AI support:**  
- **Workspace:** Open public template (epub-template) + private book (mybook-private) in one .code-workspace.  
- **Submodule:** Private repo references the public template via git submodule to control version following.  
- **Tasks:** Build EPUB from template, CSS lint, XHTML formatting. HTMLHint warns on duplicate IDs, orphan anchors, missing headings.

> Sources: 

**ID and extraction for scale:**  
- **ID format:** bk-{shorttitle}-{chap:04}-{sec:02}-{item} (collision avoidance, ordering, spreadsheet-friendly)  
- **Safe extraction:** Head-only markers like %%note + word-based capture; forbid repeated inline symbol sequences to avoid mis-extraction  
- **Prefer XPath:** Structure-first selection (e.g., //section[@data-type='note']); use regex for coarse passes, confirm via XPath post-formatting.

> Sources: 

**Standardization and quality:**  
- **Style guides:** XHTML prioritizes semantics; CSS handles visuals. Use CSS variables (e.g., --line-height, --para-spacing) per work.  
- **CI (optional):** Lint (XHTML/CSS, ID duplication) and Build (sample EPUB artifacts for public).  
- **Versioning:** SemVer (MAJOR structure changes, MINOR new templates, PATCH fixes).

> Sources: 

**Licensing and contributions:**  
- **Recommended dual license:** MIT for code/settings; CC BY 4.0 for doc snippets/figures.  
- **CONTRIBUTING:** coding rules, ID rules, lint pass, test EPUB build, PR template; clear public/private boundary.  
- **Security:** include vulnerability reporting path even for templates.  
- **GPL declaration (option):** An alternative GPL statement aligned with reuse and publishing/journalism support is provided.

> Sources: 

**Next steps:**  
1. **Initialize public repo:** scaffold, finalize README and licenses first.  
2. **Connect private repo:** import a fixed tag; override only work-specific settings.  
3. **Author AI guide:** document semantics, ID rules, CSS vars in docs/copilot-prompts.md.  
4. **First release:** v0.1.0 with separate profiles (fiction, learning materials).

> Sources:

 [Français]
 
> # Modèle EPUB optimisé pour l’assistance Copilot

**Vue d’ensemble :**  
Un modèle public permettant une production EPUB reproductible avec l’assistance IA (Copilot), tandis que les manuscrits originaux restent privés. Il concilie réutilisation par la communauté, extensions personnelles continues et soutien à l’édition/journalisme.

**Objectifs et orientation :**  
- **Réutilisation :** fournir un ensemble minimal de balises XHTML sémantiques, des thèmes CSS et des modèles OPF/nav prêts à l’emploi.  
- **Montée en échelle :** systématiser la convention d’ID et la conception d’extraction pour résister à une production à grande échelle (1000+ chapitres).  
- **Valeur publique :** viser l’éducation et le journalisme via des styles standardisés et des tâches de vérification.  
- **Frontière :** Public = modèles, réglages, outils, exemples fictifs. Privé = manuscrits, images, actifs sous contrat.

**Structure du dépôt (exemple) :**  
- **template/:**  
  - **xhtml/** ensemble sémantique minimal (chapter, section, figure, note)  
  - **css/** base absorbant les différences de lecteurs + thèmes (light/dark/serif/sans)  
  - **opf/** squelette package EPUB 3.2 (métadonnées placeholders)  
  - **nav.xhtml** modèle de TOC avec accessibilité  
- **tools/:** réglages/tâches/launch VS Code; snippets adaptés à la saisie JP; motifs regex sûrs  
- **examples/:** texte fictif sûr pour la licence & images CC0; échantillon de convention d’ID pour 1000+ chapitres  
- **docs/:** README/CONTRIBUTING/SECURITY/CHANGELOG; copilot-prompts.md (sémantique, IDs, variables CSS)

> Sources: 

**Flux VS Code et assistance IA :**  
- **Espace de travail :** ouvrir le template public (epub-template) + le livre privé (mybook-private) dans un seul .code-workspace.  
- **Sous-module :** le dépôt privé référence le template public via git submodule pour contrôler le suivi de version.  
- **Tâches :** génération EPUB, lint CSS, formatage XHTML. HTMLHint avertit sur IDs dupliqués, ancres orphelines, titres manquants.

> Sources: 

**Convention d’ID et extraction à grande échelle :**  
- **Format d’ID :** bk-{shorttitle}-{chap:04}-{sec:02}-{item} (anti-collision, ordre stable, compatible tableur)  
- **Extraction sûre :** marqueurs en début de ligne (ex. %%note) + capture par mot; interdire les séquences répétées de symboles inline  
- **Préférer XPath :** sélection structurelle (ex. //section[@data-type='note']); regex en extraction grossière, confirmation XPath après formatage.

> Sources: 

**Standardisation et qualité :**  
- **Guides de style :** XHTML priorise la sémantique; CSS gère le rendu. Variables CSS (ex. --line-height, --para-spacing) surchargées par œuvre.  
- **CI (optionnel) :** Lint (XHTML/CSS, duplication d’ID) et Build (artifacts EPUB d’exemple pour le public).  
- **Versionnage :** SemVer (MAJOR changements structurels, MINOR nouveaux templates, PATCH correctifs).

> Sources: 

**Licence et contributions :**  
- **Double licence recommandée :** MIT pour code/réglages; CC BY 4.0 pour extraits et figures.  
- **CONTRIBUTING :** règles de code, règles d’ID, lint, build d’EPUB test, modèle de PR; frontière public/privé explicite.  
- **Sécurité :** indiquer le canal de signalement des vulnérabilités, même pour un template.  
- **Déclaration GPL (option) :** une formulation GPL conforme à la réutilisation et au soutien éditorial est proposée.

> Sources: 

**Prochaines étapes :**  
1. **Initialiser le dépôt public :** squelette, README et licences d’abord.  
2. **Connecter le dépôt privé :** importer un tag figé; surcharger uniquement les réglages spécifiques à l’œuvre.  
3. **Rédiger le guide IA :** documenter sémantique, règles d’ID, variables CSS (docs/copilot-prompts.md).  
4. **Première release :** v0.1.0 avec profils séparés (fiction, matériel pédagogique).

> Sources: 


