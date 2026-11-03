# Forgejo workflows

This directory holds no workflows on purpose. Forgejo reads only the first
workflow directory it finds (`.forgejo/workflows`, then `.gitea/workflows`,
then `.github/workflows`), so its presence stops Forgejo from running
`.github/workflows/schedules.yml`, which is written for GitHub Actions and
fails on Forgejo every week.

GitHub ignores this directory and keeps running the schedule.
Delete this directory to let Forgejo run `.github/workflows` again.
