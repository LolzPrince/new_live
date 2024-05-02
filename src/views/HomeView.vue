<template>
  <div class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl mx-auto">Поиск питомца среди объявлений</p>
      </div>
      <form class="lg:flex flex-col w-full max-w-2xl mx-auto mt-6 hidden">
        <div class="flex justify-between mt-4">
          <div class="mr-2 flex-1">
            <input type="text" id="searchText" placeholder="Введите текст для поиска" class="border border-gray-300 rounded-md p-2 mt-1 w-full">
          </div>
          <div class="">
            <button type="submit" class="border border-bg-indigo-600 bg-indigo-600 text-white font-semibold rounded-md p-2 hover:bg-indigo-700 active:bg-indigo-800 mt-1 transition-colors mx-auto">Поиск питомца</button>
          </div>
        </div>
        <div class="flex justify-between mt-4">
          <div class="w-1/2 mr-2">
            <input type="text" id="district" placeholder="Введите район" class="border border-gray-300 rounded-md p-2 mt-1 w-full">
          </div>
          <div class="w-1/2">
            <select id="animal" class="border border-gray-300 rounded-md p-2 mt-1 w-full">
              <option value="" selected>Выберите вид животного</option>
              <option value="dog">Собака</option>
              <option value="cat">Кошка</option>
              <option value="bird">Птица</option>
              <option value="rabbit">Кролик</option>
            </select>
          </div>
        </div>
      </form>
      <form class="flex flex-col w-full max-w-2xl mx-auto mt-6 lg:hidden">
        <div class="flex-col justify-between mt-4">
          <input type="text" placeholder="Введите текст для поиска" class="border border-gray-300 rounded-md p-2 mt-1 w-full focus:border-black focus:border-2 focus:outline-none">
          <input type="text" placeholder="Введите район" class="border border-gray-300 rounded-md p-2 mt-1 w-full focus:border-black focus:border-2 focus:outline-none">
          <select class="border border-gray-300 rounded-md p-2 mt-1 w-full focus:border-2 focus:border-black focus:outline-none">
            <option value="" selected>Выберите вид животного</option>
            <option value="dog">Собака</option>
            <option value="cat">Кошка</option>
            <option value="bird">Птица</option>
            <option value="rabbit">Кролик</option>
          </select>
          <div class="w-full">
            <button type="submit" class="block border border-bg-indigo-600 bg-indigo-600 text-white font-semibold rounded-md p-2 hover:bg-indigo-700 active:bg-indigo-800 mt-1 transition-colors mx-auto">Поиск питомца</button>
          </div>
        </div>
      </form>
    </div>
  </div>
  <div class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-600">Важен каждый</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Найди своего друга с нами!</p>
        <p class="mt-6 text-lg leading-8 text-gray-600">Сервис "Новая жизнь" помогает найти потерянных питомцев. Оставляйте информацию о найденных животных, помогайте им вернуться к хозяевам. Владельцы потерявших питомцев могут быстро и легко искать их на нашем сайте. Давайте вместе делать добро и возвращать утраченное счастье!</p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
        <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
          <div class="relative pl-16">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 18 9 11.25l4.306 4.306a11.95 11.95 0 0 1 5.814-5.518l2.74-1.22m0 0-5.94-2.281m5.94 2.28-2.28 5.941" />
                </svg>
              </div>
              Эффективность
            </dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">Мы предоставляем быструю и удобную платформу для поиска потерянных домашних питомцев, что помогает сократить время на их возвращение к хозяевам.</dd>
          </div>
          <div class="relative pl-16">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M14.25 6.087c0-.355.186-.676.401-.959.221-.29.349-.634.349-1.003 0-1.036-1.007-1.875-2.25-1.875s-2.25.84-2.25 1.875c0 .369.128.713.349 1.003.215.283.401.604.401.959v0a.64.64 0 0 1-.657.643 48.39 48.39 0 0 1-4.163-.3c.186 1.613.293 3.25.315 4.907a.656.656 0 0 1-.658.663v0c-.355 0-.676-.186-.959-.401a1.647 1.647 0 0 0-1.003-.349c-1.036 0-1.875 1.007-1.875 2.25s.84 2.25 1.875 2.25c.369 0 .713-.128 1.003-.349.283-.215.604-.401.959-.401v0c.31 0 .555.26.532.57a48.039 48.039 0 0 1-.642 5.056c1.518.19 3.058.309 4.616.354a.64.64 0 0 0 .657-.643v0c0-.355-.186-.676-.401-.959a1.647 1.647 0 0 1-.349-1.003c0-1.035 1.008-1.875 2.25-1.875 1.243 0 2.25.84 2.25 1.875 0 .369-.128.713-.349 1.003-.215.283-.4.604-.4.959v0c0 .333.277.599.61.58a48.1 48.1 0 0 0 5.427-.63 48.05 48.05 0 0 0 .582-4.717.532.532 0 0 0-.533-.57v0c-.355 0-.676.186-.959.401-.29.221-.634.349-1.003.349-1.035 0-1.875-1.007-1.875-2.25s.84-2.25 1.875-2.25c.37 0 .713.128 1.003.349.283.215.604.401.96.401v0a.656.656 0 0 0 .658-.663 48.422 48.422 0 0 0-.37-5.36c-1.886.342-3.81.574-5.766.689a.578.578 0 0 1-.61-.58v0Z" />
                </svg>
              </div>
              Сообщество
            </dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">Мы объединяем людей и создаем сообщество поддержки и помощи в поиске потерянных животных, что увеличивает шансы на успешное возвращение домашних питомцев.</dd>
          </div>
          <div class="relative pl-16">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 5.25a3 3 0 0 1 3 3m3 0a6 6 0 0 1-7.029 5.912c-.563-.097-1.159.026-1.563.43L10.5 17.25H8.25v2.25H6v2.25H2.25v-2.818c0-.597.237-1.17.659-1.591l6.499-6.499c.404-.404.527-1 .43-1.563A6 6 0 1 1 21.75 8.25Z" />
                </svg>
              </div>
              Простота использования
            </dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">Интуитивно понятный интерфейс сайта делает процесс размещения информации о найденных или потерянных животных легким и доступным для всех пользователей.</dd>
          </div>
          <div class="relative pl-16">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12Z" />
                </svg>
              </div>
              Доброта и сострадание
            </dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">Сервис "Новая жизнь" основан на принципах доброты и сострадания к животным, что делает его местом, где каждый может помочь потерянным питомцам.</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "HomeVue"
}
</script>


