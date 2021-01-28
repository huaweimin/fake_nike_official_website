<template>
  <div class="content">
    <div class="search">
      <div class="center column">
        <ul class="nav">
          <li class="nav-title">
            男子
            <div class="drop-down-list">
              <div
                v-for="(item, index) in mans"
                :key="index"
                class="list-content"
              >
                <ul
                  v-for="(item2, index2) in item.content"
                  :key="index2"
                  :class="{ listTitle: index2 == 0 }"
                >
                  <li>
                    <a href="#">{{ item2 }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </li>
          <li class="nav-title">
            女子
            <div class="drop-down-list">
              <div
                v-for="(item, index) in women"
                :key="index"
                class="list-content"
              >
                <ul
                  v-for="(item2, index2) in item.content"
                  :key="index2"
                  :class="{ listTitle: index2 == 0, womenTitle: item2 == '运动内衣' }"
                >
                  <li>
                    <a href="#">{{ item2 }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </li>
          <li class="nav-title">
            儿童
            <div class="drop-down-list">
              <div
                v-for="(item, index) in children"
                :key="index"
                class="list-content"
              >
                <ul
                  v-for="(item2, index2) in item.content"
                  :key="index2"
                  :class="{ listTitle: index2 == 0, womenTitle: item2 == '运动内衣' }"
                >
                  <li>
                    <a href="#">{{ item2 }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </li>
          <li class="nav-title">
            专属定制
            <div class="drop-down-list">
              <div>000</div>
            </div>
          </li>
          <li class="nav-title">2021新年特辑</li>
        </ul>
      </div>
      <div class="left column">
        <svg
          class="pre-logo-svg"
          height="60px"
          width="60px"
          fill="#111"
          viewBox="0 0 69 32"
        >
          <path
            d="M68.56 4L18.4 25.36Q12.16 28 7.92 28q-4.8 0-6.96-3.36-1.36-2.16-.8-5.48t2.96-7.08q2-3.04 6.56-8-1.6 2.56-2.24 5.28-1.2 5.12 2.16 7.52Q11.2 18 14 18q2.24 0 5.04-.72z"
          ></path>
        </svg>
      </div>
      <div class="right column">
        <div class="search-button">
          <svg
            class="pre-search-input-icon"
            fill="#111"
            height="24px"
            width="24px"
            viewBox="0 0 24 24"
          >
            <path
              d="M21.71 20.29L18 16.61A9 9 0 1 0 16.61 18l3.68 3.68a1 1 0 0 0 1.42 0 1 1 0 0 0 0-1.39zM11 18a7 7 0 1 1 7-7 7 7 0 0 1-7 7z"
            ></path>
          </svg>
          <input type="text" class="search-input" placeholder="搜索" />
        </div>
        <div class="favorite">
          <a href="#">
            <svg
              width="24px"
              height="24px"
              fill="#111"
              viewBox="0 0 24 24"
              class="favorite-icon"
            >
              <path
                d="M21.11 4a6.6 6.6 0 0 0-4.79-1.92A6.27 6.27 0 0 0 12 3.84 6.57 6.57 0 0 0 2.89 4c-2.8 2.68-2.45 7.3.88 10.76l6.84 6.63A2 2 0 0 0 12 22a2 2 0 0 0 1.37-.54l.2-.19.61-.57c.6-.57 1.42-1.37 2.49-2.41l2.44-2.39 1.09-1.07c3.38-3.55 3.8-8.1.91-10.83zm-2.35 9.4l-.25.24-.8.79-2.44 2.39c-1 1-1.84 1.79-2.44 2.36L12 20l-6.83-6.68c-2.56-2.66-2.86-6-.88-7.92a4.52 4.52 0 0 1 6.4 0l.09.08a2.12 2.12 0 0 1 .32.3l.9.94.9-.94.28-.27.11-.09a4.52 4.52 0 0 1 6.43 0c1.97 1.9 1.67 5.25-.96 7.98z"
              ></path>
            </svg>
          </a>
        </div>
        <div class="shopping-cart">
          <a href="#">
            <svg
              width="24px"
              height="24px"
              fill="#111"
              viewBox="0 0 24 24"
              class="shopping-icon"
            >
              <path
                d="M16 7a1 1 0 0 1-1-1V3H9v3a1 1 0 0 1-2 0V3a2 2 0 0 1 2-2h6a2 2 0 0 1 2 2v3a1 1 0 0 1-1 1z"
              ></path>
              <path
                d="M20 5H4a2 2 0 0 0-2 2v13a3 3 0 0 0 3 3h14a3 3 0 0 0 3-3V7a2 2 0 0 0-2-2zm0 15a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V7h16z"
              ></path>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mans: [
        {
          content: [
            "精选推荐",
            "2021新春特辑",
            "新春特惠 岂止五折",
            "人气热销",
            "最新上市",
            "SNKRS 新品预览",
            "会员限定",
          ],
        },
        {
          content: [
            "鞋类",
            "所有鞋类",
            "休闲",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "Jordan",
            "拖鞋",
            "当季尖货",
            "Air Jordan 1",
            "Air Force 1",
            "Air Max",
            "专属定制",
            "最新运动鞋",
          ],
        },
        {
          content: [
            "服装",
            "所有服装",
            "连帽衫/卫衣",
            "外套/夹克",
            "紧身运动服/Baselayer",
            "运动裤/紧身裤",
            "休闲裤",
            "上衣/T恤",
            "翻领T恤",
            "球衣",
            "短裤",
            "袜子",
            "Air Max",
            "配件/装备",
          ],
        },
        {
          content: [
            "品牌",
            "Jordan",
            "NBA",
            "NikeLab",
            "Nike Sportswear",
            "ACG",
            "专属定制",
          ],
        },
        {
          content: [
            "运动",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "瑜伽",
            "滑板",
            "网球",
            "高尔夫",
          ],
        },
      ],
      women: [
        {
          content: [
            "精选推荐",
            "2021新春特辑",
            "新春特惠 岂止五折",
            "人气热销",
            "最新上市",
            "SNKRS 新品预览",
            "会员限定",
          ],
        },
        {
          content: [
            "鞋类",
            "所有鞋类",
            "休闲",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "Jordan",
            "拖鞋",
            "当季尖货",
            "Air Jordan 1",
            "Air Force 1",
            "Air Max",
            "专属定制",
            "最新运动鞋",
          ],
        },
        {
          content: [
            "服装",
            "所有服装",
            "连帽衫/卫衣",
            "外套/夹克",
            "紧身运动服/Baselayer",
            "运动裤/紧身裤",
            "休闲裤",
            "上衣/T恤",
            "翻领T恤",
            "球衣",
            "短裤",
            "袜子",
            "Air Max",
            "配件/装备",
            "运动内衣",
            "运动内衣选购指南",
            "跑步运动内衣",
            "舞蹈运动内衣",
            "瑜伽运动内衣"
          ],
        },
        {
          content: [
            "品牌",
            "Jordan",
            "NBA",
            "NikeLab",
            "Nike Sportswear",
            "ACG",
            "专属定制",
          ],
        },
        {
          content: [
            "运动",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "瑜伽",
            "滑板",
            "网球",
            "高尔夫",
          ],
        }
      ],
      children: [
        {
          content: [
            "精选推荐",
            "2021新春特辑",
            "新春特惠 岂止五折",
            "人气热销",
            "最新上市",
            "冬日保暖系列",
            "亲自系列",
          ],
        },
        {
          content: [
            "男孩鞋类",
            "所有鞋类",
            "婴童（11CM-16CM）",
            "幼童（17CM-22CM）",
            "大童（35.5-40欧码）",
            "男孩服装",
            "所有服装",
            "婴童（85CM-104CM）",
            "幼童（96CM-122CM）",
            "大童（122CM-170CM）",
          ],
        },
        {
          content: [
            "女孩鞋类",
            "所有鞋类",
            "婴童（11CM-16CM）",
            "幼童（17CM-22CM）",
            "大童（35.5-40欧码）",
            "女孩服装",
            "所有服装",
            "婴童（85CM-104CM）",
            "幼童（96CM-122CM）",
            "大童（122CM-170CM）",
          ],
        },
        {
          content: [
            "主推鞋款",
            "Jordan",
            "NBA",
            "NikeLab",
            "Nike Sportswear",
            "ACG",
            "专属定制",
          ],
        },
        {
          content: [
            "运动",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "瑜伽",
            "滑板",
            "网球",
            "高尔夫",
          ],
        },
      ],
      customMade: [
        {
          content: [
            "精选推荐4",
            "2021新春特辑",
            "新春特惠 岂止五折",
            "人气热销",
            "最新上市",
            "SNKRS 新品预览",
            "会员限定",
          ],
        },
        {
          content: [
            "鞋类",
            "所有鞋类",
            "休闲",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "Jordan",
            "拖鞋",
            "当季尖货",
            "Air Jordan 1",
            "Air Force 1",
            "Air Max",
            "专属定制",
            "最新运动鞋",
          ],
        },
        {
          content: [
            "服装",
            "所有服装",
            "连帽衫/卫衣",
            "外套/夹克",
            "紧身运动服/Baselayer",
            "运动裤/紧身裤",
            "休闲裤",
            "上衣/T恤",
            "翻领T恤",
            "球衣",
            "短裤",
            "袜子",
            "Air Max",
            "配件/装备",
          ],
        },
        {
          content: [
            "品牌",
            "Jordan",
            "NBA",
            "NikeLab",
            "Nike Sportswear",
            "ACG",
            "专属定制",
          ],
        },
        {
          content: [
            "运动",
            "跑步",
            "篮球",
            "足球",
            "健身/训练",
            "瑜伽",
            "滑板",
            "网球",
            "高尔夫",
          ],
        },
      ],
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../static/css/search.scss";
</style>
