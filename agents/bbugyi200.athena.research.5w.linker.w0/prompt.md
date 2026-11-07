#gh:gh_bobs-org__bob-cli I normally manage my crontab using the `crontab -e` command. I have a crontab
set up on my athena machine and on my macbook, but not this machine (though I likely
will at some point). This makes it difficult to manage my crontab (for me and for agents
like you). Can you help me implement this?

- I was thinking the best interface for this would be to use a single configuration file
  that are checked in (i.e. committed) to my chezmoi repo.
- When I run the `chezmoi update -a` command on my machines after updating this file,
  the expectation would be that my crontab is updated accordingly (on the machines that
  correspond with the configuration update).
- I'm not sure if agents are currently able to write/change my crontab on these machines
  currently (I don't think they do). Make sure agents have first-class support (i.e.
  easy ability to read/write my crontab on any machine from any machine) for this new
  and improved way of managing my crontabs.
- The only machine-specific part of the configuration in this file should be the unique
  machine names, which can be used to determine which crontab configuration should be
  applied for each machine.
- Review the crontab_as_code_via_chezmoi.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).

#plan %m:@xlarge %w:research.5w.linker