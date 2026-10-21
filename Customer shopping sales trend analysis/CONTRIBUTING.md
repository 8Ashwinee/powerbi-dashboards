# Contributing

Thanks for your interest in improving this project!

## Ways to contribute

- Report bugs or incorrect numbers
- Suggest new visuals, measures or pages
- Improve the documentation

## Workflow

1. **Fork** the repository and create a branch:
   ```bash
   git checkout -b feature/short-description
   ```
2. Make your changes in Power BI Desktop and save.
3. Update the docs (`docs/DATA_MODEL.md`, `docs/DASHBOARD_GUIDE.md`) and `CHANGELOG.md` if you add or change measures, tables or visuals.
4. Commit with a clear message:
   ```bash
   git commit -m "Add YoY growth measure and card"
   ```
5. Push and open a **Pull Request** describing what changed and why, with before/after screenshots.

## Guidelines

- **Binary file warning:** `.pbix` files cannot be merged. Coordinate before editing to avoid conflicts, and keep one PR per change.
- Follow existing naming conventions for measures and visuals.
- Do not commit sensitive or personally identifiable data.
- Keep the file size reasonable; avoid embedding unnecessary data.
- Test that the report opens and refreshes without errors.

## Reporting issues

Open an issue with:
- What you expected vs. what happened
- Steps to reproduce
- Power BI Desktop version
- Screenshots if relevant

## Code of conduct

Be respectful and constructive in all discussions.
