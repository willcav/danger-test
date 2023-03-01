require 'danger'
require 'json'

MAX_LINES_CHANGED = 1

def check_lines_changed
  diff = github.pr_diff
  message(git.lines_of_code)
  if 5 > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed