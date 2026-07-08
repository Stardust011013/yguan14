---
show: false
width: 6
date: 2020-01-12 00:01:00 +0800
---
<div class="m-4">
    <h5>Education</h5>
    <ul class="list-unstyled mb-1">
        {% for item in site.data.profile.education %}
        <li class="media mb-1">
            <img src="{{ item.logo | relative_url }}" alt="{{ item.name }}" style="width: 18px;" class="mr-1 mt-1">
            <div class="media-body">
                <div>
                    {% if item.url %}
                    <a class="text-body" target="_blank" rel="noopener" href="{{ item.url }}">{{ item.name }}</a>
                    {% else %}
                    {{ item.name }}
                    {% endif %}
                </div>
                <div class="small">
                    {% if item.dept_url %}
                    <a class="text-body" target="_blank" rel="noopener" href="{{ item.dept_url }}">{{ item.dept }}</a>
                    {% else %}
                    {{ item.dept }}
                    {% endif %}
                </div>
                <div class="small d-flex">
                    <div>{{ item.position }}</div>
                    <div class="mt-auto ml-auto no-break"><em>{{ item.date }}</em></div>
                </div>
            </div>
        </li>
        {% endfor %}
    </ul>
</div>
