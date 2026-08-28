#gh:gh_bobs-org__bob-cli The `bob highlights` command currently support creating Obsidian tasks from
reference note annotations using a bullet starting with `#task`. The problem is these
tasks get added directly below the `^ref` task in the corresponding reference note file,
instead of adding them to an H2 "Tasks" section (create one if it doesn't already exist
and add it to the top of the file, below the `^ref` task and a blank line--the first
task should also be separated from the "Tasks" section header by a blank line). Can you
help me fix this?

#plan #m_opus