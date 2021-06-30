<template>
  <div>
    <Header />
    <div class="flex flex-wrap w-full">
      <div class="w-full p-5">
        <div class="tab-nav-wrapper">
          <ul class="flex mb-0 list-none flex-wrap pt-3 pb-4 flex-row">
            <li class="-mb-px last:mr-0 flex-auto text-center">
              <a
                class="
                  text-xs
                  font-bold
                  uppercase
                  px-2
                  py-2
                  shadow-lg
                  rounded-l-2xl
                  block
                  leading-normal
                "
                v-on:click="toggleTabs(1)"
                v-bind:class="{
                  'text-tabColor bg-white border-gray-100': openTab !== 1,
                  'text-white bg-tabColor': openTab === 1,
                }"
              >
                Arbeitnehmer
              </a>
            </li><li class="-mb-px last:mr-0 flex-auto text-center">
              <a
                class="
                  text-xs
                  font-bold
                  uppercase
                  px-2
                  py-2
                  shadow-lg
                  rounded
                  block
                  leading-normal
                "
                v-on:click="toggleTabs(2)"
                v-bind:class="{
                  'text-tabColor bg-white border-gray-100': openTab !== 2,
                  'text-white bg-tabColor': openTab === 2,
                }"
              >
                Arbeitgeber
              </a>
            </li><li class="-mb-px last:mr-0 flex-auto text-center">
              <a
                class="
                  text-xs
                  font-bold
                  uppercase
                  px-2
                  py-2
                  shadow-lg
                  rounded-r-2xl
                  block
                  leading-normal
                "
                v-on:click="toggleTabs(3)"
                v-bind:class="{
                  'text-tabColor bg-white border-gray-100': openTab !== 3,
                  'text-white bg-tabColor': openTab === 3,
                }"
              >
                Temporärbüro
              </a>
            </li>
          </ul>
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
                v-bind:class="{ hidden: openTab !== 1, block: openTab === 1 }"
              >
                <p>
                  Collaboratively administrate empowered markets via
                  plug-and-play networks. Dynamically procrastinate B2C users
                  after installed base benefits.
                  <br />
                  <br />
                  Dramatically visualize customer directed convergence without
                  revolutionary ROI.
                </p>
              </div>
              <div
                v-bind:class="{ hidden: openTab !== 2, block: openTab === 2 }"
              >
                <p>
                  Completely synergize resource taxing relationships via premier
                  niche markets. Professionally cultivate one-to-one customer
                  service with robust ideas.
                  <br />
                  <br />
                  Dynamically innovate resource-leveling customer service for
                  state of the art customer service.
                </p>
              </div>
              <div
                v-bind:class="{ hidden: openTab !== 3, block: openTab === 3 }"
              >
                <p>
                  Efficiently unleash cross-media information without
                  cross-media value. Quickly maximize timely deliverables for
                  real-time schemas.
                  <br />
                  <br />
                  Dramatically maintain clicks-and-mortar solutions without
                  functional solutions.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<style scoped>
.tab-nav-wrapper {
  width: 360px;
  max-width: 100%;
  margin: 0 auto;
  overflow: scroll;
  scrollbar-width: none;
  margin-bottom: 20px;
  height: 50px;
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
.tab-nav-wrapper::-webkit-scrollbar {
  display: none;
  -ms-overflow-style: none; /* IE 11 */
  scrollbar-width: none; /* Firefox 64 */
}
</style>

<script>
export default {
  name: "home",
  data() {
    return {
      openTab: 1,
    };
  },
  methods: {
    toggleTabs: function (tabNumber) {
      this.openTab = tabNumber;
    },
  },
};
</script>
