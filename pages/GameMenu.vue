<template>
  <div
    class="
      w-full
      h-full
      bg-gradient-to-r
      from-purple-400
      via-Sky-500
      to-Lime-500
      overflow-x-hidden
    "
  >
    <div
      class="w-screen h-full grid place-items-center gap-5 grid-flow-row p-5"
    >
      <div class="w-full h-full flex">
        <div
          class="
            w-2/3
            h-auto
            bg-white
            shadow-5xl
            border-8 border-black
            rounded-2xl
          "
          @mouseenter="buttonsAnimation('.menuButtons', -200)"
          @mouseleave="buttonsAnimationLeave('.menuButtons')"
        >
          <img
            class="w-full h-full object-contain rounded-md"
            src="/lakeMaybe.svg"
            alt=""
          />
        </div>
        <div class="flex flex-col items-center justify-center w-1/3 m-2">
          <button
            class="
              opacity-0
              menuButtons
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
              m-1
            "
          >
            New Game
          </button>
          <button
            class="
              opacity-0
              menuButtons
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
            "
          >
            Continue
          </button>
        </div>
      </div>
      <div class="w-full h-full flex justify-end">
        <div class="flex flex-col items-center justify-center w-1/3 m-2">
          <button
            class="
              menuButtons2
              opacity-0
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
              m-1
            "
          >
            New Game
          </button>
          <button
            class="
              menuButtons2
              opacity-0
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
            "
          >
            Continue
          </button>
        </div>

        <div
          class="
            w-2/3
            h-auto
            bg-white
            shadow-5xl
            border-8 border-black
            rounded-2xl
          "
          @mouseenter="buttonsAnimation('.menuButtons2', 200)"
          @mouseleave="buttonsAnimationLeave('.menuButtons2')"
        >
          <img
            class="w-full h-full object-contain rounded-md"
            src="/houseSwamp.svg"
            alt=""
          />
        </div>
      </div>
      <div class="w-full h-full flex justify-start">
        <div
          class="
            w-2/3
            h-auto
            bg-white
            shadow-5xl
            border-8 border-black
            rounded-2xl
          "
          @mouseenter="buttonsAnimation('.menuButtons3', -200)"
          @mouseleave="buttonsAnimationLeave('.menuButtons3')"
        >
          <img
            class="w-full h-full object-contain rounded-md"
            src="/caveRock.svg"
            alt=""
          />
        </div>
        <div class="flex flex-col items-center justify-center w-1/3 m-2">
          <button
            class="
              menuButtons3
              opacity-0
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
              m-1 m-1
            "
          >
            New Game
          </button>
          <button
            class="
              menuButtons3
              opacity-0
              bg-Amber-500
              p-3
              rounded
              shadow-2xl
              w-40
              h-28
              font-bold
              text-blueGray-200 text-xl
            "
          >
            Continue
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    buttonsAnimation(element, dir) {
      const gsap = this.$gsap

      gsap.to(element, {
        opacity: 1,
        x: dir,
        stagger: 0.2,
      })
    },

    buttonsAnimationLeave(element) {
      const gsap = this.$gsap

      gsap.to(element, {
        x: 0,
        stagger: 0.2,
      })
    },
  },
}
</script>
