# Chat History - ace-run (bob-cli-df.2.1.4.2--mon)

- **TIMESTAMP:** 2026-10-28 03:50:03 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-df.2.1.4.2--mon

## Prompt

sase monitor start --command 'just --set sase_core_dir /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core install-venv && .venv/bin/python -m pytest tests/sdd/test_artifact_link_quarantine_replay_evidence.py tests/sdd/test_artifact_link_event_store_quarantine.py tests/sdd/test_artifact_link_event_quarantine_io.py -q' --reason 'Provision SASE venv and run focused replay-evidence suites for bob-cli-df.2.1.4.2'

## Response

sase tool run 3aacc7df3fef1d3284e23cd028094e82
[install-venv] Installing local sase_core_rs from /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core for local dev.
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
[sase-core-wheel-cache] miss: no exact cached wheel
🍹 Building a mixed python/rust project
🐍 Found CPython 3.14 at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/python
🔗 Found pyo3 bindings with abi3-py3.12 support
📡 Using build options features from pyproject.toml
   Compiling sase_core_py v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/crates/sase_core_py)
    Finished `release` profile [optimized] target(s) in 7m 20s
📦 Built wheel for abi3 Python ≥ 3.12 to /home/bryan/.sase/cache/sase-core-artifacts/.build-0o98yayj/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl
[rust-install] Installing cached sase_core_rs wheel from /home/bryan/.sase/cache/sase-core-artifacts/4d819aa1a31e4877ef13b36bbac4950cba25f5f7641b781e38a2193d62172a73/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl.
Resolved 1 package in 4ms
Prepared 1 package in 163ms
Installed 1 package in 4ms
 + sase-core-rs==0.43.0 (from file:///home/bryan/.sase/cache/sase-core-artifacts/4d819aa1a31e4877ef13b36bbac4950cba25f5f7641b781e38a2193d62172a73/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl)
# Keep the LSP server in lockstep with the extension: both are built
# from the same sase-core checkout, and the ACE/LSP parity tests
# compare their directive contracts.
[sase-core-wheel-cache] miss: no exact cached wheel
   Compiling libc v0.2.186
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling zerocopy v0.8.48
   Compiling memchr v2.8.0
   Compiling cfg-if v1.0.4
   Compiling crossbeam-utils v0.8.21
   Compiling serde_core v1.0.228
   Compiling find-msvc-tools v0.1.9
   Compiling shlex v1.3.0
   Compiling regex-syntax v0.8.10
   Compiling version_check v0.9.5
   Compiling siphasher v1.0.4
   Compiling autocfg v1.5.0
   Compiling serde v1.0.228
   Compiling zmij v1.0.21
   Compiling crossbeam-epoch v0.9.21
   Compiling once_cell v1.21.4
   Compiling crossbeam-deque v0.8.8
   Compiling serde_json v1.0.149
   Compiling log v0.4.29
   Compiling hashbrown v0.17.0
   Compiling ucd-trie v0.1.7
   Compiling pin-project-lite v0.2.17
   Compiling iana-time-zone v0.1.65
   Compiling equivalent v1.0.2
   Compiling bitflags v2.11.1
   Compiling smallvec v1.15.1
   Compiling itoa v1.0.18
   Compiling same-file v1.0.6
   Compiling futures-sink v0.3.32
   Compiling futures-core v0.3.32
   Compiling libm v0.2.16
   Compiling parking_lot_core v0.9.12
   Compiling typenum v1.20.0
   Compiling slab v0.4.12
   Compiling lazy_static v1.5.0
   Compiling futures-task v0.3.32
   Compiling deunicode v1.6.2
   Compiling bytes v1.11.1
   Compiling scopeguard v1.2.0
   Compiling futures-io v0.3.32
   Compiling rayon-core v1.13.0
   Compiling either v1.19.0
   Compiling clap_lex v1.1.1
   Compiling pkg-config v0.3.33
   Compiling percent-encoding v2.3.2
   Compiling vcpkg v0.2.15
   Compiling thiserror v1.0.69
   Compiling heck v0.5.0
   Compiling unicode-segmentation v1.13.3
   Compiling anstyle v1.0.14
   Compiling rustix v1.1.4
   Compiling ahash v0.8.12
   Compiling phf_shared v0.11.3
   Compiling generic-array v0.14.7
   Compiling sync_wrapper v1.0.2
   Compiling tower-layer v0.3.3
   Compiling cc v1.2.61
   Compiling num-traits v0.2.19
   Compiling tracing-core v0.1.36
   Compiling encoding_rs v0.8.35
   Compiling getrandom v0.4.2
   Compiling tower-service v0.3.3
   Compiling winnow v1.0.4
   Compiling itertools v0.11.0
   Compiling aho-corasick v1.1.4
   Compiling bstr v1.13.1
   Compiling grep-matcher v0.1.9
   Compiling clap_builder v4.6.7
   Compiling bitflags v1.3.2
   Compiling colored v2.2.0
   Compiling toml_writer v1.1.3+spec-1.1.0
   Compiling linux-raw-sys v0.12.1
   Compiling lock_api v0.4.14
   Compiling home v0.5.12
   Compiling cpufeatures v0.2.17
   Compiling winnow v0.7.15
   Compiling httparse v1.10.1
   Compiling ryu v1.0.23
   Compiling slug v0.1.6
   Compiling fallible-streaming-iterator v0.1.9
   Compiling unsafe-libyaml v0.2.11
   Compiling fastrand v2.4.1
   Compiling tinyvec v1.13.3
   Compiling fallible-iterator v0.3.0
   Compiling sharded-slab v0.1.7
   Compiling thread_local v1.1.9
   Compiling hex v0.4.3
   Compiling indexmap v2.14.0
   Compiling unicode-casefold v0.2.0
   Compiling futures-channel v0.3.32
   Compiling semver v1.0.28
   Compiling nu-ansi-term v0.50.3
   Compiling walkdir v2.5.0
   Compiling unicode-width v0.2.2
   Compiling crossbeam-channel v0.5.17
   Compiling toml_datetime v0.7.5+spec-1.1.0
   Compiling serde_spanned v1.1.2
   Compiling ppv-lite86 v0.2.21
   Compiling phf v0.11.3
   Compiling errno v0.3.14
   Compiling socket2 v0.6.3
   Compiling mio v1.2.0
   Compiling getrandom v0.2.17
   Compiling memmap2 v0.9.11
   Compiling term_size v0.3.2
   Compiling fs2 v0.4.3
   Compiling encoding_rs_io v0.1.8
   Compiling psm v0.1.24
   Compiling stacker v0.1.25
   Compiling regex-automata v0.4.14
   Compiling libsqlite3-sys v0.30.1
   Compiling toml_parser v1.1.5+spec-1.1.0
   Compiling humansize v2.1.3
   Compiling tracing-log v0.2.0
   Compiling fluent-uri v0.1.4
   Compiling etcetera v0.8.0
   Compiling block-buffer v0.10.4
   Compiling crypto-common v0.1.7
   Compiling unicode-normalization v0.1.25
   Compiling hashbrown v0.14.5
   Compiling signal-hook-registry v1.4.8
   Compiling parking_lot v0.12.5
   Compiling grep-searcher v0.1.17
   Compiling toml v0.9.12+spec-1.1.0
   Compiling rand_core v0.6.4
   Compiling globset v0.4.19
   Compiling regex v1.12.3
   Compiling matchers v0.2.0
   Compiling digest v0.10.7
   Compiling hashlink v0.9.1
   Compiling chrono v0.4.44
   Compiling tempfile v3.27.0
   Compiling rand_chacha v0.3.1
   Compiling ignore v0.4.32
   Compiling sha1 v0.10.7
   Compiling sha2 v0.10.9
   Compiling parse-zoneinfo v0.3.1
   Compiling pest v2.9.4
   Compiling rayon v1.12.0
   Compiling rand v0.8.6
   Compiling globwalk v0.9.1
   Compiling syn v2.0.117
   Compiling syn v3.0.9
   Compiling pest_meta v2.9.4
   Compiling phf_generator v0.11.3
   Compiling pest_generator v2.9.4
   Compiling clap_derive v4.6.7
   Compiling derive_arbitrary v1.5.0
   Compiling serde_derive v1.0.228
   Compiling tokio-macros v2.7.0
   Compiling futures-macro v0.3.32
   Compiling tracing-attributes v0.1.31
   Compiling thiserror-impl v1.0.69
   Compiling serde_repr v0.1.20
   Compiling phf_codegen v0.11.3
   Compiling tokio v1.52.2
   Compiling arbitrary v1.5.0
   Compiling futures-util v0.3.32
   Compiling chrono-tz-build v0.3.0
   Compiling pest_derive v2.9.4
   Compiling tracing v0.1.44
   Compiling clap v4.6.7
   Compiling table_formatter v0.6.1
   Compiling tracing-subscriber v0.3.23
   Compiling chrono-tz v0.9.0
   Compiling futures v0.3.32
   Compiling tower v0.5.3
   Compiling tokio-util v0.7.18
   Compiling clap-cargo v0.18.3
   Compiling json5 v0.4.1
   Compiling dashmap v6.1.0
   Compiling lsp-types v0.97.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tera v1.20.1
   Compiling sase_workspace_hack v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/crates/sase_workspace_hack)
   Compiling tokei v15.0.0
   Compiling tower-lsp-server v0.21.1
   Compiling rusqlite v0.32.1
   Compiling sase_core v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/crates/sase_core)
   Compiling sase_macro_lsp v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/gh/sase-org/sase-core/crates/sase_macro_lsp)
    Finished `dev-update` profile [optimized] target(s) in 3m 32s
[rust-lsp-install] Installing cached LSP binary from /home/bryan/.sase/cache/sase-core-artifacts/0eecc70aa2f59552eead0683ff8cf2ef3e15ea3a11c10a2fe53ba5ebe311a5a5/sase-macro-lsp.
[rust-lsp-install] installed /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/bin/sase-macro-lsp
uv pip install --python .venv/bin/python --no-sources $(just _core-overrides-arg) -e ".[dev]"
Resolved 98 packages in 166ms
   Building sase @ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase
      Built sase @ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase
Prepared 4 packages in 606ms
Uninstalled 1 package in 0.84ms
Installed 98 packages in 144ms
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
 + platformdirs==4.13.7
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
 + python-discovery==1.6.7
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
 - sase-core-rs==0.43.0 (from file:///home/bryan/.sase/cache/sase-core-artifacts/4d819aa1a31e4877ef13b36bbac4950cba25f5f7641b781e38a2193d62172a73/sase_core_rs-0.43.0-cp312-abi3-manylinux_2_39_x86_64.whl)
 + sase-core-rs==0.42.7
 + schedule==1.2.2
 + secretstorage==3.5.0
 + sortedcontainers==2.4.0
 + symvision==0.1.0
 + textual==8.2.8
 + tomli-w==1.2.0
 + toobig==0.1.0
 + tox==4.67.4
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase/.venv/lib/python3.14/site-packages/pytest_asyncio/plugin.py:300: PytestDeprecationWarning: The configuration option "asyncio_default_fixture_loop_scope" is unset.
The event loop scope for asynchronous fixtures will default to the "fixture" caching scope. Future versions of pytest-asyncio will default the loop scope for asynchronous fixtures to "function" scope. Set the default fixture loop scope explicitly in order to avoid unexpected behavior in the future. Valid fixture loop scopes are: "function", "class", "module", "package", "session"

  warnings.warn(PytestDeprecationWarning(_DEFAULT_FIXTURE_LOOP_SCOPE_UNSET))
.FFFFFFFFFFFFFF..                                                        [100%]
=================================== FAILURES ===================================
___________________ test_timezone_histories_order_by_instant ___________________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_timezone_histories_order_0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431ee12f50>

    def test_timezone_histories_order_by_instant(
        tmp_path: Path, monkeypatch: pytest.MonkeyPatch
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        plans = tmp_path / "plans"
        _init_repo(plans, monkeypatch)
        # Earlier instant 10:00Z spelled with +02:00 sorts lexically after 10:30Z.
        early = edge_event(
            "b" * 32,
            target="plan:202608/early.md",
            description="earlier instant",
        )
        late = edge_event(
            "b" * 32,
            target="plan:202608/late.md",
            description="later instant",
        )
        early_path = write_event(plans, early)
        _commit_all(plans, "early payload", when="2026-10-27T12:00:00+02:00")
        late_path = write_event(plans, late)
        _commit_all(plans, "late payload", when="2026-10-27T10:30:00+00:00")
    
        early_commit = _git(plans, "log", "--diff-filter=A", "--format=%H",
                            "--", early_path.relative_to(plans).as_posix()).splitlines()[-1].strip()
        late_commit = _git(plans, "log", "--diff-filter=A", "--format=%H",
                           "--", late_path.relative_to(plans).as_posix()).splitlines()[-1].strip()
        assert early_commit != late_commit
    
>       snapshot = store.artifact_link_event_snapshot(strict=True)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_quarantine_replay_evidence.py:165: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
__________ test_quarantine_reuse_preserves_bytes_across_basis_change ___________

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_quarantine_reuse_preserve0')

    def test_quarantine_reuse_preserves_bytes_across_basis_change(
        tmp_path: Path,
    ) -> None:
        first, second = _colliding_pair()
>       snapshot = reduce_artifact_link_event_inputs(
            durable_events=(first, second),
            strict=True,
        )

tests/sdd/test_artifact_link_quarantine_replay_evidence.py:176: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_store.py:443: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=({'schema_version': 1, 'project_ke...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=2, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
____________ test_quarantine_reject_different_payload_is_corruption ____________

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_quarantine_reject_differe0')

    def test_quarantine_reject_different_payload_is_corruption(
        tmp_path: Path,
    ) -> None:
        from sase.sdd._artifact_link_event_install import ArtifactLinkEventCorruptionError
    
        first, second = _colliding_pair()
>       snapshot = reduce_artifact_link_event_inputs(
            durable_events=(first, second),
            strict=True,
        )

tests/sdd/test_artifact_link_quarantine_replay_evidence.py:210: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_store.py:443: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=({'schema_version': 1, 'project_ke...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=2, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
__________ test_quarantine_wrong_path_and_wrong_project_are_blocking ___________

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_quarantine_wrong_path_and0')

    def test_quarantine_wrong_path_and_wrong_project_are_blocking(
        tmp_path: Path,
    ) -> None:
        first, second = _colliding_pair()
>       snapshot = reduce_artifact_link_event_inputs(
            durable_events=(first, second),
            strict=True,
        )

tests/sdd/test_artifact_link_quarantine_replay_evidence.py:238: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_store.py:443: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=({'schema_version': 1, 'project_ke...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=2, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
___________ test_same_batch_collision_settles_idempotently_on_retry ____________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_same_batch_collision_sett0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431795f4d0>

    def test_same_batch_collision_settles_idempotently_on_retry(
        tmp_path: Path, monkeypatch: pytest.MonkeyPatch
    ) -> None:
        redirect_sase_home(monkeypatch, tmp_path / ".sase")
        allow_machine_sidecar_writes(monkeypatch)
        from sase.sdd.artifact_link_event_publisher import publish_artifact_link_events
    
        plans = tmp_path / "plans"
        plans.mkdir(parents=True, exist_ok=True)
        _init_repo(plans, monkeypatch)
        (plans / "202609" / "a.md").parent.mkdir(parents=True, exist_ok=True)
        (plans / "202609" / "a.md").write_text("# Doc\n", encoding="utf-8")
        _commit_all(plans, "initial doc")
    
        store = ArtifactLinkStore(
            project_key=PROJECT_KEY,
            sidecar_roots={"plan": plans},
        )
        first, second = _colliding_pair()
        unrelated = edge_event(
            "b" * 32,
            target="plan:202608/fresh.md",
            description="unrelated append",
        )
>       report = publish_artifact_link_events(
            store,
            (first, second, unrelated),
            push_after_commit=False,
            mutation_origin="machine",
        )

tests/sdd/test_artifact_link_quarantine_replay_evidence.py:307: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_publish.py:185: in publish_artifact_link_events
    return _publish_event_objects_locked(
src/sase/sdd/_artifact_link_event_publish.py:227: in _publish_event_objects_locked
    snapshot = store.artifact_link_event_snapshot(
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
__ test_historical_original_wins_with_identical_timestamps_and_reversed_paths __

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_historical_original_wins_0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431edcb770>

    def test_historical_original_wins_with_identical_timestamps_and_reversed_paths(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        plans = tmp_path / "plans"
        _init_git_repo(plans, monkeypatch)
        original, replay = _colliding_pair()
        assert _digest(original) > _digest(replay)
    
        original_path = write_event(plans, original)
        _commit(plans, "original durable event")
        replay_path = write_event(plans, replay)
        _commit(plans, "conflicting replay")
        before = _git(plans, "status", "--porcelain").stdout
    
>       snapshot = store.artifact_link_event_snapshot(strict=True)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_store_quarantine.py:97: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
_____________ test_pending_replay_does_not_override_durable_winner _____________

name = 'artifact_link_collision_wire_schema_version'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_collision_wire_schema_version'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_pending_replay_does_not_o0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431778fc70>

    def test_pending_replay_does_not_override_durable_winner(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        original, replay = _colliding_pair()
        write_event(tmp_path / "plans", original)
>       append_artifact_link_outbox_event(
            project_key=PROJECT_KEY,
            agent_name="agent:pending.athena.worker",
            run_id="run-1",
            event=replay,
        )

tests/sdd/test_artifact_link_event_store_quarantine.py:152: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_outbox_io.py:159: in append_artifact_link_outbox_event
    rows = _rows_from_events((canonical,))
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
src/sase/sdd/_artifact_link_outbox_types.py:189: in rows_from_events
    return _event_rows_from_events(events)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
src/sase/sdd/_artifact_link_event_canonical.py:253: in rows_from_events
    reduction = reduce_events(events)
                ^^^^^^^^^^^^^^^^^^^^^
src/sase/sdd/_artifact_link_event_canonical.py:273: in reduce_events
    partition = partition_artifact_link_candidates(
src/sase/sdd/_artifact_link_event_collision.py:105: in partition_artifact_link_candidates
    require_rust_binding("artifact_link_collision_wire_schema_version")()
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_collision_wire_schema_version'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
____________ test_covers_row_keeps_rejected_edge_from_resurrecting _____________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_covers_row_keeps_rejected0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f4320e23290>

    def test_covers_row_keeps_rejected_edge_from_resurrecting(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        original, replay = _colliding_pair()
        write_event(tmp_path / "plans", original)
        write_event(tmp_path / "plans", replay)
    
>       snapshot = store.artifact_link_event_snapshot(strict=True)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_store_quarantine.py:181: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
______________ test_malformed_event_object_still_blocks_the_store ______________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_malformed_event_object_st0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f4320e20ad0>

    def test_malformed_event_object_still_blocks_the_store(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        original, replay = _colliding_pair()
        write_event(tmp_path / "plans", original)
        write_event(tmp_path / "plans", replay)
        bad = tmp_path / "plans" / "link-events" / "v1" / "00" / "dead.json"
        bad.parent.mkdir(parents=True, exist_ok=True)
        bad.write_text("{not json", encoding="utf-8")
    
>       snapshot = store.artifact_link_event_snapshot(strict=False)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_store_quarantine.py:213: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
_______ test_local_admission_sequence_picks_the_first_installed_payload ________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_local_admission_sequence_0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431ec9e4c0>

    def test_local_admission_sequence_picks_the_first_installed_payload(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        first, second = _colliding_pair()
        first_obj = canonical_artifact_link_event_object(first)
        second_obj = canonical_artifact_link_event_object(second)
        assert install_local_artifact_link_event(PROJECT_KEY, first_obj)
        assert install_local_artifact_link_event(PROJECT_KEY, second_obj)
    
>       snapshot = store.artifact_link_event_snapshot(strict=True)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_store_quarantine.py:232: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
________ test_digest_tie_break_without_history_keeps_the_store_writable ________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_digest_tie_break_without_0')
monkeypatch = <_pytest.monkeypatch.MonkeyPatch object at 0x7f431ed67e30>

    def test_digest_tie_break_without_history_keeps_the_store_writable(
        tmp_path: Path,
        monkeypatch: pytest.MonkeyPatch,
    ) -> None:
        store = make_store(tmp_path, monkeypatch)
        first, second = _colliding_pair()
        write_event(tmp_path / "plans", first)
        write_event(tmp_path / "plans", second)
    
>       snapshot = store.artifact_link_event_snapshot(strict=True)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_store_quarantine.py:254: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_store_core.py:115: in artifact_link_event_snapshot
    ).snapshot(
src/sase/sdd/_artifact_link_event_store.py:219: in snapshot
    persisted, persisted_errors = load_artifact_link_quarantine_records(
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
_______ test_persist_quarantine_record_is_idempotent_for_identical_bytes _______

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_persist_quarantine_record0')

    def test_persist_quarantine_record_is_idempotent_for_identical_bytes(
        tmp_path: Path,
    ) -> None:
        first, second = _colliding_events()
>       snapshot = reduce_artifact_link_event_inputs(
            durable_events=(first, second),
            strict=True,
        )

tests/sdd/test_artifact_link_event_quarantine_io.py:50: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_store.py:443: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=({'schema_version': 1, 'project_ke...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=2, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
______ test_existing_quarantine_record_with_different_bytes_is_corruption ______

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_existing_quarantine_recor0')

    def test_existing_quarantine_record_with_different_bytes_is_corruption(
        tmp_path: Path,
    ) -> None:
        first, second = _colliding_events()
>       snapshot = reduce_artifact_link_event_inputs(
            durable_events=(first, second),
            strict=True,
        )

tests/sdd/test_artifact_link_event_quarantine_io.py:83: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_store.py:443: in reduce_artifact_link_event_inputs
    snapshot.assert_healthy()
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

self = ArtifactLinkEventSnapshot(rows=(), durable_rows=(), pending_rows=(), durable_events=({'schema_version': 1, 'project_ke...=0, oldest_age_seconds=0.0, newest_age_seconds=0.0, p95_age_seconds=0.0), durable_event_count=2, pending_event_count=0)

    def assert_healthy(self) -> None:
        if self.healthy:
            return
>       raise RuntimeError(
            "artifact-link event store is invalid: "
            + _join_problems(self.blocking_problem_messages)
        )
E       RuntimeError: artifact-link event store is invalid: sase_core_rs is importable but does not expose binding 'artifact_link_collision_wire_schema_version'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/sdd/_artifact_link_event_store.py:115: RuntimeError
__________ test_malformed_quarantine_record_is_a_blocking_load_error ___________

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
>           return getattr(module, name)
                   ^^^^^^^^^^^^^^^^^^^^^
E           AttributeError: module 'sase_core_rs' has no attribute 'artifact_link_quarantine_record_validate'

src/sase/core/rust.py:69: AttributeError

The above exception was the direct cause of the following exception:

tmp_path = PosixPath('/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261028_020917/pytest-of-bryan/pytest-0/test_malformed_quarantine_reco0')

    def test_malformed_quarantine_record_is_a_blocking_load_error(
        tmp_path: Path,
    ) -> None:
        path = (
            tmp_path / "link-events" / "quarantine" / "v1" / ("a" * 32) / f"{'b' * 64}.json"
        )
        path.parent.mkdir(parents=True, exist_ok=True)
        path.write_text("{not json", encoding="utf-8")
    
>       findings, errors = load_artifact_link_quarantine_records((tmp_path,))
                           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

tests/sdd/test_artifact_link_event_quarantine_io.py:107: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
src/sase/sdd/_artifact_link_event_quarantine.py:186: in load_artifact_link_quarantine_records
    validate = require_rust_binding("artifact_link_quarantine_record_validate")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

name = 'artifact_link_quarantine_record_validate'

    def require_rust_binding(name: str) -> Any:
        """Return ``sase_core_rs.<name>`` or raise with operation-specific text.
    
        Raises:
            ImportError: when the extension module itself is not importable
                (delegated to :func:`require_rust_extension`).
            AttributeError: when the extension is importable but does not
                expose the requested binding. This typically means the wheel
                is too old or was built without the shipped bindings.
        """
        module = require_rust_extension()
        try:
            return getattr(module, name)
        except AttributeError as exc:
>           raise AttributeError(
                f"{RUST_EXTENSION_MODULE_NAME} is importable but does not expose "
                f"binding {name!r}; the installed wheel is stale or was built "
                f"without the shipped bindings. {_install_hint().capitalize()}."
            ) from exc
E           AttributeError: sase_core_rs is importable but does not expose binding 'artifact_link_quarantine_record_validate'; the installed wheel is stale or was built without the shipped bindings. Run `just install-venv` in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/external/projects/sase.

src/sase/core/rust.py:71: AttributeError
============================= slowest 20 durations =============================
5.01s setup    tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_shallow_history_marks_evidence_incomplete
0.07s call     tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_shallow_history_marks_evidence_incomplete
0.04s call     tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_timezone_histories_order_by_instant
0.04s call     tests/sdd/test_artifact_link_event_store_quarantine.py::test_local_admission_sequence_picks_the_first_installed_payload
0.02s call     tests/sdd/test_artifact_link_event_store_quarantine.py::test_historical_original_wins_with_identical_timestamps_and_reversed_paths
0.02s call     tests/sdd/test_artifact_link_event_quarantine_io.py::test_admission_sequence_assigns_monotonic_first_wins_values
0.02s call     tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_same_batch_collision_settles_idempotently_on_retry
0.01s call     tests/sdd/test_artifact_link_event_quarantine_io.py::test_attach_admission_evidence_fills_local_sequences

(12 durations < 0.005s hidden.  Use -vv to show these durations.)
=========================== short test summary info ============================
FAILED tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_timezone_histories_order_by_instant
FAILED tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_quarantine_reuse_preserves_bytes_across_basis_change
FAILED tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_quarantine_reject_different_payload_is_corruption
FAILED tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_quarantine_wrong_path_and_wrong_project_are_blocking
FAILED tests/sdd/test_artifact_link_quarantine_replay_evidence.py::test_same_batch_collision_settles_idempotently_on_retry
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_historical_original_wins_with_identical_timestamps_and_reversed_paths
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_pending_replay_does_not_override_durable_winner
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_covers_row_keeps_rejected_edge_from_resurrecting
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_malformed_event_object_still_blocks_the_store
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_local_admission_sequence_picks_the_first_installed_payload
FAILED tests/sdd/test_artifact_link_event_store_quarantine.py::test_digest_tie_break_without_history_keeps_the_store_writable
FAILED tests/sdd/test_artifact_link_event_quarantine_io.py::test_persist_quarantine_record_is_idempotent_for_identical_bytes
FAILED tests/sdd/test_artifact_link_event_quarantine_io.py::test_existing_quarantine_record_with_different_bytes_is_corruption
FAILED tests/sdd/test_artifact_link_event_quarantine_io.py::test_malformed_quarantine_record_is_a_blocking_load_error
14 failed, 3 passed in 11.32s
failed  exit=1  duration=672699ms

