# Chat History - ace-run (bob-cli-u.land--mon)

- **TIMESTAMP:** 2026-08-15 11:32:14 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** bob-cli-u.land--mon

## Prompt

sase monitor start --command 'just all && just check-scripts && just package-list && cd sase/repos/linked/bob-mac-capture && git diff --check && bash -n Tests/Fixtures/fake-bob && swift build --target CaptureCore' --reason 'Revalidate both repositories before planning the remaining bob-cli-u landing fixes'

## Response


🎨  FORMAT
────────────────────────────────────────────────
cargo fmt --check
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead
Warning: Unknown configuration option `license_template_path`
Warning: Unknown configuration option `report_fixme`
Warning: Unknown configuration option `report_todo`
Warning: can't set `indent_style = Block`, unstable features are only available in nightly channel.
Warning: can't set `wrap_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `format_code_in_doc_comments = false`, unstable features are only available in nightly channel.
Warning: can't set `comment_width = 80`, unstable features are only available in nightly channel.
Warning: can't set `normalize_comments = true`, unstable features are only available in nightly channel.
Warning: can't set `normalize_doc_attributes = false`, unstable features are only available in nightly channel.
Warning: can't set `format_strings = true`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_matchers = false`, unstable features are only available in nightly channel.
Warning: can't set `format_macro_bodies = true`, unstable features are only available in nightly channel.
Warning: can't set `empty_item_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `struct_lit_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `fn_single_line = true`, unstable features are only available in nightly channel.
Warning: can't set `where_single_line = false`, unstable features are only available in nightly channel.
Warning: can't set `imports_indent = Block`, unstable features are only available in nightly channel.
Warning: can't set `imports_layout = Mixed`, unstable features are only available in nightly channel.
Warning: can't set `merge_imports = false`, unstable features are only available in nightly channel.
Warning: can't set `reorder_impl_items = false`, unstable features are only available in nightly channel.
Warning: can't set `type_punctuation_density = Wide`, unstable features are only available in nightly channel.
Warning: can't set `space_before_colon = false`, unstable features are only available in nightly channel.
Warning: can't set `space_after_colon = true`, unstable features are only available in nightly channel.
Warning: can't set `spaces_around_ranges = false`, unstable features are only available in nightly channel.
Warning: can't set `binop_separator = Front`, unstable features are only available in nightly channel.
Warning: can't set `combine_control_expr = true`, unstable features are only available in nightly channel.
Warning: can't set `overflow_delimited_expr = false`, unstable features are only available in nightly channel.
Warning: can't set `struct_field_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `enum_discrim_align_threshold = 0`, unstable features are only available in nightly channel.
Warning: can't set `match_arm_blocks = true`, unstable features are only available in nightly channel.
Warning: can't set `force_multiline_blocks = false`, unstable features are only available in nightly channel.
Warning: can't set `brace_style = SameLineWhere`, unstable features are only available in nightly channel.
Warning: can't set `control_brace_style = AlwaysSameLine`, unstable features are only available in nightly channel.
Warning: can't set `trailing_semicolon = true`, unstable features are only available in nightly channel.
Warning: can't set `trailing_comma = Vertical`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_upper_bound = 2`, unstable features are only available in nightly channel.
Warning: can't set `blank_lines_lower_bound = 0`, unstable features are only available in nightly channel.
Warning: can't set `version = One`, unstable features are only available in nightly channel.
Warning: can't set `inline_attribute_width = 0`, unstable features are only available in nightly channel.
Warning: can't set `condense_wildcard_suffixes = false`, unstable features are only available in nightly channel.
Warning: can't set `color = Auto`, unstable features are only available in nightly channel.
Warning: can't set `required_version = "1.4.9"`, unstable features are only available in nightly channel.
Warning: can't set `unstable_features = true`, unstable features are only available in nightly channel.
Warning: can't set `skip_children = false`, unstable features are only available in nightly channel.
Warning: can't set `hide_parse_errors = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_line_overflow = false`, unstable features are only available in nightly channel.
Warning: can't set `error_on_unformatted = false`, unstable features are only available in nightly channel.
Warning: can't set `ignore = IgnoreList { path_set: {}, rustfmt_toml_path: "" }`, unstable features are only available in nightly channel.
Warning: can't set `emit_mode = Files`, unstable features are only available in nightly channel.
Warning: can't set `make_backup = false`, unstable features are only available in nightly channel.
Warning: the `fn_args_layout` option is deprecated. Use `fn_params_layout`. instead

🔍  LINT
────────────────────────────────────────────────
cargo clippy --all-targets --all-features
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12)
warning: this `if` statement can be collapsed
   --> src/native/plugins.rs:782:13
    |
782 | /             if let Some(parent) = backup_file.parent() {
783 | |                 if let Err(error) = fs::create_dir_all(parent) {
784 | |                     return Ok(FileOutcome {
785 | |                         action: FileAction::Failed,
...   |
794 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.97.0/index.html#collapsible_if
    = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
    |
782 ~             if let Some(parent) = backup_file.parent()
783 ~                 && let Err(error) = fs::create_dir_all(parent) {
784 |                     return Ok(FileOutcome {
...
792 |                     });
793 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/plugins.rs:814:9
    |
814 | /         if let Some(parent) = vault_file.parent() {
815 | |             if let Err(error) = fs::create_dir_all(parent) {
816 | |                 return Ok(FileOutcome {
817 | |                     action: FileAction::Failed,
...   |
825 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.97.0/index.html#collapsible_if
help: collapse nested if block
    |
814 ~         if let Some(parent) = vault_file.parent()
815 ~             && let Err(error) = fs::create_dir_all(parent) {
816 |                 return Ok(FileOutcome {
...
823 |                 });
824 ~             }
    |

warning: this `let...else` may be rewritten with the `?` operator
    --> src/native/projects.rs:2298:5
     |
2298 | /     let Some(&(line_number, raw_value)) = fields.first() else {
2299 | |         return None;
2300 | |     };
     | |______^ help: replace it with: `let &(line_number, raw_value) = fields.first()?;`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.97.0/index.html#question_mark
     = note: `#[warn(clippy::question_mark)]` on by default

warning: `bob-cli` (lib) generated 3 warnings (run `cargo clippy --fix --lib -p bob-cli -- ` to apply 2 suggestions)
warning: `bob-cli` (lib test) generated 3 warnings (3 duplicates)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 7.79s

🧪  TEST
────────────────────────────────────────────────
cargo test
   Compiling bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 13.50s
     Running unittests src/lib.rs (target/debug/deps/bob_cli-8aca5d667208953a)

running 578 tests
test native::capture::tests::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::clip_markers_are_terminal_forgiving_and_can_be_disabled ... ok
test native::capture::tests::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::forced_route_rejects_terminal_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::formats_bullet_line ... ok
test native::capture::tests::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::formats_scheduled_date_from_offset ... ok
test native::capture::tests::formats_sub_bullet_line ... ok
test native::capture::tests::formats_task_line ... ok
test native::capture::tests::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::inserts_after_single_top_level_task ... ok
test native::capture::tests::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::json_success_shape_is_stable ... ok
test native::capture::tests::legacy_standalone_bullet_markers_are_rejected ... ok
test native::capture::tests::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::normalizes_whitespace ... ok
test native::capture::tests::parses_picker_task_refs_strictly ... ok
test native::capture::tests::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::parses_priority_tokens ... ok
test native::capture::tests::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::parses_schedule_tokens ... ok
test native::capture::tests::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::tests::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::zeroth_section_insertion_after_frontmatter ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_clip::tests::formats_headers ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_complete::tests::empty_json_context_is_null ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::capture_complete::tests::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::json_shape_is_stable ... ok
test native::capture_complete::tests::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_complete::tests::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture_complete::tests::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_language::tests::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_complete::tests::task_block_id_completion_offers_routes_but_not_authored_ids ... ok
test native::capture_language::tests::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_complete::tests::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_language::tests::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_complete::tests::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_language::tests::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_language::tests::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_complete::tests::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_language::tests::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::capture_language::tests::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::capture_language::tests::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_complete::tests::default_task_completion_stays_identified_only ... ok
test native::capture_language::tests::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_reports_legacy_bullet_markers_without_failing ... ok
test native::capture_language::tests::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_complete::tests::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_complete::tests::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture_language::tests::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_complete::tests::all_tasks_search_keeps_identified_groups_ahead_of_unidentified ... ok
test native::capture_language::tests::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_complete::tests::all_tasks_does_not_change_pomodoro_completion ... ok
test native::capture_complete::tests::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_language::tests::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_complete::tests::all_tasks_lists_identified_tasks_before_unidentified_tasks ... ok
test native::capture_language::tests::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_complete::tests::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_language::tests::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::task_block_id_route_completes_but_authored_id_does_not ... ok
test native::capture_language::tests::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::split_capture_items_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_language::tests::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::collect_done::tests::adds_done_tasks_to_existing_source_frontmatter ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::collect_done::tests::block_ids_are_only_end_of_line_obsidian_anchors ... ok
test native::collect_done::tests::completed_child_moves_without_collecting_active_parent ... ok
test native::collect_done::tests::creates_archive_frontmatter_for_new_archive_note ... ok
test native::collect_done::tests::already_linked_source_with_existing_archive_is_not_planned ... ok
test native::collect_done::tests::block_id_deduplication_preserves_crlf_line_endings ... ok
test native::collect_done::tests::canceled_only_tasks_below_threshold_remain_in_source ... ok
test native::collect_done::tests::creates_archive_frontmatter_with_nested_source_parent ... ok
test native::collect_done::tests::creates_source_frontmatter_for_done_tasks ... ok
test native::collect_done::tests::adds_archive_parent_to_existing_frontmatter ... ok
test native::collect_done::tests::canceled_only_tasks_move_when_threshold_is_met ... ok
test native::collect_done::tests::dependency_ids_preserve_path_case_and_qualify_nested_notes ... ok
test native::collect_done::tests::collecting_tasks_adds_done_tasks_to_source ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::collect_done::tests::duplicate_moved_block_ids_are_ambiguous ... ok
test native::collect_done::tests::below_threshold_block_ids_do_not_trigger_link_repair ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::collect_done::tests::duplicate_moved_block_ids_become_unique_archive_ids ... ok
test native::collect_done::tests::duplicate_moved_block_ids_do_not_rewrite_links ... ok
test native::collect_done::tests::extracts_block_ids_from_every_moved_task_block_line ... ok
test native::collect_done::tests::extracts_nested_blocks_and_continuations ... ok
test native::collect_done::tests::existing_archive_with_stale_metadata_creates_archive_only_plan ... ok
test native::collect_done::tests::inserts_missing_archive_type_frontmatter ... ok
test native::collect_done::tests::existing_archive_creates_metadata_only_source_update ... ok
test native::collect_done::tests::leaves_correct_archive_frontmatter_unchanged ... ok
test native::collect_done::tests::leaves_correct_done_tasks_frontmatter_unchanged ... ok
test native::collect_done::tests::includes_nested_path_note_when_it_meets_threshold ... ok
test native::collect_done::tests::maps_archive_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::maps_source_notes_to_obsidian_wiki_links ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::collect_done::tests::parses_attached_short_threshold_option ... ok
test native::collect_done::tests::parses_default_threshold ... ok
test native::collect_done::tests::maps_source_notes_to_archive_notes ... ok
test native::collect_done::tests::parses_short_threshold_equals_option ... ok
test native::collect_done::tests::missing_archive_without_threshold_tasks_is_not_planned ... ok
test native::collect_done::tests::parses_short_threshold_option ... ok
test native::collect_done::tests::parses_threshold_equals_option ... ok
test native::collect_done::tests::parses_threshold_option ... ok
test native::collect_done::tests::prepends_archive_frontmatter_when_existing_note_has_none ... ok
test native::collect_done::tests::preserves_crlf_when_adding_done_tasks_frontmatter ... ok
test native::collect_done::tests::preserves_crlf_when_repairing_archive_frontmatter ... ok
test native::collect_done::tests::preserves_line_endings_in_source_and_archive ... ok
test native::collect_done::tests::recognizes_done_and_canceled_task_lines_only ... ok
test native::collect_done::tests::rejects_zero_threshold ... ok
test native::collect_done::tests::replaces_stale_archive_type_frontmatter ... ok
test native::collect_done::tests::replaces_stale_done_tasks_frontmatter ... ok
test native::collect_done::tests::updates_existing_archive_parent_frontmatter ... ok
test native::collect_done::tests::unqualifiable_paths_do_not_abort_identity_indexing ... ok
test native::collect_done::tests::task_moving_plan_writes_archive_with_nested_source_parent ... ok
test native::collect_done::tests::source_block_id_keeps_links_pointing_at_source ... ok
test native::collect_done::tests::scans_markdown_files_with_exclusions_and_threshold ... ok
test native::config::tests::rejects_missing_priority_property ... ok
test native::config::tests::rejects_blank_label ... ok
test native::config::tests::rejects_empty_levels ... ok
test native::config::tests::parses_deployed_config ... ok
test native::config::tests::rejects_missing_schedules ... ok
test native::config::tests::rejects_blank_value ... ok
test native::collect_done::tests::markdown_repair_skips_wikilink_spans ... ok
test native::collect_done::tests::repairs_simple_markdown_inline_block_links ... ok
test native::collect_done::tests::leaves_ambiguous_basename_links_unchanged ... ok
test native::collect_done::tests::existing_archive_block_ids_reserve_original_ids ... ok
test native::collect_done::tests::planned_source_and_archive_contents_are_link_repaired ... ok
test native::collect_done::tests::block_id_suffix_selection_preserves_distinct_moved_ids ... ok
test native::collect_done::tests::task_moving_plan_repairs_links_in_separate_notes ... ok
test native::collect_done::tests::generated_and_template_directories_are_not_collected_or_repaired ... ok
test native::collect_done::tests::self_heals_preexisting_block_links_to_archive ... ok
test native::collect_done::tests::block_id_suffix_selection_skips_existing_candidates ... ok
test native::collect_done::tests::dependency_metadata_repair_rewrites_exact_tokens_only ... ok
test native::config::tests::rejects_negative_min_days ... ok
test native::collect_done::tests::link_repair_scan_includes_done_notes ... ok
test native::config::tests::roll_offset_p4_window_hits_both_extremes ... ok
test native::collect_done::tests::repairs_same_note_nested_and_unique_basename_links ... ok
test native::config::tests::roll_offset_returns_fixed_value_when_min_equals_max ... ok
test native::collect_done::tests::link_repair_uses_renamed_unique_moved_block_id ... ok
test native::collect_done::tests::repairs_wikilinks_embeds_and_aliases_to_moved_blocks ... ok
test native::config::tests::rejects_missing_value ... ok
test native::dataview::tasks::filter::tests::global_filter_removal_only_removes_the_first_occurrence ... ok
test native::collect_done::tests::dependency_metadata_repair_supports_task_field_grammar_and_skips_code ... ok
test native::dataview::tasks::filter::tests::absolute_ranges_are_inclusive_and_order_independent ... ok
test native::config::tests::rejects_min_greater_than_max ... ok
test native::dataview::tasks::filter::tests::numbered_ranges_cover_year_month_quarter_and_iso_week ... ok
test native::config::tests::tolerates_unusual_sibling_properties ... ok
test native::dataview::tasks::filter::tests::relative_ranges_use_iso_weeks_and_calendar_boundaries ... ok
test native::dataview::tasks::filter::tests::weekday_and_offset_dates_are_pinned_to_now ... ok
test native::config::tests::resolve_config_path_expands_tilde_in_xdg_config_home ... ok
test native::config::tests::resolve_config_path_falls_back_to_home_dot_config ... ok
test native::dataview::tasks::index::tests::heading_parser_supports_atx_and_setext_headings ... ok
test native::collect_done::tests::self_healing_is_idempotent_after_links_are_repaired ... ok
test native::collect_done::tests::generated_tag_pages_do_not_make_source_basename_ambiguous ... ok
test native::config::tests::rejects_non_integer_min_days ... ok
test native::config::tests::resolve_config_path_falls_back_to_xdg_config_home ... ok
test native::dataview::tasks::parse::tests::boolean_chains_use_tasks_precedence_and_allow_operand_apostrophes ... ok
test native::config::tests::resolve_config_path_ignores_empty_env_values ... ok
test native::dataview::tasks::parse::tests::numbered_date_ranges_optional_priority_is_and_status_boundary_parse ... ok
test native::dataview::tasks::parse::tests::parses_every_v8_sort_group_and_layout_key ... ok
test native::collect_done::tests::task_moves_repair_dependency_ids_in_archive_and_all_dependents ... ok
test native::dataview::tasks::parse::tests::rejects_malformed_filters_with_actionable_errors ... ok
test native::dataview::tasks::parse::tests::parses_every_filter_family_and_boolean_combinations ... ok
test native::dataview::tasks::task::tests::file_context_matches_tasks_expose_properties ... ok
test native::config::tests::rejects_value_containing_field_syntax ... ok
test native::dataview::tasks::task::tests::recurrence_rules_are_validated_and_standardized ... ok
test native::dataview::tasks::task::tests::removing_global_filter_preserves_spacing_and_only_removes_first_word ... ok
test native::dataview::tasks::task::tests::task_line_parser_matches_tasks_markers_and_spacing ... ok
test native::dataview::tasks::parse::tests::scanner_matches_tasks_line_continuation_rules ... ok
test native::dataview::tasks::task::tests::urgency_due_scheduled_and_start_boundaries_match_tasks_v8 ... ok
test native::dataview::tasks::parse::tests::ignore_global_query_can_come_from_query_file_defaults ... ok
test native::dataview::tasks::result::tests::explanations_include_expanded_preset_statements ... ok
test native::dataview::tests::dql_missing_table_identities_warn_per_row ... ok
test native::dataview::tests::dql_table_paths_use_first_identity_column ... ok
test native::dataview::tests::dql_task_paths_resolve_grouped_task_source_notes ... ok
test native::dataview::tasks::result::tests::natural_collation_is_case_insensitive_and_numeric ... ok
test native::dataview::tests::native_dql_parser_reports_representative_invalid_queries ... ok
test native::dataview::tests::native_dql_parser_accepts_phase3_command_surface ... ok
test native::dataview::tests::source_paths_are_normalized_and_deduplicated ... ok
test native::config::tests::resolve_config_path_prefers_bob_config_file ... ok
test native::dataview::tests::native_source_parser_accepts_phase3_source_surface ... ok
test native::dataview::tasks::settings::tests::unknown_task_format_falls_back_to_emoji ... ok
test native::config::tests::rejects_wrong_schedules_target ... ok
test native::highlights_ref::create::tests::marker_rejects_wikilink_parent_and_unknown_status ... ok
test native::highlights_ref::create::tests::plan_derives_ref_type_output_and_valid_marker ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_from_nested_blockquotes_and_callouts ... ok
test native::highlights_ref::create::tests::plan_embeds_markdown_stem_id_when_opted_in ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_library_pdf_even_with_force ... ok
test native::highlights_ref::create::tests::title_prefers_frontmatter_then_h1_then_stem ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_library_sidecar ... ok
test native::dataview::tests::dql_grouped_table_rows_warn_and_fail_when_strict ... ok
test native::highlights_ref::tests::annotation_task_route_suffix_is_strict_and_stripped_from_identity ... ok
test native::highlights_ref::create::tests::plan_refuses_highlights_markdown_sidecar_even_with_force ... ok
test native::dataview::tests::dql_list_paths_use_list_pair_identity ... ok
test native::highlights_ref::tests::frontmatter_projection_uses_marker_fields_without_fallback_parent ... ok
test native::highlights_ref::tests::frontmatter_projection_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::annotation_block_id_is_stable_across_space_wrapping ... ok
test native::highlights_ref::tests::frontmatter_render_preserves_unmanaged_keys ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_pdf_without_force ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_ready_reopens_terminal_to_ready ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_promotes_ready_and_back ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_with_heading_context ... ok
test native::highlights_ref::tests::highlights_ref_task_line_parser_rejects_malformed_and_duplicate_tasks ... ok
test native::highlights_ref::tests::highlights_ref_task_line_parser_recognizes_generated_pdf_task ... ok
test native::highlights_ref::tests::marker_content_decoder_preserves_pdfdoc_line_separators ... ok
test native::highlights_ref::tests::linked_sidecar_parser_keeps_wrapped_quotes_and_marker_mirror ... ok
test native::highlights_ref::tests::linked_sidecar_parser_strips_comment_bullet_markers ... ok
test native::highlights_ref::tests::marker_parser_accepts_yaml_subset_and_normalizes_keys ... ok
test native::highlights_ref::tests::annotation_task_candidate_records_route_and_processed_id ... ok
test native::highlights_ref::tests::marker_parser_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::deprecated_statuses_normalize_for_synced_inputs ... ok
test native::highlights_ref::tests::highlights_ref_task_checkbox_rewrite_and_dirty_allowance_are_narrow ... ok
test native::highlights_ref::tests::marker_parser_rejects_linked_parent_targets ... ok
test native::highlights_ref::tests::image_block_id_is_stable_across_asset_renames ... ok
test native::highlights_ref::tests::marker_renderer_rejects_unrepresentable_parent_links ... ok
test native::highlights_ref::tests::marker_parser_rejects_missing_required_keys_type_and_duplicate_status ... ok
test native::highlights_ref::tests::marker_renderer_uses_stable_key_order ... ok
test native::highlights_ref::tests::annotation_task_candidates_extract_from_comments_and_notes ... ok
test native::highlights_ref::tests::pdf_path_metadata_derives_nested_reference_paths ... ok
test native::highlights_ref::tests::missing_image_asset_error_points_at_textbundle_export ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_conflicts_with_competing_edit ... ok
test native::highlights_ref::tests::parent_canonicalization_rejects_non_scalar_values ... ok
test native::highlights_ref::tests::pdf_text_artifact_cleanup_normalizes_extraction_noise ... ok
test native::dataview::tasks::parse::tests::composes_global_defaults_presets_and_placeholders_in_order ... ok
test native::highlights_ref::tests::pipeline_fields_exclude_marker_user_projection ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_contributes_abandoned ... ok
test native::highlights_ref::tests::annotation_task_insertion_is_idempotent_and_preserves_existing_states ... ok
test native::highlights_ref::tests::processed_task_index_legacy_ht_backlink_blocks_edited_recreation ... ok
test native::highlights_ref::tests::plan_xlib_intake_maps_nested_paths_and_companions ... ok
test native::dataview::tasks::filter::tests::regex_flags_match_javascript_filtering_behavior ... ok
test native::highlights_ref::tests::plan_xlib_intake_reports_every_destination_conflict ... ok
test native::dataview::tasks::task::tests::invalid_dates_and_recurrences_match_tasks_semantics ... ok
test native::dataview::tasks::task::tests::metadata_must_be_trailing_but_tags_can_be_interleaved ... ok
test native::highlights_ref::tests::beautify_annotation_text_reflows_and_dehyphenates ... ok
test native::dataview::tasks::task::tests::unknown_status_is_todo_and_remove_global_filter_is_display_only ... ok
test native::highlights_ref::tests::sidecar_page_heading_extracts_linked_page_label ... ok
test native::highlights_ref::tests::render_sidecar_highlights_beautifies_callout_text ... ok
test native::dataview::tasks::task::tests::urgency_matches_tasks_v8_coefficients ... ok
test native::dataview::tasks::task::tests::dataview_fields_honor_delimiters_whitespace_commas_and_case ... ok
test native::dataview::tasks::task::tests::dataview_parser_extracts_all_fields_and_cleans_description ... ok
test native::highlights_ref::tests::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::tests::sidecar_parser_extracts_image_annotations_and_leaves_non_images_as_notes ... ok
test native::highlights_ref::tests::rendered_annotation_blocks_do_not_include_source_task_anchors ... ok
test native::highlights_ref::tests::render_sidecar_highlights_renders_image_assets_and_tasks ... ok
test native::highlights_ref::tests::processed_task_index_legacy_identity_blocks_recreation ... ok
test native::highlights_ref::tests::beautify_annotation_text_preserves_list_structure ... ok
test native::highlights_ref::tests::simple_sidecar_unlabeled_text_after_quote_remains_comment ... ok
test native::highlights_ref::tests::validate_library_layout_rejects_equal_and_nested_paths ... ok
test native::highlights_ref::tests::projection_snapshot_json_round_trips_compact_user_projection ... ok
test native::highlights_ref::tests::projection_three_way_merge_handles_compatible_changes ... ok
test native::highlights_ref::tests::status_validation_rejects_unsupported_and_non_scalar_values ... ok
test native::highlights_ref::tests::relative_config_paths_resolve_under_bob_dir ... ok
test native::highlights_ref::tests::projection_three_way_merge_handles_deletes_and_conflicts ... ok
test native::note_tasks::tests::block_id_lookup_distinguishes_found_non_task_duplicate_and_missing ... ok
test native::note_tasks::tests::computes_child_spans_for_mixed_indentation_blanks_and_eof ... ok
test native::note_tasks::tests::ignores_frontmatter_and_fenced_code_tasks ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_maps_all_lifecycle_states ... ok
test native::note_tasks::tests::refs_resolve_exact_shifted_stale_and_ambiguous_tasks ... ok
test native::highlights_ref::tests::processed_task_index_scans_states_indents_and_done_notes ... ok
test native::note_tasks::tests::gates_on_filter_and_cleans_descriptions_with_sections ... ok
test native::note_tasks::tests::suggests_case_matches_and_unique_nearby_block_ids_only ... ok
test native::note_tasks::tests::reads_real_statuses_and_missing_settings_fall_back_to_defaults ... ok
test native::plugins::tests::sync_reports_text_diff_for_changed_files ... ok
test native::note_tasks::tests::task_refs_parse_strictly_and_round_trip_scan_metadata ... ok
test native::plugins::tests::truncate_adds_ellipsis_only_when_needed ... ok
test native::plugins::tests::sync_only_filters_to_a_single_plugin ... ok
test native::plugins::tests::sync_summarizes_binary_and_minified_diffs ... ok
test native::plugins::tests::unreadable_repo_is_an_error ... ok
test native::plugins::tests::sync_unknown_plugin_is_an_error ... ok
test native::plugins::tests::json_shape_is_stable ... ok
test native::projects::tests::project_changes_insert_subproject_links_after_final_prj_line ... ok
test native::pomodoro::tests::completed_ledger_parser_only_accepts_x_checkbox_entries ... ok
test native::projects::tests::project_changes_replace_status_append_missing_status_and_add_hide_tag ... ok
test native::plugins::tests::vault_state_reads_enabled_disabled_and_not_installed ... ok
test native::pomodoro::tests::open_ledger_parser_requires_an_open_checkbox ... ok
test native::pomodoro::tests::unclosed_frontmatter_delimiter_is_content ... ok
test native::plugins::tests::sync_state_detects_synced_drift_and_missing ... ok
test native::projects::tests::non_project_notes_are_ignored ... ok
test native::projects::tests::project_changes_clean_duplicate_subproject_marker_lines ... ok
test native::projects::tests::project_changes_delete_subproject_line_for_stale_child ... ok
test native::projects::tests::project_changes_insert_subproject_line_above_user_bullets ... ok
test native::plugins::tests::scan_reports_states_and_counts ... ok
test native::projects::tests::project_changes_preserve_crlf_for_subproject_link_insertions ... ok
test native::projects::tests::project_changes_mark_last_child_closed_and_keep_subproject_line ... ok
test native::projects::tests::project_changes_remove_prj_fields_with_adjacent_whitespace ... ok
test native::projects::tests::project_changes_remove_prj_hide_tag_with_crlf ... ok
test native::projects::tests::project_changes_rewrite_subproject_line_in_place ... ok
test native::plugins::tests::sync_dry_run_reports_without_writing ... ok
test native::dataview::tasks::index::tests::fixture_index_builds_hierarchy_and_ignores_fences_and_dot_directories ... ok
test native::plugins::tests::backup_failure_aborts_overwrite ... ok
test native::projects::tests::project_parser_records_prj_sub_block_marker_lines ... ok
test native::projects::tests::project_changes_insert_subproject_links_after_prj_with_tab_indent ... ok
test native::plugins::tests::sync_creates_updates_and_leaves_unchanged ... ok
test native::projects::tests::project_parser_stops_prj_sub_block_at_blank_line ... ok
test native::projects::tests::project_changes_preserve_crlf_when_appending_status ... ok
test native::projects::tests::frontmatter_keys_must_start_at_column_zero ... ok
test native::task_status_hooks::tests::ambiguous_basename_does_not_resolve ... ok
test native::projects::tests::project_parser_marks_unprioritized_prj_as_on_dash ... ok
test native::projects::tests::project_parser_accepts_project_type_variants_and_counts_tasks ... ok
test native::task_status_hooks::tests::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::tests::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::tests::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::projects::tests::render_subprojects_line_formats_closed_children_after_open_children ... ok
test native::projects::tests::schedule_only_issues_still_allow_subproject_aggregation ... ok
test native::projects::tests::wikilink_target_extracts_normalized_note_names ... ok
test native::projects::tests::project_parser_records_scheduled_and_placeholder_prj ... ok
test native::task_status_hooks::tests::dependency_reference_requires_a_sole_transcluded_block_link ... ok
test native::projects::tests::project_parser_splits_surfacing_and_dash_visibility_counts ... ok
test native::task_status_hooks::tests::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::tests::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_hooks::tests::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::projects::tests::task_tag_matches_tasks_plugin_boundaries ... ok
test native::projects::tests::subproject_display_parser_scopes_schedule_and_lifecycle_markers ... ok
test native::projects::tests::scheduled_tasks_keep_subproject_ledger_planning ... ok
test native::task_status_hooks::tests::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::extracts_only_block_links_under_open_pomodoros ... ok
test native::projects::tests::task_schedule_edits_cover_contract_and_preserve_markdown ... ok
test native::projects::tests::project_sync_plan_keeps_canonical_closed_subprojects_idempotent ... ok
test native::config::tests::roll_offset_stays_within_bounds_for_many_seeds ... ok
test native::projects::tests::project_sync_plan_marks_tracked_closed_subprojects ... ok
test native::task_status_hooks::tests::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::tests::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::task_status_hooks::tests::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
test native::task_status_hooks::tests::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::task_status_hooks::tests::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::tests::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::task_status_hooks::tests::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::projects::tests::terminal_projects_do_not_reconcile_task_schedules ... ok
test native::projects::tests::project_sync_plan_matches_subproject_links_case_insensitively ... ok
test native::task_status_hooks::tests::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::task_status_hooks::tests::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::tests::rolling_reachability_is_cycle_safe_and_includes_dependencies ... ok
test runner::tests::subcommands_are_sorted_alphabetically ... ok
test native::task_status_hooks::tests::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test runner::tests::build_cli_renders_without_panicking ... ok
test native::projects::tests::subproject_state_treats_terminal_open_prj_child_as_open ... ok
warning: You appear to have cloned an empty repository.
test native::projects::tests::scheduled_tasks_precede_prj_surfacing_at_local_date_boundary ... ok
test native::projects::tests::project_schedule_accepts_quoted_dates_and_rejects_bad_dates ... ok
test native::projects::tests::project_sync_plan_reopens_terminal_project_from_open_prj ... ok
test native::projects::tests::project_sync_plan_manages_prj_hide_tag_from_open_subprojects ... ok
test native::dataview::tasks::task::tests::all_priorities_have_tasks_v8_names_numbers_and_scores ... ok
test native::dataview::tasks::index::tests::paragraphs_break_list_hierarchy ... ok
test native::dataview::tasks::index::tests::dependency_graph_matches_direct_tasks_v8_semantics ... ok
test native::dataview::tasks::task::tests::emoji_parser_extracts_all_fields_and_variant_selectors ... ok
test native::plugins::tests::sync_refuses_then_forces_a_dirty_vault_file ... ok
test native::projects::tests::subproject_parent_links_classify_open_and_terminal_prj_children ... ok
test native::dataview::tasks::index::tests::frontmatter_is_only_a_strictly_closed_column_zero_block ... ok
test native::highlights_ref::create::tests::code_break_filter_splits_long_inline_code_paths ... ok
test native::plugins::tests::sync_preserves_runtime_data_json ... ok
test native::projects::tests::project_parser_reports_malformed_and_multiple_prj_lines ... ok
test native::projects::tests::project_parser_accepts_prj_tag_and_strips_it_from_description ... ok
test native::projects::tests::project_parser_accepts_bare_project_type_and_prj_states ... ok
test native::projects::tests::project_sync_plan_reconciles_subprojects_marker_line ... ok
test native::projects::tests::project_parser_reads_parent_wikilink_target ... ok
test native::projects::tests::project_sync_plan_flips_status_without_prj_edits_after_effective_status ... ok
test native::projects::tests::project_sync_plan_removes_stale_scheduled_field ... ok
test native::projects::tests::project_sync_plan_warns_on_placeholder_while_reopening ... ok
test native::plugins::tests::pull_repo_skips_non_git_directory ... ok
test native::projects::tests::project_sync_plan_treats_user_sub_bullets_as_user_owned ... ok
test native::projects::tests::project_sync_plan_leaves_non_terminal_open_prj_status_untouched ... ok
test native::projects::tests::project_sync_plan_is_idempotent_when_prj_hide_tag_matches_dash_state ... ok
test native::projects::tests::project_sync_plan_reconciles_subproject_schedule_markers ... ok
test native::projects::tests::project_sync_plan_skips_subproject_links_without_open_prj_edits ... ok
test native::projects::tests::project_sync_plan_manages_prj_hide_tag_from_unhidden_count ... ok
test native::projects::tests::project_sync_plan_normalizes_subprojects_marker_drift ... ok
test native::projects::tests::subproject_aggregation_marks_only_schedules_after_shared_today ... ok
test native::plugins::tests::pull_repo_fast_forwards_from_remote ... ok

test result: ok. 578 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.15s

     Running unittests src/main.rs (target/debug/deps/bob-9084ccd8aa76f182)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (target/debug/deps/bob_notify-6faa0406764e9aa8)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (target/debug/deps/bob_pomodoro-09750a8fe1844cdb)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_sync.rs (target/debug/deps/bob_sync-e7d5756fda000827)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (target/debug/deps/tmux_bob_pomodoro-8c1cf7b435c28153)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli.rs (target/debug/deps/cli-d42a6366dd0d2962)

running 332 tests
test bulk_git_commit_help_is_native_only ... ok
test capture_authored_bullet_marker_on_child_line_configures_whole_capture ... ok
test capture_authored_bullets_duplicate_route_marker_across_lines_is_usage_error ... ok
test capture_authored_bullets_dry_run_reports_children_without_writing ... ok
test capture_authored_bullets_pomodoro_linked_capture_includes_children ... ok
test capture_authored_bullets_preserve_crlf_line_endings ... ok
test capture_authored_bullets_reject_orphaned_nested_lines ... ok
test capture_bare_terminal_marker_is_usage_error_and_does_not_write ... ok
test capture_batch_human_output_numbers_items ... ok
test capture_authored_bullets_use_two_space_target_indentation ... ok
test capture_authored_nested_bullets_render_under_their_owners ... ok
test capture_authored_bullets_preserve_inline_markdown_and_checkbox_text ... ok
test capture_batch_duplicate_block_id_failure_leaves_no_partial_write ... ok
test capture_authored_bullets_skip_placeholder_lines ... ok
test bulk_git_commit_commits_and_pushes_without_running_ob ... ok
test capture_authored_bullets_sub_bullet_nests_children_two_levels ... ok
test capture_json_output_is_machine_readable ... ok
test capture_legacy_standalone_marker_form_is_usage_error ... ok
test capture_malformed_pomodoro_marker_is_usage_error_without_writes ... ok
test capture_bullet_marker_order_routes_equivalently ... ok
test capture_nonterminal_schedule_token_stays_literal ... ok
test capture_parse_help_is_native_only ... ok
test capture_parse_human_output_is_plain_and_concise ... ok
test capture_parse_help_lists_options_alphabetically ... ok
test capture_parse_json_output_is_stable_and_parseable ... ok
test capture_parse_json_reports_retired_double_colon_as_migration_guidance ... ok
test capture_parse_json_reports_batch_items_with_global_ranges ... ok
test capture_parse_json_reports_wikilink_semantic_spans ... ok
test capture_parse_reads_one_stdin_line_when_text_is_omitted ... ok
test cache_extraction_writes_expected_files_and_modes ... ok
test capture_parse_json_reports_task_block_id_marker_spans_and_needs ... ok
test capture_parse_reports_diagnostics_without_failing ... ok
test capture_parse_reports_nested_sub_bullets_and_depths ... ok
test capture_parse_reports_sub_bullets_for_a_multiline_draft ... ok
test capture_parse_missing_text_is_a_usage_error ... ok
test capture_parse_reports_utf8_byte_offsets ... ok
test capture_parse_reports_orphaned_nested_bullet_diagnostic ... ok
test capture_pomodoro_dry_run_validates_and_changes_neither_note ... ok
test capture_percent_one_is_an_exact_single_clip_alias ... ok
test capture_pomodoro_link_uses_default_day_file_and_untimed_fallback ... ok
test capture_parse_never_touches_the_vault_or_clipboard ... ok
test capture_pomodoro_linked_task_updates_both_notes_and_reports_json ... ok
test capture_pomodoro_missing_daily_note_does_not_create_target ... ok
test capture_priority_dry_run_prints_schedule_log_without_writing ... ok
test capture_priority_level_one_rolls_scheduled_date_in_window ... ok
test capture_priority_renders_before_scheduled_and_before_pomodoro_block_id ... ok
test capture_priority_schedule_log_uses_the_target_notes_indent_unit ... ok
test capture_priority_level_four_rolls_scheduled_date_in_window ... ok
test capture_priority_json_includes_priority_fields_only_when_set ... ok
test capture_priority_sub_bullet_nests_schedule_log_under_the_child ... ok
test capture_reads_the_complete_piped_stdin_stream_when_text_is_absent ... ok
test capture_priority_with_explicit_schedule_skips_roll ... ok
test capture_priority_with_clip_orders_clip_children_before_schedule_log ... ok
test capture_retired_double_colon_marker_is_usage_error_without_writes ... ok
test capture_priority_out_of_range_is_usage_error_without_writes ... ok
test capture_route_override_keeps_at_tokens_literal ... ok
test capture_routed_bullet_inserts_into_section_by_prefix ... ok
test capture_routed_prefers_tasks_section_over_root_task ... ok
test capture_schedule_only_is_usage_error ... ok
test capture_scheduled_dry_run_reports_without_writing ... ok
test capture_scheduled_offset_out_of_range_is_usage_error ... ok
test capture_scheduled_zero_uses_created_date ... ok
test capture_sections_help_is_native_only ... ok
test capture_routed_prefix_inserts_and_suffix_creates_file ... ok
test capture_sections_help_lists_options_alphabetically ... ok
test capture_sections_json_lists_sections_in_order ... ok
test capture_sections_invalid_or_missing_route_errors_cleanly ... ok
test capture_scheduled_offset_routes_in_either_order ... ok
test capture_sub_bullet_task_option_keeps_at_tokens_literal ... ok
test capture_sub_bullet_task_ref_recovers_shift_and_nests_clipboard ... ok
test capture_targets_empty_vault_still_lists_inbox_default ... ok
test capture_targets_help_is_native_only ... ok
test capture_targets_help_lists_options_alphabetically ... ok
test capture_sub_bullet_uses_dominant_indent_preserves_crlf_and_dry_run ... ok
test capture_sub_bullet_inserts_with_parent_indentation_and_reports_json ... ok
test capture_targets_human_groups_and_summarizes_without_ansi ... ok
test capture_targets_json_failure_prints_error_object ... ok
test capture_priority_missing_config_file_is_io_error_without_writes ... ok
test capture_authored_bullets_bullet_capture_uses_section_prefix_with_children ... ok
test capture_complete_scopes_to_later_batch_item_and_ignores_separator ... ok
test capture_targets_json_lists_picker_targets_in_order ... ok
test capture_task_block_id_marker_creates_missing_routed_note ... ok
test capture_malformed_task_block_id_marker_is_usage_error_without_writes ... ok
test capture_sections_missing_note_returns_empty_json ... ok
test capture_complete_never_creates_the_vault_directory ... ok
test capture_dry_run_reports_without_writing ... ok
test capture_batch_dry_run_reports_all_items_without_writing ... ok
test capture_rejects_stdin_continuation_text_that_is_not_a_bullet ... ok
test capture_task_id_help_is_native_only ... ok
test capture_authored_bullets_render_task_with_children_in_order ... ok
test capture_json_omits_sub_bullets_for_an_ordinary_single_line_capture ... ok
test capture_history_without_a_provider_has_actionable_guidance ... ok
test capture_complete_discovery_failure_reports_an_actionable_error ... ok
test capture_complete_wikilink_note_json_returns_replacement_and_cursor_after ... ok
test capture_help_is_native_only ... ok
test capture_task_id_help_lists_options_alphabetically ... ok
test capture_task_block_id_dry_run_and_duplicate_preflight_do_not_write ... ok
test capture_tasks_help_is_native_only ... ok
test capture_tasks_help_lists_options_alphabetically ... ok
test capture_bullet_prefix_prefers_non_h1_and_ignores_prefix_case ... ok
test capture_unrouted_appends_to_mac_inbox ... ok
test capture_tasks_human_output_is_plain_when_piped ... ok
test capture_without_priority_token_tolerates_missing_config_file ... ok
test capture_unrouted_scheduled_offset_appends_property ... ok
test capture_tasks_json_lists_open_tasks_with_stable_picker_shape ... ok
test capture_unrouted_prefers_tasks_section_in_existing_inbox ... ok
test capture_targets_verbose_emits_skip_warnings ... ok
test dataview_help_is_native_only ... ok
test dataview_help_lists_options_alphabetically ... ok
test dataview_obsidian_dql_json_reads_query_file_and_forwards_env_vault ... ok
test dataview_obsidian_reports_missing_command_without_query_blob ... ok
test dataview_obsidian_dql_paths_extracts_and_deduplicates_note_paths ... ok
test dataview_obsidian_markdown_prints_rendered_markdown ... ok
test dataview_obsidian_query_does_not_run_ob_command ... ok
test dataview_native_where_false_returns_no_rows ... ok
test dataview_native_table_json_projects_frontmatter_rows ... ok
test capture_pomodoro_preflight_failures_leave_both_notes_untouched ... ok
test dataview_obsidian_reports_not_running_without_javascript_blob ... ok
test dataview_rejects_removed_sync_option ... ok
test dataview_obsidian_source_uses_path_command_and_sentinel_protocol ... ok
test capture_clip_marker_composes_with_schedule_routes_bullets_and_pomodoro ... ok
test dataview_native_dql_paths_walks_parent_frontmatter_headlessly ... ok
test highlights_create_help_lists_options_alphabetically ... ok
test highlights_create_dry_run_prints_plan_without_writes ... ok
test highlights_create_rejects_non_utf8_include_id_before_writes ... ok
test capture_task_id_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test dataview_obsidian_dql_paths_warn_or_fail_for_missing_identities ... ok
test dataview_obsidian_reports_missing_and_malformed_sentinel ... ok
test capture_complete_all_tasks_is_opt_in_and_plus_context_only ... ok
test highlights_create_reports_pandoc_failure_diagnostics ... ok
test dataview_obsidian_reports_protocol_errors ... ok
test highlights_ref_help_lists_subcommands_alphabetically ... ok
test highlights_ref_help_is_native_only ... ok
test highlights_create_refuses_existing_library_pdf_with_or_without_force ... ok
test dataview_rejects_unsafe_origin_and_missing_bob_dir ... ok
test dataview_rejects_invalid_argument_combinations ... ok
test highlights_ref_marker_uses_first_page_text_annotation ... ok
test dataview_native_table_paths_match_list_rows_headlessly ... ok
test highlights_ref_scan_detects_same_target_collision_before_writing ... ok
test highlights_ref_scan_allows_duplicate_basenames_in_different_ref_types ... ok
test highlights_ref_scan_default_output_reports_inline_errors ... ok
test highlights_ref_scan_continues_after_write_failure ... ok
test highlights_ref_frontmatter_missing_parent_fails_before_pdf_writeback ... ok
test highlights_ref_scan_dry_run_previews_xlib_intake_without_writes ... ok
test highlights_ref_frontmatter_unsupported_status_fails_before_pdf_writeback ... ok
test highlights_ref_scan_dry_run_reports_valid_and_invalid_pdfs ... ok
test highlights_ref_deleted_highlight_is_tombstoned ... ok
test highlights_ref_scan_help_lists_options_alphabetically ... ok
test highlights_ref_comment_edit_keeps_stable_block_id ... ok
test highlights_ref_scan_intakes_xlib_pdf_and_writes_note_in_same_run ... ok
test highlights_ref_scan_refuses_xlib_intake_conflict_before_writes ... ok
test highlights_ref_marker_edit_updates_frontmatter ... ok
test highlights_ref_rejects_wikilink_marker_parent_before_writes ... ok
test dataview_short_options_are_accepted ... ok
test all_top_level_subcommand_help_is_safe_and_plain ... ok
test highlights_ref_scan_treats_later_page_note_as_missing_marker ... ok
test highlights_ref_scan_intakes_xlib_sidecars_with_pdfs ... ok
test highlights_ref_scan_writes_valid_pdfs_despite_invalid_pdf ... ok
test highlights_ref_scan_groups_routed_tasks_with_parallel_jobs ... ok
test highlights_ref_sync_help_lists_options_alphabetically ... ok
test highlights_ref_sync_beautifies_linked_sidecar_rendering ... ok
test highlights_ref_sync_missing_routed_target_fails_before_writes ... ok
test highlights_ref_short_options_are_accepted ... ok
test highlights_ref_sync_dry_run_reads_literal_marker_newlines ... ok
test highlights_ref_conflicting_edits_fail_and_prefer_frontmatter_resolves ... ok
test highlights_ref_doctor_checks_vault_git_and_ob_without_writes ... ok
test capture_authored_bullets_duplicate_schedule_marker_across_lines_is_usage_error ... ok
test capture_authored_bullets_accept_dash_star_and_plus_markers ... ok
test capture_authored_bullets_reject_item_emptied_by_markers ... ok
test highlights_ref_scan_recurses_dry_runs_and_writes_multiple_pdfs ... ok
test highlights_ref_sync_rejects_missing_marker_parent_without_note_write ... ok
test highlights_ref_sync_rejects_missing_marker_status_without_note_write ... ok
test highlights_ref_sync_rejects_unsupported_marker_status_without_note_write ... ok
test highlights_ref_scan_default_output_is_concise ... ok
test capture_task_id_recovers_a_shifted_line_and_rejects_write_free_failures ... ok
test highlights_ref_sync_preserves_legacy_research_frontmatter ... ok
test highlights_ref_scan_jobs_flag_matches_sequential_output ... ok
test capture_forced_section_inserts_exact_bullet ... ok
test capture_history_dry_run_plans_colliding_files_without_writes ... ok
test capture_complete_wikilink_same_note_heading_uses_capture_route ... ok
test capture_complete_section_json_lists_headings_of_the_resolved_route ... ok
test capture_complete_rejects_a_cursor_that_splits_a_multibyte_character ... ok
test capture_leading_route_bullet_inserts_into_section_by_prefix ... ok
test capture_complete_rejects_a_cursor_outside_the_text ... ok
test capture_json_output_includes_scheduled_date ... ok
test capture_complete_help_is_native_only ... ok
test capture_complete_reports_utf8_byte_offsets ... ok
test capture_complete_completes_a_marker_on_a_nested_child_line ... ok
test capture_complete_human_output_is_plain_and_concise ... ok
test highlights_ref_subcommand_help_works ... ok
test capture_complete_completes_a_marker_on_a_child_line ... ok
test capture_help_lists_options_alphabetically ... ok
test capture_empty_input_is_usage_error ... ok
test capture_json_failure_prints_error_object ... ok
test capture_complete_cursor_in_body_text_is_an_empty_success ... ok
test capture_complete_empty_text_defaults_to_an_empty_draft ... ok
test capture_forced_section_requires_route ... ok
test highlights_ref_non_overlapping_edits_auto_merge_and_settle ... ok
test capture_complete_route_json_ranks_prefix_before_substring ... ok
test capture_bullet_json_reports_rendered_line ... ok
test capture_task_block_id_marker_writes_ordinary_task_and_ignores_daily_note ... ok
test highlights_ref_sync_creates_tasks_from_pdf_note_task_bullets ... ok
test capture_complete_missing_note_behind_a_resolved_route_is_an_empty_success ... ok
test capture_authored_bullets_reject_indented_or_nonbullet_lines ... ok
test capture_clip_json_always_emits_collection_fields ... ok
test capture_complete_help_lists_options_alphabetically ... ok
test capture_flat_clipboard_list_routes_normalized_children ... ok
test highlights_ref_sync_renders_sidecar_highlights_and_notes ... ok
test capture_batch_json_is_ordered_and_keeps_legacy_top_level ... ok
test highlights_ref_sync_skips_vault_scan_when_no_annotation_candidates ... ok
test highlights_ref_sync_creates_note_frontmatter_from_marker_pdf_note ... ok
test capture_complete_task_block_id_marker_completes_only_route_side ... ok
test capture_complete_task_json_only_offers_tasks_with_a_block_id ... ok
test highlights_ref_sync_preserves_manual_sections_and_rejects_missing_markers ... ok
test capture_headerless_clip_marker_renders_under_tasks_and_pomodoros ... ok
test highlights_ref_frontmatter_edit_updates_marker_when_pdf_writes_enabled ... ok
test highlights_ref_sync_renders_textbundle_image_selections ... ok
test highlights_ref_sync_supports_linked_sidecar_style ... ok
test highlights_ref_status_abandoned_rewrites_generated_task_to_cancelled ... ok
test capture_clip_failures_leave_vault_untouched ... ok
test capture_clip_uses_each_target_notes_indent_and_tabs_for_a_fresh_note ... ok
test highlights_ref_task_cancelled_scan_write_pdfs_writes_pdf_marker ... ok
test move_done_tasks_help_is_native_only ... ok
test nightly_help_exits_before_operational_work ... ok
test plugins_help_lists_subcommand_and_options ... ok
test plugins_sync_help_lists_options_alphabetically ... ok
test highlights_ref_deprecated_done_status_migrates_to_read_with_pdf_write ... ok
test move_done_tasks_warns_and_skips_git_for_non_repo_vault ... ok
test legacy_binary_help_is_safe_and_plain ... ok
test highlights_ref_dry_run_and_inspection_do_not_modify_vault_files ... ok
test highlights_ref_sync_allows_dirty_tracked_frontmatter_writeback ... ok
test pomodoro_missing_day_file_is_a_successful_noop ... ok
test pomodoro_formats_native_pomodoro_status ... ok
test pomodoro_accepts_legacy_unbolded_inline_duration_field_in_time_range ... ok
test highlights_ref_sync_skips_legacy_highlight_task_property ... ok
test highlights_ref_sync_rejects_malformed_and_duplicate_marker_lists ... ok
test plugins_list_unreadable_repo_reports_error ... ok
test capture_history_is_headerless_structured_and_composes_with_routes ... ok
test plugins_list_json_is_machine_readable ... ok
test capture_clip_saves_attachments_snippets_and_reports_dry_run ... ok
test plugins_default_subcommand_runs_list ... ok
test capture_history_provider_failures_leave_the_vault_untouched ... ok
test move_done_tasks_moves_canceled_tasks_in_non_repo_vault ... ok
test plugins_list_renders_table_and_summary ... ok
test plugins_sync_preserves_runtime_data_json ... ok
test highlights_ref_sync_routes_annotation_tasks_to_existing_root_note ... ok
test pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test plugins_sync_backs_up_overwritten_file ... ok
test highlights_ref_task_checked_sync_creates_annotation_tasks_before_closing ... ok
test projects_list_reports_prj_errors_without_aborting_scan ... ok
test projects_sync_marks_canceled_subproject_same_run ... ok
test plugins_sync_dry_run_reports_without_writing ... ok
test highlights_ref_task_checked_scan_creates_annotation_tasks_before_closing ... ok
test plugins_sync_single_plugin_copies_only_that_plugin ... ok
test projects_help_is_native_only ... ok
test highlights_ref_task_checked_competing_status_edits_fail ... ok
test projects_sync_keeps_pruned_closed_entries_gone ... ok
test projects_list_scans_project_notes_and_renders_counts ... ok
test projects_sync_shows_sole_prj_task_when_schedule_is_due ... ok
test pomodoro_help_documents_show_stale_option ... ok
test highlights_ref_sync_refuses_dirty_target_note_before_writing ... ok
test projects_schedule_errors_are_per_file_and_leave_invalid_file_untouched ... ok
test projects_sync_normalizes_mangled_subprojects_line ... ok
test highlights_ref_sync_skips_annotation_tasks_for_non_wip_statuses ... ok
test script_fallback_bob_sync_help_exits_before_work ... ok
test projects_help_lists_subcommands_and_options ... ok
test projects_sync_subproject_line_dry_run_reports_without_writing ... ok
test projects_sync_reports_prj_errors_without_aborting_scan ... ok
test projects_sync_preserves_user_sub_bullets_and_inserts_subprojects_line ... ok
test projects_sync_treats_children_without_open_prj_as_childless ... ok
test task_status_hooks_composes_daily_status_and_structural_edits ... ok
test projects_sync_reopens_parent_ledger_when_child_prj_is_reopened_same_run ... ok
test pomodoro_show_stale_keeps_no_open_day_empty ... ok
test highlights_ref_task_cancelled_competing_status_edits_fail ... ok
test projects_sync_orders_open_then_closed_subprojects_in_one_run ... ok
test projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test top_level_help_lists_commands_alphabetically_with_examples ... ok
test highlights_ref_task_ready_scan_reopens_read_ref_to_ready ... ok
test task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test task_status_hooks_help_lists_options_alphabetically ... ok
test task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test tmux_pomodoro_formats_native_pomodoro_status ... ok
test projects_sync_propagates_scheduled_task_properties_at_date_boundary ... ok
test capture_clip_options_force_or_disable_marker_parsing ... ok
test task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test projects_sync_hides_parent_projects_with_open_subprojects ... ok
test task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test projects_sync_unhides_parent_when_child_prj_is_checked_same_run ... ok
test highlights_ref_task_checked_dirty_tracked_note_is_allowed ... ok
test plugins_sync_refuses_dirty_vault_file_then_forces ... ok
test script_pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test script_fallback_help_is_safe_and_plain ... ok
test projects_sync_reconciles_future_subproject_markers_at_date_boundary ... ok
test task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test script_pomodoro_accepts_legacy_unbolded_time_range ... ok
test task_status_hooks_blocked_status_guard_writes_nothing ... ok
test highlights_ref_task_cancelled_dry_run_requires_and_writes_pdf_marker ... ok
test script_pomodoro_accepts_inline_duration_field_in_time_range ... ok
test nightly_failing_shared_sync_aborts_before_wrapped_steps ... ok
test task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test renamed_old_top_level_commands_are_unknown ... ok
test task_status_hooks_help_is_native_only ... ok
test task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker ... ok
test task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test projects_sync_updates_status_prj_hide_tag_warns_and_is_idempotent ... ok
test capture_sub_bullet_errors_are_actionable_in_human_and_json_modes ... ok
test task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test legacy_bob_sync_binary_runs_bulk_git_commit_native_path ... ok
test nightly_failed_step_still_runs_later_steps_and_exits_nonzero ... ok
test move_done_tasks_rewrites_dirty_metadata_only_source ... ok
test move_done_tasks_rewrites_dirty_candidate_files ... ok
test move_done_tasks_commits_metadata_only_archive_repairs ... ok
test move_done_tasks_rewrites_dirty_link_repair_files ... ok
test move_done_tasks_commits_link_repairs_with_collection_changes ... ok
test move_done_tasks_commits_metadata_only_source_updates ... ok
test move_done_tasks_deduplicates_archive_block_ids_and_repairs_links ... ok
test move_done_tasks_rewrites_dirty_metadata_only_archive ... ok
test move_done_tasks_commits_and_pushes_collection_changes_only ... ok
test pomodoro_stale_cutoff_is_empty_unless_requested ... ok
test public_help_surfaces_do_not_list_long_only_options ... ok
test nightly_runs_shared_sync_once_then_wrapped_steps_in_order ... ok
test plugins_list_no_pull_uses_existing_checkout ... ok
test plugins_list_pulls_repo_before_analysis ... ok
test plugins_sync_pulls_repo_before_copying ... ok
test plugins_list_json_stdout_stays_machine_readable_after_pull ... ok
test project_schedule_tasks_flip_between_dash_and_blocked_queries_when_due ... ok
test highlights_create_renders_pdf_with_outline_and_marker_when_available ... ok

test result: ok. 332 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 3.21s

     Running tests/dataview_parity.rs (target/debug/deps/dataview_parity-3c8b190f7e2aef25)

running 27 tests
test dataview_live_obsidian_parity_harness_compares_supported_native_cases ... ok
test dataview_parity_fixture_vault_covers_contract_surface ... ok
test dataview_obsidian_calendar_markdown_golden_fails_cleanly ... ok
test dataview_native_dql_from_ref_prefers_folder_when_note_also_exists ... ok
test dataview_native_function_library_supports_numeric_and_container_functions ... ok
test dataview_native_calendar_markdown_fails_cleanly ... ok
test dataview_obsidian_paths_goldens_cover_grouped_and_flattened_warnings ... ok
test dataview_obsidian_markdown_goldens_cover_supported_exports ... ok
test dataview_native_current_paths_golden_uses_fixture_vault ... ok
test dataview_native_index_skips_hidden_directories ... ok
test dataview_obsidian_dql_json_goldens_cover_result_shapes ... ok
test dataview_native_index_values_cover_yaml_inline_dates_and_links ... ok
test dataview_native_current_json_golden_uses_bob_wrapper_shape ... ok
test dataview_native_expression_core_supports_swizzling_and_lambdas ... ok
test dataview_obsidian_source_goldens_cover_source_expression_contract ... ok
test dataview_native_dql_from_accepts_source_expressions ... ok
test dataview_native_index_builds_task_and_list_objects ... ok
test dataview_native_function_library_supports_string_functions ... ok
test dataview_native_function_library_supports_constructors_and_utilities ... ok
test dataview_native_expression_core_supports_this_comparison_and_sorting ... ok
test dataview_native_function_library_works_in_where_sort_and_list ... ok
test dataview_native_expression_core_evaluates_table_and_list_values ... ok
test dataview_native_index_builds_file_metadata_and_link_graph ... ok
test dataview_native_markdown_goldens_cover_supported_exports ... ok
test dataview_native_dql_execution_supports_phase6_result_shapes ... ok
test dataview_native_source_expressions_match_fixture_goldens ... ok
test dataview_native_source_smoke_handles_generated_vault_with_many_lists ... ok

test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.51s

     Running tests/tasks_parity.rs (target/debug/deps/tasks_parity-beba8a091571df82)

running 31 tests
test tasks_live_obsidian_parity_harness_renders_and_scrapes_tasks_blocks ... ok
test path_qualified_dependency_ids_keep_duplicate_block_fragments_distinct ... ok
test hide_tags_only_removes_recognized_task_tags ... ok
test tasks_parity_fixture_vault_covers_phase1_contract ... ok
test tasks_by_function_exposes_tasks_query_context_and_real_moment_dates ... ok
test tasks_native_filterless_paths_golden_includes_underscore_folders ... ok
test tasks_native_filterless_json_golden_reads_settings_and_tasks ... ok
test blocked_note_includes_dependency_and_future_scheduled_status_reasons ... ok
test tasks_native_dashboard_defaults_run_function_filters_with_pinned_moment ... ok
test sort_by_function_evaluates_each_task_key_once ... ok
test tasks_by_function_runs_dash_filters_and_stacked_sorts ... ok
test tasks_query_parser_accepts_the_daily_note_query_surface ... ok
test tasks_result_pipeline_sorts_groups_and_limits_like_tasks_v8 ... ok
test tasks_cli_rejects_invalid_combinations_and_unsupported_surface ... ok
test tasks_note_reports_the_failing_block_context ... ok
test tasks_plugin_emoji_setting_selects_emoji_metadata_parser ... ok
test tasks_settings_have_stable_defaults_when_plugin_data_is_absent ... ok
test tasks_javascript_exposes_priority_digits_and_pins_all_moment_clocks ... ok
test tasks_query_parser_composes_dash_defaults_and_serializes_the_ast ... ok
test tasks_group_by_function_reports_array_keys_and_runtime_errors ... ok
test tasks_note_and_origin_normalize_leading_current_directory_components ... ok
test tasks_note_executes_every_dashboard_block_with_origin_defaults ... ok
test tasks_markdown_honors_tree_layout_fields_counts_and_explain ... ok
test tasks_note_identifies_blocks_in_paths_and_markdown_output ... ok
test tasks_native_boolean_and_implicit_and_filters_match_goldens ... ok
test tasks_group_by_function_keeps_null_empty_array_and_empty_string_tasks ... ok
test tasks_short_flags_files_stdin_and_comments_reach_filterless_slice ... ok
test tasks_native_date_filters_match_pinned_range_boundaries ... ok
test tasks_native_filter_families_match_fixture_goldens ... ok
test tasks_by_function_surfaces_parse_return_type_and_sort_errors ... ok
test tasks_every_native_sort_and_group_key_executes ... ok

test result: ok. 31 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.24s

     Running tests/tasks_real_vault_parity.rs (target/debug/deps/tasks_real_vault_parity-048539ae2906c481)

running 1 test
test real_vault_dash_matches_independent_raw_ground_truth_and_all_blocks_execute ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

   Doc-tests bob_cli

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s


  ✓  ALL CHECKS PASSED

bash -n scripts/bob_notify scripts/bob_pomodoro scripts/bob_sync scripts/tmux_bob_pomodoro scripts/lib/bob_shell.sh
cargo package --list
warning: manifest has no license or license-file
  |
  = note: see https://doc.rust-lang.org/cargo/reference/manifest.html#package-metadata for more info
.cargo_vcs_info.json
Cargo.lock
Cargo.toml
Cargo.toml.orig
README.md
docs/dataview.md
docs/highlights-ref-sync.md
docs/plugins.md
docs/projects.md
docs/task-status-hooks.md
justfile
scripts/bob_notify
scripts/bob_pomodoro
scripts/bob_sync
scripts/lib/bob_shell.sh
scripts/tmux_bob_pomodoro
src/bin/bob_notify.rs
src/bin/bob_pomodoro.rs
src/bin/bob_sync.rs
src/bin/tmux_bob_pomodoro.rs
src/lib.rs
src/main.rs
src/native/capture.rs
src/native/capture_clip.rs
src/native/capture_complete.rs
src/native/capture_language.rs
src/native/capture_links.rs
src/native/capture_parse.rs
src/native/capture_schedule_log.rs
src/native/capture_sections.rs
src/native/capture_targets.rs
src/native/capture_task_id.rs
src/native/capture_tasks.rs
src/native/collect_done.rs
src/native/config.rs
src/native/dataview/index.rs
src/native/dataview/tasks/filter.rs
src/native/dataview/tasks/index.rs
src/native/dataview/tasks/js.rs
src/native/dataview/tasks/mod.rs
src/native/dataview/tasks/parse.rs
src/native/dataview/tasks/render.rs
src/native/dataview/tasks/result.rs
src/native/dataview/tasks/settings.rs
src/native/dataview/tasks/task.rs
src/native/dataview/tasks/vendor/MOMENT_LICENSE
src/native/dataview/tasks/vendor/moment.min.js
src/native/dataview/value.rs
src/native/dataview.rs
src/native/env.rs
src/native/highlights_ref/create.rs
src/native/highlights_ref/mod.rs
src/native/markdown.rs
src/native/nightly.rs
src/native/note_tasks.rs
src/native/notify.rs
src/native/ob.rs
src/native/plugins.rs
src/native/pomodoro.rs
src/native/projects.rs
src/native/style.rs
src/native/sync.rs
src/native/task_status_hooks.rs
src/native.rs
src/runner.rs
src/scripts.rs
tests/cli.rs
tests/dataview_parity.rs
tests/fixtures/collect_done/nested_blocks.md
tests/fixtures/collect_done/nested_blocks_archive.md
tests/fixtures/collect_done/nested_blocks_source.md
tests/fixtures/dataview_parity/README.md
tests/fixtures/dataview_parity/vault/.obsidian/plugins/dataview/data.json
tests/fixtures/dataview_parity/vault/Archive/Old.md
tests/fixtures/dataview_parity/vault/Daily/2026-06-03.md
tests/fixtures/dataview_parity/vault/Links/Hub.md
tests/fixtures/dataview_parity/vault/Links/Target.md
tests/fixtures/dataview_parity/vault/Origins/Origin.md
tests/fixtures/dataview_parity/vault/People/Ada Lovelace.md
tests/fixtures/dataview_parity/vault/People/Grace Hopper.md
tests/fixtures/dataview_parity/vault/Projects/Alpha.md
tests/fixtures/dataview_parity/vault/Projects/Beta.md
tests/fixtures/dataview_parity/vault/Projects/Gamma.md
tests/fixtures/dataview_parity/vault/Tasks/Nested.md
tests/fixtures/dataview_parity/vault/ai_ref.md
tests/fixtures/dataview_parity/vault/ref/Alpha.md
tests/fixtures/dataview_parity/vault/ref/Beta.md
tests/fixtures/dataview_parity/vault/ref.md
tests/fixtures/highlights_ref/README.md
tests/fixtures/highlights_ref/assets/figure.png
tests/fixtures/highlights_ref/empty_sidecar.md
tests/fixtures/highlights_ref/image_sidecar.md
tests/fixtures/highlights_ref/linked_sidecar.md
tests/fixtures/highlights_ref/marker_note.txt
tests/fixtures/highlights_ref/sample_sidecar.md
tests/fixtures/pomodoro/day_with_legacy_open_pomodoro.md
tests/fixtures/pomodoro/day_with_open_pomodoro.md
tests/fixtures/pomodoro/day_without_open_pomodoro.md
tests/fixtures/task_status_hooks/2026/20260710.md
tests/fixtures/task_status_hooks/Projects/Alpha.md
tests/fixtures/task_status_hooks/dev.md
tests/fixtures/tasks_dependency_identity/Alpha.md
tests/fixtures/tasks_dependency_identity/Beta.md
tests/fixtures/tasks_dependency_identity/Dependents.md
tests/fixtures/tasks_parity/README.md
tests/fixtures/tasks_parity/vault/.obsidian/plugins/obsidian-tasks-plugin/data.json
tests/fixtures/tasks_parity/vault/.trash/Hidden.md
tests/fixtures/tasks_parity/vault/Daily/2026-07-10.md
tests/fixtures/tasks_parity/vault/Tasks/Dependencies.md
tests/fixtures/tasks_parity/vault/Tasks/MetadataDataview.md
tests/fixtures/tasks_parity/vault/Tasks/MetadataEmoji.md
tests/fixtures/tasks_parity/vault/Tasks/MissingGlobalFilter.md
tests/fixtures/tasks_parity/vault/Tasks/Nested.md
tests/fixtures/tasks_parity/vault/Tasks/Statuses.md
tests/fixtures/tasks_parity/vault/_generated/Generated.md
tests/fixtures/tasks_parity/vault/_templates/Task.md
tests/fixtures/tasks_parity/vault/blocked.md
tests/fixtures/tasks_parity/vault/dash.md
tests/tasks_parity.rs
tests/tasks_real_vault_parity.rs
Building for debugging...
[0/2] Write sources
[1/2] Write swift-version--413BBEA0737331CC.txt
[3/12] Emitting module CaptureCore
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CaptureTargetsCache.swift:39:42: warning: converting non-sendable function value to '@Sendable () -> Date' may introduce data races
37 |     public func refresh(
38 |         using client: BobProcessClient,
39 |         now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-sendable function value to '@Sendable () -> Date' may introduce data races
40 |     ) async -> CaptureTargetsSnapshot {
41 |         do {
[4/12] Compiling CaptureCore CaptureTextRanges.swift
[5/12] Compiling CaptureCore CaptureTargetsCache.swift
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CaptureTargetsCache.swift:39:42: warning: converting non-sendable function value to '@Sendable () -> Date' may introduce data races
37 |     public func refresh(
38 |         using client: BobProcessClient,
39 |         now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-sendable function value to '@Sendable () -> Date' may introduce data races
40 |     ) async -> CaptureTargetsSnapshot {
41 |         do {
[6/12] Compiling CaptureCore CompletionRowContent.swift
[7/12] Compiling CaptureCore ObsidianOpenURL.swift
[8/12] Compiling CaptureCore BobEnvironment.swift
[9/12] Compiling CaptureCore BobErrors.swift
[10/12] Compiling CaptureCore BobExecutableResolver.swift
[11/12] Compiling CaptureCore CaptureModels.swift
[12/12] Compiling CaptureCore BobProcessClient.swift
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/BobProcessClient.swift:189:21: warning: capture of 'timeoutWorkItem' with non-sendable type 'DispatchWorkItem' in a `@Sendable` closure; this is an error in the Swift 6 language mode
187 | 
188 |                 process.terminationHandler = { [weak self] completedProcess in
189 |                     timeoutWorkItem.cancel()
    |                     `- warning: capture of 'timeoutWorkItem' with non-sendable type 'DispatchWorkItem' in a `@Sendable` closure; this is an error in the Swift 6 language mode
190 |                     guard resumeGuard.markResumed() else { return }
191 | 
Build of target: 'CaptureCore' complete! (6.76s)

