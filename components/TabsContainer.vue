<template>
  <div class="flex flex-wrap w-full">
    <div class="w-full p-5">
      <div
        class="tab-nav-wrapper flex mb-0 list-none flex-wrap pt-3 pb-4 flex-row"
      >
        <div
          v-for="({ tabName }, index) in tabs"
          :key="index"
          class="-mb-px last:mr-0 text-center"
        >
          <a
            class="
              text-xs
              font-bold
              uppercase
              px-2
              py-2
              shadow-lg
              block
              leading-normal
            "
            v-on:click="toggleTabs(index)"
            v-bind:class="{
              'text-tabColor bg-white border-gray-100': openTab !== index,
              'text-white bg-tabColor': openTab === index,
              'rounded-l-2xl': index === 0,
              'rounded-r-2xl': index === tabs.length - 1,
            }"
          >
            {{ tabName }}
          </a>
        </div>
      </div>
      <div
        class="
          relative
          flex flex-col
          min-w-0
          break-words
          bg-white
          w-full
          mb-6
          shadow-lg
          rounded
        "
      >
        <div class="px-4 py-5 flex-auto">
          <div class="tab-content tab-space">
            <div
              v-for="({ paraOne, paraTwo }, index) in tabs"
              :key="index"
              v-bind:class="{
                hidden: openTab !== index,
                block: openTab === index,
              }"
            >
              <p>
                {{ paraOne }}
                <br />
                <br />
                {{ paraTwo }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.tab-nav-wrapper {
  width: 360px;
  margin: 0 auto;
  margin-bottom: 20px;
}
.tab-nav-wrapper > ul {
  padding: 0 !important;
  margin: 0 !important;
  width: 100%;
  white-space: nowrap;
  display: ruby;
  z-index: 100;
}
.tab-nav-wrapper ul li {
  cursor: pointer;
  transition: color 0.15s ease-in;
  min-width: 160px;
}
</style>

<script>
export default {
  name: "home",
  data() {
    return {
      openTab: 1,
      tabs: [
        {
          tabName: "Arbeitnehmer",
          paraOne:
            "Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits.",
          paraTwo:
            "Dramatically visualize customer directed convergence without revolutionary ROI.",
        },
        {
          tabName: "Arbeitgeber",
          paraOne:
            "Completely synergize resource taxing relationships via premier niche markets. Professionally cultivate one-to-one customer service with robust ideas.",
          paraTwo:
            "Dynamically innovate resource-leveling customer service for state of the art customer service.",
        },
        {
          tabName: "Temporärbüro",
          paraOne:
            "Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas.",
          paraTwo:
            "Dramatically maintain clicks-and-mortar solutions without functional solutions.",
        },
      ],
    };
  },
  methods: {
    toggleTabs: function (tabNumber) {
      this.openTab = tabNumber;
    },
  },
};
</script>