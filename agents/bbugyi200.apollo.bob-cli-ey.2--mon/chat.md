# Chat History - ace-run (bob-cli-ey.2--mon)

- **TIMESTAMP:** 2026-11-01 01:32:04 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-ey.2--mon

## Prompt

sase monitor start --command 'just check' --reason 'run command'

## Response

sase tool run 3a4ba1951eca329bfb0cb49e5daf3fac

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/mod.rs:17:
 use serde_json::json;
 
 use super::{
[31m-    capture_clip, capture_language,
[m[32m+    capture_clip, capture_drawers, capture_language,
[m     capture_language::{
         is_block_id, unused_project_note_offer_pomodoro_error,
         unused_project_note_pomodoro_error, AuthoredSubBullet, CaptureKind,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/mod.rs:24:
[31m-        CaptureParseOptions, ClipRequest, ParsedCaptureItem, ParsedCaptureText,
[m[31m-        ParsedDependencyTarget, ParsedDependencyTargetKind, ParsedRelation,
[m[31m-        PomodoroAdjustSpec, PomodoroCloseSpec, PomodoroShiftSpec,
[m[31m-        PomodoroStartSpec, ProjectNoteForm, RelationDirection, SubBulletTarget,
[m[31m-        DrawerSelector, TaskToggleIntent,
[m[32m+        CaptureParseOptions, ClipRequest, DrawerSelector, ParsedCaptureItem,
[m[32m+        ParsedCaptureText, ParsedDependencyTarget, ParsedDependencyTargetKind,
[m[32m+        ParsedRelation, PomodoroAdjustSpec, PomodoroCloseSpec,
[m[32m+        PomodoroShiftSpec, PomodoroStartSpec, ProjectNoteForm,
[m[32m+        RelationDirection, SubBulletTarget, TaskToggleIntent,
[m         POMODORO_CLOSE_INTERNAL_BULLETS_ERROR, POMODORO_START_FORCED_ERROR,
     },
     capture_pomodoro_close, capture_pomodoro_start, capture_pomodoros,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/mod.rs:32:
[31m-    capture_project_note, capture_schedule_log, capture_drawers,
[m[31m-    capture_task_toggle, capture_templates, collect_done, config,
[m[31m-    env as bob_env, markdown, note_tasks,
[m[32m+    capture_project_note, capture_schedule_log, capture_task_toggle,
[m[32m+    capture_templates, collect_done, config, env as bob_env, markdown,
[m[32m+    note_tasks,
[m     note_tasks::{BlockIdLookup, RefLookup},
     plan_budget, pomodoro,
     projects::{
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/mod.rs:152:
     SectionHeading,
 };
 pub(crate) use sub_bullet::{
[31m-    MANAGED_TASK_LOG_LABELS, dominant_indent_unit, first_child_indentation,
[m[32m+    dominant_indent_unit, first_child_indentation,
[m     first_direct_managed_log_start, leading_spaces_or_tabs_len,
     leading_whitespace, list_item_body, list_marker_len,
     nearest_shallower_list_item_parent, parse_managed_task_log_marker,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/mod.rs:159:
[31m-    ManagedTaskLogKind,
[m[32m+    ManagedTaskLogKind, MANAGED_TASK_LOG_LABELS,
[m };
 
 pub(crate) fn run(args: Vec<OsString>) -> i32 {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:107:
             // Load catalog for spelling (best-effort; empty on failure).
             let catalog = capture_drawers::load_drawer_catalog(bob_dir)
                 .unwrap_or_default();
[31m-            let drawers =
[m[31m-                capture_drawers::drawers(&contents, parent);
[m[32m+            let drawers = capture_drawers::drawers(&contents, parent);
[m             let block_id = parent.block_id.as_deref();
             match capture_drawers::resolve_drawer_for_write(
                 &drawers,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:122:
                     capture_drawers::DrawerResolveOutcome::Existing {
                         drawer,
                     } => {
[31m-                        let insertion =
[m[31m-                            capture_drawers::drawer_insertion(&contents, &drawer);
[m[32m+                        let insertion = capture_drawers::drawer_insertion(
[m[32m+                            &contents, &drawer,
[m[32m+                        );
[m                         (
                             insertion.offset,
                             insertion.indentation,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:151:
                                 format!("{}{}", parent.indentation, unit)
                             })
                         })
[31m-                        .unwrap_or_else(|| {
[m[31m-                            format!("{}\t", parent.indentation)
[m[31m-                        });
[m[32m+                        .unwrap_or_else(|| format!("{}\t", parent.indentation));
[m                         let header_offset = first_direct_managed_log_start(
                             &lines,
                             parent.line_index,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:160:
                             parent.block_end,
                         )
                         .unwrap_or(parent.block_end);
[31m-                        let header_block = format!("{drawer_indent}- {title}\n");
[m[32m+                        let header_block =
[m[32m+                            format!("{drawer_indent}- {title}\n");
[m                         let header_addition =
                             insertion_text_preserving_line_endings(
                                 &contents,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:167:
                                 header_offset,
                                 &header_block,
                             );
[31m-                        let with_header =
[m[31m-                            insert_at(&contents, header_offset, &header_addition);
[m[32m+                        let with_header = insert_at(
[m[32m+                            &contents,
[m[32m+                            header_offset,
[m[32m+                            &header_addition,
[m[32m+                        );
[m                         planner.stage(target, with_header.clone())?;
                         // Re-read staged (includes our header plus any
                         // earlier batch items) and resolve as existing.
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:199:
                         };
                         let staged_drawers =
                             capture_drawers::drawers(&staged, staged_parent);
[31m-                        let Some(drawer) = staged_drawers
[m[31m-                            .iter()
[m[31m-                            .find(|d| d.title == title)
[m[32m+                        let Some(drawer) =
[m[32m+                            staged_drawers.iter().find(|d| d.title == title)
[m                         else {
                             return Err(CaptureError::io(format!(
                                 "failed to create drawer {title}"
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:208:
                             )));
                         };
[31m-                        let insertion = capture_drawers::drawer_insertion(
[m[31m-                            &staged,
[m[31m-                            drawer,
[m[31m-                        );
[m[32m+                        let insertion =
[m[32m+                            capture_drawers::drawer_insertion(&staged, drawer);
[m                         // Note: header already staged; the entry below
                         // will be staged as a second edit in the same
                         // batch transaction. Return staged-based offset
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:226:
                         let drawers = staged_drawers;
                         let parent = staged_parent;
                         // Resolve again (must be existing now).
[31m-                        let catalog = capture_drawers::load_drawer_catalog(
[m[31m-                            bob_dir,
[m[31m-                        )
[m[31m-                        .unwrap_or_default();
[m[32m+                        let catalog =
[m[32m+                            capture_drawers::load_drawer_catalog(bob_dir)
[m[32m+                                .unwrap_or_default();
[m                         let resolved2 =
                             capture_drawers::resolve_drawer_for_write(
                                 &drawers,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:251:
                             )));
                         };
                         let insertion = capture_drawers::drawer_insertion(
[31m-                            &contents,
[m[31m-                            &drawer,
[m[32m+                            &contents, &drawer,
[m                         );
                         // Stage entry against staged contents (which already
                         // has the header). We inline the entry staging here
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:264:
                             })
                             .collect::<Vec<_>>()
                             .join("\n");
[31m-                        let addition =
[m[31m-                            insertion_text_preserving_line_endings(
[m[31m-                                &contents,
[m[31m-                                insertion.offset,
[m[31m-                                &indented_block,
[m[31m-                            );
[m[32m+                        let addition = insertion_text_preserving_line_endings(
[m[32m+                            &contents,
[m[32m+                            insertion.offset,
[m[32m+                            &indented_block,
[m[32m+                        );
[m                         let placement = if insertion.offset >= contents.len() {
                             Placement::Appended
                         } else {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:375:
             capture_drawers_hint(route, parent),
         )));
     }
[31m-    if let Some(drawer) = capture_drawers::match_drawer(
[m[31m-        drawers,
[m[31m-        &selector.text,
[m[31m-        selector.exact,
[m[31m-    ) {
[m[32m+    if let Some(drawer) =
[m[32m+        capture_drawers::match_drawer(drawers, &selector.text, selector.exact)
[m[32m+    {
[m         return Ok(drawer);
     }
     let listed = format_drawer_titles(drawers);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture/sub_bullet.rs:398:
     )))
 }
 
[31m-fn is_prj_target(
[m[31m-    contents: &str,
[m[31m-    parent: &note_tasks::NoteTask,
[m[31m-) -> bool {
[m[32m+fn is_prj_target(contents: &str, parent: &note_tasks::NoteTask) -> bool {
[m     let lines = line_spans(contents);
     let Some(line) = lines.get(parent.line_index) else {
         return false;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/candidates.rs:7:
 use super::{
     model::{
         ActiveTaskCandidate, ActiveTaskPomodoroCandidate, BlockedTaskCandidate,
[31m-        Candidates, CompleteError, DependencyCandidate, PickerRelationEntry,
[m[31m-        PickerRelationship, PickerRelationshipEntry, RelationCandidate,
[m[31m-        RelationLabelSuggestion, RouteCandidate, SectionCandidate,
[m[31m-        TaskCandidate, TaskCompleteCandidate, TaskGotoCandidate,
[m[31m-        TaskLinkCandidate, TaskParentCandidate, DrawerCandidate,
[m[32m+        Candidates, CompleteError, DependencyCandidate, DrawerCandidate,
[m[32m+        PickerRelationEntry, PickerRelationship, PickerRelationshipEntry,
[m[32m+        RelationCandidate, RelationLabelSuggestion, RouteCandidate,
[m[32m+        SectionCandidate, TaskCandidate, TaskCompleteCandidate,
[m[32m+        TaskGotoCandidate, TaskLinkCandidate, TaskParentCandidate,
[m     },
     support::rank,
 };
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/candidates.rs:18:
 use crate::native::{
     capture, capture_active_tasks, capture_block_ids,
[31m-    capture_completable_tasks, capture_dependency_tasks,
[m[32m+    capture_completable_tasks, capture_dependency_tasks, capture_drawers,
[m     capture_language::{
         DependencyEntry, DependencyTarget, DependencyTargetKind,
         EditorItemParse, RelationDirection, RelationEntry,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/candidates.rs:24:
     },
[31m-    capture_link_tasks, capture_targets, capture_drawers, capture_tasks,
[m[31m-    config,
[m[32m+    capture_link_tasks, capture_targets, capture_tasks, config,
[m     note_tasks::{self, BlockIdLookup},
     pomodoro, project_dependencies, task_complete, task_relations,
     task_status_hooks,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/engine.rs:3:
 use super::{
     candidates::{
         active_task_candidates, apply_relationship_picker,
[31m-        blocked_task_candidates, dependency_candidates, link_candidates,
[m[31m-        relation_candidates, relation_label_suggestions, route_candidates,
[m[31m-        section_candidates, task_candidates, task_complete_candidates,
[m[31m-        task_goto_candidates, task_link_candidates, task_parent_candidates,
[m[31m-        drawer_candidates, TaskSearch,
[m[32m+        blocked_task_candidates, dependency_candidates, drawer_candidates,
[m[32m+        link_candidates, relation_candidates, relation_label_suggestions,
[m[32m+        route_candidates, section_candidates, task_candidates,
[m[32m+        task_complete_candidates, task_goto_candidates, task_link_candidates,
[m[32m+        task_parent_candidates, TaskSearch,
[m     },
     model::{
         Candidates, CaptureCompleteResult, CompleteError, CompletionOwner,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/engine.rs:744:
     let content = std::fs::read_to_string(&note_path).ok()?;
     let settings = crate::native::note_tasks::read_settings(bob_dir);
     let scan = crate::native::note_tasks::scan(&content, &settings);
[31m-    let parent = block_id.as_deref().and_then(|id| match scan
[m[31m-        .by_block_id(id)
[m[31m-    {
[m[31m-        crate::native::note_tasks::BlockIdLookup::Found(task) => Some(task),
[m[31m-        _ => None,
[m[31m-    });
[m[32m+    let parent =
[m[32m+        block_id
[m[32m+            .as_deref()
[m[32m+            .and_then(|id| match scan.by_block_id(id) {
[m[32m+                crate::native::note_tasks::BlockIdLookup::Found(task) => {
[m[32m+                    Some(task)
[m[32m+                }
[m[32m+                _ => None,
[m[32m+            });
[m     Some(DrawerTarget {
         route: route_label,
         block_id,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete/shell.rs:2:
 
 use super::{
     candidates::{
[31m-        active_task_candidates, blocked_task_candidates, link_candidates,
[m[31m-        relation_candidates, relation_label_suggestions, route_candidates,
[m[31m-        section_candidates, task_candidates, task_complete_candidates,
[m[31m-        task_link_candidates, task_parent_candidates, drawer_candidates,
[m[32m+        active_task_candidates, blocked_task_candidates, drawer_candidates,
[m[32m+        link_candidates, relation_candidates, relation_label_suggestions,
[m[32m+        route_candidates, section_candidates, task_candidates,
[m[32m+        task_complete_candidates, task_link_candidates, task_parent_candidates,
[m         TaskSearch,
     },
     model::{Candidates, RouteCandidateKind},
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:28:
         nearest_shallower_list_item_parent, parse_managed_task_log_marker,
         LineSpan,
     },
[31m-    capture_language,
[m[31m-    env as bob_env,
[m[32m+    capture_language, env as bob_env,
[m     markdown::fenced_lines,
     note_tasks::{self, BlockIdLookup, NoteTask, RefLookup, TaskRef},
     style::Styler,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:84:
     if !first.is_ascii_alphabetic() {
         return false;
     }
[31m-    chars.all(|byte| {
[m[31m-        byte.is_ascii_alphanumeric() || byte == b'-'
[m[31m-    })
[m[32m+    chars.all(|byte| byte.is_ascii_alphanumeric() || byte == b'-')
[m }
 
 /// Reserved drawer keys derived from existing managed-line owners, never a
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:98:
     };
     let mut keys = HashSet::new();
     // Managed task log labels (Schedule, Work, Rotten) plus Cancel Log.
[31m-    for (label, _) in
[m[31m-        crate::native::capture::MANAGED_TASK_LOG_LABELS.iter()
[m[31m-    {
[m[32m+    for (label, _) in crate::native::capture::MANAGED_TASK_LOG_LABELS.iter() {
[m         keys.insert(drawer_key(label));
     }
     keys.insert(drawer_key(dep_blocks::CANCEL_LOG_LABEL));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:242:
     let mut next = BTreeMap::new();
     let mut cache_dirty = true;
     // Per-key aggregation.
[31m-    let mut per_key_notes: BTreeMap<String, HashSet<String>> =
[m[31m-        BTreeMap::new();
[m[31m-    let mut per_key_recent: BTreeMap<String, HashSet<String>> =
[m[31m-        BTreeMap::new();
[m[32m+    let mut per_key_notes: BTreeMap<String, HashSet<String>> = BTreeMap::new();
[m[32m+    let mut per_key_recent: BTreeMap<String, HashSet<String>> = BTreeMap::new();
[m     let mut per_key_spellings: BTreeMap<String, HashMap<String, u64>> =
         BTreeMap::new();
     let mut per_key_last: BTreeMap<String, u64> = BTreeMap::new();
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:264:
             || key.starts_with("done/")
             || key.contains("/done/");
         let note = match previous.get(&key) {
[31m-            Some(cached) if cached.mtime_ns == mtime_ns && cached.size == size => {
[m[32m+            Some(cached)
[m[32m+                if cached.mtime_ns == mtime_ns && cached.size == size =>
[m[32m+            {
[m                 cached.clone()
             }
             _ => {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:299:
     let mut records: BTreeMap<String, DrawerCatalogRecord> = BTreeMap::new();
     for (key, notes) in per_key_notes {
         let recent = per_key_recent.get(&key).map_or(0, |s| s.len() as u64);
[31m-        let spellings =
[m[31m-            per_key_spellings.remove(&key).unwrap_or_default();
[m[31m-        let title = most_used_spelling(&spellings).unwrap_or_else(|| key.clone());
[m[32m+        let spellings = per_key_spellings.remove(&key).unwrap_or_default();
[m[32m+        let title =
[m[32m+            most_used_spelling(&spellings).unwrap_or_else(|| key.clone());
[m         let slug = per_key_slug
             .get(&key)
             .cloned()
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:317:
                 last_seen: per_key_last.get(&key).copied().unwrap_or(0),
                 spellings,
                 notes: {
[31m-                    let mut v: Vec<String> =
[m[31m-                        notes.into_iter().collect();
[m[32m+                    let mut v: Vec<String> = notes.into_iter().collect();
[m                     v.sort();
                     v
                 },
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:330:
     cache.records = records.clone();
     if cache_dirty {
         if let Ok(text) = serde_json::to_string(&cache) {
[31m-            let _ = crate::native::collect_done::atomic_write(
[m[31m-                &cache_path,
[m[31m-                &text,
[m[31m-            );
[m[32m+            let _ =
[m[32m+                crate::native::collect_done::atomic_write(&cache_path, &text);
[m         }
         sweep_drawer_catalog_cache(&cache.vault);
     }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:397:
     };
     let mut entries: Vec<DrawerCatalogEntry> = Vec::new();
     let mut seen_in_note: HashSet<String> = HashSet::new();
[31m-    let push_entry = |key: String, title: String, slug: String,
[m[32m+    let push_entry = |key: String,
[m[32m+                      title: String,
[m[32m+                      slug: String,
[m                       entries: &mut Vec<DrawerCatalogEntry>,
                       seen: &mut HashSet<String>| {
         if is_reserved_drawer_key(&key) {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:447:
     // H2 headings in project notes.
     if is_project_note_text(text) {
         for h2 in project_h2_entries(text) {
[31m-            push_entry(h2.key, h2.title, h2.slug, &mut entries, &mut seen_in_note);
[m[32m+            push_entry(
[m[32m+                h2.key,
[m[32m+                h2.title,
[m[32m+                h2.slug,
[m[32m+                &mut entries,
[m[32m+                &mut seen_in_note,
[m[32m+            );
[m         }
     }
     CachedDrawerNote {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:530:
 fn drawer_owned_temp_version(name: &str) -> Option<u32> {
     let inner = name.strip_prefix('.')?.strip_suffix(".tmp")?;
     let (catalog_part, pid_text) = inner.rsplit_once('.')?;
[31m-    if pid_text.is_empty()
[m[31m-        || !pid_text.bytes().all(|b| b.is_ascii_digit())
[m[31m-    {
[m[32m+    if pid_text.is_empty() || !pid_text.bytes().all(|b| b.is_ascii_digit()) {
[m         return None;
     }
     let _: u32 = pid_text.parse().ok()?;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:539:
[31m-    let rest = catalog_part.strip_suffix(".json")?.strip_prefix("catalog-v")?;
[m[32m+    let rest = catalog_part
[m[32m+        .strip_suffix(".json")?
[m[32m+        .strip_prefix("catalog-v")?;
[m     let (version, _) = parse_drawer_catalog_version_and_hash(rest)?;
     Some(version)
 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:670:
 
 #[derive(Debug, Clone, PartialEq, Eq)]
 pub(crate) enum DrawerResolveOutcome {
[31m-    Existing { drawer: Drawer },
[m[31m-    Create { title: String, key: String, slug: String },
[m[32m+    Existing {
[m[32m+        drawer: Drawer,
[m[32m+    },
[m[32m+    Create {
[m[32m+        title: String,
[m[32m+        key: String,
[m[32m+        slug: String,
[m[32m+    },
[m }
 
 #[derive(Debug, Clone, PartialEq, Eq)]
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:757:
     // Slug path.
     let slug = selector_text.to_string();
     let key_plain = slug.to_ascii_uppercase();
[31m-    let key_spaced = capture_language::normalize_task_text(
[m[31m-        &slug.replace('-', " "),
[m[31m-    )
[m[31m-    .to_ascii_uppercase();
[m[32m+    let key_spaced =
[m[32m+        capture_language::normalize_task_text(&slug.replace('-', " "))
[m[32m+            .to_ascii_uppercase();
[m     // Exact key matches (slug key or hyphen-space variant).
     let mut matches: Vec<&Drawer> = drawers
         .iter()
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:799:
     {
         return Err(DrawerResolveError::new(
             "reserved_drawer",
[31m-            format!(
[m[31m-                "LINKS is managed by Bob; name the drawer something else"
[m[31m-            ),
[m[32m+            format!("LINKS is managed by Bob; name the drawer something else"),
[m         ));
     }
     // Near-duplicate guard (slug only): strict prefix or edit distance 1.
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:842:
     slug: &str,
 ) -> Option<&'a Drawer> {
     let needle_key = slug.to_ascii_uppercase();
[31m-    let needle_spaced = capture_language::normalize_task_text(
[m[31m-        &slug.replace('-', " "),
[m[31m-    )
[m[31m-    .to_ascii_uppercase();
[m[32m+    let needle_spaced =
[m[32m+        capture_language::normalize_task_text(&slug.replace('-', " "))
[m[32m+            .to_ascii_uppercase();
[m     // Strict prefix of a drawer key.
     // Edit distance 1 from a drawer key.
     let mut candidates: Vec<&Drawer> = Vec::new();
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:899:
         if record.note_count < 2 {
             continue;
         }
[31m-        if crate::native::note_tasks::bounded_levenshtein(
[m[31m-            new_key, key, 2,
[m[31m-        )
[m[31m-        .is_some()
[m[32m+        if crate::native::note_tasks::bounded_levenshtein(new_key, key, 2)
[m[32m+            .is_some()
[m         {
             return Some(format!(
                 "new drawer {new_key} · did you mean {}?",
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:922:
 ) -> String {
     let key_plain = slug.to_ascii_uppercase();
     let key_spaced = slug.replace('-', " ").to_ascii_uppercase();
[31m-    let key_spaced = capture_language::normalize_task_text(&key_spaced)
[m[31m-        .to_ascii_uppercase();
[m[32m+    let key_spaced =
[m[32m+        capture_language::normalize_task_text(&key_spaced).to_ascii_uppercase();
[m     let mut candidates: Vec<(&String, &DrawerCatalogRecord)> = Vec::new();
     for (key, record) in records {
         if *key == key_plain || *key == key_spaced {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:955:
 }
 
 /// Enumerate qualifying drawer bullets that are direct children of `task`.
[31m-pub(crate) fn drawers(
[m[31m-    contents: &str,
[m[31m-    task: &NoteTask,
[m[31m-) -> Vec<Drawer> {
[m[32m+pub(crate) fn drawers(contents: &str, task: &NoteTask) -> Vec<Drawer> {
[m     let lines = line_spans(contents);
[31m-    let text_lines: Vec<&str> =
[m[31m-        lines.iter().map(|line| line.text).collect();
[m[32m+    let text_lines: Vec<&str> = lines.iter().map(|line| line.text).collect();
[m     let fenced = fenced_lines(&text_lines, 0..text_lines.len());
     let children =
         direct_child_list_indexes(&lines, task.line_index, task.block_end);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1386:
 }
 
 impl CaptureDrawersRequest {
[31m-    fn from_matches(
[m[31m-        matches: &ArgMatches,
[m[31m-    ) -> Result<Self, CaptureDrawersError> {
[m[32m+    fn from_matches(matches: &ArgMatches) -> Result<Self, CaptureDrawersError> {
[m         let block_id = matches.get_one::<String>("block-id");
         let task_ref = matches.get_one::<String>("task-ref");
         let parent = match (block_id, task_ref) {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1590:
     }
 }
 
[31m-fn print_success(
[m[31m-    result: &CaptureDrawersResult,
[m[31m-    output_format: OutputFormat,
[m[31m-) {
[m[32m+fn print_success(result: &CaptureDrawersResult, output_format: OutputFormat) {
[m     match output_format {
         OutputFormat::Human => print_human_success(result),
         OutputFormat::Json => println!("{}", success_json(result)),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1605:
     print!("{}", human_success(result, &styler));
 }
 
[31m-fn human_success(
[m[31m-    result: &CaptureDrawersResult,
[m[31m-    styler: &Styler,
[m[31m-) -> String {
[m[32m+fn human_success(result: &CaptureDrawersResult, styler: &Styler) -> String {
[m     let route_label = capture::route_label(&result.route);
     let mut output = format!(
         "Capture drawers {} {}",
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1657:
 }
 
 fn success_json(result: &CaptureDrawersResult) -> String {
[31m-    serde_json::to_string(result)
[m[31m-        .expect("serialize capture drawers result")
[m[32m+    serde_json::to_string(result).expect("serialize capture drawers result")
[m }
 
[31m-fn print_error(
[m[31m-    error: CaptureDrawersError,
[m[31m-    output_format: OutputFormat,
[m[31m-) -> i32 {
[m[32m+fn print_error(error: CaptureDrawersError, output_format: OutputFormat) -> i32 {
[m     match output_format {
         OutputFormat::Human => eprintln!("{COMMAND_NAME}: {}", error.message),
         OutputFormat::Json => {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1743:
             .collect()
     }
 
[31m-    fn drawer_named<'a>(
[m[31m-        drawers: &'a [Drawer],
[m[31m-        title: &str,
[m[31m-    ) -> &'a Drawer {
[m[32m+    fn drawer_named<'a>(drawers: &'a [Drawer], title: &str) -> &'a Drawer {
[m         drawers
             .iter()
             .find(|drawer| drawer.title == title)
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1786:
             parse_drawer_title("Q&A (DRAFT), V2.0/OK-GO"),
             Some("Q&A (DRAFT), V2.0/OK-GO")
         );
[32m+        assert_eq!(parse_drawer_title("WHAT'S NEXT"), Some("WHAT'S NEXT"));
[m[32m+        assert_eq!(parse_drawer_title("FUTURE  WORK"), Some("FUTURE  WORK"));
[m         assert_eq!(
[31m-            parse_drawer_title("WHAT'S NEXT"),
[m[31m-            Some("WHAT'S NEXT")
[m[31m-        );
[m[31m-        assert_eq!(
[m[31m-            parse_drawer_title("FUTURE  WORK"),
[m[31m-            Some("FUTURE  WORK")
[m[31m-        );
[m[31m-        assert_eq!(
[m             parse_drawer_title("  REQUIREMENTS  "),
             Some("REQUIREMENTS")
         );
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:1959:
             ["REQUIREMENTS", "FUTURE WORK"]
         );
         assert_eq!(tab_drawers[0].indentation, "\t");
[31m-        assert_eq!(
[m[31m-            drawer_insertion(tab, &tab_drawers[0]).indentation,
[m[31m-            "\t\t"
[m[31m-        );
[m[32m+        assert_eq!(drawer_insertion(tab, &tab_drawers[0]).indentation, "\t\t");
[m 
         let two_space = concat!(
             "- [ ] #task Parent\n",
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:2051:
             Some("FUTURE WORK")
         );
         assert_eq!(
[31m-            select_drawer(&drawers, "FUTURE WORK")
[m[31m-                .map(|drawer| drawer.line),
[m[32m+            select_drawer(&drawers, "FUTURE WORK").map(|drawer| drawer.line),
[m             Some(3)
         );
         assert_eq!(
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_drawers.rs:2197:
         );
         assert!(contents[..offset].ends_with("\r\n"));
         assert_eq!(
[31m-            drawer_insertion(
[m[31m-                contents,
[m[31m-                drawer_named(&drawers, "FUTURE WORK")
[m[31m-            )
[m[31m-            .offset,
[m[32m+            drawer_insertion(contents, drawer_named(&drawers, "FUTURE WORK"))
[m[32m+                .offset,
[m             contents.len()
         );
     }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:787:
                         SpanKind::DependencySigil
                     },
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.spans.push(Span {
                     start: entry.note_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:799:
                         SpanKind::DependencyNote
                     },
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.spans.push(Span {
                     start: entry.block_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:811:
                         SpanKind::DependencyBlockId
                     },
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if sigil == b'*' {
                     result.blocked_entries.push(entry.clone());
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:835:
                     end: *end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if sigil == b'*' {
                     result.blocked_partials.push((*start, *end));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:859:
                     end: invalid.end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if sigil == b'*' {
                     result.blocked_invalid.push(invalid.clone());
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1092:
                     end: entry.start + entry.sigil_len(),
                     kind: SpanKind::RelationSigil,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.spans.push(Span {
                     start: entry.note_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1100:
                     end: entry.note_end,
                     kind: SpanKind::RelationNote,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.spans.push(Span {
                     start: entry.block_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1108:
                     end: entry.block_end,
                     kind: SpanKind::RelationBlockId,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if let Some(separator) = entry.separator {
                     result.spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1117:
                         end: separator.1,
                         kind: SpanKind::RelationLabelSeparator,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let (Some(label_start), Some(label_end)) =
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1129:
                         end: label_end,
                         kind: SpanKind::RelationLabel,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 result.relation_entries.push(entry.clone());
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1150:
                     end: *end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.relation_target_partials.push((*start, *end));
             }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1170:
                     end: *end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.relation_label_partials.push((*start, *end));
             }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/dependencies.rs:1190:
                     end: invalid.end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 result.relation_invalid.push(InvalidDependency {
                     raw: invalid.raw.clone(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:104:
                 end: token.end,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             requires_body: false,
             pomodoro_start: None,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:283:
                         ));
                     }
                 }
[31m-            } else if !crate::native::capture_drawers::is_drawer_slug(section)
[m[31m-            {
[m[32m+            } else if !crate::native::capture_drawers::is_drawer_slug(section) {
[m                 return TokenParse::Invalid(token_diagnostic(
                     token,
                     "invalid_drawer",
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:381:
         end: sep_start + 1,
         kind: SpanKind::ProjectNoteSeparator,
         project_note: Some(ProjectNoteForm::Create),
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     // Route span is first when present; separator sits right after it.
     if marker_parse
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:441:
         end: sep_start + 1,
         kind: SpanKind::ProjectNoteSeparator,
         project_note: Some(ProjectNoteForm::Offer),
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     // Route span is first when present; separator sits right after it.
     if marker_parse
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:608:
                 end: seal_start + 1,
                 kind: SpanKind::ProjectNoteMarker,
                 project_note: Some(ProjectNoteForm::Create),
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             };
             if !name.is_empty() {
                 marker_parse.spans.insert(
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:623:
                     end: seal_start + 2,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             insert_caret_separator_span(token, route_part, &mut marker_parse);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1269:
                 end: suffix_start + 2,
                 kind: SpanKind::PomodoroClose,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             if let Some((start, end)) = in_progress {
                 marker_parse.spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1278:
                     end,
                     kind: SpanKind::PomodoroCloseInProgress,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = park {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1288:
                     end,
                     kind: SpanKind::PomodoroClosePark,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = complete {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1298:
                     end,
                     kind: SpanKind::PomodoroCloseComplete,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = drop {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1308:
                     end,
                     kind: SpanKind::PomodoroCloseDrop,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             marker_parse.pomodoro_close = Some(spec);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1338:
                 end: suffix_start + 2,
                 kind: SpanKind::PomodoroClose,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             if let Some((start, end)) = in_progress {
                 marker_parse.spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1347:
                     end,
                     kind: SpanKind::PomodoroCloseInProgress,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = park {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1357:
                     end,
                     kind: SpanKind::PomodoroClosePark,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = complete {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1367:
                     end,
                     kind: SpanKind::PomodoroCloseComplete,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some((start, end)) = drop {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1377:
                     end,
                     kind: SpanKind::PomodoroCloseDrop,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             marker_parse.spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1386:
                 end: separator.1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             marker_parse.pomodoro_close = Some(spec);
             marker_parse.mode = EditorMode::Incomplete;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1565:
         end: seal_start + 1,
         kind: SpanKind::ProjectNoteOfferMarker,
         project_note: Some(ProjectNoteForm::Offer),
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     if !name.is_empty() {
         marker_parse
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1660:
                         end: token.start + end,
                         kind: SpanKind::PomodoroStart,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
             }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1673:
                     end: token.start + end,
                     kind: SpanKind::PomodoroName,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             parsed.spans.sort_by_key(|span| (span.start, span.end));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1733:
                     end: token.start + prefix_hash_rel + 1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some(raw) = raw_suffix {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1752:
                             end: token.start + equals_rel + 1 + suffix.len(),
                             kind: SpanKind::PomodoroStart,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     } else if raw.starts_with('#')
                         || raw.starts_with('@')
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1769:
                                 end: token.start + equals_rel + 1,
                                 kind: SpanKind::PomodoroStart,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                     }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1787:
                                 + timing_text.len(),
                             kind: SpanKind::PomodoroStart,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                     let effective = effective_start_timing(&suffix, &timing);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1821:
                             end: token.start + hash_rel + 1,
                             kind: SpanKind::InteractivePlaceholder,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1840:
                     end: token.start + hash + 1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if equals_rel < hash && raw_suffix.is_none() {
                     extra_spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1849:
                         end: token.start + hash,
                         kind: SpanKind::PomodoroStart,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
             }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1928:
                     end: token.start + equals_rel + 1 + suffix_len,
                     kind: SpanKind::PomodoroStart,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             } else {
                 parsed.spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1937:
                     end: token.start + equals_rel + 1,
                     kind: SpanKind::PomodoroStart,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             // Name span (bare or hash, `#` itself never in a span).
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1953:
                     end: name_start + name_text.len(),
                     kind: SpanKind::PomodoroName,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             // Placeholder on the dangling `@` (last byte).
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:1964:
                 end: token.start + at_rel + 1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             parsed.spans.sort_by_key(|span| (span.start, span.end));
             parsed.mode = EditorMode::Incomplete;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:2010:
                     end: token.end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 }],
                 requires_body: false,
                 pomodoro_start: None,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:2032:
                 end: token.end,
                 kind: SpanKind::Route,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             requires_body: true,
             pomodoro_start: None,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:2136:
                 end: right_start,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
     } else {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:2168:
                 end: third_start,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         } else {
             spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_classify.rs:2177:
                 end: content_end,
                 kind: third.kind,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
     }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:787:
                 end: token.end,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             diagnostics: Vec::new(),
             sub_bullets: Vec::new(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:836:
                 end: token.end,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             diagnostics: Vec::new(),
             sub_bullets: Vec::new(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:910:
                 end,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             Vec::new(),
         )),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:935:
                         end: dependency.start + 1,
                         kind: SpanKind::TaskCompleteSigil,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                     Span {
                         start: dependency.start + 1,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:943:
                         end: dependency.block_start - 1,
                         kind: SpanKind::TaskCompleteNote,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                     Span {
                         start: dependency.block_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:951:
                         end: dependency.block_end,
                         kind: SpanKind::TaskCompleteBlockId,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                 ],
                 Vec::new(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:1037:
         end: token.end,
         kind: SpanKind::InteractivePlaceholder,
         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     });
     spans.sort_by_key(|span| (span.start, span.end));
     Some(EditorItemOutcome {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:1151:
                     end: token.end,
                     kind: SpanKind::RefUrl,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 }],
                 diagnostics: Vec::new(),
                 sub_bullets: Vec::new(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:1207:
                         end: url_token.end,
                         kind: SpanKind::RefUrl,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                     Span {
                         start: route_token.start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:1215:
                         end: route_token.end,
                         kind: SpanKind::Route,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                 ],
                 diagnostics: Vec::new(),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2131:
                             end: token.end,
                             kind: SpanKind::InteractivePlaceholder,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2152:
                                 end: token.start + 1,
                                 kind: SpanKind::ProjectTaskLinkMarker,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                         spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2161:
                             end: token.end,
                             kind: SpanKind::ProjectTaskBlockId,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2248:
                     end: route_end,
                     kind: SpanKind::ActiveTaskRoute,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: route_end + 1,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2256:
                     end: token_start + link_end,
                     kind: SpanKind::ActiveTaskBlockId,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if let Some((name_start, name_end)) = name_range
                     && name_end > name_start
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2267:
                         end: token_start + name_end,
                         kind: SpanKind::PomodoroName,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some(offset) = start_offset {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2278:
                             end: token_start + offset + 2,
                             kind: SpanKind::PomodoroClose,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                         if let Some((start, end)) = close_in_progress {
                             spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2287:
                                 end: token_start + end,
                                 kind: SpanKind::PomodoroCloseInProgress,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                         if let Some((start, end)) = close_park {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2297:
                                 end: token_start + end,
                                 kind: SpanKind::PomodoroClosePark,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                         if let Some((start, end)) = close_complete {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2307:
                                 end: token_start + end,
                                 kind: SpanKind::PomodoroCloseComplete,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                         if let Some((start, end)) = close_drop {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2317:
                                 end: token_start + end,
                                 kind: SpanKind::PomodoroCloseDrop,
                                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                title: None,
[m[32m+                                key: None,
[m                             });
                         }
                     } else {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2329:
                                     end: token_start + end,
                                     kind: SpanKind::PomodoroStart,
                                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                                    title: None,
[m[32m+                                    key: None,
[m                                 });
                             }
                         }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2393:
                     end: route_end,
                     kind: SpanKind::ActiveTaskRoute,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: route_end + 1,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2401:
                     end: token_start + link_end,
                     kind: SpanKind::ActiveTaskBlockId,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: token_start + suffix_offset,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2409:
                     end: token_start + suffix_offset + 2,
                     kind: SpanKind::PomodoroClose,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 if let Some((start, end)) = close_in_progress {
                     spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2418:
                         end: token_start + end,
                         kind: SpanKind::PomodoroCloseInProgress,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = close_park {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2428:
                         end: token_start + end,
                         kind: SpanKind::PomodoroClosePark,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = close_complete {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2438:
                         end: token_start + end,
                         kind: SpanKind::PomodoroCloseComplete,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = close_drop {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2448:
                         end: token_start + end,
                         kind: SpanKind::PomodoroCloseDrop,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2457:
                     end: token_start + separator_range.1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 local_destination_markers.push(LocalDestinationMarker {
                     start: token_start,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2544:
                     end: token_end,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             CaretItemKind::NamePartial {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2572:
                     end: route_end,
                     kind: SpanKind::ActiveTaskRoute,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: route_end + 1,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2580:
                     end: token_start + link_end,
                     kind: SpanKind::ActiveTaskBlockId,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 for (start, end) in start_ranges {
                     if end > start {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2590:
                             end: token_start + end,
                             kind: SpanKind::PomodoroStart,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2600:
                     end: token_start + name_range.0,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             CaretItemKind::TimingIncomplete {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2629:
                     end: route_end,
                     kind: SpanKind::ActiveTaskRoute,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: route_end + 1,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2637:
                     end: token_start + timing_link_end,
                     kind: SpanKind::ActiveTaskBlockId,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 for (start, end) in timing_ranges {
                     if end > start {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2647:
                             end: token_start + end,
                             kind: SpanKind::PomodoroStart,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2657:
                     end: token_start + timing_name_range.1,
                     kind: SpanKind::PomodoroName,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.push(Span {
                     start: token_start + separator_range.0,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_parse.rs:2665:
                     end: token_start + separator_range.1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             CaretItemKind::Invalid { message } => {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:58:
         end: token_end,
         kind: span_kind,
         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     let exact = parent_trimmed.len() == prefix_len && item.lines.len() == 1;
     if !exact {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:313:
         end: token_start + prefix_len,
         kind: SpanKind::PomodoroStart,
         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     }];
     if name.is_empty() {
         // Bare tokens never have an empty name; only `=#` uses the
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:326:
                 end: hash_start + 1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
     } else {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:477:
                 end: token_start + timing_offset + 1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             // Add drop span if a valid drop was typed before the dangling `@`.
             if let DropLex::Valid(_, range) = &drop_lex {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:487:
                     end: range.1,
                     kind: SpanKind::PomodoroStartDrop,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 timing_spans.sort_by_key(|span| span.start);
             }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:511:
                 end,
                 kind: SpanKind::PomodoroStart,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             spans.sort_by_key(|span| span.start);
         }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:533:
                     end: range.1,
                     kind: SpanKind::PomodoroStartDrop,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 return Some(editor_named_valid_outcome(
                     item,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:552:
                         end: range.1,
                         kind: SpanKind::PomodoroStartDrop,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:561:
                     end: sep_range.1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 return Some(editor_start_drop_incomplete_outcome(
                     item,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1066:
         },
         kind: SpanKind::PomodoroStart,
         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     enum DropLex {
         None,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1170:
                     end: token_start + timing_offset + 1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 return Some(editor_start_timing_incomplete_outcome(
                     item,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1393:
                     end: range.1,
                     kind: SpanKind::PomodoroStartDrop,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1402:
                 end: sep_range.1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             Some(editor_start_drop_incomplete_outcome(
                 item,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1482:
                         end: token_start + len,
                         kind: SpanKind::PomodoroStart,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     },
                     pomodoro_double_start_error(token_text),
                     Some((token_start, token_start + len)),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1530:
                 end: token_start + first.len(),
                 kind: SpanKind::PomodoroStart,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             },
             pomodoro_double_close_error(first, &close_spelling),
             Some((token_start, token_start + first.len())),
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1552:
                 end: token_start + first.len(),
                 kind: SpanKind::PomodoroClose,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }],
             Vec::new(),
             vec![Diagnostic {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1571:
         end: token_start + 1,
         kind: SpanKind::PomodoroClose,
         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+        title: None,
[m[32m+        key: None,
[m     };
     // `x#…` is a claimed close near miss with a teaching error, whether or
     // not the item carries extra text or child lines. It used to be prose.
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1629:
                         end,
                         kind: SpanKind::PomodoroCloseInProgress,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = lex.park_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1639:
                         end,
                         kind: SpanKind::PomodoroClosePark,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = lex.complete_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1649:
                         end,
                         kind: SpanKind::PomodoroCloseComplete,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = lex.drop_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1659:
                         end,
                         kind: SpanKind::PomodoroCloseDrop,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 return Some(editor_close_outcome(
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1681:
                         end,
                         kind: SpanKind::PomodoroCloseInProgress,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = incomplete.park_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1691:
                         end,
                         kind: SpanKind::PomodoroClosePark,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = incomplete.complete_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1701:
                         end,
                         kind: SpanKind::PomodoroCloseComplete,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 if let Some((start, end)) = incomplete.drop_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1711:
                         end,
                         kind: SpanKind::PomodoroCloseDrop,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1720:
                     end: incomplete.separator_range.1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 return Some(editor_close_outcome(
                     item,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1789:
                             end,
                             kind: SpanKind::PomodoroCloseInProgress,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                     if let Some((start, end)) = incomplete.park_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1799:
                             end,
                             kind: SpanKind::PomodoroClosePark,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                     if let Some((start, end)) = incomplete.complete_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1809:
                             end,
                             kind: SpanKind::PomodoroCloseComplete,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                     if let Some((start, end)) = incomplete.drop_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1819:
                             end,
                             kind: SpanKind::PomodoroCloseDrop,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                     spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1828:
                         end: incomplete.separator_range.1,
                         kind: SpanKind::InteractivePlaceholder,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                     EditorSelection::Incomplete(incomplete, spans)
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1847:
                 end,
                 kind: SpanKind::PomodoroCloseInProgress,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
         if let Some((start, end)) = lex.park_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1857:
                 end,
                 kind: SpanKind::PomodoroClosePark,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
         if let Some((start, end)) = lex.complete_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1867:
                 end,
                 kind: SpanKind::PomodoroCloseComplete,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
         if let Some((start, end)) = lex.drop_range {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1877:
                 end,
                 kind: SpanKind::PomodoroCloseDrop,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
         }
         spans
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1940:
                             end,
                             kind: SpanKind::PomodoroCloseLogIndex,
                             project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                            title: None,
[m[32m+                            key: None,
[m                         });
                     }
                 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:1966:
                         end: dangling.index_range.1,
                         kind: SpanKind::InteractivePlaceholder,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 base_spans.sort_by_key(|span| (span.start, span.end));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:2110:
                     end: index_range.1,
                     kind: SpanKind::InteractivePlaceholder,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
                 spans.sort_by_key(|span| (span.start, span.end));
                 return Some(editor_close_outcome(
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:2134:
                 end: index_range.1,
                 kind: SpanKind::InteractivePlaceholder,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             });
             base_spans.sort_by_key(|span| (span.start, span.end));
             let mut spec =
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:2179:
                         end,
                         kind: SpanKind::PomodoroCloseLogIndex,
                         project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                        title: None,
[m[32m+                        key: None,
[m                     });
                 }
                 spans.sort_by_key(|span| (span.start, span.end));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/editor_pomodoro.rs:2205:
                     end,
                     kind: SpanKind::PomodoroCloseLogIndex,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             base_spans.sort_by_key(|span| (span.start, span.end));
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/mod.rs:110:
 pub(crate) use self::model::ClipRequest;
 pub(crate) use self::model::CloseLogEntry;
 pub(crate) use self::model::CloseLogOrigin;
[32m+pub(crate) use self::model::DrawerSelector;
[m pub(crate) use self::model::EditorParseOptions;
 pub(crate) use self::model::ParsedCaptureDraft;
 pub(crate) use self::model::ParsedCaptureItem;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/mod.rs:127:
 pub(crate) use self::model::ProjectTaskId;
 pub(crate) use self::model::RefParentSource;
 pub(crate) use self::model::SubBulletTarget;
[31m-pub(crate) use self::model::DrawerSelector;
[m pub(crate) use self::model::TaskToggleIntent;
 pub(crate) use self::model::TemplateRowSummary;
 pub(crate) use self::pomodoro_literal::canonicalize_exact_name;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/pomodoro_literal.rs:127:
 /// names nothing valid.
 pub(crate) fn canonicalize_exact_name(decoded: &str) -> Option<String> {
     let name = super::line::normalize_task_text(decoded).to_ascii_uppercase();
[31m-    crate::native::capture_drawers::is_pomodoro_name(&name)
[m[31m-        .then_some(name)
[m[32m+    crate::native::capture_drawers::is_pomodoro_name(&name).then_some(name)
[m }
 
 /// Extend a whitespace-delimited link token through an exact-name
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/tokens.rs:127:
                     .to_string(),
             );
         }
[31m-        Some(selector)
[m[31m-            if opens_exact_name(selector) =>
[m[31m-        {
[m[32m+        Some(selector) if opens_exact_name(selector) => {
[m             let Some(lex) = lex_exact_name_after_hash(selector, selector.len())
             else {
                 return Err(
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/tokens.rs:244:
         return Some(EXPLICIT_TOGGLE_REPEATED_ERROR);
     }
     if after_at.contains('#') {
[31m-        return Some("`!` takes no drawer: write `@route+id!` without a `#drawer`");
[m[32m+        return Some(
[m[32m+            "`!` takes no drawer: write `@route+id!` without a `#drawer`",
[m[32m+        );
[m     }
     Some(EXPLICIT_TOGGLE_ONLY_MARKER_ERROR)
 }
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/type_marker.rs:128:
             index += char_len(body, index);
             continue;
         }
[31m-fn is_glued_drawer_or_r3_hash(body: &str, sigil: usize) -> bool {
[m[31m-    // Find the whitespace-delimited token containing this `#`.
[m[31m-    let token_start = body[..sigil]
[m[31m-        .rfind(|c: char| c.is_whitespace())
[m[31m-        .map(|i| i + 1)
[m[31m-        .unwrap_or(0);
[m[31m-    let token_end = body[sigil..]
[m[31m-        .find(|c: char| c.is_whitespace())
[m[31m-        .map(|i| sigil + i)
[m[31m-        .unwrap_or(body.len());
[m[31m-    let token = &body[token_start..token_end];
[m[31m-    let Some(at_pos) = token.find('@') else {
[m[31m-        return false;
[m[31m-    };
[m[31m-    let hash_in_token = match token.find('#') {
[m[31m-        Some(pos) => token_start + pos == sigil,
[m[31m-        None => false,
[m[31m-    };
[m[31m-    if !hash_in_token {
[m[31m-        return false;
[m[31m-    }
[m[31m-    // Token starts with `@` (possibly after leading chars?) and contains
[m[31m-    // `+` or `^` before the `#`. For `@dev+id#now!`, token is
[m[31m-    // `@dev+id#now!`, which has `+` before `#`.
[m[31m-    let before_hash = &token[..token.find('#').unwrap_or(0)];
[m[31m-    (before_hash.contains('+') || before_hash.contains('^'))
[m[31m-        && at_pos == 0
[m[31m-}
[m[32m+        fn is_glued_drawer_or_r3_hash(body: &str, sigil: usize) -> bool {
[m[32m+            // Find the whitespace-delimited token containing this `#`.
[m[32m+            let token_start = body[..sigil]
[m[32m+                .rfind(|c: char| c.is_whitespace())
[m[32m+                .map(|i| i + 1)
[m[32m+                .unwrap_or(0);
[m[32m+            let token_end = body[sigil..]
[m[32m+                .find(|c: char| c.is_whitespace())
[m[32m+                .map(|i| sigil + i)
[m[32m+                .unwrap_or(body.len());
[m[32m+            let token = &body[token_start..token_end];
[m[32m+            let Some(at_pos) = token.find('@') else {
[m[32m+                return false;
[m[32m+            };
[m[32m+            let hash_in_token = match token.find('#') {
[m[32m+                Some(pos) => token_start + pos == sigil,
[m[32m+                None => false,
[m[32m+            };
[m[32m+            if !hash_in_token {
[m[32m+                return false;
[m[32m+            }
[m[32m+            // Token starts with `@` (possibly after leading chars?) and contains
[m[32m+            // `+` or `^` before the `#`. For `@dev+id#now!`, token is
[m[32m+            // `@dev+id#now!`, which has `+` before `#`.
[m[32m+            let before_hash = &token[..token.find('#').unwrap_or(0)];
[m[32m+            (before_hash.contains('+') || before_hash.contains('^'))
[m[32m+                && at_pos == 0
[m[32m+        }
[m 
         // A glued `#` after `@route+id` or `@route^id` is a drawer or R3,
         // never a type marker. Skip it here; drawer parsing owns it.
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_language/type_marker.rs:1101:
             use super::model::SubBulletTarget;
             matches!(
                 target,
[31m-                SubBulletTarget::BlockId(_)
[m[31m-                    | SubBulletTarget::Ref { .. }
[m[32m+                SubBulletTarget::BlockId(_) | SubBulletTarget::Ref { .. }
[m             )
         }
         _ => false,
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_pomodoros.rs:19:
         duration_from_range_text, leading_spaces_or_tabs_len, line_spans,
         list_item_body, nearest_shallower_list_item_parent, LineSpan,
     },
[31m-    capture_language, capture_pomodoro_close, capture_pomodoros_agenda,
[m[31m-    capture_drawers, config, env as bob_env, markdown, note_tasks,
[m[32m+    capture_drawers, capture_language, capture_pomodoro_close,
[m[32m+    capture_pomodoros_agenda, config, env as bob_env, markdown, note_tasks,
[m     plan_budget, pomodoro, pomodoro_homes,
     pomodoro_themes::{Catalog as ThemeCatalog, ThemeRef},
     style::{display_width, pad_right, Styler},
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_task_wikilinks.rs:112:
                 end: token.opener + 2,
                 kind: SpanKind::WikilinkTaskDelimiter,
                 project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                title: None,
[m[32m+                key: None,
[m             }];
             if token.query_end > token.opener + 2 {
                 spans.push(Span {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_task_wikilinks.rs:121:
                     end: token.query_end,
                     kind: SpanKind::WikilinkTaskQuery,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             if let Some(closer) = token.closer {
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_task_wikilinks.rs:131:
                     end: closer + 2,
                     kind: SpanKind::WikilinkTaskDelimiter,
                     project_note: None,
[31m-            title: None,
[m[31m-            key: None,
[m[32m+                    title: None,
[m[32m+                    key: None,
[m                 });
             }
             spans
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/completion/context.rs:248:
         let task = context(&["capture", "--route", "cash", "--task", "abc"]);
         assert_eq!(task.task.as_deref(), Some("abc"));
 
[31m-        let block_id =
[m[31m-            context(&["capture-drawers", "-r", "cash", "-i", "abc"]);
[m[32m+        let block_id = context(&["capture-drawers", "-r", "cash", "-i", "abc"]);
[m         assert_eq!(block_id.task.as_deref(), Some("abc"));
 
         let repo = context(&["plugins", "sync", "--repo", "/tmp/repo"]);
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/completion/providers.rs:15:
 
 use super::{context::Context, kinds::Kind, protocol};
 use crate::native::{
[31m-    capture, capture_pomodoros, capture_targets, capture_drawers, config,
[m[32m+    capture, capture_drawers, capture_pomodoros, capture_targets, config,
[m     note_tasks, pomodoro,
 };
 
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native.rs:23:
 mod capture_completable_tasks;
 mod capture_complete;
 mod capture_dependency_tasks;
[32m+mod capture_drawers;
[m mod capture_flag_guard;
 mod capture_language;
 mod capture_link_tasks;
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native.rs:40:
 mod capture_sections;
 mod capture_targets;
 mod capture_task_id;
[31m-mod capture_drawers;
[m mod capture_task_toggle;
 mod capture_task_wikilinks;
 mod capture_tasks;
error: Recipe `check` failed on line 78 with exit code 1
failed  exit=1  duration=12350ms
verdict: undetermined; exit 1

