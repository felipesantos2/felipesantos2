<!-- ###olá 👋<br>
###Meu nome é Felipe <br>
###Atualmente eu estou estudando HTML e CSS<br>
###Wordpress e php<br>
###No futuro eu vou pro laravel<br>
depois que eu me sentir bem com HTML, CSS e o PHP<br>
###meta de virar um dev
 -->

<!--
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: felipesantos2
          template: terminal
          base: header, activity, repositories
          config_timezone: America/Sao_Paulo
          plugin_habits: yes
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_isocalendar: yes
          plugin_isocalendar_duration: full-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 16
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_lines: yes
          plugin_notable: yes
          plugin_notable_from: organization
          plugin_notable_repositories: yes
          plugin_people: yes
          plugin_people_limit: 24
          plugin_people_size: 28
          plugin_people_types: followers, following
          plugin_projects: yes
          plugin_projects_limit: 4
          plugin_stars: yes
          plugin_stars_limit: 4
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: starred
          plugin_topics_sort: activity
 



