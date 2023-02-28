MAX_LINES_CHANGED = 5

def check_lines_changed
  pr_diff = `git diff --shortstat origin/master...#{danger.github.pr_head_ref}`
  matches = /(\d+) insertions.*(\d+) deletions/.match(pr_diff)
  lines_changed = matches[1].to_i + matches[2].to_i
  message(pr_diff)
  message(matches)
  message(lines_changed)
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed