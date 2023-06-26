<template>
    <div id="Userinfo"></div>
  </template>
  <script>
  async function UserData() {
    const data = await fetch(
      "https://laiquah.github.io/jsonserver/server.json"
    );
    const jsonData = await data.json();
    console.log(jsonData);
    let peopleData = jsonData.students;
    const display = document.querySelector("#Userinfo");
    peopleData.forEach((data) => {
      display.innerHTML += `
        <div class="card">
          <div class="card-body">
            <h3 class="card-title text-center">${data.first_name} ${data.last_name}</h3>
            <p class="card-text text-center">${data.email}</p>
            </div>
          </div>
        `;
    });
  }
  UserData();
  </script>
  <style scoped>
        
  </style>