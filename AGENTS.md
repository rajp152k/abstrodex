# abstrodex

> index of abstractions — human-AI symbiosis for deep learning and complex reasoning

## purpose

- structured knowledge substrate for self-directed education
- surfaces abstractions across complicated fields (math, physics, CS, philosophy, biology, ...)
- enables progressive formalization: intuition → notation → proof → application
- optimized for AI-assisted exploration, not passive consumption

## architecture

- **polylith** (Clojure)
  - independent components, shared bases, composable projects
  - evolves without rewrites — add bricks, not layers
  - REPL-driven development as default workflow
  - single repo, many deployable artifacts when needed
- **data-first**
  - abstractions as data (EDN/maps), not opaque objects
  - relations between concepts are first-class
  - queryable, diffable, serializable by default

## stack constraints

- **CLI-native** — all primary interaction via terminal
  - TUI where warranted (e.g. navigation, search)
  - no GUI unless explicitly scoped as separate project
- **text-only output** — prose, tables, outlines, code blocks
  - diagrams generated via mermaid (rendered externally)
  - no embedded images; reference by path or URI
- **tooling assumptions**
  - unix proficiency assumed
  - editor: emacs/vim/terminal-native
  - build: clojure CLI (`clj`), polylith (`poly`)
  - version control: git (atomic commits, clean history)

## domain model (seed — will evolve)

- **abstraction**
  - name, field(s), aliases
  - definition (formal + intuitive)
  - prerequisites — directed graph of dependencies
  - examples — concrete instantiations
  - relations — generalizes / specializes / analogous-to / dual-of
- **field**
  - taxonomy of knowledge domains
  - cross-references where abstractions span fields
- **path**
  - ordered sequence of abstractions for learning
  - generated or curated
  - adaptable to learner's existing knowledge graph

## AI integration principles

- AI as interlocutor, not oracle — challenges understanding, doesn't just answer
- every AI-generated claim traceable to source or derivation
- reasoning chains explicit and inspectable
- human retains editorial authority over the index
- prompt scaffolds stored as reusable components

## conventions

- **language**: precise, compressed, no filler
  - prefer noun phrases and infinitive verbs
  - outlines over paragraphs; nesting over prose
  - define terms on first use; don't repeat definitions
- **structure**: recursive outlines (this document is the template)
  - top-level: broadest concern
  - each sub-bullet: one refinement or clarification
  - nest as deep as meaning requires; no deeper
- **naming**: kebab-case for files, namespaces, keys
- **commits**: atomic, imperative mood, scoped (`domain: add concept-of-limit`)
- **docs**: colocated with code; AGENTS.md as project-level knowledge base
