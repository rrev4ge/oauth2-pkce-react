# react-oauth2-pkce-btoa

> Authenticate against generic OAuth2 using PKCE and btoa cript method from webApi

## Install

```bash
npm install --save react-oauth2-pkce-btoa
```

## Usage

```tsx

import React from 'react'
import { AuthProvider, AuthService } from 'react-oauth2-pkce'

import { Routes } from './Routes';

const authService = new AuthService({
  clientId: process.env.REACT_APP_CLIENT_ID || 'CHANGEME',
  location: window.location,
  provider: process.env.REACT_APP_PROVIDER || 'https://sandbox.auth.ap-southeast-2.amazoncognito.com/oauth2',
  redirectUri: process.env.REACT_APP_REDIRECT_URI || window.location.origin,
  scopes: ['openid', 'profile'],
  cacheStorage: 'localStorage', // Optional ('localStorage' || 'sessionStorage') - default 'localStorage'
});

const App = () => {
  return (
    <AuthProvider authService={authService} >
      <Routes />
    </AuthProvider>
  )
}

```
