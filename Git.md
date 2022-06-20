# Git Instructions

## Git Ignore
### TypeScript
Use this [.gitignore](https://raw.githubusercontent.com/microsoft/TypeScript-Node-Starter/master/.gitignore).

## Branching
When creating a new branch for any reason, **always branch from main**, this reduces complicated relations between branches.

### Naming
To name a new branch always prefix the name with the type of change it includes.

| Type of changes | Prefix      |
|-----------------|-------------|
| New feature     | `FEATURE/`  |
| Feature change  | `CHANGE/`   |
| Bug or error    | `FIX/`      |
| Refactoring     | `REFACTOR/` |

After the prefix include a short description of what will be done. Some examples are:
- `FEATURE/settings_panel`
- `FEATURE/dark_mode`
- `CHANGE/get_less_user_info`
- `FIX/qr_reader_crash`
- `FIX/not_centered_play`
- `REFACTOR/user_service_20220615`

### Merging
When merging a branch back into `main` a pull-request needs to be created. In order for this to be merged at least one code-review is required. A pull-request should be formatted as follows:

```
# Description

~~Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.~~

Fixes # (issue)

## Type of change

Please check all relevant types.

- [ ] Bug fix (non-breaking change which fixes an issue).
- [ ] New feature (non-breaking change which adds functionality).
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected).
- [ ] This change requires a documentation update.
- [ ] Project refactoring.

# Checklist:

- [ ] My code follows the [code standard](https://github.com/Dot-Zero-Technologies/code-standard).
- [ ] I have commented my code, particularly in hard-to-understand areas.
- [ ] My changes generate no new warnings.
- [ ] Any dependent changes have been merged and published in downstream modules.
```

*[Original template](https://embeddedartistry.com/blog/2017/08/04/a-github-pull-request-template-for-your-projects/)*