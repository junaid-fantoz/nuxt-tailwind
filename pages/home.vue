<template>
  <div>
    <Header />
    <div class="flex flex-wrap w-full">
      <div class="w-full py-5">
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
            </li>
            <li class="-mb-px last:mr-0 flex-auto text-center">
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
            </li>
            <li class="-mb-px last:mr-0 flex-auto text-center">
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
            rounded
          "
        >
          <div class="flex-auto">
            <div class="tab-content tab-space">
              <div
                v-bind:class="{ hidden: openTab !== 1, block: openTab === 1 }"
              >
                <div>
                  <p class="text-gray p-5 text-center">
                    Drei einfache Schritte zu deinem neuen Job
                  </p>
                  <img
                    class="mx-auto mt-2"
                    v-bind:src="'./assets/img/tab1-bg.png'"
                  />

                  <ol>
                    <li><a>Erstellen dein Lebenslauf</a></li>
                  </ol>
                </div>
                <svg
                  id="svg"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="-300 0 950 270"
                >
                  <path
                    d="M-314,267 C105,364 400,100 812,279"
                    fill="none"
                    stroke="#E6FFFA"
                    stroke-width="120"
                    stroke-linecap="round"
                  />
                </svg>
                <div class="wavyBg py-10">
                  <ol>
                    <li><a>Erstellen dein Lebenslauf</a></li>
                  </ol>

                  <img
                    class="mx-auto mt-2"
                    v-bind:src="'./assets/img/tab2-bg.png'"
                  />
                </div>
                <svg
                  id="svg"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="-300 0 950 270"
                  v-bind:style="{ transform: 'rotate(180deg)' }"
                >
                  <path
                    d="M-314,267 C105,364 400,100 812,279"
                    fill="none"
                    stroke="#E6FFFA"
                    stroke-width="120"
                    stroke-linecap="round"
                  />
                </svg>
                <div class="pb-10">
                  <p class="text-gray p-5 text-center">
                    Drei einfache Schritte zu deinem neuen Job
                  </p>
                  <img
                    class="mx-auto mt-2"
                    v-bind:src="'./assets/img/tab3-bg.png'"
                  />

                  <ol>
                    <li><a>Erstellen dein Lebenslauf</a></li>
                  </ol>
                </div>
                <div class="py-10"></div>
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
    <Footer />
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

ol {
  list-style: none;
  counter-reset: my-awesome-counter;
  display: flex;
  flex-wrap: wrap;
  margin: 0;
  padding: 0;
}
ol li {
  counter-increment: my-awesome-counter;
  display: flex;
  width: 100%;
  font-size: 13px;
  margin-bottom: 0.5rem;
  display: inline-block;
  text-align: left;
  color: #4a5568;
}
ol li::before {
  content: counter(my-awesome-counter) ".";
  font-size: 130px;
  margin-right: 0.5rem;
  line-height: 1;
  color: #4a5568;
}
.wavyBg {
  background: #e6fffa;
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
