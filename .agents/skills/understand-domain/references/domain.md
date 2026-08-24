# Filler Paper domain

Filler Paper is a digital ring binder for notes that users can move, refine and reorganize.

Core philosophy:

> Capture first. Organize later.

The application must allow users to create blank Pages and write before deciding how the content should be organized.

A Page remains valid even when it is blank.

## Vocabulary

Use these terms consistently:

| Code             | Brazilian Portuguese interface |
| ---------------- | ------------------------------ |
| Binder           | Fichário                       |
| Divider          | Divisor                        |
| Page             | Página                         |
| Loose page       | Página solta                   |
| Unsectioned page | Página sem divisor             |
| Draft            | Rascunho                       |
| Refined          | Refinada                       |

A loose page does not belong to a binder.

An unsectioned page belongs to a binder but does not belong to a divider.

## Main concepts

### Binder

A Binder:

- has a required title;
- may have optional tags;
- may exist without dividers;
- may contain empty dividers;
- may contain pages without a divider;
- may contain pages grouped by dividers.

A Binder controls whether its unsectioned pages appear:

- before all dividers; or
- after all dividers.

Unsectioned pages cannot currently appear between two dividers.

### Divider

A Divider:

- has a required title;
- may have optional tags;
- always belongs to exactly one Binder;
- may contain no pages;
- may contain multiple ordered pages;
- cannot exist without a Binder.

There are currently no loose dividers.

Moving a Divider to another Binder also moves all its pages and preserves their internal order.

Reordering a Divider does not change the order of the pages inside it.

### Page

A Page:

- may have an optional title;
- always has a content field;
- may have empty content;
- must never have null content;
- may have optional tags;
- has a Draft or Refined status;
- may exist without a Binder;
- may belong to a Binder without a Divider;
- may belong to a Binder and one Divider;
- cannot belong to more than one Divider at a time.

If a Page belongs to a Divider:

- the Page must also belong to a Binder;
- the Page and Divider must belong to the same Binder.

Moving a Page to a Divider from another Binder also moves the Page to that Binder.

### Page organization states

Valid organization states:

#### Loose page

```text
Binder: none
Divider: none
```

#### Page without a divider

```text
Binder: present
Divider: none
```

#### Page inside a divider

```text
Binder: present
Divider: present
```

This state is invalid:

```text
Binder: none
Divider: present
```

### Refinement status

Available statuses:

- `DRAFT`
- `REFINED`

A new Page starts as `DRAFT`.

`DRAFT` represents a quick, unfinished or unorganized capture.

`REFINED` represents content that the user has intentionally cleaned, filtered or reorganized.

Status changes are explicit user decisions:

- the user may mark a Draft Page as Refined;
- editing a Refined Page does not automatically return it to Draft;
- the user may manually return a Refined Page to Draft.

Refinement and structural organization are independent.

All combinations are valid:

- loose and Draft;
- loose and Refined;
- inside a Binder and Draft;
- inside a Binder and Refined;
- inside a Divider and Draft;
- inside a Divider and Refined.

The status does not represent version history.

### Titles

Titles are required for:

- Binder;
- Divider.

Titles are optional for Page.

The interface may display a subtle `Untitled` (`Sem título` in pt-BR) placeholder or use the first content line as a visual reference.

This visual fallback must not automatically become the Page title.

### Tags

Binder, Divider and Page may have optional tags.

Tags behave like thematic labels or stickers.

They help users:

- search;
- filter;
- group related items;
- connect items from different structural locations.

The same tag may be assigned to Binders, Dividers and Pages.

Tags do not determine structural ownership.

### Search

Search should eventually support:

- Binder titles;
- Divider titles;
- Page titles;
- Page content;
- tags.

### Deleting a Divider

The safe default action is:

> Delete only the Divider.

Its pages:

- remain in the same Binder;
- become unsectioned pages;
- preserve their relative order.

The user may instead choose:

> Delete the Divider and all its Pages.

This destructive option requires confirmation by typing the Divider title.

### Deleting a Binder

The safe default action is:

> Delete only the Binder.

In this case:

- its Dividers are removed;
- its Pages are preserved;
- all preserved Pages become loose pages.

The user may instead choose:

> Delete the Binder, its Dividers and all its Pages.

This destructive option requires confirmation by typing the Binder title.

### Trash

Deleted items remain in Trash for 30 days before permanent deletion.

They may be restored during this period.

When restoring a Page whose previous Binder no longer exists, the Page is restored as a loose page.

The complete restoration behavior for deleted Binders and Dividers has not yet been defined.

### Current product scope

The first useful version should eventually support:

- creating Binders;
- quickly creating blank Pages;
- editing Page content;
- creating Dividers;
- moving and reordering Pages;
- moving and reordering Dividers;
- changing Pages between Draft and Refined;
- adding tags;
- searching by titles, content and tags.

This list describes the intended first version, not a requirement to implement every feature simultaneously.
