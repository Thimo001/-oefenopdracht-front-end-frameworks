<template>
    <v-navigation-drawer class="custom-navbar" expand-on-hover rail>
      <v-list class="custom-list">
        <v-list-item class="logo-item" style="padding: 0;">
          <v-list-item-avatar class="logo-avatar">
            <img
              :src="require('../assets/RealEstateCare/LogoZwart.png')"
              alt="Logo"
              class="full-width-img"
            />
          </v-list-item-avatar>
        </v-list-item>
        <v-divider class="transparent-divider"></v-divider>
        <v-list-item class="contact-item">
             <v-list-item-content class="contact-content">
                 <v-list-item-title class="white-text text-center">Thimo van de Spreng</v-list-item-title>
                 <v-list-item-subtitle class="white-text text-center">Thimo@booomdigital.nl</v-list-item-subtitle>
             </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <style>
  .custom-navbar {
    background: linear-gradient(to right, #435C69, #162730, #05121A);
    transition: background-color 0.3s;
  }
  
  .custom-navbar:hover {
    background: linear-gradient(to right, #435C69, #162730, #05121A);
  }
  
  /* Other styles */
  .logo-avatar {
    width: 100%;
  }
  
  .full-width-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  .transparent-divider {
    border-color: rgba(0, 170, 162, 0.5);
    height: 10px;
  }

  .white-text {
  color: #ffffff;
  }

  .text-center {
  display: flex;
  justify-content: center;
  }
  </style>