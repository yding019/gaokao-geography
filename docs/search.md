<div id="question-filter-app">
  <div class="filter-group">
    <label>年份：</label>
    <select id="year-select">
      <option value="all">全部</option>
      <option value="2025">2025</option>
      <option value="2024">2024</option>
      <!-- ... 更多年份 ... -->
    </select>
  </div>
  <div class="filter-group">
    <label>地区：</label>
    <select id="region-select">
      <option value="all">全部</option>
      <option value="全国甲卷">全国甲卷</option>
      <option value="山东卷">山东卷</option>
      <!-- ... 更多地区 ... -->
    </select>
  </div>
  <div class="filter-group">
    <label>主题：</label>
    <select id="topic-select">
      <option value="all">全部</option>
      <option value="工业">工业</option>
      <option value="自然地理">自然地理</option>
      <!-- ... 更多主题 ... -->
    </select>
  </div>
  <button id="search-btn">开始检索</button>
  <div id="search-results">
    <p>请选择筛选条件并点击检索</p>
  </div>
</div>