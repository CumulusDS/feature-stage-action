[![Create Release][release-badge]][release-url]
[![Import Labels][import-labels-badge]][import-labels-url]
[![Sync Labels][sync-labels-badge]][sync-labels-url]
[![PR AutoLabeler][autolabeler-badge]][autolabeler-url]
[![Assigner][assigner-badge]][assigner-url]

Description

### Inputs
#### `githubEventName`
Github event information

### Outputs
#### `stage`
The stage this action is running against

### Example usage
```yaml
      - name: Set feature stage
        id: set-feature-stage
        uses: CumulusDS/feature-stage-action@v1
        with:
          githubEventName: ${{ github.event_name }}
```

The results can be later referenced again for use in a separate step if desired using the `results` output from the step.
In order to reference the `result` output, you must assign and `id` to the step for future referencing.

```yaml
      - name: show stage
        run: echo "${{ steps.action.set-feature-stage.stage }}"
```


[release-badge]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/release.yml/badge.svg
[release-url]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/release.yml
[import-labels-badge]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/labels_import.yml/badge.svg
[import-labels-url]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/labels_import.yml
[sync-labels-badge]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/labels_sync.yml/badge.svg
[sync-labels-url]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/labels_sync.yml
[autolabeler-badge]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/autolabeler.yml/badge.svg
[autolabeler-url]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/autolabeler.yml
[assigner-badge]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/assign.yml/badge.svg
[assigner-url]: https://github.com/CumulusDS/feature-stage-action/actions/workflows/assign.yml
