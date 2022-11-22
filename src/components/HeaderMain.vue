<template>
  <section class="bg-white">
    <img :src="image" alt="image" srcset="" />
    <div class="isolate h-85 flex items-center justify-center pt-20">
      <div
        class="absolute inset-x-0 -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[-20rem]"
      >
        <svg
          class="relative left-[calc(50%-11rem)] -z-10 h-[21.1875rem] max-w-none -translate-x-1/2 rotate-[30deg] sm:left-[calc(50%-30rem)] sm:h-[42.375rem]"
          viewBox="0 0 1155 678"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill="url(#45de2b6b-92d5-4d68-a6a0-9b9b2abad533)"
            fill-opacity=".3"
            d="M317.219 518.975L203.852 678 0 438.341l317.219 80.634 204.172-286.402c1.307 132.337 45.083 346.658 209.733 145.248C936.936 126.058 882.053-94.234 1031.02 41.331c119.18 108.451 130.68 295.337 121.53 375.223L855 299l21.173 362.054-558.954-142.079z"
          />
          <defs>
            <linearGradient
              id="45de2b6b-92d5-4d68-a6a0-9b9b2abad533"
              x1="1155.49"
              x2="-78.208"
              y1=".177"
              y2="474.645"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#9089FC"></stop>
              <stop offset="1" stop-color="#FF80B5"></stop>
            </linearGradient>
          </defs>
        </svg>
      </div>

      <main>
        <div class="relative px-6 lg:px-8 pl-20 container">
          <div class="mx-auto max-w-3xl pt-8 pb-32 sm:pt-24 sm:pb-40">
            <div>
              <div>
                <h1
                  class="heading-secondary text-5xl font-bold tracking-tight sm:text-center sm:text-6xl text-gray-400 uppercase pb-8"
                >
                  {{ title }}
                </h1>
                <p class="mt-6 text-lg leading-8 text-gray-600 sm:text-center">
                  {{ description }}
                </p>

                <div class="mt-8 flex gap-x-4 sm:justify-center">
                  <a
                    href="#"
                    class="inline-block rounded-lg bg-green-600 px-4 py-1.5 text-base font-semibold leading-7 text-white shadow-sm ring-1 ring-green-600 hover:bg-green-700 hover:ring-green-700"
                  >
                    Explore now
                    <span class="text-indigo-200" aria-hidden="true"
                      >&rarr;</span
                    >
                  </a>
                  <a
                    href="#"
                    class="inline-block rounded-lg px-4 py-1.5 text-base font-semibold leading-7 text-gray-900 ring-1 ring-gray-900/10 hover:ring-gray-900/20"
                  >
                    Check out our Sessions
                    <span class="text-gray-400" aria-hidden="true">&rarr;</span>
                  </a>
                </div>
              </div>
              <div
                class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
              >
                <svg
                  class="relative left-[calc(50%+3rem)] h-[21.1875rem] max-w-none -translate-x-1/2 sm:left-[calc(50%+36rem)] sm:h-[42.375rem]"
                  viewBox="0 0 1155 678"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill="url(#ecb5b0c9-546c-4772-8c71-4d3f06d544bc)"
                    fill-opacity=".3"
                    d="M317.219 518.975L203.852 678 0 438.341l317.219 80.634 204.172-286.402c1.307 132.337 45.083 346.658 209.733 145.248C936.936 126.058 882.053-94.234 1031.02 41.331c119.18 108.451 130.68 295.337 121.53 375.223L855 299l21.173 362.054-558.954-142.079z"
                  />
                  <defs>
                    <linearGradient
                      id="ecb5b0c9-546c-4772-8c71-4d3f06d544bc"
                      x1="1155.49"
                      x2="-78.208"
                      y1=".177"
                      y2="474.645"
                      gradientUnits="userSpaceOnUse"
                    >
                      <stop stop-color="#9089FC"></stop>
                      <stop offset="1" stop-color="#FF80B5"></stop>
                    </linearGradient>
                  </defs>
                </svg>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>
  </section>
</template>

<script>
import Butter from "buttercms";

export default {
  data() {
    return {
      image: null,
      title: null,
      description: null,
    };
  },


  mounted() {
    const butter = Butter(import.meta.env.VITE_BUTTER_API_KEY);


    butter.page
      .retrieve("*", "home")
      .then((resp) => {

        ({
          image: this.image,
          title: this.title,
          description: this.description,
        } = resp.data.data.fields.header_component);
      })
      .catch(function (resp) {
        // console.log(resp);
      });
  },
};
</script>

<style scoped>
.heading-secondary {
  font-weight: 700;
  display: inline-block;
  background-image: linear-gradient(to right, #7ed56f, #28b485);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  letter-spacing: 0.2rem;
  transition: all 0.2s;
}

section {
  height: 90vh;
  display: flex;
}

@media only screen and (max-width: 768px) {
  section {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }

  img {
    height: 10rem;
  }

  h1 {
    font-size: 1rem;
  }
  p {
    font-size: 14px;
  }
  a {
    font-size: 14px;
  }
}
</style>
