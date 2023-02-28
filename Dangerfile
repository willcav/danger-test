require 'danger'

MAX_LINES_CHANGED = 5

def lines_changed(diff)
  additions = deletions = 0
  diff.each_line do |line|
    case line[0..0]
    when '+'
      additions += 1
    when '-'
      deletions += 1
    end
  end
  {additions: additions, deletions: deletions}
end

def check_lines_changed
  diff = github.pr_diff
  message(lines_changed(diff))
  if 5 > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed