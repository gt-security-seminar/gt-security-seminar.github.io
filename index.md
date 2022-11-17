---
layout: default
meta-description: "Georgia Institute of Technology Security Seminar"
---

The **Georgia Institute of Technology Security Seminar**, sponsored by [School of Cybersecurity and Privacy](https://scp.cc.gatech.edu/), is an opportunity for Georgia Tech faculty and students working in computer security and privacy to present their research and invite guest speakers. 

To receive regular updates on upcoming talks, as well as Zoom links to join them virtually, please subscribe to the mailing list.

If you're interested in presenting a talk, please contact us with a date and talk proposal.

**Founder/Organizer:** [Pradyumna Shome](https://pradyumnashome.com/)

**Email Address:** [pradyumna.shome@gatech.edu](mailto://pradyumna.shome@gatech.edu)

**Location:** Vinings, 10th Floor, Coda, 756 West Peachtree St NW, Atlanta, GA 30332

**Time:** Wednesdays at 12pm ET

**Mailing List:** [https://mailman.cc.gatech.edu/mailman/listinfo/scp-security-seminar](https://mailman.cc.gatech.edu/mailman/listinfo/scp-security-seminar)

# Upcoming Talks

<div class="talk-list">
  {% assign now_time = 'now' | date: '%s' | plus: 0 %}
  {% for talk in site.data.talks %}
  {% assign talk_time = talk.date | date: '%s' | plus: 0 %}
  {% if talk_time < now_time %}
    {% continue %}
  {% endif %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter"><a href="{{ talk.website }}">{{ talk.speaker }}</a></div>
  {% if talk.title %}
  <div><span>{{ talk.title }}</span></div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    </details>
  {% endif %}
  {% if talk.biography %}
    <details>
    <summary>Biography</summary>
    {{ talk.biography }}
    </details>
  {% endif %}
  {% if talk.recording %}
    <a href="{{ talk.recording }}">Recording</a>
  {% endif %}
  {% if talk.livestream %}
    <a href="{{ talk.livestream }}">Livestream Link</a>
  {% endif %}
  </div>
  {% endfor %}
</div>

# Past Talks

<div class="talk-list">
  {% for talk in site.data.talks %}
  {% assign talk_time = talk.date | date: '%s' | plus: 0 %}
  {% if talk_time >= now_time %}
    {% continue %}
  {% endif %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter"><a href="{{ talk.website }}">{{ talk.speaker }}</a></div>
  {% if talk.title %}
  <div><span>{{ talk.title }}</span></div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    </details>
  {% endif %}
  {% if talk.biography %}
    <details>
    <summary>Biography</summary>
    {{ talk.biography }}
    </details>
  {% endif %}
  {% if talk.recording %}
    <a href="{{ talk.recording }}">Recording</a>
  {% endif %}
  {% if talk.livestream %}
    <a href="{{ talk.livestream }}">Livestream Link</a>
  {% endif %}
  </div>
  {% endfor %}
</div>

Credit to the [Stanford Systems Seminar](https://systemsseminar.cs.stanford.edu/) for the website!
