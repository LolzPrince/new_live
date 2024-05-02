<template>
  <div class="p-4 pt-16 mx-auto max-w-screen-xl md:flex">
    <div class="grid gap-4 max-w-2xl mx-auto lg:mx-0">
      <div class="relative">
        <img class="h-auto w-full max-w-full rounded-lg object-cover object-center md:h-[480px]"
             src="./../assets/media/animals/dog-3.jpg"
             alt="" />
        <div class="absolute bottom-0 left-0 right-0 text-center text-white text-sm bg-black/30 mx-auto m-1 w-10 text-nowrap">
          1-5
        </div>
      </div>
      <div class="md:grid grid-cols-5 gap-4 hidden">
        <div>
          <img
              src="./../assets/media/animals/dog-4.jpg"
              class="object-cover w-full object-center h-20 max-w-full rounded-lg cursor-pointer opacity-60" alt="gallery-image" />
        </div>
        <div>
          <img
              src="./../assets/media/animals/dog-4.jpg"
              class="object-cover w-full object-center h-20 max-w-full rounded-lg cursor-pointer hover:opacity-75" alt="gallery-image" />
        </div>
        <div>
          <img
              src="./../assets/media/animals/dog1.jpg"
              class="object-cover w-full object-center h-20 max-w-full rounded-lg cursor-pointer hover:opacity-75" alt="gallery-image" />
        </div>
        <div>
          <img
              src="./../assets/media/animals/dog2.jpg"
              class="object-cover object-center w-full h-20 max-w-full rounded-lg cursor-pointer hover:opacity-75" alt="gallery-image" />
        </div>
        <div>
          <img
              src="./../assets/media/animals/dog-3.jpg"
              class="object-cover object-center w-full h-20 max-w-full rounded-lg cursor-pointer hover:opacity-75" alt="gallery-image" />
        </div>
      </div>
    </div>
    <div class="md:w-1/2 md:pl-4 w-full max-w-2xl mx-auto md:mx-0">
      <div class="mx-auto">
        <h3 class="sr-only">Контакты</h3>

        <dl class="max-w-md text-gray-900 divide-y divide-gray-200 dark:text-white dark:divide-gray-700">
          <div class="flex flex-col pb-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Имя нашедшего:</dt>
            <dd class="text-lg font-semibold">Ворончихин Николай Владимирович</dd>
          </div>
          <div class="flex flex-col py-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Место нахождения:</dt>
            <dd class="text-lg font-semibold">г. Ижевск, р-н. Завьяловский, ул. Ленина</dd>
          </div>
          <div class="flex flex-col pt-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Контактный номер телефона:</dt>
            <dd class="text-lg font-semibold">+7 (351) 240-04-40</dd>
          </div>
          <div class="flex flex-col pt-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Дата:</dt>
            <dd class="text-lg font-semibold">12 апреля 2024г.</dd>
          </div>
        </dl>

        <div class="space-y-6">
          <p class="text-base text-gray-900"></p>
        </div>
      </div>
    </div>
  </div>
  <div class="p-4 pt-10 mx-auto max-w-screen-xl md:flex">
    <div class="mx-auto max-w-2xl lg:mx-0 md:max-w-none">
      <h3 class="sr-only">Описание</h3>

      <div class="space-y-6">
        <p class="text-base text-gray-900">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem perferendis praesentium repudiandae voluptatem. Ex molestias optio quasi quis? Aliquid, asperiores dolor enim maiores natus quaerat quia quod suscipit totam voluptatibus?</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardView"
}
</script>
