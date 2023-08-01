<template>
  <div
    className="flex flex-col lg:flex-row  lg:justify-between lg:items-start mx-auto container max-w-[1155px] py-[52px] mt-[72px]"
  >
    <!-- {/* col_1 */} -->
    <div className="flex flex-col">
      <h2 className="md:text-4xl text-3xl font-semibold">Rogers & Co.</h2>
      <h3 className="text-2xl my-16 font-semibold">
        We would love to hear from you.
      </h3>
      <h3>info@rogers.co</h3>
      <h3>+234(0)8169169966</h3>
      <div class="mt-8">
        <h1 class="">
          Download the <span class="border-b-2">Rogers&Co brochure.pdf</span
          ><span class="ml-2">(11mb)</span>
          <a
            href=""
            download=""
          ></a>
        </h1>
      </div>
    </div>

    <!-- {/* col_2 */} -->
    <div className="flex flex-col lg:justify-between lg:flex-row gap-x-24">
      <hr />
      <!-- {/* col_2_1 */} -->
      <div className="w-64 my-12 lg:my-0">
        <h2 className="font-bold">Our Address</h2>
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
        <h2 className="font-bold">Company</h2>
        <div className="my-16">
          <!-- {footerRoute.map((path) => { return (
          <Link
            href="{path.urlPath}"
            key="{path.pathName}"
            className="mb-4 block"
          >
            <h2>{path.pathName}</h2>
          </Link>
          ); })} -->
          <div class="flex flex-col gap-y-3">
            <a
              v-for="link in links"
              class="block cursor-pointer font-bold capitalize"
              :href="link.linkUrl"
              >{{ link.linkTitle }}</a
            >
          </div>
        </div>
        <div>
          <h2 className="font-bold">follow Us On:</h2>
          <div class="flex items-center gap-x-4 mt-3">
            <AkLinkedInV1Fill />
            <AkFacebookFill />
            <AkTwitterFill />
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="text-center pt-3 pb-11">
    <h3 class="tracking-widest">© 2023 Rogers&Co. All Rights Reserved</h3>
  </div>
</template>

<script>
import { AkLinkedInV1Fill } from "@kalimahapps/vue-icons";
import { AkFacebookFill } from "@kalimahapps/vue-icons";
import { AkTwitterFill } from "@kalimahapps/vue-icons";
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
        {
          linkTitle: "Request A Quote",
          linkUrl: "welcome.com",
        },
      ],
    };
  },
};
</script>
