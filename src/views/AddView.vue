<template>
  <div class="p-4 pt-16 mx-auto max-w-screen-xl">
    <div class="mx-auto max-w-2xl text-center">
      <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl mx-auto">Подать объявление</p>
    </div>
    <div class="max-w-xl mx-auto">
      <form>
        <div class="mb-4">
          <label for="phone" class="block text-sm font-medium text-gray-700">Номер телефона</label>
          <input type="tel" placeholder="+7 (351) 240-04-40" id="phone" name="phone" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" required>
        </div>

        <div class="mb-4">
          <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
          <input type="email" placeholder="name@mail.com" id="email" name="email" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" required>
        </div>

        <div class="inline-flex items-center">
          <label class="relative -ml-2.5 flex cursor-pointer items-center rounded-full p-3" for="remember">
            <input type="checkbox"
                   class="before:content[''] peer relative h-5 w-5 cursor-pointer appearance-none rounded-md border border-blue-gray-200 transition-all before:absolute before:top-2/4 before:left-2/4 before:block before:h-12 before:w-12 before:-translate-y-2/4 before:-translate-x-2/4 before:rounded-full before:bg-blue-gray-500 before:opacity-0 before:transition-opacity checked:border-gray-900 checked:bg-gray-900 checked:before:bg-gray-900 hover:before:opacity-10"
                   id="remember" />
            <span
                class="absolute text-white transition-opacity opacity-0 pointer-events-none top-2/4 left-2/4 -translate-y-2/4 -translate-x-2/4 peer-checked:opacity-100">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5" viewBox="0 0 20 20" fill="currentColor"
                   stroke="currentColor" stroke-width="1">
                <path fill-rule="evenodd"
                      d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                      clip-rule="evenodd"></path>
              </svg>
            </span>
          </label>
          <label class="mt-px font-light text-gray-700 cursor-pointer select-none" for="remember">
            <p class="flex items-center font-sans text-sm antialiased font-normal leading-normal text-gray-700">
              Согласие на Автоматическую регистрацию
            </p>
          </label>
        </div>

        <div class="mb-4">
          <label for="animal" class="block text-sm font-medium text-gray-700">Вид животного</label>
          <select id="animal" class="border border-gray-300 rounded-md p-2 mt-1 w-full">
            <option value="" selected>Выберите вид животного</option>
            <option value="dog">Собака</option>
            <option value="cat">Кошка</option>
            <option value="bird">Птица</option>
            <option value="rabbit">Кролик</option>
          </select>
        </div>

        <div class="mb-4">
          <label class="block text-sm font-medium text-gray-700">Фото найденного животного (не более 5)</label>
          <!--<input type="file" @change="onFileChange" id="animal-photo" name="animal-photo" accept="image/*" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" multiple>-->

          <div class="flex items-center justify-center w-full">
            <label for="dropzone-file" class="flex flex-col items-center justify-center w-full h-64 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
              <div class="relative flex flex-col items-center justify-center pt-5 pb-6">
                <svg class="w-8 h-8 mb-4 text-gray-500 dark:text-gray-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 16">
                  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 13h3a3 3 0 0 0 0-6h-.025A5.56 5.56 0 0 0 16 6.5 5.5 5.5 0 0 0 5.207 5.021C5.137 5.017 5.071 5 5 5a4 4 0 0 0 0 8h2.167M10 15V6m0 0L8 8m2-2 2 2"/>
                </svg>
                <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                <p class="text-xs text-gray-500 dark:text-gray-400">PNG, JPG (MAX. 260x260px)</p>
              </div>
              <input @change="onFileChange" id="dropzone-file" type="file" class="absolute max-w-xl mx-auto h-244 w-full z_1" multiple/>
            </label>
          </div>

          <div class="md:grid grid-cols-5 gap-4 hidden mt-2" v-if="images.length">
            <div v-for="(image, i) in images" :key="{i}">
              <img
                  :src="image"
                  class="object-cover w-full object-center h-20 max-w-full rounded-lg cursor-pointer opacity-30" alt="gallery-image" />
              <button @click="removeImage(i)">удалить</button>
            </div>
          </div>
        </div>

        <div class="mb-4">
          <label for="additional-info" class="block text-sm font-medium text-gray-700">Описание</label>
          <textarea id="additional-info" name="additional-info" rows="3" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"></textarea>
        </div>

        <div class="mb-4">
          <label for="district" class="block text-sm font-medium text-gray-700">Район</label>
          <input type="text" id="district" name="district" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500">
        </div>

        <div class="mb-4">
          <label for="date" class="block text-sm font-medium text-gray-700">Дата</label>
          <input type="date" id="date" name="date" class="block w-full p-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500">
        </div>

        <div class="inline-flex items-center">
          <label class="relative -ml-2.5 flex cursor-pointer items-center rounded-full p-3" for="remember2">
            <input type="checkbox"
                   class="before:content[''] peer relative h-5 w-5 cursor-pointer appearance-none rounded-md border border-blue-gray-200 transition-all before:absolute before:top-2/4 before:left-2/4 before:block before:h-12 before:w-12 before:-translate-y-2/4 before:-translate-x-2/4 before:rounded-full before:bg-blue-gray-500 before:opacity-0 before:transition-opacity checked:border-gray-900 checked:bg-gray-900 checked:before:bg-gray-900 hover:before:opacity-10"
                   id="remember2" />
            <span
                class="absolute text-white transition-opacity opacity-0 pointer-events-none top-2/4 left-2/4 -translate-y-2/4 -translate-x-2/4 peer-checked:opacity-100">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5" viewBox="0 0 20 20" fill="currentColor"
                   stroke="currentColor" stroke-width="1">
                <path fill-rule="evenodd"
                      d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                      clip-rule="evenodd"></path>
              </svg>
            </span>
          </label>
          <label class="mt-px font-light text-gray-700 cursor-pointer select-none" for="remember2">
            <p class="flex items-center font-sans text-sm antialiased font-normal leading-normal text-gray-700">
              Согласие на обработку Персональных данных
            </p>
          </label>
        </div>

        <button type="submit" class="block border border-bg-indigo-600 bg-indigo-600 text-white font-semibold rounded-md p-2 hover:bg-indigo-700 active:bg-indigo-800 mt-1 transition-colors mx-auto">Отправить</button>
      </form>
    </div>
  </div>
</template>
<style>
.h-244{
  max-height: 244px;
  height: 100%;
}
.z_1{
  z-index: 10;
  opacity: 0;
}
</style>
<script>
export default {
  name: "AddView",
  data:()=>({
    images:[]
  }),
  methods: ({
    onFileChange(e) {
      this.createImages(e.target.files || e.dataTransfer.files);
    },
    createImages(files) {
      [...files].forEach(file => {
        const reader = new FileReader();
        reader.onload = e => this.images.push(e.target.result);
        reader.readAsDataURL(file);
      });
    },
    removeImage(index) {
      this.images.splice(index, 1);
    },
  }),
}
</script>