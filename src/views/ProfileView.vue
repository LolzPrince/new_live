<template>
  <div class="pt-16 mx-auto max-w-2xl px-4 sm:px-6 lg:max-w-7xl lg:px-8 flex-col lg:flex-row lg:flex">
    <div class="lg:w-1/2 w-auto lg:mx-0 mx-auto">
      <div class="mt-2 block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
        <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
      </div>
    </div>
    <div class="lg:w-1/2 w-auto lg:mx-0 mx-auto">
      <div class="mx-auto max-w-md">
        <h3 class="sr-only">Профиль</h3>

        <dl class="max-w-md text-gray-900 divide-y divide-gray-200 dark:text-white dark:divide-gray-700">
          <div class="flex flex-col pb-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">ФИО:</dt>
            <dd class="text-lg font-semibold">Ворончихин Николай Владимирович</dd>
          </div>
          <div class="flex flex-col py-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Email:</dt>
            <dd class="text-lg font-semibold">matem9629@gmail.com</dd>
          </div>
          <div class="flex flex-col pt-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Контактный номер телефона:</dt>
            <dd class="text-lg font-semibold">+7 (351) 240-04-40</dd>
          </div>
          <div class="flex flex-col pt-3">
            <dt class="mb-1 text-gray-500 md:text-lg dark:text-gray-400">Дата регистрации:</dt>
            <dd class="text-lg font-semibold">12 апреля 2024г.</dd>
          </div>
        </dl>

        <div class="space-y-6">
          <p class="text-base text-gray-900"></p>
        </div>
      </div>
    </div>
  </div>
  <div class="mx-auto max-w-2xl px-4 sm:px-6 lg:max-w-7xl lg:px-8 hidden lg:block">
    <div class="bg-white py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <dl class="grid grid-cols-1 gap-x-8 gap-y-16 text-center lg:grid-cols-3">
          <div class="mx-auto flex max-w-xs flex-col gap-y-4">
            <dt class="text-base leading-7 text-gray-600">Добавлено</dt>
            <dd class="order-first text-3xl font-semibold tracking-tight text-gray-900 sm:text-5xl">44</dd>
          </div>
          <div class="mx-auto flex max-w-xs flex-col gap-y-4">
            <dt class="text-base leading-7 text-gray-600">Найдено</dt>
            <dd class="order-first text-3xl font-semibold tracking-tight text-gray-900 sm:text-5xl">17</dd>
          </div>
          <div class="mx-auto flex max-w-xs flex-col gap-y-4">
            <dt class="text-base leading-7 text-gray-600">Дней с регистрации</dt>
            <dd class="order-first text-3xl font-semibold tracking-tight text-gray-900 sm:text-5xl">4626</dd>
          </div>
        </dl>
      </div>
    </div>

  </div>
  <div class="mx-auto max-w-2xl px-4 sm:px-6 lg:max-w-7xl lg:px-8">
    <ul class="flex flex-wrap -mb-px text-sm font-medium text-center" id="default-tab" data-tabs-toggle="#default-tab-content" role="tablist">
      <li class="me-2" role="presentation">
        <button :class="{active_page:this.activePage === 'active'}" @click="this.activePage='active'" class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300" id="active" data-tabs-target="#активные" type="button" role="tab" aria-controls="profile" aria-selected="false">Активные</button>
      </li>
      <li class="me-2" role="presentation">
        <button :class="{active_page:this.activePage === 'moderation'}" @click="this.activePage='moderation'" class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300" id="moderation" data-tabs-target="#модерация" type="button" role="tab" aria-controls="dashboard" aria-selected="false">Модерация</button>
      </li>
      <li class="me-2" role="presentation">
        <button :class="{active_page:this.activePage === 'found'}" @click="this.activePage='found'" class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300" id="found" data-tabs-target="#найдено" type="button" role="tab" aria-controls="found" aria-selected="false">Найдено</button>
      </li>
      <li role="presentation">
        <button :class="{active_page:this.activePage === 'archive'}" @click="this.activePage='archive'" class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300" id="archive" data-tabs-target="#архив" type="button" role="tab" aria-controls="archive" aria-selected="false">Архив</button>
      </li>
    </ul>
  </div>
  <div id="default-tab-content">
    <!--Страница Активные-->
    <div :class="{hidden:this.activePage !== 'active'}" class="mx-auto max-w-2xl lg:max-w-7xl" id="active" role="tabpanel" aria-labelledby="active-tab">
      <div class="mx-auto max-w-2xl px-4 sm:px-6 py-3 lg:max-w-7xl lg:px-8">
        <h2 class="sr-only">Активные объявления</h2>

        <div class="grid grid-cols-1 sm:grid-cols-2 py-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 sm:gap-x-6 xl:gap-x-8 w-full bg-gray-200">
          <router-link to="/card" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Завьяловский</p>
            </div>
          </router-link>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
        </div>
        <div class="flex items-center justify-between border-t border-gray-200 bg-white px-4 py-3 sm:px-6 mt-6">
          <div class="flex flex-1 justify-between sm:hidden">
            <a href="#" class="relative inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50">Предыдущий</a>
            <a href="#" class="relative ml-3 inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50">Следующий</a>
          </div>
          <div class="hidden sm:flex sm:flex-1 sm:items-center sm:justify-between">
            <div>
              <p class="text-sm text-gray-700">
                Показано
                <span class="font-medium">1</span>
                по
                <span class="font-medium">12</span>
                из
                <span class="font-medium">97</span>
                результатов
              </p>
            </div>
            <div>
              <nav class="isolate inline-flex -space-x-px rounded-md shadow-sm" aria-label="Pagination">
                <a href="#" class="relative inline-flex items-center rounded-l-md px-2 py-2 text-gray-400 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">
                  <span class="sr-only">Предыдущий</span>
                  <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M12.79 5.23a.75.75 0 01-.02 1.06L8.832 10l3.938 3.71a.75.75 0 11-1.04 1.08l-4.5-4.25a.75.75 0 010-1.08l4.5-4.25a.75.75 0 011.06.02z" clip-rule="evenodd" />
                  </svg>
                </a>
                <!-- Current: "z-10 bg-indigo-600 text-white focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600", Default: "text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:outline-offset-0" -->
                <a href="#" aria-current="page" class="relative z-10 inline-flex items-center bg-indigo-600 px-4 py-2 text-sm font-semibold text-white focus:z-20 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">1</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">2</a>
                <a href="#" class="relative hidden items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0 md:inline-flex">3</a>
                <span class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-700 ring-1 ring-inset ring-gray-300 focus:outline-offset-0">...</span>
                <a href="#" class="relative hidden items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0 md:inline-flex">8</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">9</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">10</a>
                <a href="#" class="relative inline-flex items-center rounded-r-md px-2 py-2 text-gray-400 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">
                  <span class="sr-only">Следующий</span>
                  <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z" clip-rule="evenodd" />
                  </svg>
                </a>
              </nav>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--Объявления на Модерации-->
    <div :class="{hidden:this.activePage !== 'moderation'}" class="mx-auto max-w-2xl lg:max-w-7xl" id="moderation" role="tabpanel" aria-labelledby="moderation-tab">
      <div class="mx-auto max-w-2xl px-4 sm:px-6 py-3 lg:max-w-7xl lg:px-8">
        <h2 class="sr-only">Модерация объявлений</h2>

        <div class="grid grid-cols-1 sm:grid-cols-2 py-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 sm:gap-x-6 xl:gap-x-8 w-full bg-gray-200">
          <router-link to="/card" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Октябрьский</p>
            </div>
          </router-link>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="block aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog1.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900 max-w-min text-nowrap">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/dog2.jpg" alt="dog" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat1.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
          <a href="#" class="group">
            <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7 mx-auto filters__img">
              <img src="./../assets/media/animals/cat2.jpg" alt="cat" class="h-full w-full object-cover object-center group-hover:opacity-75">
            </div>
            <div class="mx-auto text__w">
              <h3 class="mt-4 text-sm text-gray-700">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto debitis earum error esse eveniet ex excepturi fuga...</h3>
              <p class="mt-1 text-lg font-medium text-gray-900">р-н Завьяловский</p>
            </div>
          </a>
        </div>
        <div class="flex items-center justify-between border-t border-gray-200 bg-white px-4 py-3 sm:px-6 mt-6">
          <div class="flex flex-1 justify-between sm:hidden">
            <a href="#" class="relative inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50">Предыдущий</a>
            <a href="#" class="relative ml-3 inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50">Следующий</a>
          </div>
          <div class="hidden sm:flex sm:flex-1 sm:items-center sm:justify-between">
            <div>
              <p class="text-sm text-gray-700">
                Показано
                <span class="font-medium">1</span>
                по
                <span class="font-medium">12</span>
                из
                <span class="font-medium">97</span>
                результатов
              </p>
            </div>
            <div>
              <nav class="isolate inline-flex -space-x-px rounded-md shadow-sm" aria-label="Pagination">
                <a href="#" class="relative inline-flex items-center rounded-l-md px-2 py-2 text-gray-400 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">
                  <span class="sr-only">Предыдущий</span>
                  <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M12.79 5.23a.75.75 0 01-.02 1.06L8.832 10l3.938 3.71a.75.75 0 11-1.04 1.08l-4.5-4.25a.75.75 0 010-1.08l4.5-4.25a.75.75 0 011.06.02z" clip-rule="evenodd" />
                  </svg>
                </a>
                <!-- Current: "z-10 bg-indigo-600 text-white focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600", Default: "text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:outline-offset-0" -->
                <a href="#" aria-current="page" class="relative z-10 inline-flex items-center bg-indigo-600 px-4 py-2 text-sm font-semibold text-white focus:z-20 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">1</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">2</a>
                <a href="#" class="relative hidden items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0 md:inline-flex">3</a>
                <span class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-700 ring-1 ring-inset ring-gray-300 focus:outline-offset-0">...</span>
                <a href="#" class="relative hidden items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0 md:inline-flex">8</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">9</a>
                <a href="#" class="relative inline-flex items-center px-4 py-2 text-sm font-semibold text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">10</a>
                <a href="#" class="relative inline-flex items-center rounded-r-md px-2 py-2 text-gray-400 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0">
                  <span class="sr-only">Следующий</span>
                  <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z" clip-rule="evenodd" />
                  </svg>
                </a>
              </nav>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--Найденные животные-->
    <div :class="{hidden:this.activePage !== 'found'}" class="mx-auto max-w-2xl lg:max-w-7xl" id="found" role="tabpanel" aria-labelledby="found-tab">
      <div class="mx-auto max-w-2xl px-4 sm:px-6 py-3 lg:max-w-7xl lg:px-8">
        <h2 class="sr-only">Найденные животные</h2>
        <p class="text-sm text-gray-500 dark:text-gray-400">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Settings tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
      </div>
    </div>
    <!--Архивные объявления-->
    <div :class="{hidden:this.activePage !== 'archive'}" class="mx-auto max-w-2xl lg:max-w-7xl" id="archive" role="tabpanel" aria-labelledby="archive-tab">
      <div class="mx-auto max-w-2xl px-4 sm:px-6 py-3 lg:max-w-7xl lg:px-8">
        <h2 class="sr-only">Архивные объявления</h2>
        <p class="text-sm text-gray-500 dark:text-gray-400">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Contacts tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileView",
  data:()=>({
    activePage: "active"
  }),
}
</script>

<style scoped>
.active_page{
  -webkit-text-size-adjust: 100%;
  tab-size: 4;
  -webkit-tap-highlight-color: transparent;
  list-style: none;
  box-sizing: border-box;
  border-width: 0;
  border-style: solid;
  border-color: #e5e7eb;
  --tw-border-spacing-x: 0;
  --tw-border-spacing-y: 0;
  --tw-translate-x: 0;
  --tw-translate-y: 0;
  --tw-rotate: 0;
  --tw-skew-x: 0;
  --tw-skew-y: 0;
  --tw-scale-x: 1;
  --tw-scale-y: 1;
  --tw-scroll-snap-strictness: proximity;
  --tw-ring-offset-width: 0px;
  --tw-ring-offset-color: #fff;
  --tw-ring-color: rgb(59 130 246 / 0.5);
  --tw-ring-offset-shadow: 0 0 #0000;
  --tw-ring-shadow: 0 0 #0000;
  --tw-shadow: 0 0 #0000;
  --tw-shadow-colored: 0 0 #0000;
  font-family: inherit;
  font-feature-settings: inherit;
  font-variation-settings: inherit;
  font-size: 100%;
  font-weight: inherit;
  line-height: inherit;
  letter-spacing: inherit;
  margin: 0;
  text-transform: none;
  -webkit-appearance: button;
  background-color: transparent;
  background-image: none;
  cursor: pointer;
  display: inline-block;
  border-top-left-radius: 0.5rem;
  border-top-right-radius: 0.5rem;
  border-bottom-width: 2px;
  --tw-border-opacity: 1;
  border-bottom-color: rgb(79 70 229 / var(--tw-border-opacity));
  padding: 1rem;
  --tw-text-opacity: 1;
  color: rgb(79 70 229 / var(--tw-text-opacity));
}
</style>