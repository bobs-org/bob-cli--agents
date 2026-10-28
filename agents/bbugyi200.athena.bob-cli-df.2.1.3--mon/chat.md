# Chat History - ace-run (bob-cli-df.2.1.3--mon)

- **TIMESTAMP:** 2026-10-28 00:34:43 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-df.2.1.3--mon

## Prompt

sase monitor start --command 'SASE_CORE_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core just test tests/main/test_artifact_link_outbox_drain.py tests/sdd/test_artifact_link_event_publisher.py tests/main/test_artifact_cli_link_add.py tests/main/test_artifact_link_outbox_io.py tests/sdd/test_artifact_link_event_store_quarantine.py' --reason 'Run focused artifact-link publication quarantine tests against the pinned core contract'

## Response

sase tool run 7ce72ff4b57788720c68a5263a136bed
Using CPython 3.14.7
Creating virtual environment at: .venv
Activate with: source .venv/bin/activate
Traceback (most recent call last):
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/tools/refresh_linked_checkout", line 30, in <module>
    raise SystemExit(main())
                     ~~~~^^
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/tools/refresh_linked_checkout", line 21, in main
    from sase._linked_repo_workspaces import refresh_clean_linked_checkout
ModuleNotFoundError: No module named 'sase'
[validate_sase_core_rs_version] sase-core checkout is ahead of sase's compatibility window: source version 0.43.0 from /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/Cargo.toml does not satisfy `sase`'s `sase-core-rs==0.42.7` dependency in pyproject.toml. No action is needed: editable installs build from the checkout regardless, and `tools/ratchet_core_pin` moves the published pin on the release branch at release time.
[validate_sase_core_rs] sase-core-rs is not installed
[validate_dependency_group] 'packaging' is not installed; dependency versions cannot be checked
[validate_editable_metadata] 'sase' is not installed in this environment
[core-source] no built-from stamp for the linked sase-core source; flagging an extension rebuild.
[setup] Note: the sase-core checkout is ahead of the published sase-core-rs pin in pyproject.toml; dev installs build from /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core regardless. This is normal — the release-branch reconciler ratchets the published pin at release time, so no action is needed here.
[setup] Rebuilding sase_core_rs: linked sase-core source changed since the extension was built.
Traceback (most recent call last):
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/tools/refresh_linked_checkout", line 30, in <module>
    raise SystemExit(main())
                     ~~~~^^
  File "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/tools/refresh_linked_checkout", line 21, in main
    from sase._linked_repo_workspaces import refresh_clean_linked_checkout
ModuleNotFoundError: No module named 'sase'
[validate_sase_core_rs_version] sase-core checkout is ahead of sase's compatibility window: source version 0.43.0 from /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/Cargo.toml does not satisfy `sase`'s `sase-core-rs==0.42.7` dependency in pyproject.toml. No action is needed: editable installs build from the checkout regardless, and `tools/ratchet_core_pin` moves the published pin on the release branch at release time.
[rust-install] Note: the sase-core checkout is ahead of the published sase-core-rs pin in pyproject.toml; dev builds from /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core ignore it. This is normal — the release-branch reconciler ratchets the published pin at release time, so no action is needed here.
# Harden cargo crate downloads against transient crates.io flakiness.
# CI has hit `curl ... [16] Error in the HTTP2 framing layer` while
# maturin's `cargo metadata` fetches deps; disabling HTTP/2 multiplexing
# and raising the retry count makes the download resilient. Both are
# overridable from the environment.
# Capture the source identity after the checkout refresh above and before
# the build below. It is written to the venv only after a successful
# install (wheel-cache hit or `maturin develop` alike), so an edit made
# during the build still reads as stale on the next check.
[rust-install] Installing cached sase_core_rs wheel from /home/bryan/.sase/cache/sase-core-artifacts/0a9a23242e8a10f4af702a295767a397441e49ed01993f74927ee4a4016abebd/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl.
Resolved 1 package in 8ms
Prepared 1 package in 4ms
Installed 1 package in 10ms
 + sase-core-rs==0.43.0 (from file:///home/bryan/.sase/cache/sase-core-artifacts/0a9a23242e8a10f4af702a295767a397441e49ed01993f74927ee4a4016abebd/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl)
# Keep the LSP server in lockstep with the extension: both are built
# from the same sase-core checkout, and the ACE/LSP parity tests
# compare their directive contracts.
[rust-lsp-install] Installing cached LSP binary from /home/bryan/.sase/cache/sase-core-artifacts/a8e2c09f0078867fe9560c1ac3c789ab0d54132aa9278d465df7a8550ae26f14/sase-macro-lsp.
[rust-lsp-install] installed /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/sase-macro-lsp
Resolved 98 packages in 160ms
   Building sase @ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase
      Built sase @ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase
Prepared 2 packages in 846ms
Installed 97 packages in 231ms
 + ast-serialize==0.13.1
 + asttokens==3.0.2
 + attrs==26.1.0
 + bracex==3.2
 + build==1.6.1
 + cachetools==7.2.6
 + certifi==2026.10.23
 + cffi==2.1.1
 + charset-normalizer==3.5.2
 + colorama==0.4.6
 + coverage==7.17.0
 + cryptography==50.0.2
 + distlib==0.4.4
 + docutils==0.23
 + execnet==2.1.2
 + executing==2.3.0
 + filelock==4.2.4
 + hypothesis==6.170.12
 + id==1.6.1
 + idna==3.20
 + iniconfig==2.3.1
 + inline-snapshot==0.36.1
 + jaraco-classes==3.4.0
 + jaraco-context==6.1.2
 + jaraco-functools==4.6.0
 + jeepney==0.9.0
 + jinja2==3.1.6
 + jsonschema==4.26.0
 + jsonschema-specifications==2025.9.1
 + keyring==25.7.0
 + librt==0.16.0
 + linkify-it-py==2.2.0
 + markdown-it-py==4.2.0
 + markupsafe==3.0.4
 + mdit-py-plugins==0.6.1
 + mdurl==0.1.2
 + more-itertools==11.2.1
 + mypy==2.4.0
 + mypy-extensions==1.1.0
 + nh3==0.3.7
 + packaging==26.3
 + pathspec==1.1.1
 + pillow==13.0.0
 + platformdirs==4.13.6
 + pluggy==1.7.0
 + pycparser==3.12
 + pygments==2.19.2
 + pyinstrument==5.1.3
 + pyproject-api==1.12.2
 + pyproject-hooks==1.3.3
 + pytest==9.2.0
 + pytest-asyncio==1.4.1
 + pytest-cov==7.1.0
 + pytest-mock==3.17.0
 + pytest-xdist==3.8.0
 + python-discovery==1.6.6
 + pyyaml==6.0.3
 + readme-renderer==46.0
 + referencing==0.37.0
 + requests==2.34.2
 + requests-toolbelt==1.0.0
 + resvg-py==0.3.3
 + rfc3986==2.0.0
 + rich==15.0.0
 + rpds-py==2026.9.1
 + ruamel-yaml==0.19.1
 + ruff==0.17.3
 + sase==0.18.1 (from file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase)
 + schedule==1.2.2
 + secretstorage==3.5.0
 + sortedcontainers==2.4.0
 + symvision==0.1.0
 + textual==8.2.8
 + tomli-w==1.2.0
 + toobig==0.1.0
 + tox==4.67.3
 + tree-sitter==0.26.0
 + tree-sitter-bash==0.25.1
 + tree-sitter-css==0.25.0
 + tree-sitter-go==0.25.0
 + tree-sitter-html==0.23.2
 + tree-sitter-java==0.23.5
 + tree-sitter-javascript==0.25.0
 + tree-sitter-json==0.24.8
 + tree-sitter-markdown==0.5.4
 + tree-sitter-python==0.25.0
 + tree-sitter-regex==0.25.0
 + tree-sitter-rust==0.24.2
 + tree-sitter-sql==0.3.11
 + tree-sitter-toml==0.7.0
 + tree-sitter-xml==0.7.0
 + tree-sitter-yaml==0.7.2
 + twine==7.0.0
 + typing-extensions==4.16.0
 + urllib3==2.8.0
 + virtualenv==21.15.1
 + wcmatch==11.2
.venv/bin/python tools/setup_required_plugins
[setup] Installing required plugin sase-github>=0.2.5.
[setup] Installing required plugin sase-research-artifacts>=0.2.0.

┌───────────────────────────────────────────────────────┐
│                RUNNING: just test                     │
└───────────────────────────────────────────────────────┘

---------- Running pytest (parallel, no coverage)... ----------
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
============================= test session starts ==============================
platform linux -- Python 3.14.7, pytest-9.2.0, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase
configfile: pyproject.toml
plugins: mock-3.17.0, cov-7.1.0, inline-snapshot-0.36.1, asyncio-1.4.1, hypothesis-6.170.12, platformdirs-4.13.6, xdist-3.8.0
asyncio: mode=Mode.AUTO, debug=False, asyncio_default_fixture_loop_scope=None, asyncio_default_test_loop_scope=function
created: 7/7 workers
7 workers [39 items]

..................F......F..F..........                                  [100%]

═══════════════════════════════ inline-snapshot ════════════════════════════════
INFO: inline-snapshot was disabled because you used xdist. This means that tests
with snapshots will continue to run, but snapshot(x) will only return x and 
inline-snapshot will not be able to fix snapshots or generate reports.


=================================== FAILURES ===================================
________ test_conflicting_edge_remove_is_quarantined_before_projection _________
[gw0] linux -- Python 3.14.7 /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/python

tmp_path = PosixPath('/var/tmp/sase-5ecca506/pytest-of-bryan/pytest-1/popen-gw0/test_conflicting_edge_remove_i0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7fea334f5e10>

    def test_conflicting_edge_remove_is_quarantined_before_projection(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        redirect_sase_home(monkeypatch, tmp_path / ".sase")
        allow_machine_sidecar_writes(monkeypatch)
        plans = tmp_path / "plans"
        _init_repo(plans, "202609/a.md")
        store = ArtifactLinkStore(
            project_key="gh_sase-org__sase",
            sidecar_roots={"plan": plans},
        )
        operation_id = "e" * 32
        original = observation_or_put_event_from_row(
            _row(
                source="plan:202609/a.md",
                relation="related",
                target="plan:202609/original.md",
                description="original edge",
            ),
            project_key=store.project_key,
            operation_id=operation_id,
        )
        publish_artifact_link_events(
            store,
            (original,),
            push_after_commit=False,
            mutation_origin="machine",
        )
>       remove = edge_remove_event(
            project_key=store.project_key,
            operation_id=operation_id,
            source_ref="plan:202609/a.md",
            relation="related",
            target_ref="plan:202609/original.md",
            created_by="agent:event.athena.worker",
            origin="manual",
            created_at="2026-09-09T00:00:00Z",
            observed_operation_ids=(operation_id,),
        )

tests/sdd/test_artifact_link_event_publisher.py:271: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_canonical.py:181: in edge_remove_event
    return canonical_event(
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

event = {'schema_version': 1, 'project_key': 'gh_sase-org__sase', 'operation_id': 'eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee', 'created_by': 'agent:event.athena.worker', ...}

    def canonical_event(event: Mapping[str, Any]) -> dict[str, Any]:
        """Canonicalize one event through the Rust event contract."""
    
>       return dict(require_rust_binding("artifact_link_event_canonicalize")(dict(event)))
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
E       ValueError: validation: observed_operation_ids cannot reference its own operation_id `eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee`

src/sase/sdd/_artifact_link_event_canonical.py:206: ValueError
__ test_link_add_survives_historical_collision_and_doctor_reports_quarantine ___
[gw3] linux -- Python 3.14.7 /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/python

tmp_path = PosixPath('/var/tmp/sase-5ecca506/pytest-of-bryan/pytest-1/popen-gw3/test_link_add_survives_histori0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f607a9b8d50>
capsys = <_pytest.capture.CaptureFixture object at 0x7f60735291d0>

    def test_link_add_survives_historical_collision_and_doctor_reports_quarantine(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
        capsys: pytest.CaptureFixture[str],
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        patch_link_ops_store(monkeypatch, store)
        monkeypatch.setattr(
            "sase.artifact_cli.link_health.resolve_artifact_link_store",
            lambda: store,
        )
        stub_resolve_cli_reference(
            monkeypatch,
            lambda _ref, **_kwargs: SimpleNamespace(
                resolution=SimpleNamespace(status="exact", resolved_path=None)
            ),
        )
        plans = store.sidecar_roots["plan"]
        documents = plans / "202608"
        documents.mkdir()
        (documents / "a.md").write_text("# A\n", encoding="utf-8")
        (documents / "b.md").write_text("# B\n", encoding="utf-8")
        _git(plans, "add", "-A")
        _git(plans, "commit", "-m", "add artifact-link test documents")
    
        operation_id = "9" * 32
>       original = observation_or_put_event_from_row(
            {
                "schema_version": 1,
                "source_ref": "plan:202608/a.md",
                "relation": "related",
                "target_ref": "plan:202608/original.md",
                "description": "historical winner",
                "origin": "manual",
                "created_by": "bbugyi200.athena.y2",
                "created_at": "2026-08-18T23:40:00Z",
                "uses": 1,
            },
            project_key=store.project_key,
            operation_id=operation_id,
        )

tests/main/test_artifact_cli_link_add.py:166: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_canonical.py:109: in observation_or_put_event_from_row
    canonical_row = validate_artifact_link_row(row)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

row = {'schema_version': 1, 'source_ref': 'plan:202608/a.md', 'relation': 'related', 'target_ref': 'plan:202608/original.md', ...}

    def validate_artifact_link_row(row: Mapping[str, Any]) -> dict[str, Any]:
        """Canonicalize and validate one v2 row through sase-core."""
    
>       return dict(require_rust_binding("artifact_link_validate_row")(dict(row)))
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
E       ValueError: validation: unsupported artifact link schema_version 1; expected 2

src/sase/sdd/_artifact_link_store_support.py:317: ValueError
__________ test_publish_event_rejects_same_path_with_different_bytes ___________
[gw4] linux -- Python 3.14.7 /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/python

tmp_path = PosixPath('/var/tmp/sase-5ecca506/pytest-of-bryan/pytest-1/popen-gw4/test_publish_event_rejects_sam0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7fb5e75865f0>

    def test_publish_event_rejects_same_path_with_different_bytes(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        redirect_sase_home(monkeypatch, tmp_path / ".sase")
        allow_machine_sidecar_writes(monkeypatch)
        plans = tmp_path / "plans"
        _init_repo(plans, "202609/a.md")
        store = ArtifactLinkStore(
            project_key="gh_sase-org__sase",
            sidecar_roots={"plan": plans},
        )
        event = observation_or_put_event_from_row(
            _row(source="plan:202609/a.md", target="agent:reader", origin="manual"),
            project_key=store.project_key,
            operation_id="bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb",
        )
        event_object = canonical_artifact_link_event_object(event)
        path = plans / event_object.relative_path
        path.parent.mkdir(parents=True, exist_ok=True)
        path.write_text("{}\n", encoding="utf-8")
    
        with pytest.raises(ArtifactLinkEventCorruptionError):
>           publish_artifact_link_events(
                store,
                (event,),
                push_after_commit=False,
                mutation_origin="machine",
            )

tests/sdd/test_artifact_link_event_publisher.py:148: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_publish.py:182: in publish_artifact_link_events
    return _publish_event_objects_locked(
src/sase/sdd/_artifact_link_event_publish.py:224: in _publish_event_objects_locked
    snapshot = store.artifact_link_event_snapshot(
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:228: in snapshot
    return reduce_artifact_link_event_inputs(
src/sase/sdd/_artifact_link_event_store.py:441: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=(), pending_events=(), accepted_ev...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=0, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: link-events/v1/35/3595a69327a95b89114bf1dc487cee046ce7a98ee90afa2c4d3f0bd5d6b7a5e3.json: validation: event is not a valid ArtifactLinkEventWire: missing field `schema_version`

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
============================= slowest 20 durations =============================
7.35s call     tests/main/test_artifact_link_outbox_io.py::test_caller_supplied_id_append_scans_only_matching_lines
6.01s setup    tests/main/test_artifact_link_outbox_io.py::test_identical_event_reappend_against_parked_is_a_noop
5.99s setup    tests/sdd/test_artifact_link_event_publisher.py::test_publish_bead_owner_without_bead_store_stays_pending
5.99s setup    tests/sdd/test_artifact_link_event_store_quarantine.py::test_historical_original_wins_with_identical_timestamps_and_reversed_paths
5.97s setup    tests/main/test_artifact_cli_link_add.py::test_add_artifact_link_requires_reason
5.96s setup    tests/sdd/test_artifact_link_event_publisher.py::test_conflicting_edge_remove_is_quarantined_before_projection
5.84s setup    tests/main/test_artifact_link_outbox_drain.py::test_drain_publishes_machine_alias_but_retains_unreleased_read
5.84s setup    tests/main/test_artifact_link_outbox_drain.py::test_drain_allows_trusted_machine_derived_events_without_evidence
2.75s call     tests/main/test_artifact_link_outbox_drain.py::test_drain_allows_trusted_machine_derived_events_without_evidence
0.86s call     tests/main/test_artifact_cli_link_add.py::test_unchanged_add_retries_unpublished_partial_root
0.75s call     tests/main/test_artifact_cli_link_add.py::test_absent_remove_retries_unpublished_tombstone
0.66s call     tests/sdd/test_artifact_link_event_publisher.py::test_publish_event_writes_dual_document_roots_and_replays_idempotently
0.63s call     tests/sdd/test_artifact_link_event_publisher.py::test_publish_event_quarantines_committed_collision_and_keeps_store_writable
0.46s call     tests/main/test_artifact_link_outbox_io.py::test_minted_id_append_performs_no_per_line_binding_calls
0.42s call     tests/main/test_artifact_link_outbox_drain.py::test_mixed_collision_drain_retries_after_quarantine_commit_before_outbox_rewrite
0.41s call     tests/sdd/test_artifact_link_event_publisher.py::test_publish_bead_only_events_get_local_history_before_bead_receipt
0.36s call     tests/sdd/test_artifact_link_event_publisher.py::test_publish_bead_only_event_quarantines_local_operation_collision
0.31s call     tests/main/test_artifact_link_outbox_drain.py::test_repeated_drain_after_partial_failure_does_not_double_count_uses
0.27s call     tests/main/test_artifact_link_outbox_drain.py::test_drain_publishes_machine_alias_but_retains_unreleased_read
0.25s call     tests/main/test_artifact_cli_link_add.py::test_add_list_rm_round_trip
=========================== short test summary info ============================
FAILED tests/sdd/test_artifact_link_event_publisher.py::test_conflicting_edge_remove_is_quarantined_before_projection
FAILED tests/main/test_artifact_cli_link_add.py::test_link_add_survives_historical_collision_and_doctor_reports_quarantine
FAILED tests/sdd/test_artifact_link_event_publisher.py::test_publish_event_rejects_same_path_with_different_bytes
======================== 3 failed, 36 passed in 25.55s =========================
error: recipe `test` failed on line 588 with exit code 1
failed  exit=1  duration=33450ms

