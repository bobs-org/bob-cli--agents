- **PLAN:**
  [202608/normalize_mac_capture_bullet_paste.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/normalize_mac_capture_bullet_paste.md)
- **AGENTS:**
  - [bbugyi200.athena.091--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.091.md)

When the user copies a bullet list that they want to paste into the bob-mac-capture
panel, they type the title of the task/note, then use the `<ctrl+j>` keymap to insert a
newline and a `- `. They then paste the bullet list. The problem is that the first `- `
from the pasted in bullet list creates a duplicate (i.e. `- - `). Can you help me fix
this by removing this extra dash automatically when the user pastes in content to a line
containing only a bullet? Make sure that you correct indentation appropriately as well.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
