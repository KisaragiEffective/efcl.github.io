require 'rake-jekyll'

Rake::Jekyll::GitDeployTask.new(:deploy) do |t|
    # master branch for machine
    t.deploy_branch = 'master'

    # Skip commit and push when building a pull request or env. variable
    # SKIP_COMMIT represents truthy.
    t.skip_commit = -> {
        ENV['CI_PULL_REQUEST'].nil? ||
        %w[yes y true 1].include?(ENV['SKIP_COMMIT'].to_s.downcase) ||
        !ENV['CIRCLE_BRANCH'].to_s.include?("develop")
    }
end
