require 'danger'

MAX_LINES_CHANGED = 5

def check_lines_changed
  pr_diff = github.pr_diff
  lines_changed = pr_diff.lines_of_code
  message(lines_changed)
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed