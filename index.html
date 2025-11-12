---
layout: none
title: Sample Files
---
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{{ page.title }}</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans JP", "Hiragino Kaku Gothic ProN", Meiryo, sans-serif; line-height: 1.6; margin: 24px; }
    h1 { font-size: 20px; margin: 0 0 16px; }
    p.note { color: #555; margin: 0 0 16px; }
    ul { list-style: none; padding: 0; margin: 0; }
    li { border: 1px solid #e5e5e5; border-radius: 8px; padding: 12px 14px; margin: 10px 0; display: flex; align-items: center; justify-content: space-between; gap: 12px; }
    .name { font-weight: 600; overflow-wrap: anywhere; }
    .ext { color: #666; font-size: 12px; }
    .actions { display: flex; gap: 8px; white-space: nowrap; }
    a.button { display: inline-block; padding: 6px 10px; border: 1px solid #ccc; border-radius: 6px; text-decoration: none; color: #111; background: #fafafa; }
    a.button:hover { background: #f0f0f0; }
    .empty { color: #777; }
  </style>
  {% assign doc_exts = "doc,docx" | split: "," %}
  {% assign pdf_exts = "pdf" | split: "," %}
  {% assign office_exts = "ppt,pptx,xls,xlsx" | split: "," %}
</head>
<body>
  <h1>ファイル一覧（files/ 配下）</h1>
  <p class="note">このリポジトリの <code>files/</code> ディレクトリに PDF や Word（.doc, .docx）を置くと自動で一覧表示され、新しいタブで確認できます。</p>

  {% assign targets = site.static_files | where_exp: "f", "f.path contains '/files/'" %}
  {% assign items = "" | split: "" %}
  {% for f in targets %}
    {% assign ext = f.extname | remove: "." | downcase %}
    {% if doc_exts contains ext or pdf_exts contains ext or office_exts contains ext %}
      {% assign items = items | push: f %}
    {% endif %}
  {% endfor %}

  {% if items.size == 0 %}
    <p class="empty">まだ対象ファイルがありません。<code>files/</code> に PDF や Word ファイルを追加してください。</p>
  {% else %}
    <ul>
      {% for f in items %}
        {% assign ext = f.extname | remove: "." | downcase %}
        {% assign filename = f.path | split: "/" | last %}
        <li>
          <div>
            <div class="name">{{ filename }}</div>
            <div class="ext">.{{ ext }}</div>
          </div>
          <div class="actions">
            {% if ext == "pdf" %}
              <a class="button" href="{{ f.path | absolute_url }}" target="_blank" rel="noopener">PDFを開く</a>
            {% elsif ext == "doc" or ext == "docx" or ext == "ppt" or ext == "pptx" or ext == "xls" or ext == "xlsx" %}
              {% assign absolute = f.path | absolute_url %}
              {% assign encoded = absolute | uri_escape %}
              <a class="button" href="https://view.officeapps.live.com/op/view.aspx?src={{ encoded }}" target="_blank" rel="noopener">Office Viewerで開く</a>
              <a class="button" href="{{ f.path | absolute_url }}" target="_blank" rel="noopener">直接開く/ダウンロード</a>
            {% else %}
              <a class="button" href="{{ f.path | absolute_url }}" target="_blank" rel="noopener">開く</a>
            {% endif %}
          </div>
        </li>
      {% endfor %}
    </ul>
  {% endif %}
</body>
</html>


