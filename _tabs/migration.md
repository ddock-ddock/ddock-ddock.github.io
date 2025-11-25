---
icon: fas fa-route
order: 8
mermaid: true
---
{% include lang.html %}

마이그레이션 - 타사 ERP 데이터 추출 가이드

<div class="category-root">
  {% assign tag_groups = "회계,전자결재" | split: "," %}
  {% for tag in tag_groups %}
    {% assign posts = site.posts | where_exp: "p", "p.tags contains '마이그레이션' and p.tags contains tag" %}
    {% if posts.size > 0 %}
      <div class="folder-box">
        <div class="folder-header"
             onclick="this.classList.toggle('open'); this.nextElementSibling.classList.toggle('hidden')">
          <i class="far fa-folder-open fa-fw text-muted"></i>
          {{ tag }} 마이그레이션
          <small class="text-muted">{{ posts | size }} 포스트</small>
          <i class="fas fa-chevron-down arrow-icon"></i>
        </div>
        <ul class="folder-list hidden">
          {% for post in posts %}
            <li class="folder-item">
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </li>
          {% endfor %}
        </ul>
      </div>
    {% endif %}
  {% endfor %}
</div>

<style>
.category-root {
  margin-top: 1.5rem;
}
.folder-box {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 6px;
  margin-bottom: 1rem;
  overflow: hidden;
}
.hidden {
  display: none;
}
.folder-header {
  display: flex;
  align-items: center;
  padding: 0.75rem 1rem;
  font-weight: 600;
  cursor: pointer;
  background: #f7f7f7;         
  border-bottom: 1px solid #ddd;
  color: #222;
}
.folder-header .text-muted {
  margin-left: 0.5rem;
  color: #666;
  font-size: 0.9rem;
}
.arrow-icon {
  margin-left: auto;
  color: #666;
  transition: transform 0.2s ease;
}
.folder-header.open .arrow-icon {
  transform: rotate(180deg);
}
.folder-list {
  list-style: none;
  margin: 0;
  padding: 0;
  border-top: 1px solid #ddd;
}
.folder-item {
  padding: 0.75rem 1rem;
  border-bottom: 1px solid #ddd;
}
.folder-item:last-child {
  border-bottom: none;
}
.folder-item a {
  color: #0066cc;                 
  text-decoration: none;
}
.folder-item a:hover {
  text-decoration: underline;
}

@media (prefers-color-scheme: dark) {
  .folder-box {
    background: #1e1e1e;
    border: 1px solid #333;
  }
  .folder-header {
    background: #2a2a2a;
    border-bottom: 1px solid #333;
    color: #fff;
  }
  .folder-header .text-muted {
    color: #aaa;
  }
  .arrow-icon {
    color: #aaa;
  }
  .folder-list {
    border-top: 1px solid #333;
  }
  .folder-item {
    border-bottom: 1px solid #333;
  }
  .folder-item a {
    color: #59afff;      
  }
}

</style>
