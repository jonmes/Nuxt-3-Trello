<script setup>
import tag from "@/assets/svg/tag.svg?url";
import compass from "@/assets/svg/compass.svg?url";
import solution from "@/assets/svg/solutions.svg?url";
import coinbase from "@/assets/svg/coinbase.svg?url";
import johnDeer from "@/assets/svg/johndeere.svg?url";
import grand from "@/assets/svg/Grand-Hyatt.svg?url";
import google from "@/assets/svg/Google.svg?url";
import visa from "@/assets/svg/Visa.svg?url";

const setColorTheme = inject("setColorTheme");
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
        </div>
      </div>
    </section>

    <section>
      <div class="flex justify-center">
        <div class="max-w-[1263px] mx-20 flex flex-wrap">
          <hr class="border-b-[0.3px] border-opacity-20 border-gray-400 my-4" />
          <div class="flex flex-col pt-12 pb-4 px-4">
            <h1 class="text-4xl font-semibold text-center">
              It’s more than work. It’s a way of working together.
            </h1>
            <p class="text-xl font-normal text-center">
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
          <div class="flex flex-wrap justify-center items-center">
            <div class="w-3/12 flex justify-center">
              <img :src="coinbase" alt="coinbase" />
            </div>
            <div class="w-3/12 flex justify-center">
              <img :src="johnDeer" alt="johnDeer" />
            </div>
            <div class="w-3/12 flex justify-center">
              <img :src="grand" alt="Grand Hyatt" />
            </div>
            <div class="w-3/12 flex justify-center">
              <img :src="google" alt="Google" />
            </div>
            <div class="w-3/12 flex justify-center">
              <img :src="visa" alt="Visa" />
            </div>
            <div class="w-3/12 flex justify-center">
              <img
                src="/images/Zoom.png"
                alt="Zoom"
                class="max-h-20 object-contain"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section>
      <div
        class="flex flex-col justify-center max-w-[1263px] mx-20 px-4 pt-4 mb-12"
      >
        <h1 class="w-5/12 text-4xl font-medium mb-2">
          Features to help your team succeed
        </h1>
        <p class="text-xl w-8/12">
          Powering a productive team means using a powerful tool (and plenty of
          snacks). From meetings and projects to events and goal setting,
          Trello’s intuitive features give any team the ability to quickly set
          up and customize workflows for just about anything.
        </p>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
