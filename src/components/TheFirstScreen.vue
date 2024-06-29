<template>
  <div class="containers">
    <div class="containers__left">

    </div>
    <div class="containers__right">

    </div>
    <div class="containers__content">
      <div class="containers__text">
        Информационный портал для абитуриентов ВГТУ
        <h1 class="containers__heading">
          СТРОИМ БУДУЩЕЕ ВМЕСТЕ!
        </h1>
      </div>
      <div class="button red shine" ref="button">
        <span class="button__title" data-title="Выбрать профиль">Выбрать профиль</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.shineItUp(this.$refs.button);
  },
  methods: {
    reset(element) {
      let y = 50;
      let x = 50;
      element.setAttribute("data-x", x);
      element.setAttribute("data-y", y);
      element.style.setProperty("--x", x);
      element.style.setProperty("--y", y);
    },
    shineItUp(element) {
      const rect = element.getBoundingClientRect();
      const data = {
        top: rect.top,
        left: rect.left,
        bottom: rect.top + rect.height,
        right: rect.left + rect.width,
        width: rect.width,
        height: rect.height
      };

      element.addEventListener("mouseout", () => {
        this.reset(element);
      });
      element.addEventListener("mousemove", (e) => {
        if (
            e.clientX + 20 >= data.left &&
            e.clientX - 20 <= data.right &&
            e.clientY + 20 >= data.top &&
            e.clientY - 20 <= data.bottom
        ) {
          const x = Math.round((100 / data.width) * (e.clientX - data.left));
          const y = Math.round((100 / data.height) * (e.clientY - data.top));
          element.setAttribute("data-x", x);
          element.setAttribute("data-y", y);
          element.style.setProperty("--x", x);
          element.style.setProperty("--y", y);
        } else {
          this.reset(element);
        }
      });
    }
  }
};
</script>

<style lang="scss" scoped>
body {
  min-height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1em;
}

.button {
  padding: 1em 2em;
  width: max-content;
  font-size: 1em;
  margin: 0 auto;
  border: 0px;
  transition: all 0.3s cubic-bezier(0, 1.22, 0.67, 1.17);
  border-radius: 1em;
  box-shadow: 0 0 1em 0 rgba(0, 0, 0, 0);
  position: relative;
  transform-style: preserve-3d;
  box-shadow: 0.5em 0.5em 1em 0 rgba(0, 0, 0, 0), 0 -3px 0 0 rgba(0, 0, 0, 0.15) inset;
  transform: scale(var(--s, 1)) rotateX(calc(((var(--y) - 50) * -1) * 0.25deg))
  rotateY(calc(((var(--x) - 50)) * 0.25deg)) translateZ(var(--z, .1em));
}

.button::before,
.button::after {
  width: 100%;
  height: 100%;
  position: absolute;
  left: 50%;
  top: 50%;
  display: block;
  content: "";
  transform: translate(-50%, -50%);
}

.button::after {
  width: calc(100% + 2em);
  height: calc(100% + 2em);
}

.button::before {
  background-image: linear-gradient(
          to right bottom,
          transparent 25%,
          rgba(255, 255, 255, 0.25),
          transparent 75%
  );
  background-size: 200% 200%;
  background-position: calc(var(--x) * 1%) calc(var(--y) * 1%);
  transform: translate(-50%, -50%);
  transition: all 0.3s cubic-bezier(0, 1.22, 0.67, 1.17);
  border-radius: inherit;
}

.button.red {
  border: 1px solid #E5D283;
}

.button span {
  position: relative;
  z-index: 1;
  display: block;
  transform: translateZ(0em);
  transition: all 0.3s ease-in-out;
  transform-style: preserve-3d;
}

.button span::before {
  position: absolute;
  transform: translate(-1px, -1px) translateZ(0em);
  color: #E5D283;
  content: attr(data-title);
  transition: all 0.3s ease-in-out;
  transform-style: preserve-3d;
}

.button:hover {
  --s: 1.05;
  --z: 1em;
  box-shadow: 0.5em 0.5em 1em 0 rgba(0, 0, 0, 0.1), 0 -3px 0 0 rgba(0, 0, 0, 0.15) inset;
}

.button:hover span::before {
  transform: translate(-1px, -1px) translateZ(1em);
}
.containers {
  font-family: Noto Sans, sans-serif;
  position: relative;
  display: flex;
  height: 100vh;

  align-items: center;
  justify-content: center;
}

.containers__left {
  height: 100vh;
  width: 100vw;
  background-image: url("@/assets/img/53060002.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: absolute;
  z-index: 1;
  filter: brightness(80%)
}

.containers__right {
  height: 100vh;
  width: 100vw;
  background-image: url("@/assets/img/5.svg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: absolute;
  z-index: 2;

}

.containers__content {
  position: relative;
  color: white;
  z-index: 4;
  text-align: center;
  font-family: "Microsoft YaHei";

}

.containers__text{
  margin-bottom: 10%;
}


</style>