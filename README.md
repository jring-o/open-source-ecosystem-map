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

## Contributing

This map is intentionally incomplete — there are many organizations doing important work in open source that aren't listed yet. Contributions are welcome.

### Adding an organization

1. Open `index.html`
2. Find the appropriate category and subcategory
3. Add a new `<span class="org">` element following the existing pattern:

```html
<span class="org" data-tip="Brief description of what the org does.">Organization Name <span class="tax-badge badge-TYPE">LABEL</span> <span class="region-flag">FLAG</span></span>
```

**Badge types:**

| Class | Label | Use for |
|-------|-------|---------|
| `badge-c3` | (c)(3) | US 501(c)(3) charitable nonprofits |
| `badge-c6` | (c)(6) | US 501(c)(6) trade associations |
| `badge-nonprofit` | nonprofit | Non-US nonprofits or general nonprofit status |
| `badge-corp` | corp | For-profit companies |
| `badge-gov` | gov | Government programs |
| `badge-igo` | IGO | Intergovernmental organizations |
| `badge-sub` | sub-org | Sub-foundations (e.g., CNCF under Linux Foundation) |

**Region flags** use HTML entity codes for country flag emoji (e.g., `&#x1F1FA;&#x1F1F8;` for US, `&#x1F1E9;&#x1F1EA;` for Germany). Use `&#x1F310;` (globe) for global/distributed organizations.

### Guidelines

- Every organization should have a `data-tip` tooltip with a concise, factual description
- Place organizations in the most specific applicable subcategory
- If no existing subcategory fits, propose a new one in your PR
- Keep descriptions neutral and factual — this is a reference map, not a ranking

### Categories

| Category | What belongs here |
|----------|-------------------|
| Umbrella Foundations & Fiscal Sponsors | Multi-project foundations, fiscal hosts, LF sub-foundations |
| Security | Standards, auditing, infrastructure protection |
| Government & Public Sector | Direct funding programs, recognition frameworks |
| Single-Project & Language Foundations | Language/runtime foundations, applications, OS/infra, data/protocols |
| Advocacy & Policy | Software freedom, policy/standards, legal services |
| Funding Mechanisms & Platforms | Direct-to-maintainer, pledge models, philanthropies |
| Community Networks | Regional community building |
| Domain-Specific | Science & data, industry & civic tech, hardware, education, AI & ML |

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Credits

Created and maintained by [Jonathan Starr](https://github.com/jring-o) as part of the [Open Source Endowment](https://endowment.dev) project.
