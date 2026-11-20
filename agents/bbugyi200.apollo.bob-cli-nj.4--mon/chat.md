# Chat History - ace-run (bob-cli-nj.4--mon)

- **TIMESTAMP:** 2026-11-19 20:02:38 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-nj.4--mon

## Prompt

sase monitor start --command 'while sase agent list -j | rg -q bob-cli-no.2; do sleep 30; done; bob plugins sync' --reason 'Wait for workspace 16 agent bob-cli-no.2 to finish before retrying protected bob-navigation-hotkeys sync'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Traceback (most recent call last):
  File "/home/bryan/.local/bin/sase", line 10, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 19, in main
    _main(hit)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/entry.py", line 117, in _main
    dispatch_initial_commands(args, parser)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/_dispatch_initial.py", line 20, in dispatch_initial_commands
    handle_agent_command(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/main/agent_handler.py", line 16, in handle_agent_command
    handle_agents_list(args)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 43, in handle_agents_list
    _print_json(agents)
  File "/home/bryan/projects/github/sase-org/sase/src/sase/agents/cli_list.py", line 52, in _print_json
    json.dump(payload, sys.stdout, indent=2)
  File "/usr/lib/python3.12/json/__init__.py", line 180, in dump
    fp.write(chunk)
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe
Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
BrokenPipeError: [Errno 32] Broken pipe

