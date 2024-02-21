# Danger test

## Danger
Danger run during CI process and give teams the chance to automate common code review chores. Whenever someone creates a PR, a check will run and then Danger will comment what’s wrong in the PR.

### Project Features
- There is 1 rule added in this repo just for example, that check the maximum lines changed in one PR and set a comment on the PR thread

```Ruby
MAX_LINES_CHANGED = 1

def check_lines_changed
  total_lines_changed = git.lines_of_code
  if total_lines_changed > MAX_LINES_CHANGED
    warn("Seu PR excede o número máximo de linhas (#{MAX_LINES_CHANGED}). Por favor, considere dividí-lo em PRs menores.")
  end
end

check_lines_changed
```
