MAX_LINES_CHANGED = 5

def check_lines_changed()
  pr_diff = github.pr_diff
  added_lines = pr_diff.added_lines
  deleted_lines = pr_diff.deleted_lines
  message(added_lines)
  message(deleted_lines)
  lines_changed = added_lines + deleted_lines
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed()