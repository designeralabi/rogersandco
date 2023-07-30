<template>
  <div
    className="flex flex-col lg:flex-row px-6 py-12  lg:justify-between lg:items-start mx-auto container bg-red-200 xl:px-28 lg:px-0 "
  >
    {/* col_1 */}
    <div className="flex flex-col">
      <h2 className="md:text-4xl text-3xl font-semibold">Rogers & Co.</h2>
      <h3 className="text-2xl my-16 font-semibold">
        We would love to hear from you.
      </h3>
      <h3>info@rogers.co</h3>
      <h3>+234(0)8169169966</h3>
    </div>

    {/* col_2 */}
    <div className="flex flex-col lg:justify-between lg:flex-row gap-x-24">
      <hr />
      {/* col_2_1 */}
      <div className="w-64 my-12 lg:my-0">
        <h2 className="font-bold">Our Address</h2>
        {/* lagos_cel */}
        <div className="my-16">
          <h3 className="font-bold">Lagos State</h3>
          <p className="mt-8">
            1637, Ademola Adetokunbo Street, Victoria Island, Lagos, Nigeria
          </p>
        </div>
        {/* abuja_cel */}
        <div className="mt-16">
          <h3 className="font-bold">Abuja office:</h3>
          <p className="mt-8">
            Suite 312B Samfa Plaza, Plot 2055 Ndola Crescent, Wuse, Zone 5,
            Abuja
          </p>
        </div>
      </div>

      <hr />

      {/* col_2_2 */}
      <div className="my-12 lg:my-0">
        <h2 className="font-bold">Company</h2>
        <div className="my-16">
          {footerRoute.map((path) => { return (
          <Link
            href="{path.urlPath}"
            key="{path.pathName}"
            className="mb-4 block"
          >
            <h2>{path.pathName}</h2>
          </Link>
          ); })}
        </div>
        <div>
          <h2 className="font-bold">follow Us On:</h2>
        </div>
      </div>
    </div>
  </div>
</template>
