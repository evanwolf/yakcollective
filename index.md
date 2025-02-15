---
---
# The Yak Collective

The Yak Collective is a network of over 300 independent consultants, coaches, and freelancers with varied technical and creative skills. You can learn more about us on the [About page](/about/).

We are available both for individual projects on specific topics that match our skills, and for larger collaborative projects we can take on as a group, bringing together the mix of skills necessary. Check out our [members](/members/) and [projects](/projects/), read some of [our latest thoughts](/writings/), and get in touch with any of us if you'd like to learn more.

Follow us on [Twitter](https://twitter.com/yak_collective), [Facebook](https://www.facebook.com/theyakcollective/), or [LinkedIn](https://www.linkedin.com/company/yak-collective/) to stay in the loop.

## Featured Yak

{% assign member_id = site.data.featured_yak.name | replace: ".md", "" | replace: ".html", "" %}
{% include widget-member-card.html member=member_id %}

## Most Recent Project

{% assign project = site.pages | where: "layout", "page-project"
                               | where_exp: "project", "project.date <= site.time or site.future == true"
                               | sort: "date"
                               | reverse
                               | first %}
{% assign project_id = project.name | replace: ".md", "" | replace: ".html", "" %}
{% include widget-project-box.html project=project_id %}
