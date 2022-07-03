<script setup>
import tag from "@/assets/svg/tag.svg?url";
import compass from "@/assets/svg/compass.svg?url";
import solution from "@/assets/svg/solutions.svg?url";
import coinbase from "@/assets/svg/coinbase.svg?url";
import johnDeer from "@/assets/svg/johnDeere.svg?url";
import grand from "@/assets/svg/Grand-Hyatt.svg?url";
import google from "@/assets/svg/Google.svg?url";
import visa from "@/assets/svg/Visa.svg?url";
import zoom from "@/assets/svg/Zoom.svg?url";
import view from "@/assets/svg/view.svg?url";
import backImg from "@/assets/svg/card-back.svg";
import { gsap } from "gsap";

const setColorTheme = inject("setColorTheme");
const icons = ref(null);
const pageShow = ref(false);
const tobeShown = ref(null)
const companys = [
  { icn: coinbase, alt: "coinbase" },
  { icn: johnDeer, alt: "johnDeer" },
  { icn: grand, alt: "grand" },
  { icn: google, alt: "google" },
  { icn: visa, alt: "visa" },
  { icn: zoom, cls: "max-h-20 object-contain", alt: "zoom" },
];

onMounted(() => {
  pageShow.value = true;
});

const beforeEnter = (el) => {
  el.style.opacity = 0;
  el.style.transform = "translateY(100px)";
};

const enter = (el, done) => {
  gsap.to(el, {
    opacity: 1,
    y: 0,
    duration: 1,
    onComplete: done,
    delay: el.dataset.index * 0.2,
  });
};

</script>
<template>
  <div>
    <section class="bg-gradient-to-b from-[#eae6ff] flex flex-col items-center">
      <div class="pt-20 grid grid-cols-3 justify-items-center max-w-[1263px]">
        <div class="col-span-2 w-10/12 flex flex-col justify-center">
          <h1 class="text-5xl font-semibold">
            Trello helps teams move work forward.
          </h1>
          <h2 class="text-xl font-normal mt-4">
            Collaborate, manage projects, and reach new productivity peaks. From
            high rises to the home office, the way your team works is
            unique—accomplish it all with Trello.
          </h2>
          <button
            class="mt-10 self-start text-base text-white rounded-md px-4 py-3 bg-[#0066ff] hover:bg-[#0747a6]"
          >
            Sign up - it's free ok
          </button>
        </div>
        <div>
          <div class="">
            <img
              src="/images/trello_home_cover.png"
              class="max-h-[450px] object-contain"
            />
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="flex justify-center">
        <div class="max-w-[1263px] mx-20 flex justify-center flex-wrap">
          <hr class="border-b-[0.3px] border-opacity-20 border-gray-400 my-4" />
          <div class="flex flex-col pt-12 pb-4 px-4">
            <h1 class="text-4xl font-semibold text-center">
              It’s more than work. It’s a way of working together.
            </h1>
            <p class="text-xl font-normal text-center px-6">
              Start with a Trello board, lists, and cards. Customize and expand
              with more features as your teamwork grows. Manage projects,
              organize tasks, and build team spirit—all in one place.
            </p>
            <button
              class="mt-10 self-center text-base text-white rounded-md px-4 py-3 bg-[#0066ff] hover:bg-[#0747a6]"
            >
              Start doing
            </button>
            <div class="flex justify-center p-4">
              <img
                src="/images/board.png"
                class="object-contain max-w-[951px]"
              />
            </div>
            <p class="text-xl mb-6 text-center">
              Join over 2,000,000 teams worldwide that are using Trello to get
              more done.
            </p>
          </div>
          <TransitionGroup
            appear
            :css="false"
            @before-enter="beforeEnter"
            @enter="enter"
            tag="ul"
            name="list"
            class="flex self-center flex-wrap justify-center items-center"
          >
            <li
              class="w-3/12 flex justify-center"
              v-for="(icon, i) in companys"
              :key="i"
              :data-index="i"
              v-if="pageShow"
              ref="tobeShown"
            >
              <img :src="icon.icn" :class="icon?.cls" :alt="icon.alt" />
            </li>
          </TransitionGroup>
        </div>
      </div>
    </section>
    <section class="flex mt-20 justify-center">
      <div class="max-w-[1263px] mx-20">
        <div class="px-4 pt-4 mb-12">
          <h1 class="text-4xl font-medium w-5/12 mb-3">
            Features to help your team succeed
          </h1>
          <p class="text-xl w-6/12 text-gray-500">
            Powering a productive team means using a powerful tool (and plenty
            of snacks). From meetings and projects to events and goal setting,
            Trello’s intuitive features give any team the ability to quickly set
            up and customize workflows for just about anything.
          </p>
        </div>
        <div class="h-16"></div>
        <div class="flex justify-between">
          <div class="flex-1 max-w-[475px] p-4">
            <img :src="view" class="max-w-[415px] object-contain" />
          </div>
          <div class="flex-1 p-4">
            <div class="max-w-[665px]">
              <h4 class="font-medium mb-2">CHOOSE A VIEW</h4>
              <h2 class="text-4xl font-medium pb-4 mb-2">
                The board is just the beginning
              </h2>
              <p class="mb-6 text-xl text-gray-500">
                Lists and cards are the building blocks of organizing work on a
                Trello board. Grow from there with task assignments, timelines,
                productivity metrics, calendars, and more.
              </p>

              <button class="text-2xl font-medium">+ Learn more</button>
            </div>
          </div>
        </div>

        <div class="h-16"></div>
        <div class="flex justify-between flex-row-reverse">
          <div class="flex-1 max-w-[475px] p-4">
            <img :src="backImg" class="max-w-[340px] object-contain" />
          </div>
          <div class="flex-1 p-4">
            <div class="max-w-[665px]">
              <h4 class="font-medium mb-2">DIVE INTO THE DETAILS</h4>
              <h2 class="text-4xl font-medium pb-4 mb-2">
                Cards contain everything you need
              </h2>
              <p class="mb-6 text-xl text-gray-500">
                Trello cards are your portal to more organized work—where every
                single part of your task can be managed, tracked, and shared
                with teammates. Open any card to uncover an ecosystem of
                checklists, due dates, attachments, conversations, and more.
              </p>

              <button class="text-2xl font-medium">+ Learn more</button>
            </div>
          </div>
        </div>

        <div class="h-16"></div>
        <div class="flex justify-between">
          <div class="flex-1 max-w-[475px] p-4">
            <img
              src="/images/automation.png"
              class="max-w-[442px] object-contain"
            />
          </div>
          <div class="flex-1 p-4">
            <div class="max-w-[665px]">
              <h4 class="font-medium mb-2">MEET YOUR NEW BUTLER</h4>
              <h2 class="text-4xl font-medium pb-4 mb-2">No-code automation</h2>
              <p class="mb-6 text-xl text-gray-500">
                Let the robots do the work—so your team can focus on work that
                matters. With Trello’s built-in automation, Butler, reduce the
                number of tedious tasks (and clicks) on your project board by
                harnessing the power of automation across your entire team.
              </p>

              <button class="text-2xl font-medium">+ Learn more</button>
            </div>
          </div>
        </div>

        <div class="h-16"></div>
        <div class="flex flex-row-reverse justify-between">
          <div class="flex-1 max-w-[475px] p-4">
            <img
              src="/images/power-ups.png"
              class="max-w-[375px] object-contain"
            />
          </div>
          <div class="flex-1 p-4">
            <div class="max-w-[665px]">
              <h4 class="font-medium mb-2">POWER-UPS</h4>
              <h2 class="text-4xl font-medium pb-4 mb-2">
                Integrate top work tools
              </h2>
              <p class="mb-6 text-xl text-gray-500">
                Easily connect the apps your team already uses into your Trello
                workflow, or add a Power-Up that helps fine-tune one specific
                need. With hundreds of Power-Ups available, your team’s workflow
                wishes are covered.
              </p>
              <button class="text-2xl font-medium">+ Learn more</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="flex justify-center">
        <div class="max-w-[1263px] mx-20">
          <hr
            class="border-b-[0.3px] border-opacity-20 border-gray-400 my-10"
          />
          <div class="grid grid-cols-3">
            <div class="flex">
              <img class="self-start max-w-[62px] m-4" :src="tag" />
              <div class="flex flex-col p-4">
                <h2 class="text-2xl font-medium">See Trello pricing</h2>
                <p class="text-base font-normal">
                  Whether you’re a team of 2 or 2,000, Trello can be customized
                  for your organization. Explore which option is best for you.
                </p>
                <button
                  class="mt-10 self-start text-base text-white rounded-md px-4 py-3 bg-[#0066ff] hover:bg-[#0747a6]"
                >
                  Compare pricing
                </button>
              </div>
            </div>
            <div class="flex">
              <img class="self-start max-w-[62px] m-4" :src="compass" />
              <div class="flex flex-col p-4">
                <h2 class="text-2xl font-medium">What is Trello?</h2>
                <p class="text-base font-normal">
                  Trello is the visual tool that empowers your team to manage
                  any type of project, workflow, or task tracking.
                </p>
                <button
                  class="mt-10 self-start text-base text-white rounded-md px-4 py-3 bg-[#0066ff] hover:bg-[#0747a6]"
                >
                  Tour Trello
                </button>
              </div>
            </div>
            <div class="flex">
              <img
                class="self-start max-w-[62px] m-4 object-contain"
                :src="solution"
              />
              <div class="flex flex-col p-4">
                <h2 class="text-2xl font-medium">Discover Trello Enterprise</h2>
                <p class="text-base font-normal">
                  The productivity tool teams love, paired with the features and
                  security needed for scale.
                </p>
                <button
                  class="mt-10 self-start text-base text-white rounded-md px-4 py-3 bg-[#0066ff] hover:bg-[#0747a6]"
                >
                  Learn more
                </button>
              </div>
            </div>
            <div></div>
            <div></div>
          </div>
          <hr
            class="border-b-[0.3px] border-opacity-20 border-gray-400 my-10"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
