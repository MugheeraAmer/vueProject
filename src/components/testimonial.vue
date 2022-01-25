<template>
  <div class="testimonial-container">
    <div class="detail detail1">
      <img src="" alt="" />
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit rerum
        quod voluptatibus illo, ullam eius similique hic pariatur aspernatur
        aliquid dicta quam nisi excepturi ut consectetur temporibus non? Laborum
        voluptatibus facilis placeat ut dolores voluptatem voluptates quis
        quisquam, porro incidunt vitae fugit est inventore voluptas vel
        deserunt, numquam repellendus ad?
      </p>
    </div>
    <div class="detail detail2">
      <img src="" alt="" />
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum rem
        repellat doloremque recusandae? Fugit dolore itaque aspernatur, nostrum
        sapiente, tempore possimus reiciendis expedita, minus vitae nisi
        excepturi consequuntur quisquam explicabo laborum ab aut earum
        molestiae. Perferendis totam sequi possimus assumenda similique omnis
        laborum labore beatae modi error! Modi, repellendus repudiandae?
      </p>
    </div>
    <div class="detail detail3">
      <img src="" alt="" />
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur
        mollitia aliquam quasi ipsum maxime error, obcaecati, ab quas excepturi
        doloremque hic sapiente est rerum! Sequi id voluptas nam maiores. Omnis
        eum perferendis beatae, aliquid suscipit placeat architecto magnam nisi
        reiciendis?
      </p>
    </div>
    <div class="detail detail4">
      <img src="" alt="" />
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. At ipsum
        aliquid amet assumenda officiis fugiat odit ut, a laudantium harum
        delectus saepe temporibus reiciendis explicabo alias id ipsa quisquam
        expedita, accusantium consequuntur dolorem quaerat nam. Velit dolores
        autem cupiditate modi.
      </p>
    </div>
    <div class="detail detail5">
      <img src="" alt="" />
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum sed
        delectus soluta nesciunt officiis sapiente neque veniam earum dicta
        eveniet enim porro animi obcaecati voluptates ipsa vitae et asperiores,
        nulla magni cum. Quam nihil, similique fuga iure eum consequatur
        voluptate?
      </p>
    </div>
    <button
      @click="
        hideButtonLoc > 0 && buttonText == 'Hide Template'
          ? hideTestimonials()
          : showTestimonials()
      "
    >
      {{ buttonText }}
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      buttonText: "Hide Template",
      hideButtonLoc: 5,
    };
  },

  methods: {
    hideTestimonials() {
      if (this.hideButtonLoc == 5) {
        document.querySelector(".detail5").classList.add("hidetestimonial");
        this.hideButtonLoc--;
      } else if (this.hideButtonLoc == 4) {
        document.querySelector(".detail4").classList.add("hidetestimonial");
        this.hideButtonLoc--;
      } else if (this.hideButtonLoc == 3) {
        document.querySelector(".detail3").classList.add("hidetestimonial");
        this.hideButtonLoc--;
      } else if (this.hideButtonLoc == 2) {
        document.querySelector(".detail2").classList.add("hidetestimonial");
        this.hideButtonLoc--;
      } else if (this.hideButtonLoc == 1) {
        document.querySelector(".detail1").classList.add("hidetestimonial");
        this.hideButtonLoc--;
        this.buttonText = "Show Template";
        console.log(this.hideButtonLoc);
      }
    },
    showTestimonials() {
      if (this.hideButtonLoc == 4) {
        document.querySelector(".detail5").classList.remove("hidetestimonial");
        this.hideButtonLoc++;
        this.buttonText = "Hide Template";
      } else if (this.hideButtonLoc == 3) {
        document.querySelector(".detail4").classList.remove("hidetestimonial");
        this.hideButtonLoc++;
      } else if (this.hideButtonLoc == 2) {
        document.querySelector(".detail3").classList.remove("hidetestimonial");
        this.hideButtonLoc++;
      } else if (this.hideButtonLoc == 1) {
        document.querySelector(".detail2").classList.remove("hidetestimonial");
        this.hideButtonLoc++;
      } else if (this.hideButtonLoc == 0) {
        document.querySelector(".detail1").classList.remove("hidetestimonial");
        this.hideButtonLoc++;
      }
    },
  },
};
</script>

<style>
.testimonial-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;
  background: var(--primary-color);
}
.detail {
  display: grid;
  grid-template-columns: 1fr 1fr;
  height: 25vh;
  transition: all 2s ease;
}
img {
  width: 50%;
  height: 80%;
  border-radius: 10px;
  margin: auto;
  background: var(--ternary-color);
}
.detail p {
  text-align: center;
  margin: auto 0;
  padding: 0 2rem;
}

button {
  width: 12rem;
  padding: 1rem 2rem;
  background: var(--secondary-color);
  color: white;
  font-size: 1rem;
  transition: background 500ms ease;
  margin: 2rem 0;
}

button:hover {
  background: var(--primary-color);
}

.hidetestimonial {
  visibility: hidden;
  height: 0;
  opacity: 0;
  transition: all 2s ease;
}
</style>
