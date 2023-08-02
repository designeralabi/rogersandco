<template>
  <div class="">
    <!-- hero section -->
    <AppHeader />
    <!-- main_hero -->
    <div
      class="w-full p-[98px] h-[368px] flex items-center justify-center bg-[url('./assets/teamwork_bg.png')] bg-no-repeat bg-cover relative"
    >
      <div
        class="bg-black/80 top-0 bottom-0 left-0 right-0 w-full absolute h-full z-10"
      ></div>
      <h3 class="text-center text-[28px] font-bold z-30">About Us</h3>
    </div>
    <!-- hero -->
    <div class="bg-[#252533] py-[80px]">
      <div
        class="max-w-[1155px] flex items-center mx-auto gap-x-[122px] justify-between"
      >
        <div class="">
          <img
            :src="float_a"
            alt="float_a"
            width="238px"
            class="w-[238px] translate-x-40"
          />
          <img
            :src="float_b"
            alt="float_b"
            width="238px"
            class="w-[238px] z-30"
          />
        </div>
        <div class="w-[517px]">
          <h3 class="font-bold text-[32px] my-4">About Rogers & Co.</h3>
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
          <p class="mt-8">
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
    <div class="py-[60px]">
      <h3 class="text-yellow-200 text-center mb-5">WE ARE AWESOME</h3>
      <h3 class="text-center text-3xl font-bold">Why Choose Us</h3>
      <div
        class="grid grid-cols-4 rounded-md my-[98px] gap-x-[40px] max-w-[1155px] mx-auto"
      >
        <div
          v-for="choose in chooses"
          class="p-[21px] w-[210] gap-x-[21px] flex flex-col text-center items-center justify-center bg-[#252533] text-white"
          :key="choose.title"
        >
          <img
            :src="choose.icon"
            :alt="choose.title"
            class="w-[60px] h-[60px]"
          />
          <h3 class="font-bold text-lg my-[28px]">{{ choose.title }}</h3>
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
    <div class="bg-[#252533] py-[80px]">
      <h3 class="uppercase text-center text-yellow-200 my-[16px]">
        Meet the Team
      </h3>
      <h3 class="text-center font-bold text-3xl mb-11">Our Team Members</h3>
      <div class="grid grid-cols-4 max-w-[1155px] mx-auto my-[80px] gap-12">
        <div
          v-for="team in teams"
          :key="team.name"
        >
          <div class="w-[210px] h-[260px]">
            <img
              :src="team.imgUrl"
              :alt="team.name"
              width="210px"
              height="260px"
              class="w-full h-full object-cover"
            />
          </div>

          <div class="mt-5">
            <h3>{{ team.name }}</h3>
            <h3 class="text-yellow-200">{{ team.position }}</h3>
          </div>
        </div>
      </div>
    </div>

    <!-- footer -->
    <footerCard />
  </div>
</template>

<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";
import research from "../assets/icons/Research.png";
import idea from "../assets/icons/Idea.png";
import conversation from "../assets/icons/Conversation.png";
import seo from "../assets/icons/Seo.png";
import ayodeji from "../assets/teams/Ayodeji_Aderoju.png";
import adedotun from "../assets/teams/Adedotun_Aderibigbe.png";
import anne from "../assets/teams/Anne_Noah.png";
import olaleye from "../assets/teams/Olaleye_Similoluwa.png";
import peter from "../assets/teams/Peter_Oduntan.png";
import tolu from "../assets/teams/Toluwalase_Atolagbe.png";
import float_a from "../assets/float_a.png";
import float_b from "../assets/float_b.png";
export default {
  components: {
    name: "About",
    AppHeader,
    footerCard,
  },
  data() {
    return {
      float_a: float_a,
      float_b: float_b,
      chooses: [
        {
          icon: research,
          title: "Research and Analysis",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: conversation,
          title: "Negotiation and Power",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: idea,
          title: "Creative and Innovative solutions",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
        {
          icon: seo,
          title: "Transparency and Ease of work",
          content:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry.",
        },
      ],
      teams: [
        {
          name: "Ayodeji Aderoju",
          position: "Managing Partner",
          imgUrl: ayodeji,
        },
        {
          name: "Adedotun Aderibigbe",
          position: "Lead Designer",
          imgUrl: adedotun,
        },
        {
          name: "Peter Oduntan",
          position: "Digital Products Lead (Software)",
          imgUrl: peter,
        },
        {
          name: "Anne Noah",
          position: "Business Development",
          imgUrl: anne,
        },
        {
          name: "Toluwalase Atolagbe",
          position: "Hardware Lead",
          imgUrl: tolu,
        },
        {
          name: "Olaleye Similoluwa",
          position: "Media",
          imgUrl: olaleye,
        },
      ],
    };
  },
};
</script>
