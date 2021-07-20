
# Warn when there is a big PR
warn("Big PR") if git.lines_of_code > 500

# Give a warning if the PR description is empty
warn("Please provide a PR description") if github.pr_body.length < 5

# Give a warning when a PR is over expected size
warn("This PR is quite a big one! Try splitting this into separate tasks next time 🙂") if git.lines_of_code > 500

message("Thank you for your work @#{github.pr_author} 🎉 You might find a few suggestions from me below 😉")


# AndroidLint
android_lint.report_file = "artifact/lint-report/lint-results-debug.xml"
android_lint.skip_gradle_task = true
android_lint.severity = "Warning"
android_lint.filtering = false
android_lint.lint(inline_mode: true)

# APK Stats
apkstats.apkanalyzer_path = ".github/apkanalyzer/apkanalyzer"
apkstats.apk_filepath = "artifact/build-apk/app-debug.apk"
apkstats.file_size #=> Fixnum
apkstats.download_size #=> Fixnum
apkstats.required_features #=> Array<String> | Nil
apkstats.non_required_features #=> Array<String> | Nil
apkstats.permissions #=> Array<String> | Nil
apkstats.min_sdk #=> String | Nil
apkstats.target_sdk #=> String | Nils
apkstats.reference_count #=> Fixnum
apkstats.dex_count #=> Fixnum
