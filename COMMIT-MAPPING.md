# 候选 ↔ 真实提交 ↔ 树 映射（可读交付）

回应平台第 4 条 CODE 意见中的「272 完整登记与 509 根树映射仍缺独立可读对照」与「登记完整提交链接 404 原因未确认」。生成时间 2026-10-19T06:10:26Z。

## 结论口径（先说边界）

1. **平台候选 id 不是 Git 提交 id。** 用候选 id 拼 `/commit/<候选id>` 必然 404，这是标识符类型问题，不需要仓库权限即可判定。
2. 下表由学员本机**独立反查**得到：取平台 `show` 返回的每个候选 `tree` 字段，在分支 `codex/task-01-harness`（远端 tip 实测 `88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca`，`git ls-remote` 于 2026-10-19T06:10:26Z 复测）的全部提交里，找 `git log -1 --format=%T` 与之全等的提交。**匹配依据是树 OID 全等**，不是平台字段声明，也不是自述。
3. 可核性边界：教师若打不开课程练习仓库（私有），就只能核对本公开仓库内的文件与逐张哈希，无法独立复核第 2 条的反查过程。所以本轮把「教师必须能读」的东西（15 张 PNG 原图与 `layout-report.json` 及逐张哈希）放进本仓库；把「需要私有仓库权限才能复核」的提交树反查写成下面的可执行口径。本人不将反查过程表述为已由教师独立复核。

## 已建立全等映射的候选（13/16）

| 候选 id | 候选 tree | 全等提交 | 相对父提交路径数 | 提交说明 | 父提交 |
|---|---|---|---|---|---|
| `54f4b2dd-1547-49bb-875d-ad932df7bad8` | `3dede69e73206b15f8e0342382b4b22ab6bfed56` | `3ac3c633c69ea8b307cf8ea2b9e36480b9b1b274` | 18 | feat(task-03): buyer browsing and spec selection | `83f68b821204` |
| `701d2e08-812d-4220-a99b-fcb6b8ba5530` | `2b4e2ce6d46bec815c5c3116c9c248d7c5a0a6bc` | `81187100a325f45cfa1cbd4738f8e8602cd2114a` | 5 | docs(task-03): add readable verification reports for readback item 3 | `d65fde3b179c` |
| `1318335f-aac2-4adb-8145-c7b5468f832f` | `7ea9baa956a8fb8c16fa5b71c5ab71283be877b3` | `5686781012495ac0e04365cebaf5a140871f4a7e` | 6 | docs(task-03): strengthen assertions per teacher review feedback | `81187100a325` |
| `1465fd38-4fbc-479a-a120-383ba557116f` | `e65cf27a62fe4c6882ab4921eeab1d331c23f77b` | `0e561c96cc54ef770456bf56e6335f3d7e386ab0` | 7 | test(task-03): add readable source-mapping and layout capture scripts | `35c104f5d73c` |
| `50eb704c-e382-4567-8800-63742ffb4887` | `69d2326a4844b950a5b47f7929a1886a101a78bb` | `bcb9e9f879784b311351739f3bea6656ab609e3b` | 3 | docs(task-03): record per-state hit-test, text and screenshot fingerprints | `0e561c96cc54` |
| `387d7efc-a55d-4c11-b152-605a73578fd0` | `6e471206c33277e56c5aafdb3493267ddd7d7cd3` | `94ef27a66eb69af44258469142582440d70054eb` | 5 | docs(task-03): roll the rerun evidence into the readable report | `bcb9e9f87978` |
| `0dd869c4-9168-4ebd-b173-b1ab9cfd3ef6` | `e133436594a8436a5c86f5068fe3e7060a9a7ccc` | `7b24ef9f1da1b28e935780871050b6129dadc80b` | 4 | fix(task-03): resolve buyer sessions and inventory feedback | `94ef27a66eb6` |
| `cc37c673-f850-4c57-bbbb-fdd7dac6dc5a` | `d34852e90be0505981c5c5dea64d6accac179f4d` | `03cfeb6e280d135f71488e3f66a0fd273704f6b1` | 2 | fix(task-03): keep buyer sessions out of host routes | `7b24ef9f1da1` |
| `1921f5cb-250c-4a7e-95d1-5d7d70deefbd` | `13e1bda09403c1c893103d5b994daf96f79a33ab` | `b9f376ddf3f874d2dacbb315e593792ad736e11a` | 2 | fix(task-03): reject non-host sessions on host routes | `03cfeb6e280d` |
| `50901424-6e8e-4905-a2dd-dcf0541b93aa` | `ad9358c8ba38e342b1e73e5e4d9611feb69358a6` | `272944c4f28a4a55f1a643919f613d87f22e6efd` | 3 | docs(task-03): align latest verification evidence | `b9f376ddf3f8` |
| `9e4f955d-60b2-44d1-9965-70645e70bdc5` | `2088d51d17cf98b6fe860df0b9ae8ed624400242` | `0208ae7a5178dfdcba736bf52754b0fc282cfc2b` | 6 | docs(task-03): re-run current-version assertions with session gating | `272944c4f28a` |
| `9bc48ead-8f50-46a6-ae54-2a7455605e76` | `f8062427a67a67c9dc8dd46ef159bbd39057b6a4` | `643e29f9d7eee8981d5ce5e78a6c6aaafef47e2d` | 3 | docs(task-03): record current-version layout and text assertions | `0208ae7a5178` |
| `f7a797a0-c7a9-4558-9ea2-e5c12ef9c8fb` | `1803436b8763c309737720cca7d6f9cb393b6ea9` | `88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca` | 3 | docs(task-03): write the current-version readable verification report | `bb7e0a90fd03` |

与第 4 条直接相关的两项：

- 登记提交 `272944c4f28a4a55f1a643919f613d87f22e6efd`（根树 `ad9358c8ba38e342b1e73e5e4d9611feb69358a6`）＝ 候选 `50901424-6e8e-4905-a2dd-dcf0541b93aa`（tree `ad9358c8ba38e342b1e73e5e4d9611feb69358a6`）的全等提交。
- 截图写入提交 `bb7e0a90fd03d688aa0c6c3497e266e19f411ea4` 含二进制差异，按候选通道限制**不作为候选**，只能作分支仓库文件读取；其 `docs/evidence/task-03-screenshots/` 下 15 张 PNG 与 `layout-report.json` 已逐张原样放入本公开仓库，逐文件哈希与 blob OID 见 `task-03-screenshots/MANIFEST.md`。

## 业务源码同一性（可复算，不依赖权限）

- `packages/` 子树 OID：`99555a2a0422d2661cc5bee31a6d3803a2dc69a8`
- 该子树同时是业务提交 `b9f376ddf3f874d2dacbb315e593792ad736e11a`、登记提交 `272944c4f28a4a55f1a643919f613d87f22e6efd` 与分支 tip `88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca` 的 `packages/` 子树。三者同树，所以「本轮未改业务源码」是可复算事实，不只是自述。
- 历史代码基线 `3ac3c633c69ea8b307cf8ea2b9e36480b9b1b274` 的 `packages/` 子树是 `1165260c21a5415acb1b3d93ac9bbf9e82a598ee`，与上者不同，因此旧「与 3ac 全等」与旧 38/72 口径不再用于当前组合。

## 未能建立全等映射的候选（3 个，如实保留）

- `68129c90-d978-4b91-8384-420b6a990eb5`（tree `f66817485111d97c393b6e7316ecbc898e208350`）：该 tree 对象在仓库对象库中存在（`git cat-file -t` 返回 tree），内容是全仓 152 条目快照，但既不是本分支任何提交的根树，也不是根目录的直接子树，推测属早期重写历史或其他分支状态。**本人不猜测其对应提交，不把它计入映射结论。**
- `09479a33-d85c-4bf7-9575-e0b4ece4aa66`（tree `948cc93a6537557bc60661ca7521f66f412e47e1`）：该 tree 对象在仓库对象库中存在（`git cat-file -t` 返回 tree），内容是全仓 152 条目快照，但既不是本分支任何提交的根树，也不是根目录的直接子树，推测属早期重写历史或其他分支状态。**本人不猜测其对应提交，不把它计入映射结论。**
- `fc9cdd85-6876-456a-86b9-b5e2d1be4644`（tree `092d4ec9f368ae2eb17db538822ffa499267dda4`）：该 tree 对象在仓库对象库中存在（`git cat-file -t` 返回 tree），内容是全仓 152 条目快照，但既不是本分支任何提交的根树，也不是根目录的直接子树，推测属早期重写历史或其他分支状态。**本人不猜测其对应提交，不把它计入映射结论。**

## 关于 404

- 平台给出的 `https://github.com/fly-ai-academy/practice-…` 是私有课程仓库。教师按 40 位完整提交打开仍 404，与「候选 id 被误当提交」是两类问题：前者属访问权限/访问渠道，后者属标识符类型。
- 本人无法在本地验证教师账号对该私有仓库的可见性，也不会擅自改动课程仓库可见性、远端配置或平台登记项。若需要教师获得私有仓库读取权限，请由教师与项目负责人确认；本轮改用本公开仓库提供第 4 条要求的可读原文件与哈希对照。

## 复核口径

教师有私有仓库权限时可自行执行：

```text
git rev-list 88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca | while read c; do echo "$(git log -1 --format=%T $c) $c"; done
git rev-parse 88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca:packages
git cat-file -p <候选 tree OID>
git merge-base --is-ancestor <上表每个提交> 88b5a5a17b4ae3ac2b87a1e8f580d2960b284eca && echo reachable
```

无需私有仓库权限即可执行的本仓库核对：`sha256sum task-03-screenshots/*.png`（或 Windows `certutil -hashfile <png> SHA256`），结果应与 `task-03-screenshots/MANIFEST.md` 表格逐张全等，且这些哈希值本身已登记在平台已审候选的 `docs/evidence/task-03-layout-raw.txt` 中。
