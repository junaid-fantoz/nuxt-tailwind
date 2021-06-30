<template>
  <div class="flex flex-wrap w-full">
    <div class="w-full">
      <div class="wavyBg py-5">
        <p class="heading py-5 text-center">Deine Job website</p>
        <img class="mx-auto mt-2" v-bind:src="'./assets/img/headerImg.png'" />
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
      <div class="tab-nav-wrapper">
        <ul class="flex mb-0 list-none pt-3 pb-4 flex-row">
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
            <div v-bind:class="{ hidden: openTab !== 1, block: openTab === 1 }">
              <div>
                <p class="text-gray p-5 text-center">
                  Drei einfache Schritte zu deinem neuen Job
                </p>
                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab1-bg.png'"
                />

                <div class="numberList">1.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>
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
                <div class="numberList">2.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>

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
                <div class="numberList">3.</div>
                <div class="numberListText pt-36">
                  Erstellen dein Lebenslauf
                </div>

                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab3-bg.png'"
                />
              </div>
              <div class="py-10"></div>
            </div>
            <div v-bind:class="{ hidden: openTab !== 2, block: openTab === 2 }">
              <div>
                <p class="text-gray p-5 text-center">
                  Drei einfache Schritte zu deinem neuen Job
                </p>
                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab1-bg.png'"
                />

                <div class="numberList">1.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>
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
                <div class="numberList">2.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>

                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab22-2.png'"
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
                <div class="numberList">3.</div>
                <div class="numberListText pt-36">
                  Wähle deinen neuen Mitarbeiter aus
                </div>

                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab22-3.png'"
                />
              </div>
              <div class="py-10"></div>
            </div>
            <div v-bind:class="{ hidden: openTab !== 3, block: openTab === 3 }">
              <div>
                <p class="text-gray p-5 text-center">
                  Drei einfache Schritte zu deinem neuen Job
                </p>
                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab1-bg.png'"
                />

                <div class="numberList">1.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>
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
                <div class="numberList">2.</div>
                <div class="numberListText mt-36">
                  Erstellen dein Lebenslauf
                </div>

                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab32-1.png'"
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
                <div class="numberList">3.</div>
                <div class="numberListText pt-36">
                  Erstellen dein Lebenslauf
                </div>

                <img
                  class="mx-auto mt-2"
                  v-bind:src="'./assets/img/tab32-2.png'"
                />
              </div>
              <div class="py-10"></div>
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

.wavyBg {
  background: #e6fffa;
}
.heading {
  font-size: 50px;
}
.numberList {
  font-size: 148px;
  float: left;
  color: #4a5568;
}
.numberListText {
  font-size: 17px;
  vertical-align: bottom;
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
