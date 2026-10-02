# Prácticum 2027 — Classical Conversations RD

Landing page del Prácticum 2027 (Ciencias). Sitio estático en Netlify con pago por Stripe Checkout
(`netlify/functions/create-checkout-session.js`).

Variables de entorno en Netlify: `STRIPE_SECRET_KEY`, `PRICE_ADULTO`, `PRICE_NINO`, `PRICE_ALMUERZO`
(precios de Stripe creados para 2027). Códigos promocionales: `CCRD2027`, `HOMELIFE`.

Vista previa local: `python3 -m http.server 4727` y abrir http://localhost:4727/

Investigación de contenido, diseño y UX en `docs/`.
