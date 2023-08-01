<template>
  <div>
    <!-- main_hero -->
    <div class="w-full">
      <h3>About Us</h3>
    </div>
    <!-- hero -->
    <div>
      <div>
        <div>
          <h3>About Rogers & Co.</h3>
          <p>
            Rogers & Co. is a leading technology organization at the forefront
            of delivering seamless solutions for both software and hardware
            projects. With a proven track record of excellence, we are dedicated
            to guiding our clients through every step of their technological
            journey. With a customer-centric approach, we collaborate closely
            with our clients, understanding their goals and requirements to
            deliver tailor-made solutions. Our commitment to quality and
            precision enables us to deliver projects on time and within budget,
            ensuring utmost satisfaction.
          </p>
          <p>
            Through years of experience, we have mastered the art of efficient
            project management, leveraging cutting-edge tools and methodologies
            to optimize processes and foster innovation. Our passion for
            technology drives us to continuously explore emerging trends,
            guaranteeing that our clients benefit from the latest advancements
            in the industry. Rogers & Co. takes pride in empowering businesses
            to achieve their technological aspirations, whether it’s developing
            robust software applications or implementing sophisticated hardware
            systems. Our focus on transparency, communication, and adaptability
            ensures that our clients remain informed and engaged throughout the
            project lifecycle.
          </p>
        </div>
      </div>
    </div>

    <!-- we are awesome -->
    <div>
      <h3>WE ARE AWESOME</h3>
      <h3>Why Choose Us</h3>
      <div class="grid grid-cols- my-[98px]">
        <div
          v-for="choose in chooses"
          class="p-[21px] flex flex-col text-center"
          :key="choose.title"
        >
          <img
            :src="choose.icon"
            :alt="choose.title"
          />
          <h3 class="font-bold my-[28px]">{{ choose.title }}</h3>
          <p>{{ choose.content }}</p>
        </div>
      </div>
      <div class="flex items-center gap-x-[43px] justify-center">
        <h2>Let’s Start A New Project Together</h2>
        <button
          class="flex items-center bg-[#FEF200] rounded-[40px] font-bold text-black py-[18px] px-[24px]"
        >
          request a Quote <span class="ml-4"> <AkChevronRight /></span>
        </button>
      </div>
    </div>

    <!-- meet the team -->
    <div></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      chooses: [
        {
          icon: "",
          title: "Research and Analysis",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: "",
          title: "Negotiation and Power",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: "",
          title: "Creative and Innovative solutions",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: "",
          title: "Transparency and Ease of work",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
      ],
      teams: [
        {
          name: "Ayodeji Aderoju",
          position: "Managing Partner",
          imgUrl: "#",
        },
        {
          name: "Adedotun Aderibigbe",
          position: "Lead Designer",
          imgUrl: "#",
        },
        {
          name: "Peter Oduntan",
          position: "Digital Products Lead (Software)",
          imgUrl: "#",
        },
        {
          name: "Anne Noah",
          position: "Business Development",
          imgUrl: "#",
        },
        {
          name: "Toluwalase Atolagbe",
          position: "Hardware Lead",
          imgUrl: "#",
        },
        {
          name: "Olaleye Similoluwa",
          position: "Media",
          imgUrl: "#",
        },
      ],
    };
  },
};
</script>
