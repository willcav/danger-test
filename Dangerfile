require 'danger'

MAX_LINES_CHANGED = 5

def check_lines_changed
  diff = github.pr_diff
  message(git)
  if 5 > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed