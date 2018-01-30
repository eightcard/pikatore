## 部分的なスタイル適用
以下のようなhtmlとcssがある。

```html
<table class="animal_table">
  <thead class="table_header">
    <tr>
      <th>Kind of animal</th>
      <th>Merit</th>
      <th>Demerit</th>
    </tr>
  </thead>
  <tbody class="table_body">
    <tr>
      <td>dog</td>
      <td>heartful</td>
      <td>noisy</td>
    </tr>
    <tr>
      <td>cat</td>
      <td>cute</td>
      <td>selfish</td>
    </tr>
  </tbody>
</table>
```

```css
.animal_table {
  border: solid 2px;
  border-collapse: collapse;
}

.table_header th {
  border: solid 1px #000000;
  padding: 5px;
}

.table_body td {
  border: solid 1px #000000;
  padding: 5px;
}
```
上記に対し、1行目の中の要素のみ文字色を青色にするためのスタイル定義を追記しなさい。
