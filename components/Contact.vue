<template>
  <v-container>
    <v-col align="center" class="mb-12">
      <h2>Contact</h2>
      <form action="#" class="mt-5">
        <div>
          <label for="name">お名前</label>
          <input id="name" type="text" name="youe-name" />
        </div>
        <div>
          <label for="email">メールアドレス</label>
          <input id="email" type="email" name="your-email" />
        </div>
        <div>
          <label for="message">メッセージ</label>
          <textarea id="message" name="your-message"></textarea>
        </div>
        <input type="submit" class="button" value="送信" /></form></v-col
  ></v-container>
</template>
<style scoped>
form div {
  margin-bottom: 14px;
}
label {
  font-size: 1.125rem;
  margin-bottom: 10px;
  display: block;
}
input[type='text'],
input[type='email'],
textarea {
  background: rgba(255, 255, 255, 0.5);
  border: 1px lightgray solid;
  border-radius: 5px;
  padding: 10px;
  font-size: 1rem;
}
input[type='text'],
input[type='email'] {
  width: 100%;
  max-width: 800px;
}
textarea {
  width: 100%;
  max-width: 800px;
  height: 10rem;
}
input[type='submit'] {
  border: none;
  cursor: pointer;
  line-height: 1;
}
</style>
