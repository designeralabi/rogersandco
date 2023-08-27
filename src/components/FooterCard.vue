<template>
  <div class="bg-[#3F4041] z-50 pl-44 relative">
    <div
      class="bg-white h-[130px] block absolute top-0 -z-20 w-full left-0 right-0"
    ></div>
    <div
      className="flex flex-col lg:flex-row  h-[650px] lg:justify-between lg:items-start pl-[100px] pr-[70px] pt-[95px] pb-[50px] bg-[#555657] text-white"
    >
      <!-- {/* col_1 */} -->
      <div className="flex flex-col">
        <div>
          <img
            :src="imgPath"
            alt="logo"
            class="w-[180px] invert"
          />
        </div>
        <h3 className="text-4xl text-white my-16 font-semibold">
          We would love to hear from you.
        </h3>
        <h3 class="mb-8 max-w-[550px] font-inter">
          If you have a project or collaboration that you would like to discuss
          with us, or if you are curious to hear more about how we can help you,
          we look forward to hearing from you.
        </h3>
        <h3>info@rogers.co</h3>
        <h3>+234(0)8169169966</h3>
        <div class="mt-8">
          <h1>
            Download the
            <span
              class="border-b-2 hover:bg-gray-900 transition-all border-gray-900 ease-in-out"
            >
              <a
                href="/src/assets/Rogers & Co Company Profile V2.pdf"
                download="rogers brochure"
                >Rogers&Co brochure.pdf</a
              > </span
            ><span class="ml-2">(11mb) here</span>
          </h1>
        </div>
      </div>

      <!-- {/* col_2 */} -->
      <div className="flex flex-col lg:justify-between lg:flex-row gap-x-24">
        <hr />
        <!-- {/* col_2_1 */} -->
        <div className="w-64 my-12 lg:my-0">
          <!-- {/* lagos_cel */} -->
          <div className="my-16">
            <h3 className="font-bold">Lagos State</h3>
            <p className="mt-8">
              1637, Ademola Adetokunbo Street, Victoria Island, Lagos, Nigeria
            </p>
          </div>
          <!-- {/* abuja_cel */} -->
          <div className="mt-16">
            <h3 className="font-bold">Abuja office:</h3>
            <p className="mt-8">
              Suite 312B Samfa Plaza, Plot 2055 Ndola Crescent, Wuse, Zone 5,
              Abuja
            </p>
          </div>
        </div>

        <hr />

        <!-- {/* col_2_2 */} -->
        <div className="my-12 lg:my-0">
          <div className="my-16">
            <div class="flex flex-col gap-y-3">
              <a
                v-for="link in links"
                class="block cursor-pointer font-bold capitalize"
                :href="link.linkUrl"
                >{{ link.linkTitle }}</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center text-sm pt-5 pb-11 text-white flex justify-between">
      <h3 class="tracking-widest">© 2023 Rogers&Co. All Rights Reserved</h3>
      <div class="flex items-center gap-x-4 mr-16">
        <h2 className="font-bold">follow Us On -</h2>
        <div class="flex items-center gap-x-4">
          <AkLinkedInV1Fill />
          <AkFacebookFill />
          <AkTwitterFill />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { AkLinkedInV1Fill } from "@kalimahapps/vue-icons";
import { AkFacebookFill } from "@kalimahapps/vue-icons";
import { AkTwitterFill } from "@kalimahapps/vue-icons";
import logo from "../assets/logo_800_white_background.png";
export default {
  components: {
    AkLinkedInV1Fill,
    AkFacebookFill,
    AkTwitterFill,
  },
  data() {
    return {
      links: [
        {
          linkTitle: "home",
          linkUrl: "welcome.com",
        },
        {
          linkTitle: "Software",
          linkUrl: "welcome.com",
        },
        {
          linkTitle: "Hardware",
          linkUrl: "welcome.com",
        },
        {
          linkTitle: "About Us",
          linkUrl: "welcome.com",
        },
        {
          linkTitle: "Our Services",
          linkUrl: "welcome.com",
        },
      ],
      imgPath: logo,
    };
  },
};
</script>
