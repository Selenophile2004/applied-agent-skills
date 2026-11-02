# Actual-template inventory and Persian RTL QA

Record the supplied file's canvas/orientation, master-layout relationships, layout names/IDs, placeholder types/indices, font/color roles, fields, footer/legal blocks and authorized logos. Do not import indices or geometry from another template.

Map communication roles to actual available layouts. Missing assets/fonts are input or rendering constraints, not permission for silent substitution.

## Bidirectional behavior
Test Persian paragraphs, mixed Persian/Latin phrases, dates, negative values and chart labels in the actual renderer. RTL direction and right alignment are separate controls. Preserve numeral conventions and inspect visual order; split runs/boxes where needed.

## Editability
Preserve native requested charts/tables/shapes and recoverable data. A screenshot is not an editable chart. Use supported authoring operations to retain relationships rather than copying isolated slide XML.

## Evidence per final slide
Record manifest ID, layout, text coverage, source status, editable-element status and visual findings. Inspect readable renders for overflow, clipping, collisions, alignment, contrast, bidi errors, substitution and stale template content. Contact sheets locate issues but do not replace readable inspection.

Rerender corrections and shared dependents. Shared font/layout changes can invalidate every preview. Reconcile final text with the accepted manifest and validate actual package/exports. Report missing native-app/renderer checks honestly.
