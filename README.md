# https-dinho7x.github.io
dinho7x/
│
├── index.html        (Login)
├── register.html     (Cadastro)
├── painel.html       (Painel do usuário)
├── style.css         (Tema dragão)
├── script.js         (IA de sensibilidade)
├── firebase.js       (Login)
└── assets/
    └── dragao.png

function gerarSensibilidade(dpi, estilo) {
  let base = dpi / 10;

  if (estilo === "agressivo") base += 20;
  if (estilo === "preciso") base -= 10;

  return {
    geral: Math.min(200, base + 30),
    redDot: Math.min(200, base + 20),
    scope2x: Math.min(200, base + 10),
    scope4x: Math.min(200, base),
    awm: Math.min(200, base - 10)
  };
}

import { initializeApp } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-app.js";
import { getAuth, signInWithEmailAndPassword } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-auth.js";

const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_DOMINIO.firebaseapp.com",
  projectId: "dinho7x"
};

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);