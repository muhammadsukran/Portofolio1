<template>
    <div class="profile-container">
      <img src="@/components/icons/Profile.png" alt="Profile Picture" class="profile-img" />
    </div>
  </template>
  
  <style scoped>
  .profile-container {
    position: fixed;
    top: 80px;
    bottom: 20px; 
    left: 20px; 
    z-index: 1; 
  }
  
  .profile-img {
    width: 250px; 
    height: auto; 
    border-radius: 50%;
  }
  </style>
  