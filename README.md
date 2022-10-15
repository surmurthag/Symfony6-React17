SYMFONY6 REACT17

De nos jours, avec la montée en puissance des frameworks frontaux comme Angular, React et Vue.js, les backends sans tête sont devenus de plus en plus populaires.

Cependant, la création et la maintenance de deux bases de code distinctes (frontend + backend / API) peuvent rapidement devenir un problème.

Grâce au **[Webpack Encore de Symfony](https://symfony.com/doc/current/frontend.html#webpack-encore)**, le regroupement de
React à l’intérieur d’une application Symfony devient un jeu d’enfant. Il offre également de sérieux avantages, par exemple en s’appuyant sur la couche de sécurité de Symfony pour l’authentification et la gestion des sessions.

Je vais vous expliquer étape par étape ci-dessous comment obtenir une application web Symfony + React

Installez [Symfony binaire](https://symfony.com/download) ,  puis: [node js ](https://nodejs.org/en/download/)

# Créer une application Symfony dans le répertoire symfony-react
$ composer create-project symfony/skeleton:"6.1.*" Symfony6_React

$ cd Symfony6-React

$ composer require symfony/webpack-encore-bundle webapp symfony/apache-pack

# npm package manager
npm i react@17.0.2 react-dom@17.0.2 prop-types@15.6.2 --save

$ npm run dev-server

# Ajoutez la ligne suivante dans webpack.config.js:

<pre class="  language-javascript"><code class="  language-javascript">Encore

<span class="token operator">...</span>

<span class="token comment">// uncomment if you use React</span>
<span class="token punctuation">.</span><span class="token function">enableReactPreset()</span><span class="token punctuation">(</span><span class="token punctuation">)</span>

<span class="token operator">...</span>