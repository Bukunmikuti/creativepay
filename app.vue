<template>
  <Navbar />
  <section id="hero" class="flex gap-10 flex-col justify-center items-center">
    <div class="bg-slate-300 py-2 px-6 mx-32 mt-12 rounded-3xl tracking-tight font-bold text-sm text-gray-900 opacity-50">
      <p>
        <span>Creativepay 2023 release</span>
        <span class="bg-gray-900 rounded-full mx-3 px-2"></span>
        <span>Job seeker</span>
      </p>
    </div>
    <p class="text-5xl font-bold border md:mx-52 text-center leading-tight ">
      Empowering Creative Professionals to Find the Perfect Job
    </p>
    <p class="text-gray-900 text-lg tracking-tight font-bold text-center opacity-50 border md:mx-52">
      We offer a user-friendly interface and advanced search filters that allow
      you to narrow down your search and find the right job faster.
    </p>
    <div class="flex justify-center p-8 gap-8 items-center border rounded-lg">
      <div>
        <p class="number">20.5+</p>
        <p>Million Users</p>
      </div>
      <div>
        <p class="number">7.8 B+</p>
        <p>Jobs Posted</p>
      </div>
      <div>
        <p class="number">201 M</p>
        <p>Proposals Sent</p>
      </div>
    </div>
    <button class="text-white p-4 rounded-3xl tracking-tight font-semibold text-xl">Get started</button>
  </section>
</template>

<style scoped>
#hero>div:first-child {
  letter-spacing: -0.05em;
}

#hero>p:first-child {
  background: linear-gradient(93.66deg, #1C1F32 -1.44%, #1C1F32 -1.43%, #6260DD 76.08%);

}

#hero>button {
  background: rgba(98, 96, 221, 1);
}

#hero .number {
  color: rgba(67, 67, 122, 1);
  font-size: 40px;
  font-weight: bold;
  text-align: center;
  letter-spacing: -0.05em;
}
</style>