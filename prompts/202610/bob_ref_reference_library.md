- **PLAN:**
  [202610/bob_ref_reference_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)
- **AGENTS:**
  - [bbugyi200.athena.research.3s.linker.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md)

I would like to migrate the `bob highlights` command to a new `bob ref` command that
supports all of the same commands that the `bob highlights` command currently does but
also adds new commands that make it easy for agents (and myself) to see what references
I have read, which I am tracking / plan to read, which I've finished reading, etc... Can
you help me implement this?

- The main use-case for this command would be for agents that are recommending new
  reading material for me (these agents would find it useful to know what articles /
  papers I have already read).
- With that said, I also think it would be useful to be able to read the annotations
  that I left on these reference PDFs (using the Highlights app on my macbook). These
  are automatically written to markdown files in the ~/bob/ref/ directory.
- Review the bob_ref_reference_library_migration.md file in the research sidecar repo
  for context and inspiration before planning. I agree with all of the recommendations
  made in that research file. Also, make sure to integrate the work from the bob-cli-4s
  epic bead, which was created and completed after this research was performed.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
