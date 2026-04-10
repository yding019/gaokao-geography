# 🔍 多维筛选真题

请选择年份、卷名和主题，点击“筛选”按钮，下方将列出符合条件的题目。

<div id="filter-form">
  <label>年份：</label>
  <select id="year">
    <option value="">不限</option>
    <option value="2025">2025</option>
    <option value="2024">2024</option>
    <option value="2023">2023</option>
    <option value="2022">2022</option>
  </select>

  <label>卷名：</label>
  <select id="paper">
    <option value="">不限</option>
    <option value="全国甲卷">全国甲卷</option>
    <option value="全国乙卷">全国乙卷</option>
    <option value="山东卷">山东卷</option>
    <option value="北京卷">北京卷</option>
    <!-- 根据你的实际卷名添加更多 -->
  </select>

  <label>主题：</label>
  <select id="topic">
    <option value="">不限</option>
    <option value="人口">人口</option>
    <option value="聚落">聚落</option>
    <option value="农业">农业</option>
    <option value="工业">工业</option>
    <option value="服务业">服务业</option>
    <option value="交通运输业">交通运输业</option>
    <option value="区域发展">区域发展</option>
    <option value="宇宙环境">宇宙环境</option>
    <option value="地形">地形</option>
    <option value="气候">气候</option>
    <option value="水">水</option>
    <option value="土壤">土壤</option>
    <option value="生物">生物</option>
  </select>

  <button onclick="doFilter()">筛选</button>
</div>

<script>
function doFilter() {
  const year = document.getElementById('year').value;
  const paper = document.getElementById('paper').value;
  const topic = document.getElementById('topic').value;
  let tags = [];
  if (year) tags.push(year);
  if (paper) tags.push(paper);
  if (topic) tags.push(topic);
  const query = tags.join(' ');
  // 跳转到当前页面，带上 ?filter= 参数
  window.location.href = window.location.pathname + '?filter=' + encodeURIComponent(query);
}

// 页面加载时，读取 URL 参数并回填下拉框
window.addEventListener('DOMContentLoaded', () => {
  const params = new URLSearchParams(window.location.search);
  const filter = params.get('filter');
  if (filter) {
    const tags = filter.split(' ');
    document.getElementById('year').value = tags.find(t => ['2025','2024','2023','2022'].includes(t)) || '';
    document.getElementById('paper').value = tags.find(t => ['全国甲卷','全国乙卷','山东卷','北京卷'].includes(t)) || '';
    document.getElementById('topic').value = tags.find(t => ['人口','聚落','农业','工业','服务业','交通运输业','区域发展','宇宙环境','地形','气候','水','土壤','生物'].includes(t)) || '';
  }
});
</script>

---

## 📋 筛选结果

{pagelist}