# The Open Source Organizational Ecosystem Map

A visual reference of the organizations that make up the open source ecosystem — foundations, fiscal sponsors, security groups, advocacy orgs, funding mechanisms, community networks, government programs, and domain-specific organizations.

**[View the map](https://jring-o.github.io/open-source-ecosystem-map/)**

## About

The open source ecosystem is supported by hundreds of organizations with different structures, missions, and geographic footprints. This map attempts to make that landscape visible and navigable.

Each organization includes:
- **Category** placement (umbrella foundations, single-project, advocacy, funding, etc.)
- **Legal structure** badge (501(c)(3), 501(c)(6), nonprofit, corp, gov, IGO, sub-org)
- **Region flag** indicating country or global reach
- **Tooltip** with a brief description on hover

The map is a single self-contained HTML file with no external dependencies beyond Google Fonts. It uses a bin-packing layout algorithm to arrange category boxes efficiently.

## Taxonomy

Organizations on this map are classified by function, not by parentage. Where an org is placed depends on what it does, not who it's under.

### Legal status badges

| Badge | Meaning |
|-------|---------|
| (c)(3) | US 501(c)(3) charitable nonprofit |
| (c)(6) | US 501(c)(6) trade association |
| nonprofit | Non-US nonprofit or general nonprofit status |
| corp | For-profit company |
| gov | Government program |
| IGO | Intergovernmental organization |
| sub-org | Organization with its own executive leader and board, but not its own legal entity — operates under a parent |

### What makes a sub-org?

A sub-org has its own executive leader (ED, President, CEO, GM — title doesn't matter) and its own board of directors, but is not independently incorporated. It is legally part of a parent organization. Sub-orgs are placed in the functional category where they belong, not grouped under their parent.

### Multi-project foundation vs. fiscal host

Both live in the Umbrella Foundations & Fiscal Sponsors section. The distinction:

- **Multi-project foundation** — has at least one sub-org under it
- **Fiscal host** — hosts projects, but none of those projects have their own executive leader and board

### Independent organizations

Independently incorporated legal entities are tagged by their own legal status ((c)(3), (c)(6), nonprofit, etc.) and placed by function.

## Contributing

This map is intentionally incomplete — there are many organizations doing important work in open source that aren't listed yet. Contributions are welcome.

### Adding an organization

1. Open `index.html`
2. Find the appropriate category and subcategory
3. Add a new `<span class="org">` element following the existing pattern:

```html
<span class="org" data-tip="Brief description of what the org does.">Organization Name <span class="tax-badge badge-TYPE">LABEL</span> <span class="region-flag">FLAG</span></span>
```

**Region flags** use HTML entity codes for country flag emoji (e.g., `&#x1F1FA;&#x1F1F8;` for US, `&#x1F1E9;&#x1F1EA;` for Germany). Use `&#x1F310;` (globe) for global/distributed organizations.

### Guidelines

- Every organization should have a `data-tip` tooltip with a concise, factual description
- Place organizations in the most specific applicable subcategory
- If no existing subcategory fits, propose a new one in your PR
- Keep descriptions neutral and factual — this is a reference map, not a ranking

### Categories

| Category | What belongs here |
|----------|-------------------|
| Umbrella Foundations & Fiscal Sponsors | Multi-project foundations and fiscal hosts |
| Security | Standards, auditing, infrastructure protection |
| Government & Public Sector | Direct funding programs, recognition frameworks |
| Single-Project & Language Foundations | Language/runtime foundations, applications, OS/infra, data/protocols |
| Advocacy & Policy | Software freedom, policy/standards, legal services |
| Funding Mechanisms & Platforms | Direct-to-maintainer, pledge models, philanthropies |
| Community Networks | Regional community building |
| Domain-Specific | Science & data, industry & civic tech, hardware, education, AI & ML, cloud, energy, film |

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Credits

Created and maintained by [Jonathan Starr](https://github.com/jring-o) as part of the [Open Source Endowment](https://endowment.dev) project.
