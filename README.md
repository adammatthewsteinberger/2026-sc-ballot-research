# 2026 South Carolina Ballot Research

Candidate research and sample-ballot materials for Greenville County, South Carolina - Travelers Rest 1, for the November 3, 2026 statewide general election.

The research report is informational and does not endorse any candidate. The ballot PDF is a sample ballot; it is not a voter's official ballot and should be checked again close to the election.

## Documents

Each source PDF is intentionally retained alongside a Markdown transcription.

| Source PDF | Markdown version | Contents |
| --- | --- | --- |
| [Ballot.pdf](Ballot.pdf) | [Ballot.md](Ballot.md) | Five-page sample ballot, precinct information, candidate contests, and three local questions |
| [2026-south-carolina-sample-ballot-candidate-research.pdf](2026-south-carolina-sample-ballot-candidate-research.pdf) | [2026-south-carolina-sample-ballot-candidate-research.md](2026-south-carolina-sample-ballot-candidate-research.md) | Nine-page candidate research report covering the offices and candidates on the sample ballot |
| [greenville-travelers-rest-2026-ballot-research-guide.pdf](greenville-travelers-rest-2026-ballot-research-guide.pdf) | [greenville-travelers-rest-2026-ballot-research-guide.md](greenville-travelers-rest-2026-ballot-research-guide.md) | Twelve-page nonpartisan guide to the three local ballot questions, funding mechanics, tradeoffs, and sources |

The Markdown files preserve the source content in a text-friendly format and normalize headings, lists, tables, and page structure. The research-report and local-guide Markdown files also preserve their source PDFs' embedded hyperlinks in page-grouped source sections. The PDFs remain the authoritative visual copies.

## Tooling

This repository uses [uv](https://docs.astral.sh/uv/) for reproducible Python environments.

- vibey==1.5.0 is pinned as the repository's Vibey dependency.
- pdfplumber is included for PDF text extraction and conversion checks.
- The project is data/document-only, so the environment is configured with tool.uv.package = false.

Install the locked environment with:

~~~sh
uv sync
~~~

Confirm the requested Vibey version with:

~~~sh
uv run vibey --version
~~~

The expected output begins with vibey 1.5.0.

## Verification

The repository can be checked without changing the source PDFs:

~~~sh
uv lock --check
uv run vibey --version
uv tree --depth 1
git status --short
~~~

The PDF-to-Markdown conversion was checked against the source page counts and rendered PDF pages. Before relying on any ballot information, consult the original PDF and the election office's current materials because sample ballots, candidates, and eligibility-specific questions can change.
