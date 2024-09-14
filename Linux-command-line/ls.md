# ls

The full specification of the <b>ls</b> command includes various options that can customize <b>how files and directories are listed</b>. Here's a detailed look at the most commonly used options:

## Basic usage:

<pre>

ls [option]... [file]...
</pre>

<pre>

Ex-

<b>Input:</b>
<pre>

ls -a ./Desktop
</pre>

<b>Output:</b>
<pre>

 .   ..  'command line prac'   Linux   Linux-command-line   Python   .venv
</pre>
</pre>

## Common usage:

+ <b>-a (all):</b> Lists all files, including hidden ones (those that start with a dot).

<pre>

ls -a
</pre>

<pre>

    <b>Input</b>: ls -a

    <b>Output</b>:
    <pre>

    Desktop                                 Music          Templates
    discord.deb                             Pictures       Videos
    Documents                               Public         WhiteSur-gtk-theme
    Downloads                               Python-3.12.0
    google-chrome-stable_current_amd64.deb  snap
    </pre>
</pre>


+ <b/>-l (long format):</b>
Displays files in long format, showing details like permissions, owner, size, and modification date.

<pre>

ls -l
</pre>

<pre>

    <b>Input</b>: ls -l

    <b>Output</b>:
    <pre>

    total 207576
    drwxr-xr-x  7 rashik rashik      4096 Sep 12 12:12 Desktop
    -rw-rw-r--  1 rashik rashik 103057576 Sep 10 03:08 discord.deb
    drwxr-xr-x  2 rashik rashik      4096 Sep  7 12:46 Documents
    drwxr-xr-x  3 rashik rashik      4096 Sep 12 15:46 Downloads
    -rw-rw-r--  1 rashik rashik 109450340 Jul 30 05:08 google-chrome-stable_current_amd64.deb
    drwxr-xr-x  2 rashik rashik      4096 Aug 27 09:43 Music
    drwxr-xr-x  4 rashik rashik      4096 Aug 27 21:12 Pictures
    drwxr-xr-x  2 rashik rashik      4096 Aug  3 10:57 Public
    drwx------ 18 rashik rashik      4096 Aug  7 10:12 Python-3.12.0
    drwx------ 10 rashik rashik      4096 Sep  7 14:46 snap
    drwxr-xr-x  2 rashik rashik      4096 Aug  3 10:57 Templates
    drwxr-xr-x  2 rashik rashik      4096 Aug  3 10:57 Videos
    drwxrwxr-x  7 rashik rashik      4096 Aug  3 12:45 WhiteSur-gtk-theme
    </pre>
    
</pre>

+ <b>-h (human-readable):</b>
Used with -l, this option makes file sizes easier to read (e.g., 5K, 10M, 3G)
<pre>

Ex-

<b>Input:</b>
<pre>

ls -lh
</pre>

<b>Output:</b>
<pre>

total 203M
drwxr-xr-x  7 rashik rashik 4.0K Sep 12 12:12 Desktop
-rw-rw-r--  1 rashik rashik  99M Sep 10 03:08 discord.deb
drwxr-xr-x  2 rashik rashik 4.0K Sep  7 12:46 Documents
drwxr-xr-x  3 rashik rashik 4.0K Sep 12 15:46 Downloads
-rw-rw-r--  1 rashik rashik 105M Jul 30 05:08 google-chrome-stable_current_amd64.deb
drwxr-xr-x  2 rashik rashik 4.0K Aug 27 09:43 Music
drwxr-xr-x  4 rashik rashik 4.0K Aug 27 21:12 Pictures
drwxr-xr-x  2 rashik rashik 4.0K Aug  3 10:57 Public
drwx------ 18 rashik rashik 4.0K Aug  7 10:12 Python-3.12.0
drwx------ 10 rashik rashik 4.0K Sep  7 14:46 snap
drwxr-xr-x  2 rashik rashik 4.0K Aug  3 10:57 Templates
drwxr-xr-x  2 rashik rashik 4.0K Aug  3 10:57 Videos
drwxrwxr-x  7 rashik rashik 4.0K Aug  3 12:45 WhiteSur-gtk-theme
</pre>
</pre>

+ <b>-r (reverse):</b>
Reverses the order of the listing.
<pre>

Ex-

<b>Input:</b>
<pre>

ls -r
</pre>

<b>Output:</b>
<pre>

WhiteSur-gtk-theme  Public                                  Documents
Videos              Pictures                                discord.deb
Templates           Music                                   Desktop
snap                google-chrome-stable_current_amd64.deb
Python-3.12.0       Downloads
</pre>
</pre>

+ <b>-t (time):</b>
Sorts files by modification time, with the most recently modified first.
<pre>

Ex-

<b>Input:</b>
<pre>

ls -t
</pre>

<b>Output:</b>
<pre>

Downloads    Pictures            Templates
Desktop      Music               Videos
discord.deb  Python-3.12.0       google-chrome-stable_current_amd64.deb
snap         WhiteSur-gtk-theme
Documents    Public
</pre>
</pre>

+ <b>-S (size):</b>
Sorts files by size, with the largest first.

<pre>

Ex-

<b>Input:</b>
<pre>

ls -s
</pre>
<b>Output:</b>
<pre>

total 207576
     4 Desktop                                      4 Public
100644 discord.deb                                  4 Python-3.12.0
     4 Documents                                    4 snap
     4 Downloads                                    4 Templates
106888 google-chrome-stable_current_amd64.deb       4 Videos
     4 Music                                        4 WhiteSur-gtk-theme
     4 Pictures
</pre>
</pre>


+ <b>-d (directory):</b>
List directories themselves, not their contents.
<pre>

ex- 

<b>Input:</b>
<pre>

ls -d
</pre>

<b>Output:</b>
<pre>

.
</pre>
</pre>

+ <b>-R (recursive):</b>
Recursively lists files in all subdirectories.

<pre>

Ex-

<b>Input:</b>
<pre>

ls -R
</pre>

<b>Output:</b>

<pre>

 ls -R
.:
Desktop                                 Music          Templates
discord.deb                             Pictures       Videos
Documents                               Public         WhiteSur-gtk-theme
Downloads                               Python-3.12.0
google-chrome-stable_current_amd64.deb  snap

./Desktop:
'command line prac'   Linux   Linux-command-line   Python

'./Desktop/command line prac':
 cpfile1.txt   file1.txt   lecture0-720p-en.txt  'linux comman line'   nnn

'./Desktop/command line prac/linux comman line':
Linux-command-line

'./Desktop/command line prac/linux comman line/Linux-command-line':
egrep.md  fgrep.md  grep.md  pdfgrep.md  README.md  zgrep.md

'./Desktop/command line prac/nnn':
cpfile2.txt  cpfile3.txt  cpfile4.txt  cpfile5.txt

./Desktop/Linux:
Linux

./Desktop/Linux/Linux:
10-linux_redirects.md                          6-about_kali_linux.md
1-what_is_linux.md                             7-vi_and_vim_editor.md
2-what_is_virtualization.md                    8-nano_editor.md
3-virtual_box_setup.md                         9-how_to_use_pipe.md
4-access_remote_server_rmeotely_using_SSH.md   Linux-command-line
5-transfar_files_between_linux_and_windows.md

./Desktop/Linux/Linux/Linux-command-line:
alias.md    egrep.md      locate.md    rmdir.md      touch.md
apt.md      exit.md       lsblk.md     rm.md         traceroute.md
arch.md     export.md     lscpu.md     rm_-rf.md     tr.md
at.md       fgrep.md      ls.md        scp.md        truncate.md
awk.md      find.md       man.md       script.md     uname.md
cal.md      free.md       mkdir.md     sed.md        unzip.md
cat.md      grep.md       more.md      shuf.md       updatedb.md
cd.md       groupadd.md   mv.md        shutdown.md   uptime.md
clear.md    gunzip.md     nano.md      sort.md       useradd.md
cmp.md      gzip.md       netstat.md   source.md     vi.md
cp.md       head.md       nohup.md     split.md      wc.md
crontab.md  help.md       passwd.md    ssh.md        wget.md
curl.md     history.md    pdfgrep.md   sudo.md       which.md
cut.md      hostename.md  pgrep.md     su.md         whoami.md
date.md     id.md         ping.md      systemctl.md  zgrep.md
df.md       ifconfig.md   printenv.md  tail.md       zip.md
diff.md     jobs.md       ps.md        tar.md
du.md       kill.md       pwd.md       telnet.md
echo.md     less.md       reboot.md    top.md

./Desktop/Linux-command-line:
egrep.md  fgrep.md  grep.md  pdfgrep.md  zgrep.md

./Desktop/Python:
Python-Practices  venv

./Desktop/Python/Python-Practices:
10-Python_Tuple_Exercise          5-Python_String_Exercise
11-Python_Date_and_Time_Exercise  6-Python_Data_Structure_Exercise
1-python_basic_practice           7-Python_List_Exercise
2-python_input_and_output         8-Python_Dictionary_Exercise
3-Python_Loop_Exercise            9-Python_Set_Exercise
4-Python_Functions_Exercise

./Desktop/Python/Python-Practices/10-Python_Tuple_Exercise:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/11-Python_Date_and_Time_Exercise:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/1-python_basic_practice:
ex_10.py  ex_12.py  ex_14.py  ex_1.py  ex_3.py  ex_5.py  ex_7.py  ex_9.py
ex_11.py  ex_13.py  ex_15.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py

./Desktop/Python/Python-Practices/2-python_input_and_output:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/3-Python_Loop_Exercise:
ex_10.py  ex_13.py  ex_16.py  ex_1.py  ex_4.py  ex_7.py
ex_11.py  ex_14.py  ex_17.py  ex_2.py  ex_5.py  ex_8.py
ex_12.py  ex_15.py  ex_18.py  ex_3.py  ex_6.py  ex_9.py

./Desktop/Python/Python-Practices/4-Python_Functions_Exercise:
ex_1.py  ex_3.py  ex_5.py  ex_7.py  ex_9.py
ex_2.py  ex_4.py  ex_6.py  ex_8.py

./Desktop/Python/Python-Practices/5-Python_String_Exercise:
ex_10.py  ex_13.py  ex_16.py  ex_1.py  ex_4.py  ex_7.py
ex_11.py  ex_14.py  ex_17.py  ex_2.py  ex_5.py  ex_8.py
ex_12.py  ex_15.py  ex_18.py  ex_3.py  ex_6.py  ex_9.py

./Desktop/Python/Python-Practices/6-Python_Data_Structure_Exercise:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/7-Python_List_Exercise:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/8-Python_Dictionary_Exercise:
ex_10.py  ex_2.py  ex_4.py  ex_6.py  ex_8.py
ex_1.py   ex_3.py  ex_5.py  ex_7.py  ex_9.py

./Desktop/Python/Python-Practices/9-Python_Set_Exercise:
ex_1.py  ex_3.py  ex_5.py  ex_7.py  ex_9.py
ex_2.py  ex_4.py  ex_6.py  ex_8.py

./Desktop/Python/venv:
bin  lib  pyvenv.cfg

./Desktop/Python/venv/bin:
activate       activate.nu       pip       pip3.12  python3.12
activate.csh   activate.ps1      pip3      python
activate.fish  activate_this.py  pip-3.12  python3

./Desktop/Python/venv/lib:
python3.12

./Desktop/Python/venv/lib/python3.12:
site-packages

./Desktop/Python/venv/lib/python3.12/site-packages:
pip                   pip-23.2.1.virtualenv  _virtualenv.pth
pip-23.2.1.dist-info  __pycache__            _virtualenv.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip:
__init__.py  _internal  __main__.py  __pip-runner__.py  py.typed  _vendor

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal:
build_env.py      exceptions.py  models        self_outdated_check.py
cache.py          index          network       utils
cli               __init__.py    operations    vcs
commands          locations      pyproject.py  wheel_builder.py
configuration.py  main.py        req
distributions     metadata       resolution

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/cli:
autocompletion.py  command_context.py  main.py           req_command.py
base_command.py    __init__.py         parser.py         spinners.py
cmdoptions.py      main_parser.py      progress_bars.py  status_codes.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/commands:
cache.py          debug.py     help.py      install.py  uninstall.py
check.py          download.py  index.py     list.py     wheel.py
completion.py     freeze.py    __init__.py  search.py
configuration.py  hash.py      inspect.py   show.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/distributions:
base.py  __init__.py  installed.py  sdist.py  wheel.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/index:
collector.py  __init__.py  package_finder.py  sources.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/locations:
base.py  _distutils.py  __init__.py  _sysconfig.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/metadata:
base.py  importlib  __init__.py  _json.py  pkg_resources.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/metadata/importlib:
_compat.py  _dists.py  _envs.py  __init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/models:
candidate.py       __init__.py             search_scope.py
direct_url.py      installation_report.py  selection_prefs.py
format_control.py  link.py                 target_python.py
index.py           scheme.py               wheel.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/network:
auth.py   download.py  lazy_wheel.py  utils.py
cache.py  __init__.py  session.py     xmlrpc.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/operations:
build  check.py  freeze.py  __init__.py  install  prepare.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/operations/build:
build_tracker.py  metadata_editable.py  metadata.py        wheel_legacy.py
__init__.py       metadata_legacy.py    wheel_editable.py  wheel.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/operations/install:
editable_legacy.py  __init__.py  wheel.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/req:
constructors.py  req_file.py     req_set.py
__init__.py      req_install.py  req_uninstall.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/resolution:
base.py  __init__.py  legacy  resolvelib

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/resolution/legacy:
__init__.py  resolver.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/resolution/resolvelib:
base.py        found_candidates.py  reporter.py
candidates.py  __init__.py          requirements.py
factory.py     provider.py          resolver.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/utils:
appdirs.py             filetypes.py               packaging.py
compatibility_tags.py  glibc.py                   setuptools_build.py
compat.py              hashes.py                  subprocess.py
datetime.py            __init__.py                temp_dir.py
deprecation.py         inject_securetransport.py  unpacking.py
direct_url_helpers.py  _jaraco_text.py            urls.py
egg_link.py            logging.py                 virtualenv.py
encoding.py            _log.py                    wheel.py
entrypoints.py         misc.py
filesystem.py          models.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_internal/vcs:
bazaar.py  __init__.py   subversion.py
git.py     mercurial.py  versioncontrol.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor:
cachecontrol  __init__.py    pyproject_hooks  typing_extensions.py
certifi       msgpack        requests         urllib3
chardet       packaging      resolvelib       vendor.txt
colorama      pkg_resources  rich             webencodings
distlib       platformdirs   six.py
distro        pygments       tenacity
idna          pyparsing      tomli

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol:
adapter.py  _cmd.py        filewrapper.py  serialize.py
cache.py    compat.py      heuristics.py   wrapper.py
caches      controller.py  __init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/caches:
file_cache.py  __init__.py  redis_cache.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/certifi:
cacert.pem  core.py  __init__.py  __main__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/chardet:
big5freq.py                euctwprober.py         latin1prober.py
big5prober.py              gb2312freq.py          macromanprober.py
chardistribution.py        gb2312prober.py        mbcharsetprober.py
charsetgroupprober.py      hebrewprober.py        mbcsgroupprober.py
charsetprober.py           __init__.py            mbcssm.py
cli                        jisfreq.py             metadata
codingstatemachinedict.py  johabfreq.py           resultdict.py
codingstatemachine.py      johabprober.py         sbcharsetprober.py
cp949prober.py             jpcntx.py              sbcsgroupprober.py
enums.py                   langbulgarianmodel.py  sjisprober.py
escprober.py               langgreekmodel.py      universaldetector.py
escsm.py                   langhebrewmodel.py     utf1632prober.py
eucjpprober.py             langhungarianmodel.py  utf8prober.py
euckrfreq.py               langrussianmodel.py    version.py
euckrprober.py             langthaimodel.py
euctwfreq.py               langturkishmodel.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/chardet/cli:
chardetect.py  __init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/chardet/metadata:
__init__.py  languages.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/colorama:
ansi.py         initialise.py  tests     winterm.py
ansitowin32.py  __init__.py    win32.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/colorama/tests:
ansi_test.py         initialise_test.py  isatty_test.py  winterm_test.py
ansitowin32_test.py  __init__.py         utils.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/distlib:
compat.py    locators.py  resources.py  t64.exe     w64-arm.exe
database.py  manifest.py  scripts.py    util.py     w64.exe
index.py     markers.py   t32.exe       version.py  wheel.py
__init__.py  metadata.py  t64-arm.exe   w32.exe

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/distro:
distro.py  __init__.py  __main__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/idna:
codec.py   core.py      __init__.py   package_data.py
compat.py  idnadata.py  intranges.py  uts46data.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/msgpack:
exceptions.py  ext.py  fallback.py  __init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/packaging:
__about__.py   markers.py       specifiers.py   utils.py
__init__.py    _musllinux.py    _structures.py  version.py
_manylinux.py  requirements.py  tags.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources:
__init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/platformdirs:
android.py  __init__.py  __main__.py  version.py
api.py      macos.py     unix.py      windows.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pygments:
cmdline.py  formatter.py  lexers       regexopt.py   styles
console.py  formatters    __main__.py  scanner.py    token.py
filter.py   __init__.py   modeline.py  sphinxext.py  unistring.py
filters     lexer.py      plugin.py    style.py      util.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pygments/filters:
__init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pygments/formatters:
bbcode.py  img.py       latex.py     pangomarkup.py  terminal256.py
groff.py   __init__.py  _mapping.py  rtf.py          terminal.py
html.py    irc.py       other.py     svg.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pygments/lexers:
__init__.py  _mapping.py  python.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pygments/styles:
__init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pyparsing:
actions.py  core.py  exceptions.py  __init__.py  testing.py  util.py
common.py   diagram  helpers.py     results.py   unicode.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pyparsing/diagram:
__init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks:
_compat.py  _impl.py  __init__.py  _in_process

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process:
__init__.py  _in_process.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/requests:
adapters.py  cookies.py     _internal_utils.py  structures.py
api.py       exceptions.py  models.py           utils.py
auth.py      help.py        packages.py         __version__.py
certs.py     hooks.py       sessions.py
compat.py    __init__.py    status_codes.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/resolvelib:
compat  __init__.py  providers.py  reporters.py  resolvers.py  structs.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/resolvelib/compat:
collections_abc.py  __init__.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/rich:
abc.py             __init__.py      region.py
align.py           _inspect.py      repr.py
ansi.py            json.py          rule.py
bar.py             jupyter.py       scope.py
box.py             layout.py        screen.py
cells.py           live.py          segment.py
_cell_widths.py    live_render.py   spinner.py
color.py           logging.py       _spinners.py
color_triplet.py   _log_render.py   _stack.py
columns.py         _loop.py         status.py
console.py         __main__.py      styled.py
constrain.py       markup.py        style.py
containers.py      measure.py       syntax.py
control.py         _null_file.py    table.py
default_styles.py  padding.py       terminal_theme.py
diagnose.py        pager.py         text.py
_emoji_codes.py    palette.py       theme.py
emoji.py           _palettes.py     themes.py
_emoji_replace.py  panel.py         _timer.py
errors.py          _pick.py         traceback.py
_export_format.py  pretty.py        tree.py
_extension.py      progress_bar.py  _win32_console.py
_fileno.py         progress.py      _windows.py
file_proxy.py      prompt.py        _windows_renderer.py
filesize.py        protocol.py      _wrap.py
highlighter.py     _ratio.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/tenacity:
after.py     before_sleep.py  retry.py       _utils.py
_asyncio.py  __init__.py      stop.py        wait.py
before.py    nap.py           tornadoweb.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/tomli:
__init__.py  _parser.py  _re.py  _types.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3:
_collections.py    contrib        filepost.py  poolmanager.py  util
connectionpool.py  exceptions.py  __init__.py  request.py      _version.py
connection.py      fields.py      packages     response.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib:
_appengine_environ.py  __init__.py  pyopenssl.py      securetransport.py
appengine.py           ntlmpool.py  _securetransport  socks.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/_securetransport:
bindings.py  __init__.py  low_level.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3/packages:
backports  __init__.py  six.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3/packages/backports:
__init__.py  makefile.py  weakref_finalize.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/urllib3/util:
connection.py  request.py             ssl_.py          wait.py
__init__.py    response.py            ssltransport.py
proxy.py       retry.py               timeout.py
queue.py       ssl_match_hostname.py  url.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip/_vendor/webencodings:
__init__.py  labels.py  mklabels.py  tests.py  x_user_defined.py

./Desktop/Python/venv/lib/python3.12/site-packages/pip-23.2.1.dist-info:
AUTHORS.txt       INSTALLER    METADATA  top_level.txt
entry_points.txt  LICENSE.txt  RECORD    WHEEL

./Desktop/Python/venv/lib/python3.12/site-packages/__pycache__:
_virtualenv.cpython-312.pyc

./Documents:
'about ci_cd.pdf'
'About DevSecOps.pdf'
'About software engineer & SDLC.pdf'
'certificate--python(kaggle).png'
'computer net#1.pdf'
'computer net#2.pdf'
'computer net#3.pdf'
 CyberSecurity.pdf
 DevOpsTutorial.pdf
'DwvOps & culture.pdf'
'Ethical Hacking & Cyber Security.pdf'
 git-cheat-sheet-education.pdf
'grep aommands.pdf'
 Linux-Commands_Cheat-Sheet.png
 linux-commands-handbook.pdf
 presentation.odt

./Downloads:
programs

./Downloads/programs:
Cupertino-Sonoma.tar.xz                Python-3.12.0.tgz
kali-linux-2024.2-installer-amd64.iso

./Music:

./Pictures:
'devos map.webp'   Screenshots   Webcam

./Pictures/Screenshots:
'file mngmnt rwx codes.png'
'Linux fun commands.png'
'Screenshot from 2024-08-28 11-26-27.png'
'Screenshot from 2024-08-31 10-28-58.png'
'Screenshot from 2024-09-02 12-28-41.png'
'Screenshot from 2024-09-03 12-54-01.png'
'Screenshot from 2024-09-07 14-28-49.png'

./Pictures/Webcam:

./Public:

./Python-3.12.0:
aclocal.m4         Grammar          Misc               pyconfig.h
_bootstrap_python  Include          Modules            pyconfig.h.in
build              install-sh       Objects            python
config.guess       Lib              Parser             Python
config.log         libpython3.12.a  PC                 python-config
config.status      LICENSE          PCbuild            python-config.py
config.sub         Mac              platform           python-gdb.py
configure          Makefile         profile-run-stamp  README.rst
configure.ac       Makefile.pre     Programs           Tools
Doc                Makefile.pre.in  pybuilddir.txt

./Python-3.12.0/build:
lib.linux-x86_64-3.12  scripts-3.12

./Python-3.12.0/build/lib.linux-x86_64-3.12:
array.cpython-312-x86_64-linux-gnu.so
_asyncio.cpython-312-x86_64-linux-gnu.so
audioop.cpython-312-x86_64-linux-gnu.so
binascii.cpython-312-x86_64-linux-gnu.so
_bisect.cpython-312-x86_64-linux-gnu.so
_blake2.cpython-312-x86_64-linux-gnu.so
_bz2.cpython-312-x86_64-linux-gnu.so
cmath.cpython-312-x86_64-linux-gnu.so
_codecs_cn.cpython-312-x86_64-linux-gnu.so
_codecs_hk.cpython-312-x86_64-linux-gnu.so
_codecs_iso2022.cpython-312-x86_64-linux-gnu.so
_codecs_jp.cpython-312-x86_64-linux-gnu.so
_codecs_kr.cpython-312-x86_64-linux-gnu.so
_codecs_tw.cpython-312-x86_64-linux-gnu.so
_contextvars.cpython-312-x86_64-linux-gnu.so
_crypt.cpython-312-x86_64-linux-gnu.so
_csv.cpython-312-x86_64-linux-gnu.so
_ctypes.cpython-312-x86_64-linux-gnu.so
_ctypes_test.cpython-312-x86_64-linux-gnu.so
_curses.cpython-312-x86_64-linux-gnu.so
_curses_panel.cpython-312-x86_64-linux-gnu.so
_datetime.cpython-312-x86_64-linux-gnu.so
_decimal.cpython-312-x86_64-linux-gnu.so
_elementtree.cpython-312-x86_64-linux-gnu.so
fcntl.cpython-312-x86_64-linux-gnu.so
_gdbm.cpython-312-x86_64-linux-gnu.so
grp.cpython-312-x86_64-linux-gnu.so
_hashlib.cpython-312-x86_64-linux-gnu.so
_heapq.cpython-312-x86_64-linux-gnu.so
_json.cpython-312-x86_64-linux-gnu.so
_lsprof.cpython-312-x86_64-linux-gnu.so
math.cpython-312-x86_64-linux-gnu.so
_md5.cpython-312-x86_64-linux-gnu.so
mmap.cpython-312-x86_64-linux-gnu.so
_multibytecodec.cpython-312-x86_64-linux-gnu.so
_multiprocessing.cpython-312-x86_64-linux-gnu.so
nis.cpython-312-x86_64-linux-gnu.so
_opcode.cpython-312-x86_64-linux-gnu.so
ossaudiodev.cpython-312-x86_64-linux-gnu.so
_pickle.cpython-312-x86_64-linux-gnu.so
_posixshmem.cpython-312-x86_64-linux-gnu.so
_posixsubprocess.cpython-312-x86_64-linux-gnu.so
__pycache__
pyexpat.cpython-312-x86_64-linux-gnu.so
_queue.cpython-312-x86_64-linux-gnu.so
_random.cpython-312-x86_64-linux-gnu.so
readline.cpython-312-x86_64-linux-gnu.so
resource.cpython-312-x86_64-linux-gnu.so
select.cpython-312-x86_64-linux-gnu.so
_sha1.cpython-312-x86_64-linux-gnu.so
_sha2.cpython-312-x86_64-linux-gnu.so
_sha3.cpython-312-x86_64-linux-gnu.so
_socket.cpython-312-x86_64-linux-gnu.so
spwd.cpython-312-x86_64-linux-gnu.so
_sqlite3.cpython-312-x86_64-linux-gnu.so
_ssl.cpython-312-x86_64-linux-gnu.so
_statistics.cpython-312-x86_64-linux-gnu.so
_struct.cpython-312-x86_64-linux-gnu.so
_sysconfigdata__linux_x86_64-linux-gnu.py
syslog.cpython-312-x86_64-linux-gnu.so
termios.cpython-312-x86_64-linux-gnu.so
_testbuffer.cpython-312-x86_64-linux-gnu.so
_testcapi.cpython-312-x86_64-linux-gnu.so
_testclinic.cpython-312-x86_64-linux-gnu.so
_testimportmultiple.cpython-312-x86_64-linux-gnu.so
_testinternalcapi.cpython-312-x86_64-linux-gnu.so
_testmultiphase.cpython-312-x86_64-linux-gnu.so
_testsinglephase.cpython-312-x86_64-linux-gnu.so
unicodedata.cpython-312-x86_64-linux-gnu.so
_xxinterpchannels.cpython-312-x86_64-linux-gnu.so
xxlimited_35.cpython-312-x86_64-linux-gnu.so
xxlimited.cpython-312-x86_64-linux-gnu.so
_xxsubinterpreters.cpython-312-x86_64-linux-gnu.so
xxsubtype.cpython-312-x86_64-linux-gnu.so
_xxtestfuzz.cpython-312-x86_64-linux-gnu.so
zlib.cpython-312-x86_64-linux-gnu.so
_zoneinfo.cpython-312-x86_64-linux-gnu.so

./Python-3.12.0/build/lib.linux-x86_64-3.12/__pycache__:
_sysconfigdata__linux_x86_64-linux-gnu.cpython-312.pyc

./Python-3.12.0/build/scripts-3.12:
2to3-3.12  idle3.12  pydoc3.12

./Python-3.12.0/Doc:
about.rst        data          installing   requirements-oldest-sphinx.txt
bugs.rst         distributing  library      requirements.txt
c-api            extending     license.rst  _static
conf.py          faq           make.bat     tools
constraints.txt  glossary.rst  Makefile     tutorial
contents.rst     howto         README.rst   using
copyright.rst    includes      reference    whatsnew

./Python-3.12.0/Doc/c-api:
abstract.rst       coro.rst         iter.rst         sequence.rst
allocation.rst     datetime.rst     list.rst         set.rst
apiabiversion.rst  descriptor.rst   long.rst         slice.rst
arg.rst            dict.rst         mapping.rst      stable.rst
bool.rst           exceptions.rst   marshal.rst      structures.rst
buffer.rst         file.rst         memory.rst       sys.rst
bytearray.rst      float.rst        memoryview.rst   tuple.rst
bytes.rst          frame.rst        method.rst       typehints.rst
call.rst           function.rst     module.rst       typeobj.rst
capsule.rst        gcsupport.rst    none.rst         type.rst
cell.rst           gen.rst          number.rst       unicode.rst
codec.rst          import.rst       objbuffer.rst    utilities.rst
code.rst           index.rst        object.rst       veryhigh.rst
complex.rst        init_config.rst  objimpl.rst      weakref.rst
concrete.rst       init.rst         perfmaps.rst
contextvars.rst    intro.rst        refcounting.rst
conversion.rst     iterator.rst     reflection.rst

./Python-3.12.0/Doc/data:
python3.12.abi  refcounts.dat  stable_abi.dat

./Python-3.12.0/Doc/distributing:
index.rst

./Python-3.12.0/Doc/extending:
building.rst   extending.rst  newtypes.rst           windows.rst
embedding.rst  index.rst      newtypes_tutorial.rst

./Python-3.12.0/Doc/faq:
design.rst     gui.rst        library.rst            windows.rst
extending.rst  index.rst      programming.rst
general.rst    installed.rst  python-video-icon.png

./Python-3.12.0/Doc/howto:
annotations.rst  index.rst                 pyporting.rst
argparse.rst     instrumentation.rst       regex.rst
clinic.rst       ipaddress.rst             sockets.rst
cporting.rst     isolating-extensions.rst  sorting.rst
curses.rst       logging-cookbook.rst      unicode.rst
descriptor.rst   logging_flow.png          urllib2.rst
enum.rst         logging.rst
functional.rst   perf_profiling.rst

./Python-3.12.0/Doc/includes:
dbpickle.py                email-simple.py     newtypes
diff.py                    email-unpack.py     run-func.c
email-alternative.py       minidom-example.py  typestruct.h
email-dir.py               mp_newtype.py       tzinfo_examples.py
email-headers.py           mp_pool.py          wasm-notavail.rst
email-mime.py              mp_workers.py
email-read-alternative.py  ndiff.py

./Python-3.12.0/Doc/includes/newtypes:
custom2.c  custom4.c  pyproject.toml  sublist.c
custom3.c  custom.c   setup.py        test.py

./Python-3.12.0/Doc/installing:
index.rst

./Python-3.12.0/Doc/library:
2to3.rst                     marshal.rst
abc.rst                      math.rst
aifc.rst                     mimetypes.rst
allos.rst                    mmap.rst
archiving.rst                mm.rst
argparse.rst                 modulefinder.rst
array.rst                    modules.rst
ast.rst                      msilib.rst
asyncio-api-index.rst        msvcrt.rst
asyncio-dev.rst              multiprocessing.rst
asyncio-eventloop.rst        multiprocessing.shared_memory.rst
asyncio-exceptions.rst       netdata.rst
asyncio-extending.rst        netrc.rst
asyncio-future.rst           nis.rst
asyncio-llapi-index.rst      nntplib.rst
asyncio-platforms.rst        numbers.rst
asyncio-policy.rst           numeric.rst
asyncio-protocol.rst         operator.rst
asyncio-queue.rst            optparse.rst
asyncio.rst                  os.path.rst
asyncio-runner.rst           os.rst
asyncio-stream.rst           ossaudiodev.rst
asyncio-subprocess.rst       pathlib-inheritance.png
asyncio-sync.rst             pathlib-inheritance.svg
asyncio-task.rst             pathlib.rst
atexit.rst                   pdb.rst
audioop.rst                  persistence.rst
audit_events.rst             pickle.rst
base64.rst                   pickletools.rst
bdb.rst                      pipes.rst
binary.rst                   pkgutil.rst
binascii.rst                 platform.rst
bisect.rst                   plistlib.rst
builtins.rst                 poplib.rst
bz2.rst                      posix.rst
calendar.rst                 pprint.rst
cgi.rst                      profile.rst
cgitb.rst                    pty.rst
chunk.rst                    pwd.rst
cmath.rst                    pyclbr.rst
cmd.rst                      py_compile.rst
codecs.rst                   pydoc.rst
codeop.rst                   pyexpat.rst
code.rst                     python.rst
collections.abc.rst          queue.rst
collections.rst              quopri.rst
colorsys.rst                 random.rst
compileall.rst               readline.rst
concurrency.rst              reprlib.rst
concurrent.futures.rst       re.rst
concurrent.rst               resource.rst
configparser.rst             rlcompleter.rst
constants.rst                runpy.rst
contextlib.rst               sched.rst
contextvars.rst              secrets.rst
copyreg.rst                  security_warnings.rst
copy.rst                     selectors.rst
crypto.rst                   select.rst
crypt.rst                    shelve.rst
csv.rst                      shlex.rst
ctypes.rst                   shutil.rst
curses.ascii.rst             signal.rst
curses.panel.rst             site.rst
curses.rst                   smtplib.rst
custominterp.rst             sndhdr.rst
dataclasses.rst              socket.rst
datatypes.rst                socketserver.rst
datetime.rst                 spwd.rst
dbm.rst                      sqlite3.rst
debug.rst                    ssl.rst
decimal.rst                  statistics.rst
development.rst              stat.rst
devmode.rst                  stdtypes.rst
dialog.rst                   stringprep.rst
difflib.rst                  string.rst
dis.rst                      struct.rst
distribution.rst             subprocess.rst
doctest.rst                  sunau.rst
email.charset.rst            superseded.rst
email.compat32-message.rst   symtable.rst
email.contentmanager.rst     sysconfig.rst
email.encoders.rst           syslog.rst
email.errors.rst             sys.monitoring.rst
email.examples.rst           sys_path_init.rst
email.generator.rst          sys.rst
email.headerregistry.rst     tabnanny.rst
email.header.rst             tarfile.rst
email.iterators.rst          telnetlib.rst
email.message.rst            tempfile.rst
email.mime.rst               termios.rst
email.parser.rst             test.rst
email.policy.rst             text.rst
email.rst                    textwrap.rst
email.utils.rst              threading.rst
ensurepip.rst                _thread.rst
enum.rst                     timeit.rst
errno.rst                    time.rst
exceptions.rst               tkinter.colorchooser.rst
faulthandler.rst             tkinter.dnd.rst
fcntl.rst                    tkinter.font.rst
filecmp.rst                  tkinter.messagebox.rst
fileformats.rst              tkinter.rst
fileinput.rst                tkinter.scrolledtext.rst
filesys.rst                  tkinter.tix.rst
fnmatch.rst                  tkinter.ttk.rst
fractions.rst                tk_msg.png
frameworks.rst               tk.rst
ftplib.rst                   tokenize.rst
functional.rst               token-list.inc
functions.rst                token.rst
functools.rst                tomllib.rst
__future__.rst               traceback.rst
gc.rst                       tracemalloc.rst
getopt.rst                   trace.rst
getpass.rst                  tty.rst
gettext.rst                  tulip_coro.dia
glob.rst                     tulip_coro.png
graphlib.rst                 turtle.rst
grp.rst                      turtle-star.pdf
gzip.rst                     turtle-star.png
hashlib-blake2-tree.png      turtle-star.ps
hashlib.rst                  types.rst
heapq.rst                    typing.rst
hmac.rst                     unicodedata.rst
html.entities.rst            unittest.mock-examples.rst
html.parser.rst              unittest.mock.rst
html.rst                     unittest.rst
http.client.rst              unix.rst
http.cookiejar.rst           urllib.error.rst
http.cookies.rst             urllib.parse.rst
http.rst                     urllib.request.rst
http.server.rst              urllib.robotparser.rst
i18n.rst                     urllib.rst
idle.rst                     uuid.rst
imaplib.rst                  uu.rst
imghdr.rst                   venv.rst
importlib.metadata.rst       warnings.rst
importlib.resources.abc.rst  wave.rst
importlib.resources.rst      weakref.rst
importlib.rst                webbrowser.rst
index.rst                    windows.rst
inspect.rst                  winreg.rst
internet.rst                 winsound.rst
intro.rst                    wsgiref.rst
io.rst                       xdrlib.rst
ipaddress.rst                xml.dom.minidom.rst
ipc.rst                      xml.dom.pulldom.rst
itertools.rst                xml.dom.rst
json.rst                     xml.etree.elementtree.rst
kde_example.png              xmlrpc.client.rst
keyword.rst                  xmlrpc.rst
language.rst                 xmlrpc.server.rst
linecache.rst                xml.rst
locale.rst                   xml.sax.handler.rst
logging.config.rst           xml.sax.reader.rst
logging.handlers.rst         xml.sax.rst
logging.rst                  xml.sax.utils.rst
lzma.rst                     zipapp.rst
mailbox.rst                  zipfile.rst
mailcap.rst                  zipimport.rst
__main__.rst                 zlib.rst
markup.rst                   zoneinfo.rst

./Python-3.12.0/Doc/reference:
compound_stmts.rst  grammar.rst       lexical_analysis.rst
datamodel.rst       import.rst        simple_stmts.rst
executionmodel.rst  index.rst         toplevel_components.rst
expressions.rst     introduction.rst

./Python-3.12.0/Doc/_static:
og-image.png

./Python-3.12.0/Doc/tools:
check-warnings.py  extensions  static  templates

./Python-3.12.0/Doc/tools/extensions:
asdl_highlight.py  escape4chm.py       patchlevel.py     pyspecific.py
c_annotations.py   glossary_search.py  peg_highlight.py

./Python-3.12.0/Doc/tools/static:
changelog_search.js

./Python-3.12.0/Doc/tools/templates:
customsourcelink.html  indexcontent.html  opensearch.xml
download.html          indexsidebar.html  search.html
dummy.html             layout.html

./Python-3.12.0/Doc/tutorial:
appendix.rst        errors.rst         interpreter.rst   venv.rst
appetite.rst        floatingpoint.rst  introduction.rst  whatnow.rst
classes.rst         index.rst          modules.rst
controlflow.rst     inputoutput.rst    stdlib2.rst
datastructures.rst  interactive.rst    stdlib.rst

./Python-3.12.0/Doc/using:
cmdline.rst    editors.rst  mac.rst   venv-create.inc  win_installer.png
configure.rst  index.rst    unix.rst  windows.rst

./Python-3.12.0/Doc/whatsnew:
2.0.rst  2.4.rst  3.0.rst   3.1.rst  3.5.rst  3.9.rst
2.1.rst  2.5.rst  3.10.rst  3.2.rst  3.6.rst  changelog.rst
2.2.rst  2.6.rst  3.11.rst  3.3.rst  3.7.rst  index.rst
2.3.rst  2.7.rst  3.12.rst  3.4.rst  3.8.rst

./Python-3.12.0/Grammar:
python.gram  Tokens

./Python-3.12.0/Include:
abstract.h             iterobject.h    pymath.h
bltinmodule.h          listobject.h    pymem.h
boolobject.h           longobject.h    pyport.h
bytearrayobject.h      marshal.h       pystate.h
bytesobject.h          memoryobject.h  pystats.h
ceval.h                methodobject.h  pystrcmp.h
codecs.h               modsupport.h    pystrtod.h
compile.h              moduleobject.h  Python.h
complexobject.h        object.h        pythonrun.h
cpython                objimpl.h       pythread.h
datetime.h             opcode.h        pytypedefs.h
descrobject.h          osdefs.h        rangeobject.h
dictobject.h           osmodule.h      README.rst
dynamic_annotations.h  patchlevel.h    setobject.h
enumobject.h           pybuffer.h      sliceobject.h
errcode.h              pycapsule.h     structmember.h
exports.h              py_curses.h     structseq.h
fileobject.h           pydtrace.d      sysmodule.h
fileutils.h            pydtrace.h      traceback.h
floatobject.h          pyerrors.h      tracemalloc.h
frameobject.h          pyexpat.h       tupleobject.h
genericaliasobject.h   pyframe.h       typeslots.h
import.h               pyhash.h        unicodeobject.h
internal               pylifecycle.h   warnings.h
interpreteridobject.h  pymacconfig.h   weakrefobject.h
intrcheck.h            pymacro.h

./Python-3.12.0/Include/cpython:
abstract.h         genobject.h            pyerrors.h
bytearrayobject.h  import.h               pyfpe.h
bytesobject.h      initconfig.h           pyframe.h
cellobject.h       interpreteridobject.h  pylifecycle.h
ceval.h            listobject.h           pymem.h
classobject.h      longintrepr.h          pystate.h
code.h             longobject.h           pythonrun.h
compile.h          memoryobject.h         pythread.h
complexobject.h    methodobject.h         pytime.h
context.h          modsupport.h           setobject.h
descrobject.h      object.h               sysmodule.h
dictobject.h       objimpl.h              traceback.h
fileobject.h       odictobject.h          tupleobject.h
fileutils.h        picklebufobject.h      unicodeobject.h
floatobject.h      pthread_stubs.h        warnings.h
frameobject.h      pyctype.h              weakrefobject.h
funcobject.h       pydebug.h

./Python-3.12.0/Include/internal:
pycore_abstract.h                       pycore_intrinsics.h
pycore_asdl.h                           pycore_list.h
pycore_ast.h                            pycore_long.h
pycore_ast_state.h                      pycore_memoryobject.h
pycore_atexit.h                         pycore_moduleobject.h
pycore_atomic_funcs.h                   pycore_namespace.h
pycore_atomic.h                         pycore_object.h
pycore_bitutils.h                       pycore_object_state.h
pycore_blocks_output_buffer.h           pycore_obmalloc.h
pycore_bytes_methods.h                  pycore_obmalloc_init.h
pycore_bytesobject.h                    pycore_opcode.h
pycore_call.h                           pycore_opcode_utils.h
pycore_ceval.h                          pycore_parser.h
pycore_ceval_state.h                    pycore_pathconfig.h
pycore_code.h                           pycore_pyarena.h
pycore_compile.h                        pycore_pyerrors.h
pycore_condvar.h                        pycore_pyhash.h
pycore_context.h                        pycore_pylifecycle.h
pycore_descrobject.h                    pycore_pymath.h
pycore_dict.h                           pycore_pymem.h
pycore_dict_state.h                     pycore_pymem_init.h
pycore_dtoa.h                           pycore_pystate.h
pycore_emscripten_signal.h              pycore_pythread.h
pycore_exceptions.h                     pycore_range.h
pycore_faulthandler.h                   pycore_runtime.h
pycore_fileutils.h                      pycore_runtime_init_generated.h
pycore_fileutils_windows.h              pycore_runtime_init.h
pycore_floatobject.h                    pycore_signal.h
pycore_flowgraph.h                      pycore_sliceobject.h
pycore_format.h                         pycore_strhex.h
pycore_frame.h                          pycore_structseq.h
pycore_function.h                       pycore_symtable.h
pycore_gc.h                             pycore_sysmodule.h
pycore_genobject.h                      pycore_time.h
pycore_getopt.h                         pycore_token.h
pycore_gil.h                            pycore_traceback.h
pycore_global_objects_fini_generated.h  pycore_tracemalloc.h
pycore_global_objects.h                 pycore_tuple.h
pycore_global_strings.h                 pycore_typeobject.h
pycore_hamt.h                           pycore_typevarobject.h
pycore_hashtable.h                      pycore_ucnhash.h
pycore_import.h                         pycore_unicodeobject_generated.h
pycore_initconfig.h                     pycore_unicodeobject.h
pycore_instruments.h                    pycore_unionobject.h
pycore_interp.h                         pycore_warnings.h

./Python-3.12.0/Lib:
abc.py               idlelib          shlex.py
aifc.py              imaplib.py       shutil.py
_aix_support.py      imghdr.py        signal.py
antigravity.py       importlib        _sitebuiltins.py
argparse.py          inspect.py       site-packages
ast.py               io.py            site.py
asyncio              ipaddress.py     smtplib.py
base64.py            json             sndhdr.py
bdb.py               keyword.py       socket.py
bisect.py            lib2to3          socketserver.py
bz2.py               linecache.py     sqlite3
calendar.py          locale.py        sre_compile.py
cgi.py               logging          sre_constants.py
cgitb.py             lzma.py          sre_parse.py
chunk.py             mailbox.py       ssl.py
cmd.py               mailcap.py       statistics.py
codecs.py            _markupbase.py   stat.py
codeop.py            mimetypes.py     stringprep.py
code.py              modulefinder.py  string.py
collections          msilib           _strptime.py
_collections_abc.py  multiprocessing  struct.py
colorsys.py          netrc.py         subprocess.py
_compat_pickle.py    nntplib.py       sunau.py
compileall.py        ntpath.py        symtable.py
_compression.py      nturl2path.py    sysconfig.py
concurrent           numbers.py       tabnanny.py
configparser.py      opcode.py        tarfile.py
contextlib.py        operator.py      telnetlib.py
contextvars.py       optparse.py      tempfile.py
copy.py              os.py            test
copyreg.py           _osx_support.py  textwrap.py
cProfile.py          pathlib.py       this.py
crypt.py             pdb.py           _threading_local.py
csv.py               __phello__       threading.py
ctypes               pickle.py        timeit.py
curses               pickletools.py   tkinter
dataclasses.py       pipes.py         tokenize.py
datetime.py          pkgutil.py       token.py
dbm                  platform.py      tomllib
decimal.py           plistlib.py      traceback.py
difflib.py           poplib.py        tracemalloc.py
dis.py               posixpath.py     trace.py
doctest.py           pprint.py        tty.py
email                profile.py       turtledemo
encodings            pstats.py        turtle.py
ensurepip            pty.py           types.py
enum.py              _py_abc.py       typing.py
filecmp.py           __pycache__      unittest
fileinput.py         pyclbr.py        urllib
fnmatch.py           py_compile.py    uuid.py
fractions.py         _pydatetime.py   uu.py
ftplib.py            _pydecimal.py    venv
functools.py         pydoc_data       warnings.py
__future__.py        pydoc.py         wave.py
genericpath.py       _pyio.py         weakref.py
getopt.py            _pylong.py       _weakrefset.py
getpass.py           queue.py         webbrowser.py
gettext.py           quopri.py        wsgiref
glob.py              random.py        xdrlib.py
graphlib.py          re               xml
gzip.py              reprlib.py       xmlrpc
hashlib.py           rlcompleter.py   zipapp.py
heapq.py             runpy.py         zipfile
__hello__.py         sched.py         zipimport.py
hmac.py              secrets.py       zoneinfo
html                 selectors.py
http                 shelve.py

./Python-3.12.0/Lib/asyncio:
base_events.py      log.py              subprocess.py
base_futures.py     __main__.py         taskgroups.py
base_subprocess.py  mixins.py           tasks.py
base_tasks.py       proactor_events.py  threads.py
constants.py        protocols.py        timeouts.py
coroutines.py       __pycache__         transports.py
events.py           queues.py           trsock.py
exceptions.py       runners.py          unix_events.py
format_helpers.py   selector_events.py  windows_events.py
futures.py          sslproto.py         windows_utils.py
__init__.py         staggered.py
locks.py            streams.py

./Python-3.12.0/Lib/asyncio/__pycache__:
base_events.cpython-312.pyc      queues.cpython-312.pyc
base_futures.cpython-312.pyc     runners.cpython-312.pyc
base_subprocess.cpython-312.pyc  selector_events.cpython-312.pyc
base_tasks.cpython-312.pyc       sslproto.cpython-312.pyc
constants.cpython-312.pyc        staggered.cpython-312.pyc
coroutines.cpython-312.pyc       streams.cpython-312.pyc
events.cpython-312.pyc           subprocess.cpython-312.pyc
exceptions.cpython-312.pyc       taskgroups.cpython-312.pyc
format_helpers.cpython-312.pyc   tasks.cpython-312.pyc
futures.cpython-312.pyc          threads.cpython-312.pyc
__init__.cpython-312.pyc         timeouts.cpython-312.pyc
locks.cpython-312.pyc            transports.cpython-312.pyc
log.cpython-312.pyc              trsock.cpython-312.pyc
mixins.cpython-312.pyc           unix_events.cpython-312.pyc
protocols.cpython-312.pyc

./Python-3.12.0/Lib/collections:
abc.py  __init__.py  __pycache__

./Python-3.12.0/Lib/collections/__pycache__:
abc.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/concurrent:
futures  __init__.py  __pycache__

./Python-3.12.0/Lib/concurrent/futures:
_base.py  __init__.py  process.py  __pycache__  thread.py

./Python-3.12.0/Lib/concurrent/futures/__pycache__:
_base.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/concurrent/__pycache__:
__init__.cpython-312.pyc

./Python-3.12.0/Lib/ctypes:
_aix.py  _endian.py  __init__.py  macholib  util.py  wintypes.py

./Python-3.12.0/Lib/ctypes/macholib:
dyld.py   fetch_macholib      framework.py  README.ctypes
dylib.py  fetch_macholib.bat  __init__.py

./Python-3.12.0/Lib/curses:
ascii.py  has_key.py  __init__.py  panel.py  textpad.py

./Python-3.12.0/Lib/dbm:
dumb.py  gnu.py  __init__.py  ndbm.py

./Python-3.12.0/Lib/email:
architecture.rst   errors.py                __init__.py    _policybase.py
base64mime.py      feedparser.py            iterators.py   policy.py
charset.py         generator.py             message.py     __pycache__
contentmanager.py  header.py                mime           quoprimime.py
_encoded_words.py  headerregistry.py        _parseaddr.py  utils.py
encoders.py        _header_value_parser.py  parser.py

./Python-3.12.0/Lib/email/mime:
application.py  base.py   __init__.py  multipart.py     text.py
audio.py        image.py  message.py   nonmultipart.py

./Python-3.12.0/Lib/email/__pycache__:
base64mime.cpython-312.pyc      iterators.cpython-312.pyc
charset.cpython-312.pyc         message.cpython-312.pyc
_encoded_words.cpython-312.pyc  _parseaddr.cpython-312.pyc
encoders.cpython-312.pyc        parser.cpython-312.pyc
errors.cpython-312.pyc          _policybase.cpython-312.pyc
feedparser.cpython-312.pyc      quoprimime.cpython-312.pyc
header.cpython-312.pyc          utils.cpython-312.pyc
__init__.cpython-312.pyc

./Python-3.12.0/Lib/encodings:
aliases.py       cp869.py            koi8_r.py
ascii.py         cp874.py            koi8_t.py
base64_codec.py  cp875.py            koi8_u.py
big5hkscs.py     cp932.py            kz1048.py
big5.py          cp949.py            latin_1.py
bz2_codec.py     cp950.py            mac_arabic.py
charmap.py       euc_jis_2004.py     mac_croatian.py
cp037.py         euc_jisx0213.py     mac_cyrillic.py
cp1006.py        euc_jp.py           mac_farsi.py
cp1026.py        euc_kr.py           mac_greek.py
cp1125.py        gb18030.py          mac_iceland.py
cp1140.py        gb2312.py           mac_latin2.py
cp1250.py        gbk.py              mac_romanian.py
cp1251.py        hex_codec.py        mac_roman.py
cp1252.py        hp_roman8.py        mac_turkish.py
cp1253.py        hz.py               mbcs.py
cp1254.py        idna.py             oem.py
cp1255.py        __init__.py         palmos.py
cp1256.py        iso2022_jp_1.py     ptcp154.py
cp1257.py        iso2022_jp_2004.py  punycode.py
cp1258.py        iso2022_jp_2.py     __pycache__
cp273.py         iso2022_jp_3.py     quopri_codec.py
cp424.py         iso2022_jp_ext.py   raw_unicode_escape.py
cp437.py         iso2022_jp.py       rot_13.py
cp500.py         iso2022_kr.py       shift_jis_2004.py
cp720.py         iso8859_10.py       shift_jis.py
cp737.py         iso8859_11.py       shift_jisx0213.py
cp775.py         iso8859_13.py       tis_620.py
cp850.py         iso8859_14.py       undefined.py
cp852.py         iso8859_15.py       unicode_escape.py
cp855.py         iso8859_16.py       utf_16_be.py
cp856.py         iso8859_1.py        utf_16_le.py
cp857.py         iso8859_2.py        utf_16.py
cp858.py         iso8859_3.py        utf_32_be.py
cp860.py         iso8859_4.py        utf_32_le.py
cp861.py         iso8859_5.py        utf_32.py
cp862.py         iso8859_6.py        utf_7.py
cp863.py         iso8859_7.py        utf_8.py
cp864.py         iso8859_8.py        utf_8_sig.py
cp865.py         iso8859_9.py        uu_codec.py
cp866.py         johab.py            zlib_codec.py

./Python-3.12.0/Lib/encodings/__pycache__:
aliases.cpython-312.pyc  cp437.cpython-312.pyc     koi8_r.cpython-312.pyc
ascii.cpython-312.pyc    idna.cpython-312.pyc      utf_8.cpython-312.pyc
cp1252.cpython-312.pyc   __init__.cpython-312.pyc

./Python-3.12.0/Lib/ensurepip:
_bundled  __init__.py  __main__.py  __pycache__  _uninstall.py

./Python-3.12.0/Lib/ensurepip/_bundled:
pip-23.2.1-py3-none-any.whl

./Python-3.12.0/Lib/ensurepip/__pycache__:
__init__.cpython-312.pyc  __main__.cpython-312.pyc

./Python-3.12.0/Lib/html:
entities.py  __init__.py  parser.py  __pycache__

./Python-3.12.0/Lib/html/__pycache__:
entities.cpython-312.pyc  __init__.cpython-312.pyc  parser.cpython-312.pyc

./Python-3.12.0/Lib/http:
client.py  cookiejar.py  cookies.py  __init__.py  __pycache__  server.py

./Python-3.12.0/Lib/http/__pycache__:
client.cpython-312.pyc     cookies.cpython-312.pyc
cookiejar.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/idlelib:
autocomplete.py        debugobj_r.py   iomenu.py       scrolledlist.py
autocomplete_w.py      delegator.py    macosx.py       searchbase.py
autoexpand.py          dynoption.py    mainmenu.py     searchengine.py
browser.py             editor.py       __main__.py     search.py
calltip.py             extend.txt      multicall.py    sidebar.py
calltip_w.py           filelist.py     NEWS2x.txt      squeezer.py
ChangeLog              format.py       NEWS.txt        stackviewer.py
codecontext.py         grep.py         outwin.py       statusbar.py
colorizer.py           help_about.py   parenmatch.py   textview.py
configdialog.py        help.html       pathbrowser.py  TODO.txt
config-extensions.def  help.py         percolator.py   tooltip.py
config-highlight.def   history.py      pyparse.py      tree.py
config_key.py          HISTORY.txt     pyshell.py      undo.py
config-keys.def        hyperparser.py  query.py        util.py
config-main.def        Icons           README.txt      window.py
config.py              idle.bat        redirector.py   zoomheight.py
CREDITS.txt            idle.py         replace.py      zzdummy.py
debugger.py            idle.pyw        rpc.py
debugger_r.py          idle_test       run.py
debugobj.py            __init__.py     runscript.py

./Python-3.12.0/Lib/idlelib/Icons:
folder.gif   idle_256.png  idle_48.gif  minusnode.gif   python.gif
idle_16.gif  idle_32.gif   idle_48.png  openfolder.gif  README.txt
idle_16.png  idle_32.png   idle.ico     plusnode.gif    tk.gif

./Python-3.12.0/Lib/idlelib/idle_test:
example_noext           test_delegator.py    test_rpc.py
example_stub.pyi        test_editmenu.py     test_run.py
htest.py                test_editor.py       test_runscript.py
__init__.py             test_filelist.py     test_scrolledlist.py
mock_idle.py            test_format.py       test_searchbase.py
mock_tk.py              test_grep.py         test_searchengine.py
README.txt              test_help_about.py   test_search.py
template.py             test_help.py         test_sidebar.py
test_autocomplete.py    test_history.py      test_squeezer.py
test_autocomplete_w.py  test_hyperparser.py  test_stackviewer.py
test_autoexpand.py      test_iomenu.py       test_statusbar.py
test_browser.py         test_macosx.py       test_text.py
test_calltip.py         test_mainmenu.py     test_textview.py
test_calltip_w.py       test_multicall.py    test_tooltip.py
test_codecontext.py     test_outwin.py       test_tree.py
test_colorizer.py       test_parenmatch.py   test_undo.py
test_configdialog.py    test_pathbrowser.py  test_util.py
test_config_key.py      test_percolator.py   test_warning.py
test_config.py          test_pyparse.py      test_window.py
test_debugger.py        test_pyshell.py      test_zoomheight.py
test_debugger_r.py      test_query.py        test_zzdummy.py
test_debugobj.py        test_redirector.py   tkinter_testing_utils.py
test_debugobj_r.py      test_replace.py

./Python-3.12.0/Lib/importlib:
_abc.py                 _bootstrap.py  metadata     resources
abc.py                  __init__.py    __pycache__  simple.py
_bootstrap_external.py  machinery.py   readers.py   util.py

./Python-3.12.0/Lib/importlib/metadata:
_adapters.py     _functools.py  _itertools.py  __pycache__
_collections.py  __init__.py    _meta.py       _text.py

./Python-3.12.0/Lib/importlib/metadata/__pycache__:
_adapters.cpython-312.pyc     _itertools.cpython-312.pyc
_collections.cpython-312.pyc  _meta.cpython-312.pyc
_functools.cpython-312.pyc    _text.cpython-312.pyc
__init__.cpython-312.pyc

./Python-3.12.0/Lib/importlib/__pycache__:
_abc.cpython-312.pyc  __init__.cpython-312.pyc
abc.cpython-312.pyc   readers.cpython-312.pyc

./Python-3.12.0/Lib/importlib/resources:
abc.py        _common.py   _itertools.py  __pycache__  simple.py
_adapters.py  __init__.py  _legacy.py     readers.py

./Python-3.12.0/Lib/importlib/resources/__pycache__:
abc.cpython-312.pyc        _itertools.cpython-312.pyc
_adapters.cpython-312.pyc  _legacy.cpython-312.pyc
_common.cpython-312.pyc    readers.cpython-312.pyc
__init__.cpython-312.pyc

./Python-3.12.0/Lib/json:
decoder.py  encoder.py  __init__.py  __pycache__  scanner.py  tool.py

./Python-3.12.0/Lib/json/__pycache__:
decoder.cpython-312.pyc  __init__.cpython-312.pyc
encoder.cpython-312.pyc  scanner.cpython-312.pyc

./Python-3.12.0/Lib/lib2to3:
btm_matcher.py  fixes        main.py             __pycache__
btm_utils.py    Grammar.txt  patcomp.py          pygram.py
fixer_base.py   __init__.py  PatternGrammar.txt  pytree.py
fixer_util.py   __main__.py  pgen2               refactor.py

./Python-3.12.0/Lib/lib2to3/fixes:
fix_apply.py       fix_input.py              fix_reduce.py
fix_asserts.py     fix_intern.py             fix_reload.py
fix_basestring.py  fix_isinstance.py         fix_renames.py
fix_buffer.py      fix_itertools_imports.py  fix_repr.py
fix_dict.py        fix_itertools.py          fix_set_literal.py
fix_except.py      fix_long.py               fix_standarderror.py
fix_execfile.py    fix_map.py                fix_sys_exc.py
fix_exec.py        fix_metaclass.py          fix_throw.py
fix_exitfunc.py    fix_methodattrs.py        fix_tuple_params.py
fix_filter.py      fix_ne.py                 fix_types.py
fix_funcattrs.py   fix_next.py               fix_unicode.py
fix_future.py      fix_nonzero.py            fix_urllib.py
fix_getcwdu.py     fix_numliterals.py        fix_ws_comma.py
fix_has_key.py     fix_operator.py           fix_xrange.py
fix_idioms.py      fix_paren.py              fix_xreadlines.py
fix_import.py      fix_print.py              fix_zip.py
fix_imports2.py    fix_raise.py              __init__.py
fix_imports.py     fix_raw_input.py

./Python-3.12.0/Lib/lib2to3/pgen2:
conv.py    grammar.py   literals.py  pgen.py      tokenize.py
driver.py  __init__.py  parse.py     __pycache__  token.py

./Python-3.12.0/Lib/lib2to3/pgen2/__pycache__:
driver.cpython-312.pyc    parse.cpython-312.pyc  tokenize.cpython-312.pyc
grammar.cpython-312.pyc   pgen.cpython-312.pyc
__init__.cpython-312.pyc  token.cpython-312.pyc

./Python-3.12.0/Lib/lib2to3/__pycache__:
__init__.cpython-312.pyc

./Python-3.12.0/Lib/logging:
config.py  handlers.py  __init__.py  __pycache__

./Python-3.12.0/Lib/logging/__pycache__:
config.cpython-312.pyc  handlers.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/msilib:
__init__.py  schema.py  sequence.py  text.py

./Python-3.12.0/Lib/multiprocessing:
connection.py  managers.py           process.py           sharedctypes.py
context.py     pool.py               __pycache__          shared_memory.py
dummy          popen_fork.py         queues.py            spawn.py
forkserver.py  popen_forkserver.py   reduction.py         synchronize.py
heap.py        popen_spawn_posix.py  resource_sharer.py   util.py
__init__.py    popen_spawn_win32.py  resource_tracker.py

./Python-3.12.0/Lib/multiprocessing/dummy:
connection.py  __init__.py

./Python-3.12.0/Lib/multiprocessing/__pycache__:
connection.cpython-312.pyc        queues.cpython-312.pyc
context.cpython-312.pyc           reduction.cpython-312.pyc
forkserver.cpython-312.pyc        resource_tracker.cpython-312.pyc
__init__.cpython-312.pyc          spawn.cpython-312.pyc
popen_fork.cpython-312.pyc        synchronize.cpython-312.pyc
popen_forkserver.cpython-312.pyc  util.cpython-312.pyc
process.cpython-312.pyc

./Python-3.12.0/Lib/__phello__:
ham  __init__.py  spam.py

./Python-3.12.0/Lib/__phello__/ham:
eggs.py  __init__.py

./Python-3.12.0/Lib/__pycache__:
abc.cpython-312.pyc               numbers.cpython-312.pyc
argparse.cpython-312.pyc          opcode.cpython-312.pyc
ast.cpython-312.pyc               operator.cpython-312.pyc
base64.cpython-312.pyc            optparse.cpython-312.pyc
bisect.cpython-312.pyc            os.cpython-312.pyc
bz2.cpython-312.pyc               pathlib.cpython-312.pyc
calendar.cpython-312.pyc          pickle.cpython-312.pyc
codecs.cpython-312.pyc            pkgutil.cpython-312.pyc
_collections_abc.cpython-312.pyc  platform.cpython-312.pyc
colorsys.cpython-312.pyc          plistlib.cpython-312.pyc
_compat_pickle.cpython-312.pyc    posixpath.cpython-312.pyc
compileall.cpython-312.pyc        pprint.cpython-312.pyc
_compression.cpython-312.pyc      py_compile.cpython-312.pyc
configparser.cpython-312.pyc      queue.cpython-312.pyc
contextlib.cpython-312.pyc        quopri.cpython-312.pyc
contextvars.cpython-312.pyc       random.cpython-312.pyc
copy.cpython-312.pyc              reprlib.cpython-312.pyc
copyreg.cpython-312.pyc           selectors.cpython-312.pyc
csv.cpython-312.pyc               shlex.cpython-312.pyc
dataclasses.cpython-312.pyc       shutil.cpython-312.pyc
datetime.cpython-312.pyc          signal.cpython-312.pyc
decimal.cpython-312.pyc           _sitebuiltins.cpython-312.pyc
dis.cpython-312.pyc               site.cpython-312.pyc
enum.cpython-312.pyc              socket.cpython-312.pyc
filecmp.cpython-312.pyc           socketserver.cpython-312.pyc
fnmatch.cpython-312.pyc           ssl.cpython-312.pyc
fractions.cpython-312.pyc         stat.cpython-312.pyc
functools.cpython-312.pyc         string.cpython-312.pyc
__future__.cpython-312.pyc        stringprep.cpython-312.pyc
genericpath.cpython-312.pyc       struct.cpython-312.pyc
getpass.cpython-312.pyc           subprocess.cpython-312.pyc
gettext.cpython-312.pyc           sysconfig.cpython-312.pyc
glob.cpython-312.pyc              tarfile.cpython-312.pyc
gzip.cpython-312.pyc              tempfile.cpython-312.pyc
hashlib.cpython-312.pyc           textwrap.cpython-312.pyc
heapq.cpython-312.pyc             threading.cpython-312.pyc
hmac.cpython-312.pyc              token.cpython-312.pyc
inspect.cpython-312.pyc           tokenize.cpython-312.pyc
io.cpython-312.pyc                traceback.cpython-312.pyc
ipaddress.cpython-312.pyc         types.cpython-312.pyc
keyword.cpython-312.pyc           typing.cpython-312.pyc
linecache.cpython-312.pyc         uuid.cpython-312.pyc
locale.cpython-312.pyc            warnings.cpython-312.pyc
lzma.cpython-312.pyc              weakref.cpython-312.pyc
_markupbase.cpython-312.pyc       _weakrefset.cpython-312.pyc
mimetypes.cpython-312.pyc

./Python-3.12.0/Lib/pydoc_data:
__init__.py  _pydoc.css  topics.py

./Python-3.12.0/Lib/re:
_casefix.py   _constants.py  _parser.py
_compiler.py  __init__.py    __pycache__

./Python-3.12.0/Lib/re/__pycache__:
_casefix.cpython-312.pyc    __init__.cpython-312.pyc
_compiler.cpython-312.pyc   _parser.cpython-312.pyc
_constants.cpython-312.pyc

./Python-3.12.0/Lib/site-packages:
README.txt

./Python-3.12.0/Lib/sqlite3:
dbapi2.py  dump.py  __init__.py  __main__.py

./Python-3.12.0/Lib/test:
allsans.pem
ann_module2.py
ann_module3.py
ann_module4.py
ann_module5.py
ann_module6.py
ann_module7.py
ann_module8.py
ann_module.py
audiodata
audiotest.au
audiotests.py
audit-tests.py
autotest.py
badcert.pem
bad_coding2.py
bad_coding.py
badkey.pem
badsyntax_3131.py
badsyntax_future10.py
badsyntax_future3.py
badsyntax_future4.py
badsyntax_future5.py
badsyntax_future6.py
badsyntax_future7.py
badsyntax_future8.py
badsyntax_future9.py
badsyntax_pep3120.py
bisect_cmd.py
capath
cfgparser.1
cfgparser.2
cfgparser.3
cjkencodings
clinic.test.c
cmath_testcases.txt
coding20731.py
crashers
curses_tests.py
data
dataclass_module_1.py
dataclass_module_1_str.py
dataclass_module_2.py
dataclass_module_2_str.py
dataclass_textanno.py
datetimetester.py
decimaltestdata
dis_module.py
doctest_aliases.py
doctest_lineno.py
double_const.py
dtracedata
empty.vbs
encoded_modules
exception_hierarchy.txt
ffdh3072.pem
final_a.py
final_b.py
floating_points.txt
fork_wait.py
formatfloat_testcases.txt
future_test1.py
future_test2.py
gdb_sample.py
idnsans.pem
ieee754.txt
imghdrdata
imp_dummy.py
__init__.py
inspect_fodder2.py
inspect_fodder.py
inspect_stock_annotations.py
inspect_stringized_annotations_2.py
inspect_stringized_annotations.py
keycert2.pem
keycert3.pem
keycert4.pem
keycertecc.pem
keycert.passwd.pem
keycert.pem
leakers
levenshtein_examples.json
libregrtest
list_tests.py
lock_tests.py
mailcap.txt
__main__.py
make_ssl_certs.py
mapping_tests.py
math_testcases.txt
memory_watchdog.py
mime.types
mock_socket.py
mod_generics_cache.py
mp_fork_bomb.py
mp_preload.py
multibytecodec_support.py
nokia.pem
nosan.pem
nullbytecert.pem
nullcert.pem
pickletester.py
profilee.py
pstats.pck
pycacert.pem
pycakey.pem
pyclbr_input.py
pydocfodder.py
pydoc_mod.py
pythoninfo.py
randv2_32.pck
randv2_64.pck
randv3.pck
recursion.tar
regrtest.py
relimport.py
reperf.py
re_tests.py
revocation.crl
sample_doctest_no_docstrings.py
sample_doctest_no_doctests.py
sample_doctest.py
secp384r1.pem
selfsigned_pythontestdotnet.pem
seq_tests.py
setuptools-67.6.1-py3-none-any.whl
sgml_input.html
shadowed_super.py
signalinterproctester.py
Sine-1000Hz-300ms.aif
smtpd.py
sndhdrdata
sortperf.py
ssl_cert.pem
ssl_key.passwd.pem
ssl_key.pem
ssl_servers.py
ssltests.py
string_tests.py
subprocessdata
support
talos-2019-0758.pem
test_abc.py
test_abstract_numbers.py
test_aifc.py
test___all__.py
test_argparse.py
test_array.py
test_asdl_parser.py
test_ast.py
test_asyncgen.py
test_asyncio
_test_atexit.py
test_atexit.py
test_audioop.py
test_audit.py
test_augassign.py
test_base64.py
test_baseexception.py
test_bdb.py
test_bigaddrspace.py
test_bigmem.py
test_binascii.py
test_binop.py
test_bisect.py
test_bool.py
test_buffer.py
test_bufio.py
test_builtin.py
test_bytes.py
test_bz2.py
test_calendar.py
test_call.py
test_capi
test_cgi.py
test_cgitb.py
test_charmapcodec.py
test_class.py
test_clinic.py
test_c_locale_coercion.py
test_cmath.py
test_cmd_line.py
test_cmd_line_script.py
test_cmd.py
test_codeccallbacks.py
test_codecencodings_cn.py
test_codecencodings_hk.py
test_codecencodings_iso2022.py
test_codecencodings_jp.py
test_codecencodings_kr.py
test_codecencodings_tw.py
test_codecmaps_cn.py
test_codecmaps_hk.py
test_codecmaps_jp.py
test_codecmaps_kr.py
test_codecmaps_tw.py
testcodec.py
test_codecs.py
test_code_module.py
test_codeop.py
test_code.py
test_collections.py
test_colorsys.py
test_compare.py
test_compileall.py
test_compile.py
test_compiler_assemble.py
test_compiler_codegen.py
test_complex.py
test_concurrent_futures
test_configparser.py
test_contains.py
test_contextlib_async.py
test_contextlib.py
test_context.py
test_copy.py
test_copyreg.py
test_coroutines.py
test_cppext
test_cprofile.py
test_crashers.py
test_crypt.py
test_csv.py
test_ctypes
test_curses.py
test_dataclasses.py
test_datetime.py
test_dbm_dumb.py
test_dbm_gnu.py
test_dbm_ndbm.py
test_dbm.py
test_decimal.py
test_decorators.py
test_defaultdict.py
test_deque.py
test_descr.py
test_descrtut.py
test_devpoll.py
test_dictcomps.py
test_dict.py
test_dict_version.py
test_dictviews.py
test_difflib_expect.html
test_difflib.py
test_dis.py
test_doctest2.py
test_doctest2.txt
test_doctest3.txt
test_doctest4.txt
test_doctest.py
test_doctest.txt
test_docxmlrpc.py
test_dtrace.py
test_dynamicclassattribute.py
test_dynamic.py
_test_eintr.py
test_eintr.py
test_email
test_embed.py
_test_embed_set_config.py
_test_embed_structseq.py
test_ensurepip.py
test_enumerate.py
test_enum.py
test_eof.py
test_epoll.py
test_errno.py
test_exception_group.py
test_exception_hierarchy.py
test_exceptions.py
test_exception_variations.py
test_except_star.py
test_extcall.py
test_faulthandler.py
test_fcntl.py
test_filecmp.py
test_file_eintr.py
test_fileinput.py
test_fileio.py
test_file.py
test_fileutils.py
test_finalization.py
test_float.py
test_flufl.py
test_fnmatch.py
test_fork1.py
test_format.py
test_fractions.py
test_frame.py
test_frozen.py
test_fstring.py
test_ftplib.py
test_funcattrs.py
test_functools.py
test_future3.py
test_future4.py
test_future5.py
test___future__.py
test_future.py
test_gc.py
test_gdb.py
test_generators.py
test_generator_stop.py
test_genericalias.py
test_genericclass.py
test_genericpath.py
test_genexps.py
test_getopt.py
test_getpass.py
test_getpath.py
test_gettext.py
test_global.py
test_glob.py
test_grammar.py
test_graphlib.py
test_grp.py
test_gzip.py
test_hashlib.py
test_hash.py
test_heapq.py
test_hmac.py
test_htmlparser.py
test_html.py
test_http_cookiejar.py
test_http_cookies.py
test_httplib.py
test_httpservers.py
test_idle.py
test_imaplib.py
test_imghdr.py
test_import
test_importlib
test_index.py
test_inspect.py
test_interpreters.py
test_int_literal.py
test_int.py
test_ioctl.py
test_io.py
test_ipaddress.py
test_isinstance.py
test_iterlen.py
test_iter.py
test_itertools.py
test_json
test_keywordonlyarg.py
test_keyword.py
test_kqueue.py
test_largefile.py
test_launcher.py
test_lib2to3
test_linecache.py
test_listcomps.py
test_list.py
test_lltrace.py
test__locale.py
test_locale.py
test_logging.py
test_longexp.py
test_long.py
test_lzma.py
test_mailbox.py
test_mailcap.py
test_marshal.py
test_math_property.py
test_math.py
test_memoryio.py
test_memoryview.py
test_metaclass.py
test_mimetypes.py
test_minidom.py
test_mmap.py
test_module
test_modulefinder.py
test_monitoring.py
test_msilib.py
test_multibytecodec.py
test_multiprocessing_fork
test_multiprocessing_forkserver
test_multiprocessing_main_handling.py
_test_multiprocessing.py
test_multiprocessing_spawn
test_named_expressions.py
test_netrc.py
test_nis.py
test_nntplib.py
test_ntpath.py
test_numeric_tower.py
test_opcache.py
test__opcode.py
test_opcodes.py
test_openpty.py
test_operator.py
test_optparse.py
test_ordered_dict.py
test_os.py
test_ossaudiodev.py
test_osx_env.py
test__osx_support.py
test_pathlib.py
test_patma.py
test_pdb.py
test_peepholer.py
test_peg_generator
test_pep646_syntax.py
test_perfmaps.py
test_perf_profiler.py
test_picklebuffer.py
test_pickle.py
test_pickletools.py
test_pipes.py
test_pkg.py
test_pkgutil.py
test_platform.py
test_plistlib.py
test_poll.py
test_popen.py
test_poplib.py
test_positional_only_arg.py
test_posixpath.py
test_posix.py
test_pow.py
test_pprint.py
test_print.py
test_profile.py
test_property.py
test_pstats.py
test_pty.py
test_pulldom.py
test_pwd.py
test_pyclbr.py
test_py_compile.py
test_pydoc.py
test_pyexpat.py
test_queue.py
test_quopri.py
test_raise.py
test_random.py
test_range.py
test_readline.py
test_regrtest.py
test_repl.py
test_reprlib.py
test_re.py
test_resource.py
test_richcmp.py
test_rlcompleter.py
test_robotparser.py
test_runpy.py
test_sax.py
test_sched.py
test_scope.py
test_script_helper.py
test_secrets.py
test_selectors.py
test_select.py
test_setcomps.py
test_set.py
test_shelve.py
test_shlex.py
test_shutil.py
test_signal.py
test_site.py
test_slice.py
test_smtplib.py
test_smtpnet.py
test_sndhdr.py
test_socket.py
test_socketserver.py
test_sort.py
test_source_encoding.py
test_spwd.py
test_sqlite3
test_ssl.py
test_stable_abi_ctypes.py
test_startfile.py
test_statistics.py
test_stat.py
test_strftime.py
test_string_literals.py
test_stringprep.py
test_string.py
test_strptime.py
test_strtod.py
test_struct.py
test_structseq.py
test_subclassinit.py
test_subprocess.py
test_sunau.py
test_sundry.py
test_super.py
test_support.py
test_symtable.py
test_syntax.py
test_sysconfig.py
test_syslog.py
test_sys.py
test_sys_setprofile.py
test_sys_settrace.py
test_tabnanny.py
test_tarfile.py
testtar.tar
testtar.tar.xz
test_tcl.py
test_telnetlib.py
test_tempfile.py
test_textwrap.py
test_threadedtempfile.py
test_threading_local.py
test_threading.py
test_thread.py
test_threadsignals.py
test_timeit.py
test_timeout.py
test_time.py
test_tix.py
test_tkinter
test_tokenize.py
test_tomllib
test_tools
test_traceback.py
test_tracemalloc.py
test_trace.py
test_ttk
test_ttk_textonly.py
test_tuple.py
test_turtle.py
test_type_aliases.py
test_type_annotations.py
test_type_cache.py
test_typechecks.py
test_type_comments.py
test_type_params.py
test_types.py
test_typing.py
test_ucn.py
test_unary.py
test_unicodedata.py
test_unicode_file_functions.py
test_unicode_file.py
test_unicode_identifiers.py
test_unicode.py
test_unittest
test_univnewlines.py
test_unpack_ex.py
test_unpack.py
test_unparse.py
test_urllib2_localnet.py
test_urllib2net.py
test_urllib2.py
test_urllibnet.py
test_urllib.py
test_urllib_response.py
test_urlparse.py
test_userdict.py
test_userlist.py
test_userstring.py
test_utf8_mode.py
test_utf8source.py
test_uuid.py
test_uu.py
_test_venv_multiprocessing.py
test_venv.py
test_wait3.py
test_wait4.py
test_warnings
test_wave.py
test_weakref.py
test_weakset.py
test_webbrowser.py
test_winconsoleio.py
test_winreg.py
test_winsound.py
test_with.py
test_wmi.py
test_wsgiref.py
test_xdrlib.py
test_xml_dom_minicompat.py
test_xml_etree_c.py
test_xml_etree.py
test_xmlrpc_net.py
test_xmlrpc.py
test__xxinterpchannels.py
test_xxlimited.py
test__xxsubinterpreters.py
test_xxtestfuzz.py
test_yield_from.py
test_zipapp.py
test_zipfile
test_zipfile64.py
test_zipimport.py
test_zipimport_support.py
test_zlib.py
test_zoneinfo
tf_inherit_check.py
time_hashlib.py
tokenize_tests-latin1-coding-cookie-and-utf8-bom-sig.txt
tokenize_tests-no-coding-cookie-and-utf8-bom-sig-only.txt
tokenize_tests.txt
tokenize_tests-utf8-coding-cookie-and-no-utf8-bom-sig.txt
tokenize_tests-utf8-coding-cookie-and-utf8-bom-sig.txt
tracedmodules
_typed_dict_helper.py
typinganndata
wheel-0.40.0-py3-none-any.whl
win_console_handler.py
xmltestdata
xmltests.py
zip_cp437_header.zip
zipdir.zip
ziptestdata

./Python-3.12.0/Lib/test/audiodata:
pluck-alaw.aifc   pluck-pcm24.aiff     pluck-pcm32.aiff  pluck-pcm8.au
pluck-pcm16.aiff  pluck-pcm24.au       pluck-pcm32.au    pluck-pcm8.wav
pluck-pcm16.au    pluck-pcm24-ext.wav  pluck-pcm32.wav   pluck-ulaw.aifc
pluck-pcm16.wav   pluck-pcm24.wav      pluck-pcm8.aiff   pluck-ulaw.au

./Python-3.12.0/Lib/test/capath:
4e1295a3.0  5ed36f99.0  6e88d7b8.0  99d0fa06.0  b1930218.0  ceff1710.0

./Python-3.12.0/Lib/test/cjkencodings:
big5hkscs.txt          euc_kr.txt        iso2022_jp.txt
big5hkscs-utf8.txt     euc_kr-utf8.txt   iso2022_jp-utf8.txt
big5.txt               gb18030.txt       iso2022_kr.txt
big5-utf8.txt          gb18030-utf8.txt  iso2022_kr-utf8.txt
cp949.txt              gb2312.txt        johab.txt
cp949-utf8.txt         gb2312-utf8.txt   johab-utf8.txt
euc_jisx0213.txt       gbk.txt           shift_jis.txt
euc_jisx0213-utf8.txt  gbk-utf8.txt      shift_jis-utf8.txt
euc_jp.txt             hz.txt            shift_jisx0213.txt
euc_jp-utf8.txt        hz-utf8.txt       shift_jisx0213-utf8.txt

./Python-3.12.0/Lib/test/crashers:
bogus_code_obj.py           README
gc_inspection.py            recursive_call.py
infinite_loop_re.py         trace_at_recursion_limit.py
mutation_inside_cyclegc.py  underlying_dict.py

./Python-3.12.0/Lib/test/data:
README

./Python-3.12.0/Lib/test/decimaltestdata:
abs.decTest                dqCopyNegate.decTest
add.decTest                dqCopySign.decTest
and.decTest                dqDivide.decTest
base.decTest               dqDivideInt.decTest
clamp.decTest              dqEncode.decTest
class.decTest              dqFMA.decTest
compare.decTest            dqInvert.decTest
comparetotal.decTest       dqLogB.decTest
comparetotmag.decTest      dqMax.decTest
copyabs.decTest            dqMaxMag.decTest
copy.decTest               dqMin.decTest
copynegate.decTest         dqMinMag.decTest
copysign.decTest           dqMinus.decTest
ddAbs.decTest              dqMultiply.decTest
ddAdd.decTest              dqNextMinus.decTest
ddAnd.decTest              dqNextPlus.decTest
ddBase.decTest             dqNextToward.decTest
ddCanonical.decTest        dqOr.decTest
ddClass.decTest            dqPlus.decTest
ddCompare.decTest          dqQuantize.decTest
ddCompareSig.decTest       dqReduce.decTest
ddCompareTotal.decTest     dqRemainder.decTest
ddCompareTotalMag.decTest  dqRemainderNear.decTest
ddCopyAbs.decTest          dqRotate.decTest
ddCopy.decTest             dqSameQuantum.decTest
ddCopyNegate.decTest       dqScaleB.decTest
ddCopySign.decTest         dqShift.decTest
ddDivide.decTest           dqSubtract.decTest
ddDivideInt.decTest        dqToIntegral.decTest
ddEncode.decTest           dqXor.decTest
ddFMA.decTest              dsBase.decTest
ddInvert.decTest           dsEncode.decTest
ddLogB.decTest             exp.decTest
ddMax.decTest              extra.decTest
ddMaxMag.decTest           fma.decTest
ddMin.decTest              inexact.decTest
ddMinMag.decTest           invert.decTest
ddMinus.decTest            ln.decTest
ddMultiply.decTest         log10.decTest
ddNextMinus.decTest        logb.decTest
ddNextPlus.decTest         max.decTest
ddNextToward.decTest       maxmag.decTest
ddOr.decTest               min.decTest
ddPlus.decTest             minmag.decTest
ddQuantize.decTest         minus.decTest
ddReduce.decTest           multiply.decTest
ddRemainder.decTest        nextminus.decTest
ddRemainderNear.decTest    nextplus.decTest
ddRotate.decTest           nexttoward.decTest
ddSameQuantum.decTest      or.decTest
ddScaleB.decTest           plus.decTest
ddShift.decTest            power.decTest
ddSubtract.decTest         powersqrt.decTest
ddToIntegral.decTest       quantize.decTest
ddXor.decTest              randomBound32.decTest
decDouble.decTest          randoms.decTest
decQuad.decTest            reduce.decTest
decSingle.decTest          remainder.decTest
divide.decTest             remainderNear.decTest
divideint.decTest          rescale.decTest
dqAbs.decTest              rotate.decTest
dqAdd.decTest              rounding.decTest
dqAnd.decTest              samequantum.decTest
dqBase.decTest             scaleb.decTest
dqCanonical.decTest        shift.decTest
dqClass.decTest            squareroot.decTest
dqCompare.decTest          subtract.decTest
dqCompareSig.decTest       testall.decTest
dqCompareTotal.decTest     tointegral.decTest
dqCompareTotalMag.decTest  tointegralx.decTest
dqCopyAbs.decTest          xor.decTest
dqCopy.decTest

./Python-3.12.0/Lib/test/dtracedata:
assert_usable.d        call_stack.stp.expected  instance.py
assert_usable.stp      gc.d                     line.d
call_stack.d           gc.d.expected            line.d.expected
call_stack.d.expected  gc.py                    line.py
call_stack.py          gc.stp
call_stack.stp         gc.stp.expected

./Python-3.12.0/Lib/test/encoded_modules:
__init__.py  module_iso_8859_1.py  module_koi8_r.py

./Python-3.12.0/Lib/test/imghdrdata:
python.bmp  python.jpg  python.png  python-raw.jpg  python.webp
python.exr  python.pbm  python.ppm  python.sgi      python.xbm
python.gif  python.pgm  python.ras  python.tiff

./Python-3.12.0/Lib/test/leakers:
__init__.py  README.txt  test_ctypes.py  test_selftype.py

./Python-3.12.0/Lib/test/libregrtest:
cmdline.py   main.py  refleak.py     runtest.py   setup.py  win_utils.py
__init__.py  pgo.py   runtest_mp.py  save_env.py  utils.py

./Python-3.12.0/Lib/test/sndhdrdata:
README       sndhdr.aifc  sndhdr.au    sndhdr.sndt  sndhdr.wav
sndhdr.8svx  sndhdr.aiff  sndhdr.hcom  sndhdr.voc

./Python-3.12.0/Lib/test/subprocessdata:
fd_status.py  input_reader.py  qcat.py  qgrep.py  sigchild_ignore.py

./Python-3.12.0/Lib/test/support:
ast_helper.py         _hypothesis_stubs  script_helper.py
asynchat.py           import_helper.py   socket_helper.py
asyncore.py           __init__.py        testcase.py
bytecode_helper.py    interpreters.py    testresult.py
hashlib_helper.py     logging_helper.py  threading_helper.py
hypothesis_helper.py  os_helper.py       warnings_helper.py

./Python-3.12.0/Lib/test/support/_hypothesis_stubs:
_helpers.py  __init__.py  strategies.py

./Python-3.12.0/Lib/test/test_asyncio:
echo2.py                    test_selector_events.py
echo3.py                    test_sendfile.py
echo.py                     test_server.py
functional.py               test_sock_lowlevel.py
__init__.py                 test_sslproto.py
__main__.py                 test_ssl.py
test_base_events.py         test_streams.py
test_buffered_proto.py      test_subprocess.py
test_context.py             test_taskgroups.py
test_eager_task_factory.py  test_tasks.py
test_events.py              test_threads.py
test_futures2.py            test_timeouts.py
test_futures.py             test_transports.py
test_locks.py               test_unix_events.py
test_pep492.py              test_waitfor.py
test_proactor_events.py     test_windows_events.py
test_protocols.py           test_windows_utils.py
test_queues.py              utils.py
test_runners.py

./Python-3.12.0/Lib/test/test_capi:
check_config.py   test_eval_code_ex.py  test_misc.py
__init__.py       test_exceptions.py    test_structmembers.py
__main__.py       test_getargs.py       test_unicode.py
test_abstract.py  test_immortal.py      test_watchers.py
test_codecs.py    test_long.py
test_dict.py      test_mem.py

./Python-3.12.0/Lib/test/test_concurrent_futures:
executor.py           test_deadlock.py  test_process_pool.py  test_wait.py
__init__.py           test_future.py    test_shutdown.py      util.py
test_as_completed.py  test_init.py      test_thread_pool.py

./Python-3.12.0/Lib/test/test_cppext:
extension.cpp  __init__.py  setup.py

./Python-3.12.0/Lib/test/test_ctypes:
__init__.py               test_memfunctions.py
__main__.py               test_numbers.py
test_anon.py              test_objects.py
test_array_in_pointer.py  test_parameters.py
test_arrays.py            test_pep3118.py
test_as_parameter.py      test_pickling.py
test_bitfields.py         test_pointers.py
test_buffers.py           test_prototypes.py
test_bytes.py             test_python_api.py
test_byteswap.py          test_random_things.py
test_callbacks.py         test_refcounts.py
test_cast.py              test_repr.py
test_cfuncs.py            test_returnfuncptrs.py
test_checkretval.py       test_simplesubclasses.py
test_delattr.py           test_sizes.py
test_errno.py             test_slicing.py
test_find.py              test_stringptr.py
test_frombuffer.py        test_strings.py
test_funcptr.py           test_struct_fields.py
test_functions.py         test_structures.py
test_incomplete.py        test_unaligned_structures.py
test_init.py              test_unicode.py
test_internals.py         test_values.py
test_keeprefs.py          test_varsize_struct.py
test_libc.py              test_win32.py
test_loading.py           test_wintypes.py
test_macholib.py

./Python-3.12.0/Lib/test/test_email:
data                     test_email.py                 test_message.py
__init__.py              test__encoded_words.py        test_parser.py
__main__.py              test_generator.py             test_pickleable.py
test_asian_codecs.py     test_headerregistry.py        test_policy.py
test_contentmanager.py   test__header_value_parser.py  test_utils.py
test_defect_handling.py  test_inversion.py             torture_test.py

./Python-3.12.0/Lib/test/test_email/data:
msg_01.txt  msg_12a.txt  msg_22.txt  msg_33.txt  msg_44.txt  python.ppm
msg_02.txt  msg_12.txt   msg_23.txt  msg_34.txt  msg_45.txt  python.ras
msg_03.txt  msg_13.txt   msg_24.txt  msg_35.txt  msg_46.txt  python.sgi
msg_04.txt  msg_14.txt   msg_25.txt  msg_36.txt  msg_47.txt  python.tiff
msg_05.txt  msg_15.txt   msg_26.txt  msg_37.txt  python.bmp  python.webp
msg_06.txt  msg_16.txt   msg_27.txt  msg_38.txt  python.exr  python.xbm
msg_07.txt  msg_17.txt   msg_28.txt  msg_39.txt  python.gif  sndhdr.aifc
msg_08.txt  msg_18.txt   msg_29.txt  msg_40.txt  python.jpg  sndhdr.aiff
msg_09.txt  msg_19.txt   msg_30.txt  msg_41.txt  python.pbm  sndhdr.au
msg_10.txt  msg_20.txt   msg_31.txt  msg_42.txt  python.pgm  sndhdr.wav
msg_11.txt  msg_21.txt   msg_32.txt  msg_43.txt  python.png

./Python-3.12.0/Lib/test/test_import:
data  __init__.py  __main__.py

./Python-3.12.0/Lib/test/test_import/data:
circular_imports  package  package2  unwritable

./Python-3.12.0/Lib/test/test_import/data/circular_imports:
basic2.py    binding.py      indirect.py    source.py      subpkg2
basic.py     from_cycle1.py  rebinding2.py  subpackage.py  use.py
binding2.py  from_cycle2.py  rebinding.py   subpkg         util.py

./Python-3.12.0/Lib/test/test_import/data/circular_imports/subpkg:
subpackage2.py  util.py

./Python-3.12.0/Lib/test/test_import/data/circular_imports/subpkg2:
__init__.py  parent

./Python-3.12.0/Lib/test/test_import/data/circular_imports/subpkg2/parent:
child.py  __init__.py

./Python-3.12.0/Lib/test/test_import/data/package:
__init__.py  submodule.py

./Python-3.12.0/Lib/test/test_import/data/package2:
submodule1.py  submodule2.py

./Python-3.12.0/Lib/test/test_import/data/unwritable:
__init__.py  x.py

./Python-3.12.0/Lib/test/test_importlib:
abc.py          partial               test_namespace_pkgs.py
builtin         _path.py              test_pkg_import.py
_context.py     resources             test_spec.py
data            source                test_threaded_import.py
extension       stubs.py              test_util.py
fixtures.py     test_abc.py           test_windows.py
frozen          test_api.py           test_zip.py
import_         test_lazy.py          threaded_import_hangers.py
__init__.py     test_locks.py         util.py
__main__.py     test_main.py
namespace_pkgs  test_metadata_api.py

./Python-3.12.0/Lib/test/test_importlib/builtin:
__init__.py  __main__.py  test_finder.py  test_loader.py

./Python-3.12.0/Lib/test/test_importlib/data:
example2-1.0.0-py3-none-any.whl  example-21.12-py3-none-any.whl
example-21.12-py3.6.egg          __init__.py

./Python-3.12.0/Lib/test/test_importlib/extension:
__init__.py  test_case_sensitivity.py  test_loader.py
__main__.py  test_finder.py            test_path_hook.py

./Python-3.12.0/Lib/test/test_importlib/frozen:
__init__.py  __main__.py  test_finder.py  test_loader.py

./Python-3.12.0/Lib/test/test_importlib/import_:
__init__.py      test_fromlist.py    test___package__.py
__main__.py      test_helpers.py     test_packages.py
test_api.py      test___loader__.py  test_path.py
test_caching.py  test_meta_path.py   test_relative_imports.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs:
both_portions                 not_a_namespace_pkg  project2
missing_directory.zip         portion1             project3
module_and_namespace_package  portion2             top_level_portion1.zip
nested_portion1.zip           project1

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/both_portions:
foo

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/both_portions/foo:
one.py  two.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/module_and_namespace_package:
a_test  a_test.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/module_and_namespace_package/a_test:
empty

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/not_a_namespace_pkg:
foo

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/not_a_namespace_pkg/foo:
__init__.py  one.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/portion1:
foo

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/portion1/foo:
one.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/portion2:
foo

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/portion2/foo:
two.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project1:
parent

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project1/parent:
child

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project1/parent/child:
one.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project2:
parent

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project2/parent:
child

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project2/parent/child:
two.py

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project3:
parent

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project3/parent:
child

./Python-3.12.0/Lib/test/test_importlib/namespace_pkgs/project3/parent/child:
three.py

./Python-3.12.0/Lib/test/test_importlib/partial:
cfimport.py  pool_in_threads.py

./Python-3.12.0/Lib/test/test_importlib/resources:
data01                      test_contents.py  test_resource.py
data02                      test_custom.py    update-zips.py
data03                      test_files.py     util.py
__init__.py                 test_open.py      zipdata01
namespacedata01             test_path.py      zipdata02
_path.py                    test_reader.py
test_compatibilty_files.py  test_read.py

./Python-3.12.0/Lib/test/test_importlib/resources/data01:
binary.file  __init__.py  subdirectory  utf-16.file  utf-8.file

./Python-3.12.0/Lib/test/test_importlib/resources/data01/subdirectory:
binary.file  __init__.py

./Python-3.12.0/Lib/test/test_importlib/resources/data02:
__init__.py  one  subdirectory  two

./Python-3.12.0/Lib/test/test_importlib/resources/data02/one:
__init__.py  resource1.txt

./Python-3.12.0/Lib/test/test_importlib/resources/data02/subdirectory:
subsubdir

./Python-3.12.0/Lib/test/test_importlib/resources/data02/subdirectory/subsubdir:
resource.txt

./Python-3.12.0/Lib/test/test_importlib/resources/data02/two:
__init__.py  resource2.txt

./Python-3.12.0/Lib/test/test_importlib/resources/data03:
__init__.py  namespace

./Python-3.12.0/Lib/test/test_importlib/resources/data03/namespace:
portion1  portion2  resource1.txt

./Python-3.12.0/Lib/test/test_importlib/resources/data03/namespace/portion1:
__init__.py

./Python-3.12.0/Lib/test/test_importlib/resources/data03/namespace/portion2:
__init__.py

./Python-3.12.0/Lib/test/test_importlib/resources/namespacedata01:
binary.file  utf-16.file  utf-8.file

./Python-3.12.0/Lib/test/test_importlib/resources/zipdata01:
__init__.py  ziptestdata.zip

./Python-3.12.0/Lib/test/test_importlib/resources/zipdata02:
__init__.py  ziptestdata.zip

./Python-3.12.0/Lib/test/test_importlib/source:
__init__.py               test_file_loader.py  test_source_encoding.py
__main__.py               test_finder.py
test_case_sensitivity.py  test_path_hook.py

./Python-3.12.0/Lib/test/test_json:
__init__.py                      test_fail.py       test_scanstring.py
__main__.py                      test_float.py      test_separators.py
test_decode.py                   test_indent.py     test_speedups.py
test_default.py                  test_pass1.py      test_tool.py
test_dump.py                     test_pass2.py      test_unicode.py
test_encode_basestring_ascii.py  test_pass3.py
test_enum.py                     test_recursion.py

./Python-3.12.0/Lib/test/test_lib2to3:
data         pytree_idempotency.py  test_fixers.py  test_pytree.py
__init__.py  support.py             test_main.py    test_refactor.py
__main__.py  test_all_fixers.py     test_parser.py  test_util.py

./Python-3.12.0/Lib/test/test_lib2to3/data:
bom.py                 false_encoding.py      py2_test_grammar.py
crlf.py                fixers                 py3_test_grammar.py
different_encoding.py  infinite_recursion.py  README

./Python-3.12.0/Lib/test/test_lib2to3/data/fixers:
bad_order.py  myfixes  no_fixer_cls.py  parrot_example.py

./Python-3.12.0/Lib/test/test_lib2to3/data/fixers/myfixes:
fix_explicit.py  fix_last.py    fix_preorder.py
fix_first.py     fix_parrot.py  __init__.py

./Python-3.12.0/Lib/test/test_module:
bad_getattr2.py  bad_getattr.py   __init__.py
bad_getattr3.py  good_getattr.py

./Python-3.12.0/Lib/test/test_multiprocessing_fork:
__init__.py      test_misc.py       test_threads.py
test_manager.py  test_processes.py

./Python-3.12.0/Lib/test/test_multiprocessing_forkserver:
__init__.py      test_misc.py       test_threads.py
test_manager.py  test_processes.py

./Python-3.12.0/Lib/test/test_multiprocessing_spawn:
__init__.py      test_misc.py       test_threads.py
test_manager.py  test_processes.py

./Python-3.12.0/Lib/test/test_peg_generator:
__init__.py  test_c_parser.py    test_grammar_validator.py
__main__.py  test_first_sets.py  test_pegen.py

./Python-3.12.0/Lib/test/test_sqlite3:
__init__.py     test_cli.py    test_factory.py     test_transactions.py
__main__.py     test_dbapi.py  test_hooks.py       test_types.py
test_backup.py  test_dump.py   test_regression.py  test_userfunctions.py

./Python-3.12.0/Lib/test/test_tkinter:
__init__.py           test_geometry_managers.py  test_text.py
__main__.py           test_images.py             test_variables.py
README                test_loadtk.py             test_widgets.py
support.py            test_messagebox.py         widget_tests.py
test_colorchooser.py  test_misc.py
test_font.py          test_simpledialog.py

./Python-3.12.0/Lib/test/test_tomllib:
burntsushi.py  __init__.py  test_data.py   test_misc.py
data           __main__.py  test_error.py

./Python-3.12.0/Lib/test/test_tomllib/data:
invalid  valid

./Python-3.12.0/Lib/test/test_tomllib/data/invalid:
array
array-missing-comma.toml
array-of-tables
basic-str-ends-in-escape.toml
boolean
dates-and-times
dotted-keys
inline-table
inline-table-missing-comma.toml
invalid-comment-char.toml
invalid-escaped-unicode.toml
invalid-hex.toml
keys-and-vals
literal-str
missing-closing-double-square-bracket.toml
missing-closing-square-bracket.toml
multiline-basic-str
multiline-literal-str
non-scalar-escaped.toml
table
unclosed-multiline-string.toml
unclosed-string.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/array:
file-end-after-val.toml  unclosed-after-item.toml  unclosed-empty.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/array-of-tables:
overwrite-array-in-parent.toml  overwrite-bool-with-aot.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/boolean:
invalid-false-casing.toml  invalid-true-casing.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/dates-and-times:
invalid-day.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/dotted-keys:
access-non-table.toml    extend-defined-table.toml
extend-defined-aot.toml  extend-defined-table-with-subtable.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/inline-table:
define-twice-in-subtable.toml  override-val-with-table.toml
define-twice.toml              overwrite-implicitly.toml
file-end-after-key-val.toml    overwrite-value-in-inner-array.toml
mutate.toml                    overwrite-value-in-inner-table.toml
override-val-in-table.toml     unclosed-empty.toml
override-val-with-array.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/keys-and-vals:
ends-early-table-def.toml  only-ws-after-dot.toml
ends-early.toml            overwrite-with-deep-table.toml
no-value.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/literal-str:
unclosed.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/multiline-basic-str:
carriage-return.toml          last-line-escape.toml
escape-only.toml              unclosed-ends-in-whitespace-escape.toml
file-ends-after-opening.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/multiline-literal-str:
file-ends-after-opening.toml  unclosed.toml

./Python-3.12.0/Lib/test/test_tomllib/data/invalid/table:
eof-after-opening.toml  redefine-1.toml  redefine-2.toml

./Python-3.12.0/Lib/test/test_tomllib/data/valid:
apostrophes-in-literal-string.json  five-quotes.toml
apostrophes-in-literal-string.toml  hex-char.json
array                               hex-char.toml
boolean.json                        multiline-basic-str
boolean.toml                        no-newlines.json
dates-and-times                     no-newlines.toml
empty-inline-table.json             trailing-comma.json
empty-inline-table.toml             trailing-comma.toml
five-quotes.json

./Python-3.12.0/Lib/test/test_tomllib/data/valid/array:
array-subtables.json  open-parent-table.json
array-subtables.toml  open-parent-table.toml

./Python-3.12.0/Lib/test/test_tomllib/data/valid/dates-and-times:
datetimes.json  datetimes.toml  localtime.json  localtime.toml

./Python-3.12.0/Lib/test/test_tomllib/data/valid/multiline-basic-str:
ends-in-whitespace-escape.json  ends-in-whitespace-escape.toml

./Python-3.12.0/Lib/test/test_tools:
__init__.py  test_freeze.py  test_reindent.py
__main__.py  test_i18n.py    test_sundry.py

./Python-3.12.0/Lib/test/test_ttk:
__init__.py  test_extensions.py  test_widgets.py
__main__.py  test_style.py

./Python-3.12.0/Lib/test/test_unittest:
dummy.py            test_case.py              test_runner.py
__init__.py         test_discovery.py         test_setups.py
__main__.py         test_functiontestcase.py  test_skipping.py
support.py          test_loader.py            test_suite.py
test_assertions.py  testmock                  _test_warnings.py
test_async_case.py  test_program.py
test_break.py       test_result.py

./Python-3.12.0/Lib/test/test_unittest/testmock:
__init__.py  testasync.py     testmagicmethods.py  testsealable.py
__main__.py  testcallable.py  testmock.py          testsentinel.py
support.py   testhelpers.py   testpatch.py         testwith.py

./Python-3.12.0/Lib/test/test_warnings:
data  __init__.py  __main__.py

./Python-3.12.0/Lib/test/test_warnings/data:
import_warning.py  package_helper.py  stacklevel.py

./Python-3.12.0/Lib/test/test_zipfile:
__init__.py  __main__.py  _path  test_core.py

./Python-3.12.0/Lib/test/test_zipfile/_path:
_functools.py  _itertools.py  test_complexity.py  test_path.py
__init__.py    _support.py    _test_params.py     write-alpharep.py

./Python-3.12.0/Lib/test/test_zoneinfo:
data         __main__.py  test_zoneinfo_property.py
__init__.py  _support.py  test_zoneinfo.py

./Python-3.12.0/Lib/test/test_zoneinfo/data:
update_test_data.py  zoneinfo_data.json

./Python-3.12.0/Lib/test/tracedmodules:
__init__.py  testmod.py

./Python-3.12.0/Lib/test/typinganndata:
ann_module9.py  __init__.py

./Python-3.12.0/Lib/test/xmltestdata:
c14n-20                simple-ns.xml  test.xml
expat224_utf8_bug.xml  simple.xml     test.xml.out

./Python-3.12.0/Lib/test/xmltestdata/c14n-20:
c14nComment.xml               out_inC14N3_c14nDefault.xml
c14nDefault.xml               out_inC14N3_c14nPrefix.xml
c14nPrefixQname.xml           out_inC14N3_c14nTrim.xml
c14nPrefixQnameXpathElem.xml  out_inC14N4_c14nDefault.xml
c14nPrefix.xml                out_inC14N4_c14nTrim.xml
c14nQnameElem.xml             out_inC14N5_c14nDefault.xml
c14nQname.xml                 out_inC14N5_c14nTrim.xml
c14nQnameXpathElem.xml        out_inC14N6_c14nDefault.xml
c14nTrim.xml                  out_inNsContent_c14nDefault.xml
doc.dtd                       out_inNsContent_c14nPrefixQnameXpathElem.xml
doc.xsl                       out_inNsContent_c14nQnameElem.xml
inC14N1.xml                   out_inNsContent_c14nQnameXpathElem.xml
inC14N2.xml                   out_inNsDefault_c14nDefault.xml
inC14N3.xml                   out_inNsDefault_c14nPrefix.xml
inC14N4.xml                   out_inNsPushdown_c14nDefault.xml
inC14N5.xml                   out_inNsPushdown_c14nPrefix.xml
inC14N6.xml                   out_inNsRedecl_c14nDefault.xml
inNsContent.xml               out_inNsRedecl_c14nPrefix.xml
inNsDefault.xml               out_inNsSort_c14nDefault.xml
inNsPushdown.xml              out_inNsSort_c14nPrefix.xml
inNsRedecl.xml                out_inNsSuperfluous_c14nDefault.xml
inNsSort.xml                  out_inNsSuperfluous_c14nPrefix.xml
inNsSuperfluous.xml           out_inNsXml_c14nDefault.xml
inNsXml.xml                   out_inNsXml_c14nPrefixQname.xml
out_inC14N1_c14nComment.xml   out_inNsXml_c14nPrefix.xml
out_inC14N1_c14nDefault.xml   out_inNsXml_c14nQname.xml
out_inC14N2_c14nDefault.xml   README
out_inC14N2_c14nTrim.xml      world.txt

./Python-3.12.0/Lib/test/ziptestdata:
exe_with_z64  header.sh  testdata_module_inside_zip.py
exe_with_zip  README.md

./Python-3.12.0/Lib/tkinter:
colorchooser.py  dialog.py      font.py      messagebox.py    tix.py
commondialog.py  dnd.py         __init__.py  scrolledtext.py  ttk.py
constants.py     filedialog.py  __main__.py  simpledialog.py

./Python-3.12.0/Lib/tomllib:
__init__.py  _parser.py  _re.py  _types.py

./Python-3.12.0/Lib/turtledemo:
bytedesign.py     __init__.py       peace.py            tree.py
chaos.py          lindenmayer.py    penrose.py          turtle.cfg
clock.py          __main__.py       planet_and_moon.py  two_canvases.py
colormixer.py     minimal_hanoi.py  rosette.py          yinyang.py
forest.py         nim.py            round_dance.py
fractalcurves.py  paint.py          sorting_animate.py

./Python-3.12.0/Lib/unittest:
async_case.py  loader.py    main.py    runner.py   util.py
case.py        _log.py      mock.py    signals.py
__init__.py    __main__.py  result.py  suite.py

./Python-3.12.0/Lib/urllib:
error.py     parse.py     request.py   robotparser.py
__init__.py  __pycache__  response.py

./Python-3.12.0/Lib/urllib/__pycache__:
error.cpython-312.pyc     request.cpython-312.pyc
__init__.cpython-312.pyc  response.cpython-312.pyc
parse.cpython-312.pyc

./Python-3.12.0/Lib/venv:
__init__.py  __main__.py  scripts

./Python-3.12.0/Lib/venv/scripts:
common  nt  posix

./Python-3.12.0/Lib/venv/scripts/common:
activate  Activate.ps1

./Python-3.12.0/Lib/venv/scripts/nt:
activate.bat  deactivate.bat

./Python-3.12.0/Lib/venv/scripts/posix:
activate.csh  activate.fish

./Python-3.12.0/Lib/wsgiref:
handlers.py  __init__.py       types.py  validate.py
headers.py   simple_server.py  util.py

./Python-3.12.0/Lib/xml:
dom  etree  __init__.py  parsers  __pycache__  sax

./Python-3.12.0/Lib/xml/dom:
domreg.py        __init__.py    minidom.py     pulldom.py
expatbuilder.py  minicompat.py  NodeFilter.py  xmlbuilder.py

./Python-3.12.0/Lib/xml/etree:
cElementTree.py    ElementPath.py  __init__.py
ElementInclude.py  ElementTree.py  __pycache__

./Python-3.12.0/Lib/xml/etree/__pycache__:
ElementPath.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/xml/parsers:
expat.py  __init__.py  __pycache__

./Python-3.12.0/Lib/xml/parsers/__pycache__:
expat.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/xml/__pycache__:
__init__.cpython-312.pyc

./Python-3.12.0/Lib/xml/sax:
_exceptions.py  handler.py   saxutils.py
expatreader.py  __init__.py  xmlreader.py

./Python-3.12.0/Lib/xmlrpc:
client.py  __init__.py  __pycache__  server.py

./Python-3.12.0/Lib/xmlrpc/__pycache__:
client.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/zipfile:
__init__.py  __main__.py  _path  __pycache__

./Python-3.12.0/Lib/zipfile/_path:
glob.py  __init__.py  __pycache__

./Python-3.12.0/Lib/zipfile/_path/__pycache__:
glob.cpython-312.pyc  __init__.cpython-312.pyc

./Python-3.12.0/Lib/zipfile/__pycache__:
__init__.cpython-312.pyc  __main__.cpython-312.pyc

./Python-3.12.0/Lib/zoneinfo:
_common.py  __init__.py  __pycache__  _tzpath.py  _zoneinfo.py

./Python-3.12.0/Lib/zoneinfo/__pycache__:
_common.cpython-312.pyc  __init__.cpython-312.pyc  _tzpath.cpython-312.pyc

./Python-3.12.0/Mac:
BuildScript        Icons  Makefile.in     README.rst  Tools
Extras.install.py  IDLE   PythonLauncher  Resources

./Python-3.12.0/Mac/BuildScript:
build-installer.py  resources  seticon.m
README.rst          scripts    tk868_on_10_8_10_9.patch

./Python-3.12.0/Mac/BuildScript/resources:
background.jpg  install_certificates.command  ReadMe.rtf
Conclusion.rtf  License.rtf                   Welcome.rtf

./Python-3.12.0/Mac/BuildScript/scripts:
postflight.documentation  postflight.framework
postflight.ensurepip      postflight.patch-profile

./Python-3.12.0/Mac/Icons:
'Disk Image.icns'   PythonCompiled.icns   PythonLauncher.icns   ReadMe.txt
 IDLE.icns         'Python Folder.icns'   PythonSource.icns

./Python-3.12.0/Mac/IDLE:
IDLE.app

./Python-3.12.0/Mac/IDLE/IDLE.app:
Contents

./Python-3.12.0/Mac/IDLE/IDLE.app/Contents:
Info.plist  MacOS  PkgInfo  Resources

./Python-3.12.0/Mac/IDLE/IDLE.app/Contents/MacOS:
IDLE

./Python-3.12.0/Mac/IDLE/IDLE.app/Contents/Resources:
IDLE.icns  idlemain.py  PythonCompiled.icns  PythonSource.icns

./Python-3.12.0/Mac/PythonLauncher:
doscript.h             FileSettings.m   MyAppDelegate.m
doscript.m             Info.plist.in    MyDocument.h
English.lproj          main.m           MyDocument.m
factorySettings.plist  Makefile.in      PreferencesWindowController.h
FileSettings.h         MyAppDelegate.h  PreferencesWindowController.m

./Python-3.12.0/Mac/PythonLauncher/English.lproj:
Credits.rtf  MainMenu.nib  MyDocument.nib  PreferenceWindow.nib

./Python-3.12.0/Mac/PythonLauncher/English.lproj/MainMenu.nib:
classes.nib  info.nib  objects.nib

./Python-3.12.0/Mac/PythonLauncher/English.lproj/MyDocument.nib:
classes.nib  info.nib  objects.nib

./Python-3.12.0/Mac/PythonLauncher/English.lproj/PreferenceWindow.nib:
classes.nib  info.nib  objects.nib

./Python-3.12.0/Mac/Resources:
app  framework  iconsrc

./Python-3.12.0/Mac/Resources/app:
Info.plist.in  PkgInfo  Resources

./Python-3.12.0/Mac/Resources/app/Resources:
PythonApplet.icns  PythonInterpreter.icns

./Python-3.12.0/Mac/Resources/framework:
Info.plist.in

./Python-3.12.0/Mac/Resources/iconsrc:
IDE.psd             PythonCompiled.psd  PythonWSource.psd
PackageManager.psd  PythonIcon.psd
PythonApplet.psd    PythonSource.psd

./Python-3.12.0/Mac/Tools:
plistlib_generate_testdata.py  pythonw.c

./Python-3.12.0/Misc:
ACKS                 python-embed.pc     requirements-test.txt
coverity_model.c     python-embed.pc.in  rhel7
HISTORY              python.man          SpecialBuilds.txt
indent.pro           python.pc           stable_abi.toml
NEWS                 python.pc.in        svnmap.txt
Porting              README              valgrind-python.supp
python-config.in     README.AIX          vgrindefs
python-config.sh     README.coverity
python-config.sh.in  README.valgrind

./Python-3.12.0/Misc/rhel7:
openssl.pc  README.md  tcl.pc  tk.pc

./Python-3.12.0/Modules:
_abc.c
_abc.gcda
_abc.o
addrinfo.h
array.cpython-312-x86_64-linux-gnu.so
arraymodule.c
arraymodule.gcda
arraymodule.o
_asyncio.cpython-312-x86_64-linux-gnu.so
_asynciomodule.c
_asynciomodule.gcda
_asynciomodule.o
atexitmodule.c
atexitmodule.gcda
atexitmodule.o
audioop.c
audioop.cpython-312-x86_64-linux-gnu.so
audioop.gcda
audioop.o
binascii.c
binascii.cpython-312-x86_64-linux-gnu.so
binascii.gcda
binascii.o
_bisect.cpython-312-x86_64-linux-gnu.so
_bisectmodule.c
_bisectmodule.gcda
_bisectmodule.o
_blake2
_blake2.cpython-312-x86_64-linux-gnu.so
_bz2.cpython-312-x86_64-linux-gnu.so
_bz2module.c
_bz2module.gcda
_bz2module.o
cjkcodecs
clinic
cmath.cpython-312-x86_64-linux-gnu.so
cmathmodule.c
cmathmodule.gcda
cmathmodule.o
_codecs_cn.cpython-312-x86_64-linux-gnu.so
_codecs_hk.cpython-312-x86_64-linux-gnu.so
_codecs_iso2022.cpython-312-x86_64-linux-gnu.so
_codecs_jp.cpython-312-x86_64-linux-gnu.so
_codecs_kr.cpython-312-x86_64-linux-gnu.so
_codecsmodule.c
_codecsmodule.gcda
_codecsmodule.o
_codecs_tw.cpython-312-x86_64-linux-gnu.so
_collectionsmodule.c
_collectionsmodule.gcda
_collectionsmodule.o
config.c
config.c.in
config.o
_contextvars.cpython-312-x86_64-linux-gnu.so
_contextvarsmodule.c
_contextvarsmodule.gcda
_contextvarsmodule.o
_crypt.cpython-312-x86_64-linux-gnu.so
_cryptmodule.c
_cryptmodule.gcda
_cryptmodule.o
_csv.c
_csv.cpython-312-x86_64-linux-gnu.so
_csv.gcda
_csv.o
_ctypes
_ctypes.cpython-312-x86_64-linux-gnu.so
_ctypes_test.cpython-312-x86_64-linux-gnu.so
_curses.cpython-312-x86_64-linux-gnu.so
_cursesmodule.c
_cursesmodule.gcda
_cursesmodule.o
_curses_panel.c
_curses_panel.cpython-312-x86_64-linux-gnu.so
_curses_panel.gcda
_curses_panel.o
_datetime.cpython-312-x86_64-linux-gnu.so
_datetimemodule.c
_datetimemodule.gcda
_datetimemodule.o
_dbmmodule.c
_decimal
_decimal.cpython-312-x86_64-linux-gnu.so
_elementtree.c
_elementtree.cpython-312-x86_64-linux-gnu.so
_elementtree.gcda
_elementtree.o
errnomodule.c
errnomodule.gcda
errnomodule.o
expat
faulthandler.c
faulthandler.gcda
faulthandler.o
fcntl.cpython-312-x86_64-linux-gnu.so
fcntlmodule.c
fcntlmodule.gcda
fcntlmodule.o
_functoolsmodule.c
_functoolsmodule.gcda
_functoolsmodule.o
gcmodule.c
gcmodule.gcda
gcmodule.o
gc_weakref.txt
_gdbm.cpython-312-x86_64-linux-gnu.so
_gdbmmodule.c
_gdbmmodule.gcda
_gdbmmodule.o
getaddrinfo.c
getbuildinfo.c
getbuildinfo.gcda
getbuildinfo.o
getnameinfo.c
getpath.c
getpath.gcda
getpath_noop.c
getpath_noop.gcda
getpath_noop.o
getpath.o
getpath.py
grp.cpython-312-x86_64-linux-gnu.so
grpmodule.c
grpmodule.gcda
grpmodule.o
_hacl
_hashlib.cpython-312-x86_64-linux-gnu.so
hashlib.h
_hashopenssl.c
_hashopenssl.gcda
_hashopenssl.o
_heapq.cpython-312-x86_64-linux-gnu.so
_heapqmodule.c
_heapqmodule.gcda
_heapqmodule.o
_io
itertoolsmodule.c
itertoolsmodule.gcda
itertoolsmodule.o
_json.c
_json.cpython-312-x86_64-linux-gnu.so
_json.gcda
_json.o
ld_so_aix
ld_so_aix.in
_localemodule.c
_localemodule.gcda
_localemodule.o
_lsprof.c
_lsprof.cpython-312-x86_64-linux-gnu.so
_lsprof.gcda
_lsprof.o
_lzmamodule.c
main.c
main.gcda
main.o
makesetup
makexp_aix
math.cpython-312-x86_64-linux-gnu.so
_math.h
mathmodule.c
mathmodule.gcda
mathmodule.o
_md5.cpython-312-x86_64-linux-gnu.so
md5module.c
md5module.gcda
md5module.o
mmap.cpython-312-x86_64-linux-gnu.so
mmapmodule.c
mmapmodule.gcda
mmapmodule.o
_multibytecodec.cpython-312-x86_64-linux-gnu.so
_multiprocessing
_multiprocessing.cpython-312-x86_64-linux-gnu.so
nis.cpython-312-x86_64-linux-gnu.so
nismodule.c
nismodule.gcda
nismodule.o
_opcode.c
_opcode.cpython-312-x86_64-linux-gnu.so
_opcode.gcda
_opcode.o
_operator.c
_operator.gcda
_operator.o
ossaudiodev.c
ossaudiodev.cpython-312-x86_64-linux-gnu.so
ossaudiodev.gcda
ossaudiodev.o
overlapped.c
_pickle.c
_pickle.cpython-312-x86_64-linux-gnu.so
_pickle.gcda
_pickle.o
posixmodule.c
posixmodule.gcda
posixmodule.h
posixmodule.o
_posixshmem.cpython-312-x86_64-linux-gnu.so
_posixsubprocess.c
_posixsubprocess.cpython-312-x86_64-linux-gnu.so
_posixsubprocess.gcda
_posixsubprocess.o
pwdmodule.c
pwdmodule.gcda
pwdmodule.o
pyexpat.c
pyexpat.cpython-312-x86_64-linux-gnu.so
pyexpat.gcda
pyexpat.o
_queue.cpython-312-x86_64-linux-gnu.so
_queuemodule.c
_queuemodule.gcda
_queuemodule.o
_random.cpython-312-x86_64-linux-gnu.so
_randommodule.c
_randommodule.gcda
_randommodule.o
readline.c
readline.cpython-312-x86_64-linux-gnu.so
readline.gcda
readline.o
README
resource.c
resource.cpython-312-x86_64-linux-gnu.so
resource.gcda
resource.o
rotatingtree.c
rotatingtree.gcda
rotatingtree.h
rotatingtree.o
_scproxy.c
select.cpython-312-x86_64-linux-gnu.so
selectmodule.c
selectmodule.gcda
selectmodule.o
Setup
Setup.bootstrap
Setup.bootstrap.in
Setup.local
Setup.stdlib
Setup.stdlib.in
_sha1.cpython-312-x86_64-linux-gnu.so
sha1module.c
sha1module.gcda
sha1module.o
_sha2.cpython-312-x86_64-linux-gnu.so
sha2module.c
sha2module.gcda
sha2module.o
_sha3.cpython-312-x86_64-linux-gnu.so
sha3module.c
sha3module.gcda
sha3module.o
signalmodule.c
signalmodule.gcda
signalmodule.o
_socket.cpython-312-x86_64-linux-gnu.so
socketmodule.c
socketmodule.gcda
socketmodule.h
socketmodule.o
spwd.cpython-312-x86_64-linux-gnu.so
spwdmodule.c
spwdmodule.gcda
spwdmodule.o
_sqlite
_sqlite3.cpython-312-x86_64-linux-gnu.so
_sre
_ssl
_ssl.c
_ssl.cpython-312-x86_64-linux-gnu.so
_ssl_data_111.h
_ssl_data_300.h
_ssl_data_31.h
_ssl_data.h
_ssl.gcda
_ssl.h
_ssl.o
_stat.c
_stat.gcda
_statistics.cpython-312-x86_64-linux-gnu.so
_statisticsmodule.c
_statisticsmodule.gcda
_statisticsmodule.o
_stat.o
_struct.c
_struct.cpython-312-x86_64-linux-gnu.so
_struct.gcda
_struct.o
symtablemodule.c
symtablemodule.gcda
symtablemodule.o
syslog.cpython-312-x86_64-linux-gnu.so
syslogmodule.c
syslogmodule.gcda
syslogmodule.o
termios.c
termios.cpython-312-x86_64-linux-gnu.so
termios.gcda
termios.o
_testbuffer.c
_testbuffer.cpython-312-x86_64-linux-gnu.so
_testbuffer.gcda
_testbuffer.o
_testcapi
_testcapi.cpython-312-x86_64-linux-gnu.so
_testcapi_feature_macros.inc
_testcapimodule.c
_testcapimodule.gcda
_testcapimodule.o
_testclinic.c
_testclinic.cpython-312-x86_64-linux-gnu.so
_testclinic.gcda
_testclinic.o
_testimportmultiple.c
_testimportmultiple.cpython-312-x86_64-linux-gnu.so
_testimportmultiple.gcda
_testimportmultiple.o
_testinternalcapi.c
_testinternalcapi.cpython-312-x86_64-linux-gnu.so
_testinternalcapi.gcda
_testinternalcapi.o
_testmultiphase.c
_testmultiphase.cpython-312-x86_64-linux-gnu.so
_testmultiphase.gcda
_testmultiphase.o
_testsinglephase.c
_testsinglephase.cpython-312-x86_64-linux-gnu.so
_testsinglephase.gcda
_testsinglephase.o
_threadmodule.c
_threadmodule.gcda
_threadmodule.o
timemodule.c
timemodule.gcda
timemodule.o
tkappinit.c
_tkinter.c
tkinter.h
_tracemalloc.c
_tracemalloc.gcda
_tracemalloc.o
_typingmodule.c
_typingmodule.gcda
_typingmodule.o
unicodedata.c
unicodedata.cpython-312-x86_64-linux-gnu.so
unicodedata_db.h
unicodedata.gcda
unicodedata.o
unicodename_db.h
_uuidmodule.c
_weakref.c
_weakref.gcda
_weakref.o
_winapi.c
winreparse.h
_xxinterpchannels.cpython-312-x86_64-linux-gnu.so
_xxinterpchannelsmodule.c
_xxinterpchannelsmodule.gcda
_xxinterpchannelsmodule.o
xxlimited_35.c
xxlimited_35.cpython-312-x86_64-linux-gnu.so
xxlimited_35.gcda
xxlimited_35.o
xxlimited.c
xxlimited.cpython-312-x86_64-linux-gnu.so
xxlimited.gcda
xxlimited.o
xxmodule.c
_xxsubinterpreters.cpython-312-x86_64-linux-gnu.so
_xxsubinterpretersmodule.c
_xxsubinterpretersmodule.gcda
_xxsubinterpretersmodule.o
xxsubtype.c
xxsubtype.cpython-312-x86_64-linux-gnu.so
xxsubtype.gcda
xxsubtype.o
_xxtestfuzz
_xxtestfuzz.cpython-312-x86_64-linux-gnu.so
zlib.cpython-312-x86_64-linux-gnu.so
zlibmodule.c
zlibmodule.gcda
zlibmodule.o
_zoneinfo.c
_zoneinfo.cpython-312-x86_64-linux-gnu.so
_zoneinfo.gcda
_zoneinfo.o

./Python-3.12.0/Modules/_blake2:
blake2b2s.py       blake2module.c     blake2s_impl.c     impl
blake2b_impl.c     blake2module.gcda  blake2s_impl.gcda
blake2b_impl.gcda  blake2module.h     blake2s_impl.o
blake2b_impl.o     blake2module.o     clinic

./Python-3.12.0/Modules/_blake2/clinic:
blake2b_impl.c.h  blake2s_impl.c.h

./Python-3.12.0/Modules/_blake2/impl:
blake2b.c             blake2-config.h      blake2s-load-sse41.h
blake2b-load-sse2.h   blake2.h             blake2s-load-xop.h
blake2b-load-sse41.h  blake2-impl.h        blake2s-ref.c
blake2b-ref.c         blake2s.c            blake2s-round.h
blake2b-round.h       blake2s-load-sse2.h

./Python-3.12.0/Modules/cjkcodecs:
alg_jisx0201.h        _codecs_iso2022.o    mappings_cn.h
cjkcodecs.h           _codecs_jp.c         mappings_hk.h
clinic                _codecs_jp.gcda      mappings_jisx0213_pair.h
_codecs_cn.c          _codecs_jp.o         mappings_jp.h
_codecs_cn.gcda       _codecs_kr.c         mappings_kr.h
_codecs_cn.o          _codecs_kr.gcda      mappings_tw.h
_codecs_hk.c          _codecs_kr.o         multibytecodec.c
_codecs_hk.gcda       _codecs_tw.c         multibytecodec.gcda
_codecs_hk.o          _codecs_tw.gcda      multibytecodec.h
_codecs_iso2022.c     _codecs_tw.o         multibytecodec.o
_codecs_iso2022.gcda  emu_jisx0213_2000.h  README

./Python-3.12.0/Modules/cjkcodecs/clinic:
multibytecodec.c.h

./Python-3.12.0/Modules/clinic:
_abc.c.h                _hashopenssl.c.h      sha3module.c.h
arraymodule.c.h         _heapqmodule.c.h      signalmodule.c.h
_asynciomodule.c.h      itertoolsmodule.c.h   socketmodule.c.h
audioop.c.h             _localemodule.c.h     spwdmodule.c.h
binascii.c.h            _lsprof.c.h           _ssl.c.h
_bisectmodule.c.h       _lzmamodule.c.h       _statisticsmodule.c.h
_bz2module.c.h          mathmodule.c.h        _struct.c.h
cmathmodule.c.h         md5module.c.h         symtablemodule.c.h
_codecsmodule.c.h       _opcode.c.h           syslogmodule.c.h
_collectionsmodule.c.h  _operator.c.h         termios.c.h
_contextvarsmodule.c.h  overlapped.c.h        _testclinic.c.h
_cryptmodule.c.h        _pickle.c.h           _testinternalcapi.c.h
_csv.c.h                posixmodule.c.h       _testmultiphase.c.h
_cursesmodule.c.h       _posixsubprocess.c.h  _tkinter.c.h
_curses_panel.c.h       pwdmodule.c.h         _tracemalloc.c.h
_datetimemodule.c.h     pyexpat.c.h           _typingmodule.c.h
_dbmmodule.c.h          _queuemodule.c.h      unicodedata.c.h
_elementtree.c.h        _randommodule.c.h     _weakref.c.h
fcntlmodule.c.h         readline.c.h          _winapi.c.h
_functoolsmodule.c.h    resource.c.h          zlibmodule.c.h
gcmodule.c.h            selectmodule.c.h      _zoneinfo.c.h
_gdbmmodule.c.h         sha1module.c.h
grpmodule.c.h           sha2module.c.h

./Python-3.12.0/Modules/_ctypes:
callbacks.c     cfield.c      _ctypes.o          stgdict.c
callbacks.gcda  cfield.gcda   _ctypes_test.c     stgdict.gcda
callbacks.o     cfield.o      _ctypes_test.gcda  stgdict.o
callproc.c      _ctypes.c     _ctypes_test.h
callproc.gcda   _ctypes.gcda  _ctypes_test.o
callproc.o      ctypes.h      malloc_closure.c

./Python-3.12.0/Modules/_decimal:
_decimal.c     _decimal.o    libmpdec    tests
_decimal.gcda  docstrings.h  README.txt

./Python-3.12.0/Modules/_decimal/libmpdec:
basearith.c     crt.c           io.c               numbertheory.h
basearith.gcda  crt.gcda        io.gcda            numbertheory.o
basearith.h     crt.h           io.h               README.txt
basearith.o     crt.o           io.o               sixstep.c
bench.c         difradix2.c     libmpdec.a         sixstep.gcda
bench_full.c    difradix2.gcda  literature         sixstep.h
bits.h          difradix2.h     mpalloc.c          sixstep.o
constants.c     difradix2.o     mpalloc.gcda       transpose.c
constants.h     examples        mpalloc.h          transpose.gcda
constants.o     fnt.c           mpalloc.o          transpose.h
context.c       fnt.gcda        mpdecimal.c        transpose.o
context.gcda    fnt.h           mpdecimal.gcda     typearith.h
context.o       fnt.o           mpdecimal.h        umodarith.h
convolute.c     fourstep.c      mpdecimal.o        vcdiv64.asm
convolute.gcda  fourstep.gcda   mpsignal.c
convolute.h     fourstep.h      numbertheory.c
convolute.o     fourstep.o      numbertheory.gcda

./Python-3.12.0/Modules/_decimal/libmpdec/examples:
compare.c  divmod.c    pow.c     README.txt  sqrt.c
div.c      multiply.c  powmod.c  shift.c

./Python-3.12.0/Modules/_decimal/libmpdec/literature:
bignum.txt  matrix-transform.txt  mulmod-ppro.txt  six-step.txt
fnt.py      mulmod-64.txt         REFERENCES.txt   umodarith.lisp

./Python-3.12.0/Modules/_decimal/tests:
bench.py     formathelper.py  README.txt
bignum.py    randdec.py       runall.bat
deccheck.py  randfloat.py     runall-memorydebugger.sh

./Python-3.12.0/Modules/expat:
ascii.h           iasciitab.h  siphash.h      xmlrole.c     xmltok.h
asciitab.h        internal.h   utf8tab.h      xmlrole.gcda  xmltok_impl.c
COPYING           latin1tab.h  winconfig.h    xmlrole.h     xmltok_impl.h
expat_config.h    libexpat.a   xmlparse.c     xmlrole.o     xmltok_ns.c
expat_external.h  nametab.h    xmlparse.gcda  xmltok.c      xmltok.o
expat.h           pyexpatns.h  xmlparse.o     xmltok.gcda

./Python-3.12.0/Modules/_hacl:
Hacl_Hash_MD5.c      Hacl_Hash_SHA2.c     Hacl_Streaming_Types.h
Hacl_Hash_MD5.gcda   Hacl_Hash_SHA2.gcda  include
Hacl_Hash_MD5.h      Hacl_Hash_SHA2.h     internal
Hacl_Hash_MD5.o      Hacl_Hash_SHA2.o     libHacl_Hash_SHA2.a
Hacl_Hash_SHA1.c     Hacl_Hash_SHA3.c     python_hacl_namespaces.h
Hacl_Hash_SHA1.gcda  Hacl_Hash_SHA3.gcda  README.md
Hacl_Hash_SHA1.h     Hacl_Hash_SHA3.h     refresh.sh
Hacl_Hash_SHA1.o     Hacl_Hash_SHA3.o

./Python-3.12.0/Modules/_hacl/include:
krml

./Python-3.12.0/Modules/_hacl/include/krml:
fstar_uint128_struct_endianness.h  internal
FStar_UInt128_Verified.h           lowstar_endianness.h
FStar_UInt_8_16_32_64.h            types.h

./Python-3.12.0/Modules/_hacl/include/krml/internal:
target.h

./Python-3.12.0/Modules/_hacl/internal:
Hacl_Hash_MD5.h  Hacl_Hash_SHA1.h  Hacl_Hash_SHA2.h  Hacl_Hash_SHA3.h

./Python-3.12.0/Modules/_io:
bufferedio.c     clinic       iobase.o        stringio.gcda
bufferedio.gcda  fileio.c     _iomodule.c     stringio.o
bufferedio.o     fileio.gcda  _iomodule.gcda  textio.c
bytesio.c        fileio.o     _iomodule.h     textio.gcda
bytesio.gcda     iobase.c     _iomodule.o     textio.o
bytesio.o        iobase.gcda  stringio.c      winconsoleio.c

./Python-3.12.0/Modules/_io/clinic:
bufferedio.c.h  fileio.c.h  _iomodule.c.h  textio.c.h
bytesio.c.h     iobase.c.h  stringio.c.h   winconsoleio.c.h

./Python-3.12.0/Modules/_multiprocessing:
clinic                multiprocessing.h  posixshmem.gcda  semaphore.gcda
multiprocessing.c     multiprocessing.o  posixshmem.o     semaphore.o
multiprocessing.gcda  posixshmem.c       semaphore.c

./Python-3.12.0/Modules/_multiprocessing/clinic:
multiprocessing.c.h  posixshmem.c.h  semaphore.c.h

./Python-3.12.0/Modules/_sqlite:
blob.c           microprotocols.c       row.gcda
blob.gcda        microprotocols.gcda    row.h
blob.h           microprotocols.h       row.o
blob.o           microprotocols.o       statement.c
clinic           module.c               statement.gcda
connection.c     module.gcda            statement.h
connection.gcda  module.h               statement.o
connection.h     module.o               util.c
connection.o     prepare_protocol.c     util.gcda
cursor.c         prepare_protocol.gcda  util.h
cursor.gcda      prepare_protocol.h     util.o
cursor.h         prepare_protocol.o
cursor.o         row.c

./Python-3.12.0/Modules/_sqlite/clinic:
blob.c.h  connection.c.h  cursor.c.h  module.c.h  row.c.h

./Python-3.12.0/Modules/_sre:
clinic  sre_constants.h  sre.h      sre.o
sre.c   sre.gcda         sre_lib.h  sre_targets.h

./Python-3.12.0/Modules/_sre/clinic:
sre.c.h

./Python-3.12.0/Modules/_ssl:
cert.c  clinic  debughelpers.c  misc.c

./Python-3.12.0/Modules/_ssl/clinic:
cert.c.h

./Python-3.12.0/Modules/_testcapi:
abstract.c       float.o                 pyos.gcda
abstract.gcda    gc.c                    pyos.o
abstract.o       gc.gcda                 pytime.c
buffer.c         gc.o                    pytime.gcda
buffer.gcda      getargs.c               pytime.o
buffer.o         getargs.gcda            README.txt
clinic           getargs.o               structmember.c
code.c           heaptype.c              structmember.gcda
code.gcda        heaptype.gcda           structmember.o
code.o           heaptype.o              testcapi_long.h
datetime.c       heaptype_relative.c     unicode.c
datetime.gcda    heaptype_relative.gcda  unicode.gcda
datetime.o       heaptype_relative.o     unicode.o
dict.c           immortal.c              util.h
dict.gcda        immortal.gcda           vectorcall.c
dict.o           immortal.o              vectorcall.gcda
docstring.c      long.c                  vectorcall_limited.c
docstring.gcda   long.gcda               vectorcall_limited.gcda
docstring.o      long.o                  vectorcall_limited.o
exceptions.c     mem.c                   vectorcall.o
exceptions.gcda  mem.gcda                watchers.c
exceptions.o     mem.o                   watchers.gcda
float.c          parts.h                 watchers.o
float.gcda       pyos.c

./Python-3.12.0/Modules/_testcapi/clinic:
exceptions.c.h  float.c.h  vectorcall.c.h  watchers.c.h

./Python-3.12.0/Modules/_xxtestfuzz:
dictionaries            fuzz_json_loads_corpus     _xxtestfuzz.c
fuzz_csv_reader_corpus  fuzz_sre_compile_corpus    _xxtestfuzz.gcda
fuzzer.c                fuzz_struct_unpack_corpus  _xxtestfuzz.o
fuzzer.gcda             fuzz_tests.txt
fuzzer.o                README.rst

./Python-3.12.0/Modules/_xxtestfuzz/dictionaries:
fuzz_json_loads.dict  fuzz_sre_compile.dict

./Python-3.12.0/Modules/_xxtestfuzz/fuzz_csv_reader_corpus:
test.csv

./Python-3.12.0/Modules/_xxtestfuzz/fuzz_json_loads_corpus:
empty_array.json   pass1.json  pass3.json
empty_object.json  pass2.json  simple_array.json

./Python-3.12.0/Modules/_xxtestfuzz/fuzz_sre_compile_corpus:
anchor_links  characters  isbn  phone_number

./Python-3.12.0/Modules/_xxtestfuzz/fuzz_struct_unpack_corpus:
hello_string  long_zero  varied_format_string

./Python-3.12.0/Objects:
abstract.c                    listobject.o
abstract.gcda                 listsort.txt
abstract.o                    lnotab_notes.txt
boolobject.c                  locations.md
boolobject.gcda               longobject.c
boolobject.o                  longobject.gcda
bytearrayobject.c             longobject.o
bytearrayobject.gcda          memoryobject.c
bytearrayobject.o             memoryobject.gcda
bytes_methods.c               memoryobject.o
bytes_methods.gcda            methodobject.c
bytes_methods.o               methodobject.gcda
bytesobject.c                 methodobject.o
bytesobject.gcda              moduleobject.c
bytesobject.o                 moduleobject.gcda
call.c                        moduleobject.o
call.gcda                     namespaceobject.c
call.o                        namespaceobject.gcda
capsule.c                     namespaceobject.o
capsule.gcda                  object.c
capsule.o                     object.gcda
cellobject.c                  object_layout_312.gv
cellobject.gcda               object_layout_312.png
cellobject.o                  object_layout_full_312.gv
classobject.c                 object_layout_full_312.png
classobject.gcda              object_layout.md
classobject.o                 object.o
clinic                        obmalloc.c
codeobject.c                  obmalloc.gcda
codeobject.gcda               obmalloc.o
codeobject.o                  odictobject.c
complexobject.c               odictobject.gcda
complexobject.gcda            odictobject.o
complexobject.o               picklebufobject.c
descrobject.c                 picklebufobject.gcda
descrobject.gcda              picklebufobject.o
descrobject.o                 rangeobject.c
dictnotes.txt                 rangeobject.gcda
dictobject.c                  rangeobject.o
dictobject.gcda               README
dictobject.o                  setobject.c
enumobject.c                  setobject.gcda
enumobject.gcda               setobject.o
enumobject.o                  sliceobject.c
exception_handling_notes.txt  sliceobject.gcda
exceptions.c                  sliceobject.o
exceptions.gcda               stringlib
exceptions.o                  structseq.c
fileobject.c                  structseq.gcda
fileobject.gcda               structseq.o
fileobject.o                  tupleobject.c
floatobject.c                 tupleobject.gcda
floatobject.gcda              tupleobject.o
floatobject.o                 typeobject.c
frame_layout.md               typeobject.gcda
frameobject.c                 typeobject.o
frameobject.gcda              typeslots.inc
frameobject.o                 typeslots.py
funcobject.c                  typevarobject.c
funcobject.gcda               typevarobject.gcda
funcobject.o                  typevarobject.o
genericaliasobject.c          unicodectype.c
genericaliasobject.gcda       unicodectype.gcda
genericaliasobject.o          unicodectype.o
genobject.c                   unicodeobject.c
genobject.gcda                unicodeobject.gcda
genobject.o                   unicodeobject.o
interpreteridobject.c         unicodetype_db.h
interpreteridobject.gcda      unionobject.c
interpreteridobject.o         unionobject.gcda
iterobject.c                  unionobject.o
iterobject.gcda               weakrefobject.c
iterobject.o                  weakrefobject.gcda
listobject.c                  weakrefobject.o
listobject.gcda

./Python-3.12.0/Objects/clinic:
bytearrayobject.c.h  descrobject.c.h  listobject.c.h    structseq.c.h
bytesobject.c.h      dictobject.c.h   longobject.c.h    tupleobject.c.h
classobject.c.h      enumobject.c.h   memoryobject.c.h  typeobject.c.h
codeobject.c.h       floatobject.c.h  moduleobject.c.h  typevarobject.c.h
complexobject.c.h    funcobject.c.h   odictobject.c.h   unicodeobject.c.h

./Python-3.12.0/Objects/stringlib:
asciilib.h    find_max_char.h  stringlib_find_two_way_notes.txt
clinic        join.h           transmogrify.h
codecs.h      localeutil.h     ucs1lib.h
count.h       partition.h      ucs2lib.h
ctype.h       README.txt       ucs4lib.h
eq.h          replace.h        undef.h
fastsearch.h  split.h          unicode_format.h
find.h        stringdefs.h

./Python-3.12.0/Objects/stringlib/clinic:
transmogrify.h.h

./Python-3.12.0/Parser:
action_helpers.c     parser.gcda        pegen.gcda          token.gcda
action_helpers.gcda  parser.o           pegen.h             tokenizer.c
action_helpers.o     peg_api.c          pegen.o             tokenizer.gcda
asdl_c.py            peg_api.gcda       Python.asdl         tokenizer.h
asdl.py              peg_api.o          string_parser.c     tokenizer.o
myreadline.c         pegen.c            string_parser.gcda  token.o
myreadline.gcda      pegen_errors.c     string_parser.h
myreadline.o         pegen_errors.gcda  string_parser.o
parser.c             pegen_errors.o     token.c

./Python-3.12.0/PC:
classicAppCompat.can.xml     launcher.c          python_nt.rc
classicAppCompat.cat         launcher-usage.txt  python_uwp.cpp
classicAppCompat.sccd        layout              python_ver_rc.h
clinic                       _msi.c              pythonw_exe.rc
config.c                     msvcrtmodule.c      readme.txt
config_minimal.c             pyconfig.h          sqlite3.rc
crtlicense.txt               pylauncher.rc       store_info.txt
dl_nt.c                      pyshellext.cpp      _testconsole.c
errmap.h                     pyshellext.def      validate_ucrtbase.py
frozen_dllmain.c             pyshellext.rc       WinMain.c
icons                        python3dll.c        winreg.c
invalid_parameter_handler.c  python_exe.rc       winsound.c
launcher2.c                  python.manifest     _wmimodule.cpp

./Python-3.12.0/PC/clinic:
_msi.c.h          _testconsole.c.h  winsound.c.h
msvcrtmodule.c.h  winreg.c.h        _wmimodule.cpp.h

./Python-3.12.0/PC/icons:
idlex150.png   pyc.icns  py.ico        pythonw.ico      setup.icns
idlex44.png    pyc.ico   py.png        pythonw.svg      setup.ico
launcher.icns  pyc.svg   py.svg        pythonwx150.png  setup.svg
launcher.ico   pyd.icns  python.icns   pythonwx44.png
launcher.svg   pyd.ico   python.ico    pythonx150.png
logo.svg       pyd.svg   python.svg    pythonx44.png
logox128.png   py.icns   pythonw.icns  pythonx50.png

./Python-3.12.0/PC/layout:
__init__.py  __main__.py  main.py  support

./Python-3.12.0/PC/layout/support:
appxmanifest.py  filesets.py  nuspec.py   props.py
catalog.py       __init__.py  options.py  python.props
constants.py     logging.py   pip.py

./Python-3.12.0/PCbuild:
_asyncio.vcxproj                  pythonw_uwp.vcxproj
_asyncio.vcxproj.filters          pythonw_uwp.vcxproj.filters
blurb.bat                         pythonw.vcxproj
build.bat                         pythonw.vcxproj.filters
build_env.bat                     pywlauncher.vcxproj
_bz2.vcxproj                      pywlauncher.vcxproj.filters
_bz2.vcxproj.filters              _queue.vcxproj
clean.bat                         _queue.vcxproj.filters
_ctypes_test.vcxproj              readme.txt
_ctypes_test.vcxproj.filters      regen.targets
_ctypes.vcxproj                   rmpyc.py
_ctypes.vcxproj.filters           rt.bat
_decimal.vcxproj                  select.vcxproj
_decimal.vcxproj.filters          select.vcxproj.filters
Directory.Build.props             _socket.vcxproj
Directory.Build.targets           _socket.vcxproj.filters
_elementtree.vcxproj              _sqlite3.vcxproj
_elementtree.vcxproj.filters      sqlite3.vcxproj
env.bat                           _sqlite3.vcxproj.filters
env.ps1                           sqlite3.vcxproj.filters
field3.py                         _ssl.vcxproj
find_msbuild.bat                  _ssl.vcxproj.filters
find_python.bat                   tcltk.props
fix_encoding.py                   tcl.vcxproj
_freeze_module.vcxproj            _testbuffer.vcxproj
_freeze_module.vcxproj.filters    _testbuffer.vcxproj.filters
get_external.py                   _testcapi.vcxproj
get_externals.bat                 _testcapi.vcxproj.filters
_hashlib.vcxproj                  _testclinic.vcxproj
_hashlib.vcxproj.filters          _testclinic.vcxproj.filters
idle.bat                          _testconsole.vcxproj
libffi.props                      _testconsole.vcxproj.filters
liblzma.vcxproj                   _testembed.vcxproj
liblzma.vcxproj.filters           _testembed.vcxproj.filters
_lzma.vcxproj                     _testimportmultiple.vcxproj
_lzma.vcxproj.filters             _testimportmultiple.vcxproj.filters
_msi.vcxproj                      _testinternalcapi.vcxproj
_msi.vcxproj.filters              _testinternalcapi.vcxproj.filters
_multiprocessing.vcxproj          _testmultiphase.vcxproj
_multiprocessing.vcxproj.filters  _testmultiphase.vcxproj.filters
openssl.props                     _testsinglephase.vcxproj
openssl.vcxproj                   _testsinglephase.vcxproj.filters
_overlapped.vcxproj               tix.vcxproj
_overlapped.vcxproj.filters       _tkinter.vcxproj
pcbuild.proj                      _tkinter.vcxproj.filters
pcbuild.sln                       tk.vcxproj
prepare_libffi.bat                unicodedata.vcxproj
prepare_ssl.bat                   unicodedata.vcxproj.filters
prepare_ssl.py                    urlretrieve.py
prepare_tcltk.bat                 _uuid.vcxproj
pyexpat.vcxproj                   _uuid.vcxproj.filters
pyexpat.vcxproj.filters           venvlauncher.vcxproj
pylauncher.vcxproj                venvlauncher.vcxproj.filters
pylauncher.vcxproj.filters        venvwlauncher.vcxproj
pyproject.props                   venvwlauncher.vcxproj.filters
pyshellext.vcxproj                winsound.vcxproj
pyshellext.vcxproj.filters        winsound.vcxproj.filters
python3dll.vcxproj                _wmi.vcxproj
python3dll.vcxproj.filters        _wmi.vcxproj.filters
pythoncore.vcxproj                xxlimited_35.vcxproj
pythoncore.vcxproj.filters        xxlimited_35.vcxproj.filters
python.props                      xxlimited.vcxproj
python_uwp.vcxproj                xxlimited.vcxproj.filters
python_uwp.vcxproj.filters        _zoneinfo.vcxproj
python.vcxproj                    _zoneinfo.vcxproj.filters
python.vcxproj.filters

./Python-3.12.0/Programs:
_bootstrap_python.c     _freeze_module.py          _testembed.c
_bootstrap_python.gcda  freeze_test_frozenmain.py  _testembed.gcda
_bootstrap_python.o     python.c                   _testembed.o
_freeze_module          python.gcda                test_frozenmain.h
_freeze_module.c        python.o                   test_frozenmain.py
_freeze_module.gcda     README
_freeze_module.o        _testembed

./Python-3.12.0/Python:
adaptive.md             frozenmain.gcda       preconfig.o
asdl.c                  frozenmain.o          pyarena.c
asdl.gcda               frozen_modules        pyarena.gcda
asdl.o                  frozen.o              pyarena.o
asm_trampoline.o        future.c              pyctype.c
asm_trampoline.S        future.gcda           pyctype.o
assemble.c              future.o              pyfpe.c
assemble.gcda           generated_cases.c.h   pyfpe.gcda
assemble.o              getargs.c             pyfpe.o
ast.c                   getargs.gcda          pyhash.c
ast.gcda                getargs.o             pyhash.gcda
ast.o                   getcompiler.c         pyhash.o
ast_opt.c               getcompiler.gcda      pylifecycle.c
ast_opt.gcda            getcompiler.o         pylifecycle.gcda
ast_opt.o               getcopyright.c        pylifecycle.o
ast_unparse.c           getcopyright.gcda     pymath.c
ast_unparse.gcda        getcopyright.o        pymath.gcda
ast_unparse.o           getopt.c              pymath.o
bltinmodule.c           getopt.gcda           pystate.c
bltinmodule.gcda        getopt.o              pystate.gcda
bltinmodule.o           getplatform.c         pystate.o
bootstrap_hash.c        getplatform.gcda      pystrcmp.c
bootstrap_hash.gcda     getplatform.o         pystrcmp.gcda
bootstrap_hash.o        getversion.c          pystrcmp.o
bytecodes.c             getversion.gcda       pystrhex.c
ceval.c                 getversion.o          pystrhex.gcda
ceval.gcda              hamt.c                pystrhex.o
ceval_gil.c             hamt.gcda             pystrtod.c
ceval_gil.gcda          hamt.o                pystrtod.gcda
ceval_gil.o             hashtable.c           pystrtod.o
ceval_macros.h          hashtable.gcda        Python-ast.c
ceval.o                 hashtable.o           Python-ast.gcda
clinic                  import.c              Python-ast.o
codecs.c                importdl.c            pythonrun.c
codecs.gcda             importdl.gcda         pythonrun.gcda
codecs.o                importdl.h            pythonrun.o
compile.c               importdl.o            Python-tokenize.c
compile.gcda            import.gcda           Python-tokenize.gcda
compile.o               import.o              Python-tokenize.o
condvar.h               initconfig.c          pytime.c
context.c               initconfig.gcda       pytime.gcda
context.gcda            initconfig.o          pytime.o
context.o               instrumentation.c     README
deepfreeze              instrumentation.gcda  specialize.c
dtoa.c                  instrumentation.o     specialize.gcda
dtoa.gcda               intrinsics.c          specialize.o
dtoa.o                  intrinsics.gcda       stdlib_module_names.h
dup2.c                  intrinsics.o          structmember.c
dynamic_annotations.c   legacy_tracing.c      structmember.gcda
dynamic_annotations.o   legacy_tracing.gcda   structmember.o
dynload_hpux.c          legacy_tracing.o      suggestions.c
dynload_shlib.c         makeopcodetargets.py  suggestions.gcda
dynload_shlib.gcda      marshal.c             suggestions.o
dynload_shlib.o         marshal.gcda          symtable.c
dynload_stub.c          marshal.o             symtable.gcda
dynload_win.c           modsupport.c          symtable.o
emscripten_signal.c     modsupport.gcda       sysmodule.c
errors.c                modsupport.o          sysmodule.gcda
errors.gcda             mysnprintf.c          sysmodule.o
errors.o                mysnprintf.gcda       thread.c
fileutils.c             mysnprintf.o          thread.gcda
fileutils.gcda          mystrtoul.c           thread_nt.h
fileutils.o             mystrtoul.gcda        thread.o
flowgraph.c             mystrtoul.o           thread_pthread.h
flowgraph.gcda          opcode_metadata.h     thread_pthread_stubs.h
flowgraph.o             opcode_targets.h      traceback.c
formatter_unicode.c     pathconfig.c          traceback.gcda
formatter_unicode.gcda  pathconfig.gcda       traceback.o
formatter_unicode.o     pathconfig.o          tracemalloc.c
frame.c                 perf_trampoline.c     tracemalloc.gcda
frame.gcda              perf_trampoline.gcda  tracemalloc.o
frame.o                 perf_trampoline.o     _warnings.c
frozen.c                preconfig.c           _warnings.gcda
frozenmain.c            preconfig.gcda        _warnings.o

./Python-3.12.0/Python/clinic:
bltinmodule.c.h  instrumentation.c.h  sysmodule.c.h
context.c.h      marshal.c.h          traceback.c.h
import.c.h       Python-tokenize.c.h  _warnings.c.h

./Python-3.12.0/Python/deepfreeze:
deepfreeze.c  deepfreeze.gcda  deepfreeze.o  README.txt

./Python-3.12.0/Python/frozen_modules:
abc.h                            importlib.machinery.h  posixpath.h
codecs.h                         importlib.util.h       README.txt
_collections_abc.h               io.h                   runpy.h
frozen_only.h                    ntpath.h               _sitebuiltins.h
genericpath.h                    os.h                   site.h
getpath.h                        __phello__.h           stat.h
__hello__.h                      __phello__.ham.eggs.h  zipimport.h
importlib._bootstrap_external.h  __phello__.ham.h
importlib._bootstrap.h           __phello__.spam.h

./Python-3.12.0/Tools:
build            freeze       nuget                        ssl
buildbot         gdb          patchcheck                   stringbench
c-analyzer       i18n         peg_generator                tz
cases_generator  importbench  README                       unicode
ccbench          iobench      requirements-hypothesis.txt  unittestgui
clinic           msi          scripts                      wasm

./Python-3.12.0/Tools/build:
check_extension_modules.py        generate_token.py
deepfreeze.py                     parse_html5_entities.py
freeze_modules.py                 __pycache__
generate_global_objects.py        smelly.py
generate_levenshtein_examples.py  stable_abi.py
generate_opcode_h.py              umarshal.py
generate_re_casefix.py            update_file.py
generate_sre_constants.py         verify_ensurepip_wheels.py
generate_stdlib_module_names.py

./Python-3.12.0/Tools/build/__pycache__:
generate_global_objects.cpython-312.pyc  umarshal.cpython-312.pyc

./Python-3.12.0/Tools/buildbot:
build.bat     clean.bat         remotePythonInfo.bat
buildmsi.bat  remoteDeploy.bat  test.bat

./Python-3.12.0/Tools/c-analyzer:
c_analyzer     check-c-globals.py  distutils        table-file.py
c-analyzer.py  c_parser            must-resolve.sh  TODO
c_common       cpython             README

./Python-3.12.0/Tools/c-analyzer/c_analyzer:
analyze.py  datafiles.py  info.py  __init__.py  __main__.py  match.py

./Python-3.12.0/Tools/c-analyzer/c_common:
clsutil.py  __init__.py  logging.py  scriptutil.py  tables.py
fsutil.py   iterutil.py  misc.py     strutil.py

./Python-3.12.0/Tools/c-analyzer/c_parser:
datafiles.py  __init__.py  match.py  preprocessor
info.py       __main__.py  parser    source.py

./Python-3.12.0/Tools/c-analyzer/c_parser/parser:
_common.py              _func_body.py  _info.py     _regexes.py
_compound_decl_body.py  _global.py     __init__.py

./Python-3.12.0/Tools/c-analyzer/c_parser/preprocessor:
common.py  errors.py  gcc.py  __init__.py  __main__.py  pure.py

./Python-3.12.0/Tools/c-analyzer/cpython:
_analyzer.py       _capi.py   globals-to-fix.tsv  __init__.py  __main__.py
_builtin_types.py  _files.py  ignored.tsv         known.tsv    _parser.py

./Python-3.12.0/Tools/c-analyzer/distutils:
bcppcompiler.py     dep_util.py  msvc9compiler.py  spawn.py
ccompiler.py        errors.py    _msvccompiler.py  unixccompiler.py
cygwinccompiler.py  __init__.py  msvccompiler.py   util.py
debug.py            log.py       README

./Python-3.12.0/Tools/cases_generator:
generate_cases.py          lexer.py   plexer.py  test_generator.py
interpreter_definition.md  parser.py  README.md

./Python-3.12.0/Tools/ccbench:
ccbench.py

./Python-3.12.0/Tools/clinic:
clinic.py  cpp.py  mypy.ini  requirements-dev.txt

./Python-3.12.0/Tools/freeze:
bkfile.py                 hello.py         regen_frozen.py
checkextensions.py        makeconfig.py    test
checkextensions_win32.py  makefreeze.py    win32.html
extensions_win32.ini      makemakefile.py  winmakemakefile.py
flag.py                   parsesetup.py
freeze.py                 README

./Python-3.12.0/Tools/freeze/test:
freeze.py  Makefile  ok.py

./Python-3.12.0/Tools/gdb:
libpython.py

./Python-3.12.0/Tools/i18n:
makelocalealias.py  msgfmt.py  pygettext.py

./Python-3.12.0/Tools/importbench:
importbench.py  README

./Python-3.12.0/Tools/iobench:
iobench.py

./Python-3.12.0/Tools/msi:
appendpath                 get_externals.bat  sdktools.psm1
build.bat                  launcher           sign_build.ps1
buildrelease.bat           lib                tcltk
bundle                     make_appx.ps1      test
common_en-US.wxl_template  make_cat.ps1       testrelease.bat
common.wxs                 make_zip.proj      ucrt
core                       msi.props          uploadrelease.bat
csv_to_wxs.py              msi.targets        uploadrelease.proj
dev                        path               uploadrelease.ps1
doc                        pip                wix.props
exe                        purge.py
generate_md5.py            README.txt

./Python-3.12.0/Tools/msi/appendpath:
appendpath_en-US.wxl  appendpath.wixproj  appendpath.wxs

./Python-3.12.0/Tools/msi/bundle:
bootstrap       Default.ARM64.xsl  packagegroups         snapshot.wixproj
bundle.targets  Default.thm        releaselocal.wixproj
bundle.wxl      Default.wxl        releaseweb.wixproj
bundle.wxs      full.wixproj       SideBar.png

./Python-3.12.0/Tools/msi/bundle/bootstrap:
LICENSE.txt  pythonba.cpp  pythonba.vcxproj
pch.cpp      pythonba.def  PythonBootstrapperApplication.cpp
pch.h        pythonba.sln  resource.h

./Python-3.12.0/Tools/msi/bundle/packagegroups:
core.wxs  doc.wxs       lib.wxs             postinstall.wxs
crt.wxs   exe.wxs       packageinstall.wxs  tcltk.wxs
dev.wxs   launcher.wxs  pip.wxs             test.wxs

./Python-3.12.0/Tools/msi/core:
core_d.wixproj  core_en-US.wxl  core_pdb.wixproj  core.wixproj
core_d.wxs      core_files.wxs  core_pdb.wxs      core.wxs

./Python-3.12.0/Tools/msi/dev:
dev_d.wixproj  dev_en-US.wxl  dev.wixproj
dev_d.wxs      dev_files.wxs  dev.wxs

./Python-3.12.0/Tools/msi/doc:
doc_en-US.wxl_template  doc.wixproj  doc.wxs

./Python-3.12.0/Tools/msi/exe:
exe_d.wixproj           exe_files.wxs    exe_reg.wxs
exe_d.wxs               exe_pdb.wixproj  exe.wixproj
exe_en-US.wxl_template  exe_pdb.wxs      exe.wxs

./Python-3.12.0/Tools/msi/launcher:
launcher_en-US.wxl  launcher_reg.wxs  launcher.wxs
launcher_files.wxs  launcher.wixproj

./Python-3.12.0/Tools/msi/lib:
lib_d.wixproj  lib_en-US.wxl  lib_pdb.wixproj  lib.wixproj
lib_d.wxs      lib_files.wxs  lib_pdb.wxs      lib.wxs

./Python-3.12.0/Tools/msi/path:
path_en-US.wxl  path.wixproj  path.wxs

./Python-3.12.0/Tools/msi/pip:
pip_en-US.wxl  pip.wixproj  pip.wxs

./Python-3.12.0/Tools/msi/tcltk:
tcltk_d.wixproj           tcltk_files.wxs    tcltk_reg.wxs
tcltk_d.wxs               tcltk_pdb.wixproj  tcltk.wixproj
tcltk_en-US.wxl_template  tcltk_pdb.wxs      tcltk.wxs

./Python-3.12.0/Tools/msi/test:
test_d.wixproj  test_en-US.wxl  test_pdb.wixproj  test.wixproj
test_d.wxs      test_files.wxs  test_pdb.wxs      test.wxs

./Python-3.12.0/Tools/msi/ucrt:
ucrt_en-US.wxl  ucrt.wixproj  ucrt.wxs

./Python-3.12.0/Tools/nuget:
build.bat           pythondaily.nuspec          pythonx86.nuspec
make_pkg.proj       pythondaily.symbols.nuspec
pythonarm32.nuspec  python.nuspec

./Python-3.12.0/Tools/patchcheck:
patchcheck.py  reindent.py  untabify.py

./Python-3.12.0/Tools/peg_generator:
data      mypy.ini  peg_extension   requirements.pip
Makefile  pegen     pyproject.toml  scripts

./Python-3.12.0/Tools/peg_generator/data:
cprog.py  top-pypi-packages-365-days.json  xxl.zip

./Python-3.12.0/Tools/peg_generator/pegen:
ast_dump.py        grammar_visualizer.py  parser.py
build.py           __init__.py            python_generator.py
c_generator.py     keywordgen.py          sccutils.py
first_sets.py      __main__.py            testutil.py
grammar_parser.py  metagrammar.gram       tokenizer.py
grammar.py         parser_generator.py    validator.py

./Python-3.12.0/Tools/peg_generator/peg_extension:
__init__.py  peg_extension.c

./Python-3.12.0/Tools/peg_generator/scripts:
ast_timings.py             find_max_nesting.py  joinstats.py
benchmark.py               grammar_grapher.py   test_parse_directory.py
download_pypi_packages.py  __init__.py          test_pypi_packages.py

./Python-3.12.0/Tools/scripts:
2to3                 idle3         summarize_stats.py
checkpip.py          pydoc3        var_access_benchmark.py
combinerefs.py       README
divmod_threshold.py  run_tests.py

./Python-3.12.0/Tools/ssl:
make_ssl_data.py  multissltests.py

./Python-3.12.0/Tools/stringbench:
README  stringbench.py

./Python-3.12.0/Tools/tz:
zdump.py

./Python-3.12.0/Tools/unicode:
comparecodecs.py    genmap_schinese.py  listcodecs.py
gencjkcodecs.py     genmap_support.py   Makefile
gencodec.py         genmap_tchinese.py  makeunicodedata.py
genmap_japanese.py  genwincodec.py      mkstringprep.py
genmap_korean.py    genwincodecs.bat    python-mappings

./Python-3.12.0/Tools/unicode/python-mappings:
CP1140.TXT  diff               GB2312.TXT             KOI8-U.TXT
CP273.TXT   gb-18030-2000.xml  jisx0213-2004-std.txt  TIS-620.TXT

./Python-3.12.0/Tools/unicode/python-mappings/diff:
jisx0213-2000-std.txt.diff  jisx0213-2004-std.txt.diff

./Python-3.12.0/Tools/unittestgui:
README.txt  unittestgui.py

./Python-3.12.0/Tools/wasm:
config.site-wasm32-emscripten  README.md            wasm_build.py
config.site-wasm32-wasi        Setup.local.example  wasm_webserver.py
python.html                    wasi-env
python.worker.js               wasm_assets.py

./snap:
asciiquarium  nmap               snap-store        vlc
firefox       pycharm-community  telegram-desktop  whatsapp-linux-app

./snap/asciiquarium:
42  common  current

./snap/asciiquarium/42:

./snap/asciiquarium/common:

./snap/firefox:
4793  4848  common  current

./snap/firefox/4793:

./snap/firefox/4848:

./snap/firefox/common:

./snap/nmap:
3545  common  current

./snap/nmap/3545:

./snap/nmap/common:

./snap/pycharm-community:
407  408  common  current

./snap/pycharm-community/407:

./snap/pycharm-community/408:

./snap/pycharm-community/common:

./snap/snap-store:
1113  638  common  current

./snap/snap-store/1113:

./snap/snap-store/638:

./snap/snap-store/common:

./snap/telegram-desktop:
6117  6146  common  current

./snap/telegram-desktop/6117:

./snap/telegram-desktop/6146:

./snap/telegram-desktop/common:

./snap/vlc:
3777  common  current

./snap/vlc/3777:

./snap/vlc/common:
vlcrc

./snap/whatsapp-linux-app:
2  common  current

./snap/whatsapp-linux-app/2:

./snap/whatsapp-linux-app/common:

./Templates:

./Videos:

./WhiteSur-gtk-theme:
clean-git.sh  install.sh       parse-sass.sh  release  src
COPYING       make-release.sh  README.md      shell    tweaks.sh

./WhiteSur-gtk-theme/release:
WhiteSur-Dark-nord.tar.xz        WhiteSur-Light-nord.tar.xz
WhiteSur-Dark-solid-nord.tar.xz  WhiteSur-Light-solid-nord.tar.xz
WhiteSur-Dark-solid.tar.xz       WhiteSur-Light-solid.tar.xz
WhiteSur-Dark.tar.xz             WhiteSur-Light.tar.xz

./WhiteSur-gtk-theme/shell:
lib-core.sh  lib-flatpak.sh  lib-install.sh

./WhiteSur-gtk-theme/src:
assets  main  other  sass

./WhiteSur-gtk-theme/src/assets:
cinnamon     gtk      metacity-1            unity
gnome-shell  gtk-2.0  render-all-assets.sh  xfwm4

./WhiteSur-gtk-theme/src/assets/cinnamon:
assets-Dark        theme-blue        theme-orange       theme-red-nord
assets-Dark-nord   theme-blue-nord   theme-orange-nord  theme-yellow
assets-Light       theme-green       theme-pink         theme-yellow-nord
assets-Light-nord  theme-green-nord  theme-pink-nord    thumbnails
common-assets      theme-grey        theme-purple
make-assets.sh     theme-grey-nord   theme-purple-nord
theme              theme-nord        theme-red

./WhiteSur-gtk-theme/src/assets/cinnamon/assets-Dark:
calendar-arrow-left.svg   menu-solid.svg       toggle-off.svg
calendar-arrow-right.svg  menu.svg             trash-icon.svg
checkbox-off.svg          radiobutton-off.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/assets-Dark-nord:
calendar-arrow-left.svg   menu-solid.svg       toggle-off.svg
calendar-arrow-right.svg  menu.svg             trash-icon.svg
checkbox-off.svg          radiobutton-off.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/assets-Light:
calendar-arrow-left.svg   menu-solid.svg       toggle-off.svg
calendar-arrow-right.svg  menu.svg             trash-icon.svg
checkbox-off.svg          radiobutton-off.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/assets-Light-nord:
calendar-arrow-left.svg   menu-solid.svg       toggle-off.svg
calendar-arrow-right.svg  menu.svg             trash-icon.svg
checkbox-off.svg          radiobutton-off.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/common-assets:
add-workspace-hover.svg  close-active.svg  close.svg
add-workspace.svg        close-hover.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-blue:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-blue-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-green:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-green-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-grey:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-grey-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-orange:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-orange-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-pink:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-pink-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-purple:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-purple-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-red:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-red-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-yellow:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/theme-yellow-nord:
add-workspace-active.svg  corner-ripple.svg  toggle-on.svg
checkbox.svg              radiobutton.svg

./WhiteSur-gtk-theme/src/assets/cinnamon/thumbnails:
make-thumbnails.sh              thumbnail-Light-blue-nord.png
render-thumbnails.sh            thumbnail-Light-blue.png
thumbnail-Dark-blue-nord.png    thumbnail-Light-green-nord.png
thumbnail-Dark-blue.png         thumbnail-Light-green.png
thumbnail-Dark-green-nord.png   thumbnail-Light-grey-nord.png
thumbnail-Dark-green.png        thumbnail-Light-grey.png
thumbnail-Dark-grey-nord.png    thumbnail-Light-nord.png
thumbnail-Dark-grey.png         thumbnail-Light-orange-nord.png
thumbnail-Dark-nord.png         thumbnail-Light-orange.png
thumbnail-Dark-orange-nord.png  thumbnail-Light-pink-nord.png
thumbnail-Dark-orange.png       thumbnail-Light-pink.png
thumbnail-Dark-pink-nord.png    thumbnail-Light.png
thumbnail-Dark-pink.png         thumbnail-Light-purple-nord.png
thumbnail-Dark.png              thumbnail-Light-purple.png
thumbnail-Dark-purple-nord.png  thumbnail-Light-red-nord.png
thumbnail-Dark-purple.png       thumbnail-Light-red.png
thumbnail-Dark-red-nord.png     thumbnail-Light-yellow-nord.png
thumbnail-Dark-red.png          thumbnail-Light-yellow.png
thumbnail-Dark-yellow-nord.png  thumbnail.svg
thumbnail-Dark-yellow.png

./WhiteSur-gtk-theme/src/assets/gnome-shell:
activities        make-assets.sh    theme-grey-nord    theme-purple-nord
activities-black  theme             theme-nord         theme-red
assets-Dark       theme-blue        theme-orange       theme-red-nord
assets-Light      theme-blue-nord   theme-orange-nord  theme-yellow
backgrounds       theme-green       theme-pink         theme-yellow-nord
common-assets     theme-green-nord  theme-pink-nord
icons             theme-grey        theme-purple

./WhiteSur-gtk-theme/src/assets/gnome-shell/activities:
activities-apple.svg   activities-gnome.svg     activities-tux.svg
activities-arch.svg    activities-manjaro.svg   activities-ubuntu.svg
activities-budgie.svg  activities-mxlinux.svg   activities-void.svg
activities-debian.svg  activities-opensuse.svg  activities-zorin.svg
activities-fedora.svg  activities-popos.svg
activities-gentoo.svg  activities-simple.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/activities-black:
activities-apple.svg   activities-gnome.svg     activities-tux.svg
activities-arch.svg    activities-manjaro.svg   activities-ubuntu.svg
activities-budgie.svg  activities-mxlinux.svg   activities-void.svg
activities-debian.svg  activities-opensuse.svg  activities-zorin.svg
activities-fedora.svg  activities-popos.svg
activities-gentoo.svg  activities-simple.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/assets-Dark:
calendar-arrow-left.svg   calendar-today.svg  toggle-off.svg
calendar-arrow-right.svg  checkbox-off.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/assets-Light:
calendar-arrow-left.svg   calendar-today.svg  toggle-off.svg
calendar-arrow-right.svg  checkbox-off.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/backgrounds:
background-blank.png        background-blur.png    background-default.png
background-blur-darken.png  background-darken.png

./WhiteSur-gtk-theme/src/assets/gnome-shell/common-assets:
dash-placeholder.svg  process-working.svg      window-close.svg
no-events.svg         view-app-grid.svg        window-close-symbolic.svg
noise-texture.svg     window-close-active.svg
no-notifications.svg  window-close-hover.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/icons:
scalable

./WhiteSur-gtk-theme/src/assets/gnome-shell/icons/scalable:
actions  status

./WhiteSur-gtk-theme/src/assets/gnome-shell/icons/scalable/actions:
carousel-arrow-back-symbolic.svg
carousel-arrow-next-symbolic.svg
carousel-arrow-previous-symbolic.svg
color-pick.svg
dark-mode-symbolic.svg
pointer-double-click-symbolic.svg
pointer-drag-symbolic.svg
pointer-primary-click-symbolic.svg
pointer-secondary-click-symbolic.svg
preview-close-symbolic.svg
record-screen-symbolic.svg
screencast-recorded-symbolic.svg
screenshot-recorded-symbolic.svg
screenshot-ui-area-symbolic.svg
screenshot-ui-display-symbolic.svg
screenshot-ui-show-pointer-symbolic.svg
screenshot-ui-window-symbolic.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/icons/scalable/status:
eye-not-looking-symbolic.svg
eye-open-negative-filled-symbolic.svg
keyboard-caps-lock-filled-symbolic.svg
keyboard-caps-lock-symbolic.svg
keyboard-enter-symbolic.svg
keyboard-hide-symbolic.svg
keyboard-layout-filled-symbolic.svg
keyboard-layout-symbolic.svg
keyboard-shift-filled-symbolic.svg
keyboard-shift-symbolic.svg
message-indicator-symbolic.svg
no-events-symbolic.svg
no-notifications-symbolic.svg
screen-privacy-disabled-symbolic.svg
screen-privacy-symbolic.svg
stop-symbolic.svg
window-close-symbolic.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-blue:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-blue-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-green:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-green-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-grey:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-grey-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-orange:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-orange-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-pink:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-pink-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-purple:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-purple-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-red:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-red-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-yellow:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gnome-shell/theme-yellow-nord:
checkbox.svg  more-results.svg  toggle-on.svg

./WhiteSur-gtk-theme/src/assets/gtk:
common-assets  scalable  thumbnails  windows-assets

./WhiteSur-gtk-theme/src/assets/gtk/common-assets:
assets      render-assets.sh          sidebar-assets.svg
assets.svg  render-sidebar-assets.sh  sidebar-assets.txt
assets.txt  sidebar-assets            theme_assets.txt

./WhiteSur-gtk-theme/src/assets/gtk/common-assets/assets:
combobox-arrow@2.png
combobox-arrow-dark@2.png
combobox-arrow-dark.png
combobox-arrow.png
slider-horz-scale-has-marks-above@2.png
slider-horz-scale-has-marks-above-active@2.png
slider-horz-scale-has-marks-above-active.png
slider-horz-scale-has-marks-above-hover@2.png
slider-horz-scale-has-marks-above-hover.png
slider-horz-scale-has-marks-above-insensitive@2.png
slider-horz-scale-has-marks-above-insensitive.png
slider-horz-scale-has-marks-above.png
slider-horz-scale-has-marks-below@2.png
slider-horz-scale-has-marks-below-active@2.png
slider-horz-scale-has-marks-below-active.png
slider-horz-scale-has-marks-below-hover@2.png
slider-horz-scale-has-marks-below-hover.png
slider-horz-scale-has-marks-below-insensitive@2.png
slider-horz-scale-has-marks-below-insensitive.png
slider-horz-scale-has-marks-below.png
slider-vert-scale-has-marks-above@2.png
slider-vert-scale-has-marks-above-active@2.png
slider-vert-scale-has-marks-above-active.png
slider-vert-scale-has-marks-above-hover@2.png
slider-vert-scale-has-marks-above-hover.png
slider-vert-scale-has-marks-above-insensitive@2.png
slider-vert-scale-has-marks-above-insensitive.png
slider-vert-scale-has-marks-above.png
slider-vert-scale-has-marks-below@2.png
slider-vert-scale-has-marks-below-active@2.png
slider-vert-scale-has-marks-below-active.png
slider-vert-scale-has-marks-below-hover@2.png
slider-vert-scale-has-marks-below-hover.png
slider-vert-scale-has-marks-below-insensitive@2.png
slider-vert-scale-has-marks-below-insensitive.png
slider-vert-scale-has-marks-below.png

./WhiteSur-gtk-theme/src/assets/gtk/common-assets/sidebar-assets:
sidebar-view-active-180px@2.png
sidebar-view-active-180px-dark@2.png
sidebar-view-active-180px-dark.png
sidebar-view-active-180px.png
sidebar-view-active-200px@2.png
sidebar-view-active-200px-dark@2.png
sidebar-view-active-200px-dark.png
sidebar-view-active-200px.png
sidebar-view-active-220px@2.png
sidebar-view-active-220px-dark@2.png
sidebar-view-active-220px-dark.png
sidebar-view-active-220px.png
sidebar-view-active-240px@2.png
sidebar-view-active-240px-dark@2.png
sidebar-view-active-240px-dark.png
sidebar-view-active-240px.png
sidebar-view-active-260px@2.png
sidebar-view-active-260px-dark@2.png
sidebar-view-active-260px-dark.png
sidebar-view-active-260px.png
sidebar-view-active-280px@2.png
sidebar-view-active-280px-dark@2.png
sidebar-view-active-280px-dark.png
sidebar-view-active-280px.png
sidebar-view-checked-180px@2.png
sidebar-view-checked-180px-dark@2.png
sidebar-view-checked-180px-dark.png
sidebar-view-checked-180px.png
sidebar-view-checked-200px@2.png
sidebar-view-checked-200px-dark@2.png
sidebar-view-checked-200px-dark.png
sidebar-view-checked-200px.png
sidebar-view-checked-220px@2.png
sidebar-view-checked-220px-dark@2.png
sidebar-view-checked-220px-dark.png
sidebar-view-checked-220px.png
sidebar-view-checked-240px@2.png
sidebar-view-checked-240px-dark@2.png
sidebar-view-checked-240px-dark.png
sidebar-view-checked-240px.png
sidebar-view-checked-260px@2.png
sidebar-view-checked-260px-dark@2.png
sidebar-view-checked-260px-dark.png
sidebar-view-checked-260px.png
sidebar-view-checked-280px@2.png
sidebar-view-checked-280px-dark@2.png
sidebar-view-checked-280px-dark.png
sidebar-view-checked-280px.png
sidebar-view-hover-180px@2.png
sidebar-view-hover-180px-dark@2.png
sidebar-view-hover-180px-dark.png
sidebar-view-hover-180px.png
sidebar-view-hover-200px@2.png
sidebar-view-hover-200px-dark@2.png
sidebar-view-hover-200px-dark.png
sidebar-view-hover-200px.png
sidebar-view-hover-220px@2.png
sidebar-view-hover-220px-dark@2.png
sidebar-view-hover-220px-dark.png
sidebar-view-hover-220px.png
sidebar-view-hover-240px@2.png
sidebar-view-hover-240px-dark@2.png
sidebar-view-hover-240px-dark.png
sidebar-view-hover-240px.png
sidebar-view-hover-260px@2.png
sidebar-view-hover-260px-dark@2.png
sidebar-view-hover-260px-dark.png
sidebar-view-hover-260px.png
sidebar-view-hover-280px@2.png
sidebar-view-hover-280px-dark@2.png
sidebar-view-hover-280px-dark.png
sidebar-view-hover-280px.png

./WhiteSur-gtk-theme/src/assets/gtk/scalable:
checkbox-checked-big-symbolic.svg  radio-mixed-symbolic.svg
checkbox-checked-symbolic@2.svg    window-close-symbolic@2.svg
checkbox-checked-symbolic.svg      window-close-symbolic.svg
checkbox-mixed-symbolic@2.svg      window-maximize-symbolic@2.svg
checkbox-mixed-symbolic.svg        window-maximize-symbolic.svg
combobox-arrow-symbolic@2.svg      window-minimize-symbolic@2.svg
combobox-arrow-symbolic.svg        window-minimize-symbolic.svg
radio-checked-symbolic@2.svg       window-restore-symbolic@2.svg
radio-checked-symbolic.svg         window-restore-symbolic.svg
radio-mixed-symbolic@2.svg

./WhiteSur-gtk-theme/src/assets/gtk/thumbnails:
make-thumbnails.sh              thumbnail-Light-blue-nord.png
render-thumbnails.sh            thumbnail-Light-blue.png
thumbnail-Dark-blue-nord.png    thumbnail-Light-green-nord.png
thumbnail-Dark-blue.png         thumbnail-Light-green.png
thumbnail-Dark-green-nord.png   thumbnail-Light-grey-nord.png
thumbnail-Dark-green.png        thumbnail-Light-grey.png
thumbnail-Dark-grey-nord.png    thumbnail-Light-nord.png
thumbnail-Dark-grey.png         thumbnail-Light-orange-nord.png
thumbnail-Dark-nord.png         thumbnail-Light-orange.png
thumbnail-Dark-orange-nord.png  thumbnail-Light-pink-nord.png
thumbnail-Dark-orange.png       thumbnail-Light-pink.png
thumbnail-Dark-pink-nord.png    thumbnail-Light.png
thumbnail-Dark-pink.png         thumbnail-Light-purple-nord.png
thumbnail-Dark.png              thumbnail-Light-purple.png
thumbnail-Dark-purple-nord.png  thumbnail-Light-red-nord.png
thumbnail-Dark-purple.png       thumbnail-Light-red.png
thumbnail-Dark-red-nord.png     thumbnail-Light-yellow-nord.png
thumbnail-Dark-red.png          thumbnail-Light-yellow.png
thumbnail-Dark-yellow-nord.png  thumbnail.svg
thumbnail-Dark-yellow.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets:
assets.txt                  titlebutton            titlebutton-small
render-alt-assets.sh        titlebutton-alt        windows-assets.svg
render-alt-small-assets.sh  titlebutton-alt-nord   windows-nord-assets.svg
render-assets.sh            titlebutton-alt-small
render-small-assets.sh      titlebutton-nord

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton-alt:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton-alt-nord:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton-alt-small:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton-nord:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk/windows-assets/titlebutton-small:
titlebutton-close@2.png
titlebutton-close-active@2.png
titlebutton-close-active-dark@2.png
titlebutton-close-active-dark.png
titlebutton-close-active.png
titlebutton-close-backdrop@2.png
titlebutton-close-backdrop-dark@2.png
titlebutton-close-backdrop-dark.png
titlebutton-close-backdrop-hover@2.png
titlebutton-close-backdrop-hover-dark@2.png
titlebutton-close-backdrop-hover-dark.png
titlebutton-close-backdrop-hover.png
titlebutton-close-backdrop.png
titlebutton-close-dark@2.png
titlebutton-close-dark.png
titlebutton-close-hover@2.png
titlebutton-close-hover-dark@2.png
titlebutton-close-hover-dark.png
titlebutton-close-hover.png
titlebutton-close.png
titlebutton-maximize@2.png
titlebutton-maximize-active@2.png
titlebutton-maximize-active-dark@2.png
titlebutton-maximize-active-dark.png
titlebutton-maximize-active.png
titlebutton-maximize-backdrop@2.png
titlebutton-maximize-backdrop-dark@2.png
titlebutton-maximize-backdrop-dark.png
titlebutton-maximize-backdrop-hover@2.png
titlebutton-maximize-backdrop-hover-dark@2.png
titlebutton-maximize-backdrop-hover-dark.png
titlebutton-maximize-backdrop-hover.png
titlebutton-maximize-backdrop.png
titlebutton-maximize-dark@2.png
titlebutton-maximize-dark.png
titlebutton-maximize-hover@2.png
titlebutton-maximize-hover-dark@2.png
titlebutton-maximize-hover-dark.png
titlebutton-maximize-hover.png
titlebutton-maximize.png
titlebutton-minimize@2.png
titlebutton-minimize-active@2.png
titlebutton-minimize-active-dark@2.png
titlebutton-minimize-active-dark.png
titlebutton-minimize-active.png
titlebutton-minimize-backdrop@2.png
titlebutton-minimize-backdrop-dark@2.png
titlebutton-minimize-backdrop-dark.png
titlebutton-minimize-backdrop-hover@2.png
titlebutton-minimize-backdrop-hover-dark@2.png
titlebutton-minimize-backdrop-hover-dark.png
titlebutton-minimize-backdrop-hover.png
titlebutton-minimize-backdrop.png
titlebutton-minimize-dark@2.png
titlebutton-minimize-dark.png
titlebutton-minimize-hover@2.png
titlebutton-minimize-hover-dark@2.png
titlebutton-minimize-hover-dark.png
titlebutton-minimize-hover.png
titlebutton-minimize.png
titlebutton-restore@2.png
titlebutton-restore-active@2.png
titlebutton-restore-active-dark@2.png
titlebutton-restore-active-dark.png
titlebutton-restore-active.png
titlebutton-restore-backdrop@2.png
titlebutton-restore-backdrop-dark@2.png
titlebutton-restore-backdrop-dark.png
titlebutton-restore-backdrop-hover@2.png
titlebutton-restore-backdrop-hover-dark@2.png
titlebutton-restore-backdrop-hover-dark.png
titlebutton-restore-backdrop-hover.png
titlebutton-restore-backdrop.png
titlebutton-restore-dark@2.png
titlebutton-restore-dark.png
titlebutton-restore-hover@2.png
titlebutton-restore-hover-dark@2.png
titlebutton-restore-hover-dark.png
titlebutton-restore-hover.png
titlebutton-restore.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0:
assets-common-Dark            assets-Dark.svg
assets-common-Dark-nord       assets-Dark-yellow
assets-common-Dark-nord.svg   assets-Dark-yellow-nord
assets-common-Dark.svg        assets-Light
assets-common-Light           assets-Light-blue
assets-common-Light-nord      assets-Light-blue-nord
assets-common-Light-nord.svg  assets-Light-green
assets-common-Light.svg       assets-Light-green-nord
assets-common.txt             assets-Light-grey
assets-Dark                   assets-Light-grey-nord
assets-Dark-blue              assets-Light-nord
assets-Dark-blue-nord         assets-Light-orange
assets-Dark-green             assets-Light-orange-nord
assets-Dark-green-nord        assets-Light-pink
assets-Dark-grey              assets-Light-pink-nord
assets-Dark-grey-nord         assets-Light-purple
assets-Dark-nord              assets-Light-purple-nord
assets-Dark-orange            assets-Light-red
assets-Dark-orange-nord       assets-Light-red-nord
assets-Dark-pink              assets-Light.svg
assets-Dark-pink-nord         assets-Light-yellow
assets-Dark-purple            assets-Light-yellow-nord
assets-Dark-purple-nord       assets-theme.txt
assets-Dark-red               make-assets.sh
assets-Dark-red-nord          render-assets.sh

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-common-Dark:
arrow-down-insens.png
arrow-down.png
arrow-down-prelight.png
arrow-down-small-insens.png
arrow-down-small.png
arrow-down-small-prelight.png
arrow-left-insens.png
arrow-left.png
arrow-left-prelight.png
arrow-right-insens.png
arrow-right.png
arrow-right-prelight.png
arrow-up-insens.png
arrow-up.png
arrow-up-prelight.png
arrow-up-small-insens.png
arrow-up-small.png
arrow-up-small-prelight.png
border.png
button-hover.png
button-insensitive.png
button.png
checkbox-checked-insensitive.png
checkbox-unchecked-insensitive.png
checkbox-unchecked.png
combo-entry-border.png
combo-entry-border-rtl.png
combo-entry-button-insensitive.png
combo-entry-button-insensitive-rtl.png
combo-entry-button.png
combo-entry-button-rtl.png
combo-entry-insensitive-notebook.png
combo-entry-insensitive-notebook-rtl.png
combo-entry-insensitive.png
combo-entry-insensitive-rtl.png
combo-entry-notebook.png
combo-entry-notebook-rtl.png
combo-entry.png
combo-entry-rtl.png
down-background-disable.png
down-background-disable-rtl.png
down-background.png
down-background-rtl.png
entry-background-disabled.png
entry-background.png
entry-bg.png
entry-border-bg.png
entry-disabled-bg.png
entry-disabled-notebook.png
entry-disabled-toolbar.png
entry-notebook.png
entry-toolbar.png
focus-line.png
frame-gap-end.png
frame-gap-start.png
frame.png
handle-h.png
handle-v.png
inline-toolbar.png
line-h.png
line-v.png
menu-arrow.png
menu-arrow-prelight.png
menubar.png
menu-checkbox-checked-insensitive.png
menu-checkbox-unchecked-insensitive.png
menu-checkbox-unchecked.png
menu-radio-checked-insensitive.png
menu-radio-unchecked-insensitive.png
menu-radio-unchecked.png
menu-separator.png
minus.png
notebook-gap-horiz.png
notebook-gap-vert.png
notebook.png
null.png
plus.png
radio-checked-insensitive.png
radio-unchecked-insensitive.png
radio-unchecked.png
slider-horiz-active.png
slider-horiz-insens.png
slider-horiz.png
slider-horiz-prelight.png
slider-insensitive.png
slider.png
slider-prelight.png
slider-vert-active.png
slider-vert-insens.png
slider-vert.png
slider-vert-prelight.png
tab-bottom-active.png
tab-left-active.png
tab-right-active.png
tab-top-active.png
toolbar-button-active-hover.png
toolbar-button-active.png
toolbar.png
tree_header.png
trough-horizontal.png
trough-progressbar.png
trough-progressbar_v.png
trough-scrollbar-horiz.png
trough-scrollbar-vert.png
trough-vertical.png
up-background-disable.png
up-background-disable-rtl.png
up-background.png
up-background-rtl.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-common-Dark-nord:
arrow-down-insens.png
arrow-down.png
arrow-down-prelight.png
arrow-down-small-insens.png
arrow-down-small.png
arrow-down-small-prelight.png
arrow-left-insens.png
arrow-left.png
arrow-left-prelight.png
arrow-right-insens.png
arrow-right.png
arrow-right-prelight.png
arrow-up-insens.png
arrow-up.png
arrow-up-prelight.png
arrow-up-small-insens.png
arrow-up-small.png
arrow-up-small-prelight.png
border.png
button-hover.png
button-insensitive.png
button.png
checkbox-checked-insensitive.png
checkbox-unchecked-insensitive.png
checkbox-unchecked.png
combo-entry-border.png
combo-entry-border-rtl.png
combo-entry-button-insensitive.png
combo-entry-button-insensitive-rtl.png
combo-entry-button.png
combo-entry-button-rtl.png
combo-entry-insensitive-notebook.png
combo-entry-insensitive-notebook-rtl.png
combo-entry-insensitive.png
combo-entry-insensitive-rtl.png
combo-entry-notebook.png
combo-entry-notebook-rtl.png
combo-entry.png
combo-entry-rtl.png
down-background-disable.png
down-background-disable-rtl.png
down-background.png
down-background-rtl.png
entry-background-disabled.png
entry-background.png
entry-bg.png
entry-border-bg.png
entry-disabled-bg.png
entry-disabled-notebook.png
entry-disabled-toolbar.png
entry-notebook.png
entry-toolbar.png
focus-line.png
frame-gap-end.png
frame-gap-start.png
frame.png
handle-h.png
handle-v.png
inline-toolbar.png
line-h.png
line-v.png
menu-arrow.png
menu-arrow-prelight.png
menubar.png
menu-checkbox-checked-insensitive.png
menu-checkbox-unchecked-insensitive.png
menu-checkbox-unchecked.png
menu-radio-checked-insensitive.png
menu-radio-unchecked-insensitive.png
menu-radio-unchecked.png
menu-separator.png
minus.png
notebook-gap-horiz.png
notebook-gap-vert.png
notebook.png
null.png
plus.png
radio-checked-insensitive.png
radio-unchecked-insensitive.png
radio-unchecked.png
slider-horiz-active.png
slider-horiz-insens.png
slider-horiz.png
slider-horiz-prelight.png
slider-insensitive.png
slider.png
slider-prelight.png
slider-vert-active.png
slider-vert-insens.png
slider-vert.png
slider-vert-prelight.png
tab-bottom-active.png
tab-left-active.png
tab-right-active.png
tab-top-active.png
toolbar-button-active-hover.png
toolbar-button-active.png
toolbar.png
tree_header.png
trough-horizontal.png
trough-progressbar.png
trough-progressbar_v.png
trough-scrollbar-horiz.png
trough-scrollbar-vert.png
trough-vertical.png
up-background-disable.png
up-background-disable-rtl.png
up-background.png
up-background-rtl.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-common-Light:
arrow-down-insens.png
arrow-down.png
arrow-down-prelight.png
arrow-down-small-insens.png
arrow-down-small.png
arrow-down-small-prelight.png
arrow-left-insens.png
arrow-left.png
arrow-left-prelight.png
arrow-right-insens.png
arrow-right.png
arrow-right-prelight.png
arrow-up-insens.png
arrow-up.png
arrow-up-prelight.png
arrow-up-small-insens.png
arrow-up-small.png
arrow-up-small-prelight.png
border.png
button-active-hover.png
button-active.png
button-hover.png
button-insensitive.png
button.png
checkbox-checked-insensitive.png
checkbox-unchecked-insensitive.png
checkbox-unchecked.png
combo-entry-border.png
combo-entry-border-rtl.png
combo-entry-button-active.png
combo-entry-button-active-rtl.png
combo-entry-button-insensitive.png
combo-entry-button-insensitive-rtl.png
combo-entry-button.png
combo-entry-button-rtl.png
combo-entry-insensitive-notebook.png
combo-entry-insensitive-notebook-rtl.png
combo-entry-insensitive.png
combo-entry-insensitive-rtl.png
combo-entry-notebook.png
combo-entry-notebook-rtl.png
combo-entry.png
combo-entry-rtl.png
down-background-disable.png
down-background-disable-rtl.png
down-background.png
down-background-rtl.png
entry-background-disabled.png
entry-background.png
entry-bg.png
entry-border-bg.png
entry-disabled-bg.png
entry-disabled-notebook.png
entry-disabled-toolbar.png
entry-notebook.png
entry-toolbar.png
focus-line.png
frame-gap-end.png
frame-gap-start.png
frame.png
handle-h.png
handle-v.png
inline-toolbar.png
line-h.png
line-v.png
menu-arrow.png
menu-arrow-prelight.png
menubar.png
menu-checkbox-checked-insensitive.png
menu-checkbox-unchecked-insensitive.png
menu-checkbox-unchecked.png
menu-radio-checked-insensitive.png
menu-radio-unchecked-insensitive.png
menu-radio-unchecked.png
menu-separator.png
minus.png
notebook-gap-horiz.png
notebook-gap-vert.png
notebook.png
null.png
plus.png
radio-checked-insensitive.png
radio-unchecked-insensitive.png
radio-unchecked.png
slider-horiz-active.png
slider-horiz-insens.png
slider-horiz.png
slider-horiz-prelight.png
slider-insensitive.png
slider.png
slider-prelight.png
slider-vert-active.png
slider-vert-insens.png
slider-vert.png
slider-vert-prelight.png
tab-bottom-active.png
tab-left-active.png
tab-right-active.png
tab-top-active.png
toolbar-button-active-hover.png
toolbar-button-active.png
toolbar.png
tree_header.png
trough-horizontal.png
trough-progressbar.png
trough-progressbar_v.png
trough-scrollbar-horiz.png
trough-scrollbar-vert.png
trough-vertical.png
up-background-disable.png
up-background-disable-rtl.png
up-background.png
up-background-rtl.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-common-Light-nord:
arrow-down-insens.png
arrow-down.png
arrow-down-prelight.png
arrow-down-small-insens.png
arrow-down-small.png
arrow-down-small-prelight.png
arrow-left-insens.png
arrow-left.png
arrow-left-prelight.png
arrow-right-insens.png
arrow-right.png
arrow-right-prelight.png
arrow-up-insens.png
arrow-up.png
arrow-up-prelight.png
arrow-up-small-insens.png
arrow-up-small.png
arrow-up-small-prelight.png
border.png
button-active-hover.png
button-active.png
button-hover.png
button-insensitive.png
button.png
checkbox-checked-insensitive.png
checkbox-unchecked-insensitive.png
checkbox-unchecked.png
combo-entry-border.png
combo-entry-border-rtl.png
combo-entry-button-active.png
combo-entry-button-active-rtl.png
combo-entry-button-insensitive.png
combo-entry-button-insensitive-rtl.png
combo-entry-button.png
combo-entry-button-rtl.png
combo-entry-insensitive-notebook.png
combo-entry-insensitive-notebook-rtl.png
combo-entry-insensitive.png
combo-entry-insensitive-rtl.png
combo-entry-notebook.png
combo-entry-notebook-rtl.png
combo-entry.png
combo-entry-rtl.png
down-background-disable.png
down-background-disable-rtl.png
down-background.png
down-background-rtl.png
entry-background-disabled.png
entry-background.png
entry-bg.png
entry-border-bg.png
entry-disabled-bg.png
entry-disabled-notebook.png
entry-disabled-toolbar.png
entry-notebook.png
entry-toolbar.png
focus-line.png
frame-gap-end.png
frame-gap-start.png
frame.png
handle-h.png
handle-v.png
inline-toolbar.png
line-h.png
line-v.png
menu-arrow.png
menu-arrow-prelight.png
menubar.png
menu-checkbox-checked-insensitive.png
menu-checkbox-unchecked-insensitive.png
menu-checkbox-unchecked.png
menu-radio-checked-insensitive.png
menu-radio-unchecked-insensitive.png
menu-radio-unchecked.png
menu-separator.png
minus.png
notebook-gap-horiz.png
notebook-gap-vert.png
notebook.png
null.png
plus.png
radio-checked-insensitive.png
radio-unchecked-insensitive.png
radio-unchecked.png
slider-horiz-active.png
slider-horiz-insens.png
slider-horiz.png
slider-horiz-prelight.png
slider-insensitive.png
slider.png
slider-prelight.png
slider-vert-active.png
slider-vert-insens.png
slider-vert.png
slider-vert-prelight.png
tab-bottom-active.png
tab-left-active.png
tab-right-active.png
tab-top-active.png
toolbar-button-active-hover.png
toolbar-button-active.png
toolbar.png
tree_header.png
trough-horizontal.png
trough-progressbar.png
trough-progressbar_v.png
trough-scrollbar-horiz.png
trough-scrollbar-vert.png
trough-vertical.png
up-background-disable.png
up-background-disable-rtl.png
up-background.png
up-background-rtl.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-blue:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-blue-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-green:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-green-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-grey:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-grey-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-orange:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-orange-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-pink:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-pink-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-purple:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-purple-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-red:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-red-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-yellow:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Dark-yellow-nord:
button-active-hover.png             entry-active-toolbar.png
button-active.png                   entry-border-active-bg.png
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-button-active.png       menu-radio-checked.png
combo-entry-button-active-rtl.png   pathbar_button_active.png
combo-entry-focus-notebook.png      pathbar_button_prelight.png
combo-entry-focus-notebook-rtl.png  progressbar.png
combo-entry-focus.png               progressbar_v.png
combo-entry-focus-rtl.png           radio-checked.png
entry-active-bg.png                 trough-horizontal-active.png
entry-active-notebook.png           trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-blue:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-blue-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-green:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-green-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-grey:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-grey-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-orange:
checkbox-checked.png                menu-checkbox-checked.png
combo-entry-border-focus.png        menuitem.png
combo-entry-border-focus-rtl.png    menu-radio-checked.png
combo-entry-focus-notebook.png      pathbar_button_active.png
combo-entry-focus-notebook-rtl.png  pathbar_button_prelight.png
combo-entry-focus.png               progressbar.png
combo-entry-focus-rtl.png           progressbar_v.png
entry-active-bg.png                 radio-checked.png
entry-active-notebook.png           trough-horizontal-active.png
entry-active-toolbar.png            trough-vertical-active.png
menubar_button.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-orange-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-pink:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-pink-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-purple:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-purple-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-red:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-red-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-yellow:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/gtk-2.0/assets-Light-yellow-nord:
checkbox-checked.png                menubar_button.png
combo-entry-border-focus.png        menu-checkbox-checked.png
combo-entry-border-focus-rtl.png    menuitem.png
combo-entry-focus-notebook.png      menu-radio-checked.png
combo-entry-focus-notebook-rtl.png  pathbar_button_active.png
combo-entry-focus.png               pathbar_button_prelight.png
combo-entry-focus-rtl.png           progressbar.png
entry-active-bg.png                 progressbar_v.png
entry-active-notebook.png           radio-checked.png
entry-active-toolbar.png            trough-horizontal-active.png
entry-border-active-bg.png          trough-vertical-active.png

./WhiteSur-gtk-theme/src/assets/metacity-1:
thumbnail-Dark-nord.png   thumbnail-Light.png  titlebuttons-Dark-nord
thumbnail-Dark.png        thumbnail.svg        titlebuttons-Light
thumbnail-Light-nord.png  titlebuttons-Dark    titlebuttons-Light-nord

./WhiteSur-gtk-theme/src/assets/metacity-1/titlebuttons-Dark:
titlebutton-backdrop.svg
titlebutton-close-active.svg
titlebutton-close-backdrop-active.svg
titlebutton-close-backdrop.svg
titlebutton-close-hover.svg
titlebutton-close.svg
titlebutton-maximize-active.svg
titlebutton-maximize-backdrop-active.svg
titlebutton-maximize-backdrop.svg
titlebutton-maximize-hover.svg
titlebutton-maximize.svg
titlebutton-menu-active.svg
titlebutton-menu-backdrop-active.svg
titlebutton-menu-backdrop.svg
titlebutton-menu-hover.svg
titlebutton-menu.svg
titlebutton-minimize-active.svg
titlebutton-minimize-backdrop-active.svg
titlebutton-minimize-backdrop.svg
titlebutton-minimize-hover.svg
titlebutton-minimize.svg
titlebutton-shade-active.svg
titlebutton-shade-backdrop-active.svg
titlebutton-shade-backdrop.svg
titlebutton-shade-hover.svg
titlebutton-shade.svg
titlebutton-unmaximize-active.svg
titlebutton-unmaximize-backdrop-active.svg
titlebutton-unmaximize-backdrop.svg
titlebutton-unmaximize-hover.svg
titlebutton-unshade-active.svg
titlebutton-unshade-backdrop-active.svg
titlebutton-unshade-backdrop.svg
titlebutton-unshade-hover.svg
titlebutton-unshade.svg

./WhiteSur-gtk-theme/src/assets/metacity-1/titlebuttons-Dark-nord:
titlebutton-backdrop.svg
titlebutton-close-active.svg
titlebutton-close-backdrop-active.svg
titlebutton-close-backdrop.svg
titlebutton-close-hover.svg
titlebutton-close.svg
titlebutton-maximize-active.svg
titlebutton-maximize-backdrop-active.svg
titlebutton-maximize-backdrop.svg
titlebutton-maximize-hover.svg
titlebutton-maximize.svg
titlebutton-menu-active.svg
titlebutton-menu-backdrop-active.svg
titlebutton-menu-backdrop.svg
titlebutton-menu-hover.svg
titlebutton-menu.svg
titlebutton-minimize-active.svg
titlebutton-minimize-backdrop-active.svg
titlebutton-minimize-backdrop.svg
titlebutton-minimize-hover.svg
titlebutton-minimize.svg
titlebutton-shade-active.svg
titlebutton-shade-backdrop-active.svg
titlebutton-shade-backdrop.svg
titlebutton-shade-hover.svg
titlebutton-shade.svg
titlebutton-unmaximize-active.svg
titlebutton-unmaximize-backdrop-active.svg
titlebutton-unmaximize-backdrop.svg
titlebutton-unmaximize-hover.svg
titlebutton-unshade-active.svg
titlebutton-unshade-backdrop-active.svg
titlebutton-unshade-backdrop.svg
titlebutton-unshade-hover.svg
titlebutton-unshade.svg

./WhiteSur-gtk-theme/src/assets/metacity-1/titlebuttons-Light:
titlebutton-backdrop.svg
titlebutton-close-active.svg
titlebutton-close-backdrop-active.svg
titlebutton-close-backdrop.svg
titlebutton-close-hover.svg
titlebutton-close.svg
titlebutton-maximize-active.svg
titlebutton-maximize-backdrop-active.svg
titlebutton-maximize-backdrop.svg
titlebutton-maximize-hover.svg
titlebutton-maximize.svg
titlebutton-menu-active.svg
titlebutton-menu-backdrop-active.svg
titlebutton-menu-backdrop.svg
titlebutton-menu-hover.svg
titlebutton-menu.svg
titlebutton-minimize-active.svg
titlebutton-minimize-backdrop-active.svg
titlebutton-minimize-backdrop.svg
titlebutton-minimize-hover.svg
titlebutton-minimize.svg
titlebutton-shade-active.svg
titlebutton-shade-backdrop-active.svg
titlebutton-shade-backdrop.svg
titlebutton-shade-hover.svg
titlebutton-shade.svg
titlebutton-unmaximize-active.svg
titlebutton-unmaximize-backdrop-active.svg
titlebutton-unmaximize-backdrop.svg
titlebutton-unmaximize-hover.svg
titlebutton-unshade-active.svg
titlebutton-unshade-backdrop-active.svg
titlebutton-unshade-backdrop.svg
titlebutton-unshade-hover.svg
titlebutton-unshade.svg

./WhiteSur-gtk-theme/src/assets/metacity-1/titlebuttons-Light-nord:
titlebutton-backdrop.svg
titlebutton-close-active.svg
titlebutton-close-backdrop-active.svg
titlebutton-close-backdrop.svg
titlebutton-close-hover.svg
titlebutton-close.svg
titlebutton-maximize-active.svg
titlebutton-maximize-backdrop-active.svg
titlebutton-maximize-backdrop.svg
titlebutton-maximize-hover.svg
titlebutton-maximize.svg
titlebutton-menu-active.svg
titlebutton-menu-backdrop-active.svg
titlebutton-menu-backdrop.svg
titlebutton-menu-hover.svg
titlebutton-menu.svg
titlebutton-minimize-active.svg
titlebutton-minimize-backdrop-active.svg
titlebutton-minimize-backdrop.svg
titlebutton-minimize-hover.svg
titlebutton-minimize.svg
titlebutton-shade-active.svg
titlebutton-shade-backdrop-active.svg
titlebutton-shade-backdrop.svg
titlebutton-shade-hover.svg
titlebutton-shade.svg
titlebutton-unmaximize-active.svg
titlebutton-unmaximize-backdrop-active.svg
titlebutton-unmaximize-backdrop.svg
titlebutton-unmaximize-hover.svg
titlebutton-unshade-active.svg
titlebutton-unshade-backdrop-active.svg
titlebutton-unshade-backdrop.svg
titlebutton-unshade-hover.svg
titlebutton-unshade.svg

./WhiteSur-gtk-theme/src/assets/unity:
close_focused_normal.png
close_focused_prelight.png
close_focused_pressed.png
close.png
close_unfocused.png
close_unfocused_prelight.png
close_unfocused_pressed.png
launcher_arrow_ltr_19-1.svg
launcher_arrow_ltr_19.svg
launcher_arrow_ltr_37.svg
launcher_arrow_outline_ltr_19.svg
launcher_arrow_outline_ltr_37.svg
launcher_arrow_outline_rtl_19.svg
launcher_arrow_outline_rtl_37.svg
launcher_arrow_rtl_19.svg
launcher_arrow_rtl_37.svg
launcher_icon_back_150.svg
launcher_icon_back_54.svg
launcher_icon_edge_150.svg
launcher_icon_edge_54.svg
launcher_icon_glow_200.svg
launcher_icon_glow_62.svg
launcher_icon_selected_back_150.svg
launcher_icon_selected_back_54.svg
launcher_icon_shadow_200.svg
launcher_icon_shadow_62.svg
launcher_icon_shine_150.svg
launcher_icon_shine_54.svg
launcher_pip_ltr_19.svg
launcher_pip_ltr_37.svg
launcher_pip_rtl_19.svg
launcher_pip_rtl_37.svg
maximize_focused_normal.png
maximize_focused_prelight.png
maximize_focused_pressed.png
maximize.png
maximize_unfocused.png
maximize_unfocused_prelight.png
maximize_unfocused_pressed.png
minimize_focused_normal.png
minimize_focused_prelight.png
minimize_focused_pressed.png
minimize.png
minimize_unfocused.png
minimize_unfocused_prelight.png
minimize_unfocused_pressed.png
modes
sheet_style_close_focused.png
sheet_style_close_focused_prelight.png
sheet_style_close_focused_pressed.png
unmaximize_focused_normal.png
unmaximize_focused_prelight.png
unmaximize_focused_pressed.png
unmaximize.png
unmaximize_unfocused.png
unmaximize_unfocused_prelight.png
unmaximize_unfocused_pressed.png

./WhiteSur-gtk-theme/src/assets/unity/modes:
launcher_bfb-flat.png  launcher_bfb_ns.png  ubuntu-square.svg

./WhiteSur-gtk-theme/src/assets/xfwm4:
assets-Dark             assets-Dark.svg         assets-Light-nord.svg
assets-Dark-hdpi        assets-Dark-xhdpi       assets-Light-nord-xhdpi
assets-Dark-nord        assets-Light            assets-Light.svg
assets-Dark-nord-hdpi   assets-Light-hdpi       assets-Light-xhdpi
assets-Dark-nord.svg    assets-Light-nord       assets.txt
assets-Dark-nord-xhdpi  assets-Light-nord-hdpi  render-assets.sh

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark-hdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark-nord:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark-nord-hdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark-nord-xhdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Dark-xhdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light-hdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light-nord:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light-nord-hdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light-nord-xhdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/assets/xfwm4/assets-Light-xhdpi:
bottom-active.png              menu-inactive.png
bottom-inactive.png            menu-pressed.png
bottom-left-active.png         right-active.png
bottom-left-inactive.png       right-inactive.png
bottom-right-active.png        shade-active.png
bottom-right-inactive.png      shade-inactive.png
close-active.png               shade-pressed.png
close-inactive.png             stick-active.png
close-prelight.png             stick-inactive.png
close-pressed.png              stick-pressed.png
hide-active.png                title-1-active.png
hide-inactive.png              title-1-inactive.png
hide-prelight.png              title-2-active.png
hide-pressed.png               title-2-inactive.png
left-active.png                title-3-active.png
left-inactive.png              title-3-inactive.png
maximize-active.png            title-4-active.png
maximize-inactive.png          title-4-inactive.png
maximize-prelight.png          title-5-active.png
maximize-pressed.png           title-5-inactive.png
maximize-toggled-active.png    top-left-active.png
maximize-toggled-inactive.png  top-left-inactive.png
maximize-toggled-prelight.png  top-right-active.png
maximize-toggled-pressed.png   top-right-inactive.png
menu-active.png

./WhiteSur-gtk-theme/src/main:
cinnamon  gnome-shell  gtk-2.0  gtk-3.0  gtk-4.0  metacity-1  xfwm4

./WhiteSur-gtk-theme/src/main/cinnamon:
cinnamon-Dark.scss  cinnamon-Light.scss

./WhiteSur-gtk-theme/src/main/gnome-shell:
gnome-shell-theme.gresource.xml  shell-3-28  shell-42-0  shell-46-0
pad-osd.css                      shell-40-0  shell-44-0

./WhiteSur-gtk-theme/src/main/gnome-shell/shell-3-28:
gnome-shell-Dark.scss  gnome-shell-Light.scss

./WhiteSur-gtk-theme/src/main/gnome-shell/shell-40-0:
gnome-shell-Dark.scss  gnome-shell-Light.scss

./WhiteSur-gtk-theme/src/main/gnome-shell/shell-42-0:
gnome-shell-Dark.scss  gnome-shell-Light.scss

./WhiteSur-gtk-theme/src/main/gnome-shell/shell-44-0:
gnome-shell-Dark.scss  gnome-shell-Light.scss

./WhiteSur-gtk-theme/src/main/gnome-shell/shell-46-0:
gnome-shell-Dark.scss  gnome-shell-Light.scss

./WhiteSur-gtk-theme/src/main/gtk-2.0:
common                  gtkrc-Dark-purple-nord  gtkrc-Light-orange-nord
gtkrc-Dark              gtkrc-Dark-red          gtkrc-Light-pink
gtkrc-Dark-blue         gtkrc-Dark-red-nord     gtkrc-Light-pink-nord
gtkrc-Dark-blue-nord    gtkrc-Dark-yellow       gtkrc-Light-purple
gtkrc-Dark-green        gtkrc-Dark-yellow-nord  gtkrc-Light-purple-nord
gtkrc-Dark-green-nord   gtkrc-Light             gtkrc-Light-red
gtkrc-Dark-grey         gtkrc-Light-blue        gtkrc-Light-red-nord
gtkrc-Dark-grey-nord    gtkrc-Light-blue-nord   gtkrc-Light-yellow
gtkrc-Dark-nord         gtkrc-Light-green       gtkrc-Light-yellow-nord
gtkrc-Dark-orange       gtkrc-Light-green-nord  make-gtkrc.sh
gtkrc-Dark-orange-nord  gtkrc-Light-grey        menubar-toolbar-Dark.rc
gtkrc-Dark-pink         gtkrc-Light-grey-nord   menubar-toolbar-Light.rc
gtkrc-Dark-pink-nord    gtkrc-Light-nord
gtkrc-Dark-purple       gtkrc-Light-orange

./WhiteSur-gtk-theme/src/main/gtk-2.0/common:
apps.rc  main.rc  panel.rc  xfce-notify.rc

./WhiteSur-gtk-theme/src/main/gtk-3.0:
gtk-Dark.scss  gtk.gresource.xml  gtk-Light.scss  make_gresource_xml.sh

./WhiteSur-gtk-theme/src/main/gtk-4.0:
gtk-Dark.scss  gtk.gresource.xml  gtk-Light.scss  make_gresource_xml.sh

./WhiteSur-gtk-theme/src/main/metacity-1:
metacity-theme-3.xml  metacity-theme-Dark.xml  metacity-theme-Light.xml

./WhiteSur-gtk-theme/src/main/xfwm4:
themerc-Dark  themerc-Light

./WhiteSur-gtk-theme/src/other:
dash-to-dock  firefox  plank

./WhiteSur-gtk-theme/src/other/dash-to-dock:
_dash-to-dock-3.scss  stylesheet-3.scss
_dash-to-dock-4.scss  stylesheet-4.scss

./WhiteSur-gtk-theme/src/other/firefox:
common            userChrome-Monterey-alt.css  userContent-WhiteSur.css
customChrome.css  userChrome-Monterey.css      WhiteSur
Monterey          userChrome-WhiteSur.css
README.md         userContent-Monterey.css

./WhiteSur-gtk-theme/src/other/firefox/common:
drag-window-headerbar-buttons.css  pages
hide-single-tab.css                parts
hide-window-buttons.css            rounded-window-maximized.css
icons                              symbolic-tab-icons.css
left-tab-close-button.css          system-icons.css
matching-autocomplete-width.css    titlebuttons

./WhiteSur-gtk-theme/src/other/firefox/common/icons:
applications-engineering-symbolic.svg
application-x-addon-blocked-symbolic.svg
application-x-addon-symbolic.svg
audio-muted-symbolic-light.svg
audio-muted-symbolic.svg
audio-playing-symbolic-light.svg
audio-playing-symbolic.svg
autoplay-media-blocked-symbolic.svg
autoplay-media-symbolic.svg
blocked-permission-symbolic.svg
bookmarks-symbolic.svg
bullet-symbolic.svg
character-symbolic.svg
checkbox-checked-symbolic.svg
checkbox-symbolic.svg
drm-symbolic.svg
edit-copy-symbolic.svg
edit-cut-symbolic.svg
edit-find-symbolic.svg
edit-paste-symbolic.svg
firefox-view.svg
folder-download-symbolic.svg
folder-locked-symbolic.svg
folder-symbolic-light.svg
folder-symbolic.svg
forget-history-symbolic.svg
geo.svg
go-next-symbolic-light.svg
go-next-symbolic.svg
go-previous-symbolic-light.svg
go-previous-symbolic.svg
icon.svg
import-symbolic.svg
info-symbolic-light.svg
info-symbolic.svg
key-symbolic.svg
library-symbolic.svg
mail-unread-symbolic.svg
microphone-symbolic.svg
network-workgroup-symbolic-light.svg
network-workgroup-symbolic.svg
notification-symbolic.svg
open-folder-symbolic.svg
open-menu-symbolic.svg
page-action.svg
page-symbolic.svg
pan-down-symbolic-light.svg
pan-down-symbolic.svg
pan-end-symbolic-light.svg
pan-end-symbolic.svg
pan-start-symbolic.svg
pan-up-symbolic.svg
permissions-granted.svg
persistent-storage.svg
picture-in-picture-open.svg
preferences-system-symbolic.svg
preferences-system-time-symbolic-light.svg
preferences-system-time-symbolic.svg
printer-symbolic.svg
process-stop-symbolic.svg
process-working-symbolic-black.svg
process-working-symbolic-light.svg
process-working-symbolic.svg
radio-checked-symbolic.svg
radio-symbolic.svg
reader-mode.svg
save-folder-symbolic.svg
save-to-pocket-light.svg
save-to-pocket-open-light.svg
save-to-pocket-open.svg
save-to-pocket.svg
screen-blocked-symbolic.svg
screenshot-symbolic.svg
screen-symbolic.svg
security-broken-symbolic.svg
security-warning-symbolic.svg
select-symbolic.svg
starred-symbolic.svg
star-symbolic.svg
sync.svg
tab-audio-blocked-small-light.svg
tab-audio-blocked-small.svg
tab-new-symbolic.svg
tab-sync-symbolic-light.svg
tab-sync-symbolic.svg
toggle-right-sidebar-symbolic.svg
toggle-sidebar-symbolic.svg
tool-profiler.svg
tracking-protection-animatable.svg
tracking-protection.svg
translations.svg
user-home-symbolic.svg
user-not-tracked-dark.svg
user-not-tracked.svg
view-fullscreen-symbolic.svg
view-more-horizontal-symbolic.svg
view-refresh-symbolic.svg
view-restore-symbolic.svg
window-close-symbolic-light.svg
window-close-symbolic.svg
window-maximize-symbolic.svg
window-minimize-symbolic.svg
window-new-symbolic.svg
window-restore-symbolic.svg
zoom-in-symbolic.svg
zoom-out-symbolic.svg

./WhiteSur-gtk-theme/src/other/firefox/common/pages:
common.css  newtab.css  privatebrowsing.css  reader.css

./WhiteSur-gtk-theme/src/other/firefox/common/parts:
buttons.css        entries.css                   popups-contents.css
buttons-fixes.css  findbar.css                   popups.css
controls.css       headerbar.css                 remove-white-flash.css
csd.css            headerbar-private-urlbar.css  titlebutton-dark.css
custom-icons.css   icons.css                     titlebutton-light.css
dialogs.css        notification.css              video-player.css

./WhiteSur-gtk-theme/src/other/firefox/common/titlebuttons:
titlebutton-backdrop-dark.svg
titlebutton-backdrop.svg
titlebutton-close-active-dark.svg
titlebutton-close-active.svg
titlebutton-close-backdrop-dark.svg
titlebutton-close-backdrop.svg
titlebutton-close-dark.svg
titlebutton-close-hover-dark.svg
titlebutton-close-hover.svg
titlebutton-close.svg
titlebutton-maximize-active-dark.svg
titlebutton-maximize-active.svg
titlebutton-maximize-backdrop-dark.svg
titlebutton-maximize-backdrop.svg
titlebutton-maximize-dark.svg
titlebutton-maximize-hover-dark.svg
titlebutton-maximize-hover.svg
titlebutton-maximize.svg
titlebutton-minimize-active-dark.svg
titlebutton-minimize-active.svg
titlebutton-minimize-backdrop-dark.svg
titlebutton-minimize-backdrop.svg
titlebutton-minimize-dark.svg
titlebutton-minimize-hover-dark.svg
titlebutton-minimize-hover.svg
titlebutton-minimize.svg
titlebutton-unmaximize-active-dark.svg
titlebutton-unmaximize-active.svg
titlebutton-unmaximize-backdrop-dark.svg
titlebutton-unmaximize-backdrop.svg
titlebutton-unmaximize-hover-dark.svg
titlebutton-unmaximize-hover.svg

./WhiteSur-gtk-theme/src/other/firefox/Monterey:
colors                    parts                      theme-alt.css
left_header_button_3.css  right_header_button_3.css  theme.css
left_header_button_4.css  right_header_button_4.css
left_header_button_5.css  right_header_button_5.css

./WhiteSur-gtk-theme/src/other/firefox/Monterey/colors:
dark.css  light.css

./WhiteSur-gtk-theme/src/other/firefox/Monterey/parts:
headerbar-urlbar.css  tabsbar.css      toolbox.css
tabsbar-alt.css       toolbox-alt.css

./WhiteSur-gtk-theme/src/other/firefox/WhiteSur:
colors  parts  theme.css

./WhiteSur-gtk-theme/src/other/firefox/WhiteSur/colors:
dark.css  light.css

./WhiteSur-gtk-theme/src/other/firefox/WhiteSur/parts:
headerbar-urlbar.css  tabsbar.css  toolbox.css

./WhiteSur-gtk-theme/src/other/plank:
theme-Dark  theme-Light

./WhiteSur-gtk-theme/src/other/plank/theme-Dark:
dock.theme

./WhiteSur-gtk-theme/src/other/plank/theme-Light:
dock.theme

./WhiteSur-gtk-theme/src/sass:
cinnamon              gtk                  _theme-options-temp.scss
_colors-palette.scss  _gtk-base.scss       _variables.scss
_colors.scss          _gtk-base-temp.scss
gnome-shell           _theme-options.scss

./WhiteSur-gtk-theme/src/sass/cinnamon:
_common.scss  _drawing.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell:
common                 extensions-46-0        _widgets-42-0.scss
_common.scss           _extensions-46-0.scss  widgets-44-0
_drawing.scss          widgets-3-28           _widgets-44-0.scss
extensions-3-28        _widgets-3-28.scss     widgets-46-0
_extensions-3-28.scss  widgets-40-0           _widgets-46-0.scss
extensions-40-0        _widgets-40-0.scss
_extensions-40-0.scss  widgets-42-0

./WhiteSur-gtk-theme/src/sass/gnome-shell/common:
_a11y.scss           _ibus-popup.scss      _popovers.scss
_app-grid.scss       _keyboard.scss        _screen-shield.scss
_base.scss           _login-dialog.scss    _scrollbars.scss
_buttons.scss        _looking-glass.scss   _search-entry.scss
_calendar.scss       _message-list.scss    _search-results.scss
_check-box.scss      _misc.scss            _slider.scss
_corner-ripple.scss  _network-dialog.scss  _switcher-popup.scss
_dash.scss           _notifications.scss   _switches.scss
_dialogs.scss        _osd.scss             _tiled-previews.scss
_entries.scss        _overview.scss        _workspace-switcher.scss
_hotplug.scss        _panel.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/extensions-3-28:
_dash-to-dock.scss  _misc.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/extensions-40-0:
_dash-to-dock.scss  _misc.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/extensions-46-0:
_dash-to-dock.scss  _misc.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/widgets-3-28:
_app-grid.scss      _other.scss     _window-picker.scss
_dash.scss          _overview.scss  _workspace-thumbnails.scss
_login-dialog.scss  _panel.scss
_osd.scss           _popovers.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/widgets-40-0:
_app-grid.scss  _panel.scss          _window-picker.scss
_dash.scss      _popovers.scss       _workspace-thumbnails.scss
_osd.scss       _screen-shield.scss
_overview.scss  _search-entry.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/widgets-42-0:
_app-grid.scss  _popovers.scss        _screenshot.scss
_osd.scss       _quick-settings.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/widgets-44-0:
_app-grid.scss  _quick-settings.scss

./WhiteSur-gtk-theme/src/sass/gnome-shell/widgets-46-0:
_app-grid.scss  _dash.scss  _message-list.scss  _notifications.scss

./WhiteSur-gtk-theme/src/sass/gtk:
apps            _colors-libadwaita.scss  _common-4.0.scss
_apps-3.0.scss  _colors-public.scss      _drawing.scss
_apps-4.0.scss  _common-3.0.scss

./WhiteSur-gtk-theme/src/sass/gtk/apps:
_budgie.scss      _gnome-40.0.scss  _lightdm.scss  _nemo.scss
_elementary.scss  _granite.scss     _mate.scss     _unity.scss
_gnome-3.22.scss  _libadwaita.scss  _misc.scss     _xfce.scss
rashik@rashik-HP-Laptop-15-da1xxx:~$ 
</pre>
</pre>

+ <b>-1 (one per line):</b>
Displays one file per line.
<pre>

Ex- 

<b>Input:</b>
<pre>

ls -1
</pre>

<b>Output:</b>
<pre>

Desktop
discord.deb
Documents
Downloads
google-chrome-stable_current_amd64.deb
Music
Pictures
Public
Python-3.12.0
snap
Templates
Videos
WhiteSur-gtk-theme
</pre>
</pre>

+ <b>--color:</b>
Displays different file types in color for better visualization.

<pre>

<b>Input:</b>
<pre>

ls -color
</pre>

<b>Output:</b>

<pre>

total 148
drwxrwxr-x 2 rashik   4096 Sep  7 15:02  nnn
drwxrwxr-x 3 rashik   4096 Sep  8 10:09 'linux comman line'
-rw-rw-r-- 1 rashik 127823 Sep 12 15:46  lecture0-720p-en.txt
-rw-rw-r-- 1 rashik   6615 Sep 12 12:42  file1.txt
-rw-rw-r-- 1 rashik    465 Sep  7 15:02  cpfile1.txt
</pre>
</pre>


## Combined Options:

You can combine options for more detailed listings:

<pre>

ls -lah
</pre>

This command will list all files, including hidden ones, in long format with human-readable file sizes.

<pre>

Ex-

<b>Input:</b>
<pre>

ls -lah
</pre>

<b>Output:</b>

<pre>

total 156K
drwxrwxr-x 4 rashik rashik 4.0K Sep 14 09:47  .
drwxr-xr-x 7 rashik rashik 4.0K Sep 12 12:12  ..
-rw-rw-r-- 1 rashik rashik  465 Sep  3 11:59  cpfile1.txt
-rw-rw-r-- 1 rashik rashik 6.5K Sep 12 12:42  file1.txt
-rw-rw-r-- 1 rashik rashik 125K Sep 12 15:44  lecture0-720p-en.txt
drwxrwxr-x 3 rashik rashik 4.0K Sep  3 14:17 'linux comman line'
drwxrwxr-x 2 rashik rashik 4.0K Sep  7 15:02  nnn
</pre>

<b>Input:</b>
<pre>

ls -ltrh
</pre>

<b>Output:</b>
<pre>

total 148K
-rw-rw-r-- 1 rashik rashik  465 Sep  3 11:59  cpfile1.txt
drwxrwxr-x 3 rashik rashik 4.0K Sep  3 14:17 'linux comman line'
drwxrwxr-x 2 rashik rashik 4.0K Sep  7 15:02  nnn
-rw-rw-r-- 1 rashik rashik 6.5K Sep 12 12:42  file1.txt
-rw-rw-r-- 1 rashik rashik 125K Sep 12 15:44  lecture0-720p-en.txt
</pre>
</pre>

