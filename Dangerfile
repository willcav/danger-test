MAX_LINES_CHANGED = 5

warn("Danger warning")

def check_lines_changed
  added_lines = diff.added_lines
  deleted_lines = diff.deleted_lines
  message(added_lines)
  message(deleted_lines)
  lines_changed = added_lines + deleted_lines
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end