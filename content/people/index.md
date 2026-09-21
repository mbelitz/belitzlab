---
title: People
date: 2022-10-24

type: landing

sections:
  - block: people
    content:
      title: Meet the Team
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
          - Principal Investigator
          - Postdocs
          - Grad Students
          - Undergraduate Researchers
          - Alumni
      sort_by: Params.last_name
      sort_ascending: true
    design:
      show_interests: false
      show_role: true
      show_social: true

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        Interested in joining the lab? We welcome inquiries from prospective students at all career stages (M.S., Ph.D., postdocs). Please read [how to apply](../resources/how-to-apply/) for details.

        <script>
        document.addEventListener('DOMContentLoaded', function () {
          document.querySelectorAll('.wg-people .people-person').forEach(function (card) {
            var nameLink = card.querySelector('.portrait-title h2 a');
            var title = card.querySelector('.portrait-title');
            if (!nameLink || !title || title.querySelector('.bl-learn-more')) return;
            var link = document.createElement('a');
            link.href = nameLink.getAttribute('href');
            link.className = 'bl-learn-more';
            link.innerHTML = 'Learn more &rarr;';
            title.appendChild(link);
          });
        });
        </script>
    design:
      columns: '1'
---