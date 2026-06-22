<script setup lang="ts">
const apiBaseUrl = import.meta.env.VITE_API_BASE_URL || 'https://api.yuanzhoulv.cloud'
const adminUrl = import.meta.env.VITE_ADMIN_URL || 'https://admin.yuanzhoulv.cloud'

const capabilities = [
  {
    title: '智能企划与设计',
    text: '沉淀趋势、版型、面料与工艺知识，辅助完成选品企划、灵感生成和可落地性评估。',
  },
  {
    title: 'AI 商拍与营销内容',
    text: '围绕商品卖点、品牌调性和渠道规则，生成适配抖音、天猫、小红书等渠道的营销素材。',
  },
  {
    title: '智能导购与尺码推荐',
    text: '结合体型、体感、版型与历史退货原因，提升转化率并降低尺码不合适导致的退货。',
  },
  {
    title: '商品与供应链优化',
    text: '通过需求预测、库存分析、补货建议和退货归因，帮助企业提升周转与经营决策质量。',
  },
]

const metrics = [
  '商品内容生产提效',
  '退货原因智能归因',
  '尺码推荐与导购转化',
  '库存周转与补货优化',
]
</script>

<template>
  <main class="page-shell">
    <section class="hero">
      <nav class="nav">
        <div class="brand">
          <span class="brand-mark">布</span>
          <span>布卓 Fashion AI</span>
        </div>
        <div class="nav-links">
          <a href="#scenarios">场景</a>
          <a href="#architecture">架构</a>
          <a :href="adminUrl" target="_blank" rel="noreferrer">后台管理</a>
        </div>
      </nav>

      <div class="hero-grid">
        <div class="hero-copy">
          <p class="eyebrow">Footwear & Apparel Vertical AI Platform</p>
          <h1>鞋服行业智能体平台</h1>
          <p class="lead">
            连接设计、商品、营销、导购与供应链，用行业 Know-how、多模态理解和业务闭环，
            帮助鞋服企业从“生成内容”升级为“解释原因、辅助决策、驱动增长”。
          </p>
          <div class="actions">
            <a class="primary" :href="apiBaseUrl" target="_blank" rel="noreferrer">查看 API 状态</a>
            <a class="secondary" :href="adminUrl" target="_blank" rel="noreferrer">进入管理后台</a>
          </div>
          <div class="badges">
            <span>可控</span>
            <span>可信</span>
            <span>可解释</span>
            <span>可落地</span>
          </div>
        </div>

        <div class="hero-card" aria-label="Fashion Agent overview">
          <div class="card-glow"></div>
          <p class="card-title">Fashion Agent</p>
          <div class="orbit">
            <span>设计</span>
            <span>营销</span>
            <span>导购</span>
            <span>供应链</span>
          </div>
          <div class="reasoning-core">
            <strong>Reasoning Engine</strong>
            <small>版型 × 体感 × 退货 × 库存</small>
          </div>
        </div>
      </div>
    </section>

    <section id="scenarios" class="section">
      <p class="section-label">Core Scenarios</p>
      <h2>优先从高 ROI 场景切入</h2>
      <div class="cards">
        <article v-for="item in capabilities" :key="item.title" class="capability-card">
          <h3>{{ item.title }}</h3>
          <p>{{ item.text }}</p>
        </article>
      </div>
    </section>

    <section id="architecture" class="section split-section">
      <div>
        <p class="section-label">Architecture</p>
        <h2>从数据底座到业务智能体</h2>
        <p class="body-text">
          平台以商品图像、SKU 属性、尺码版型、库存、销售、退货、趋势报告等数据为基础，
          通过 RAG、多模态模型、行业知识库和业务系统接口，形成可执行的鞋服行业智能体。
        </p>
      </div>
      <div class="pipeline">
        <span>数据治理</span>
        <span>知识图谱 / RAG</span>
        <span>多模态理解</span>
        <span>业务智能体</span>
      </div>
    </section>

    <section class="section metrics">
      <div v-for="metric in metrics" :key="metric" class="metric-card">
        {{ metric }}
      </div>
    </section>

    <footer class="footer">
      <span>© 2026 布卓 Fashion AI</span>
      <span>API: {{ apiBaseUrl }}</span>
      <span>Admin: {{ adminUrl }}</span>
    </footer>
  </main>
</template>
