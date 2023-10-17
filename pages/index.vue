<template>
    <h1>Index Page</h1>

    <Counter name = "One"></Counter>
    <Counter :name="`Counter` + `Two`"></Counter>

    <img src="~/assets/img/cat.png" alt="">
    <img src="/images/cat.png" alt="">
  </template>