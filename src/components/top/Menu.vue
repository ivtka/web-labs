<template>
  <menu>
    <li>
      <button class="icon">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="13"
          height="11"
          viewBox="0 0 13 11"
        >
          <g>
            <g>
              <path
                fill="#2b6"
                d="M0 0h9v2H0zm0 3h12v2H0zm0 3h10v2H0zm0 3h13v2H0z"
              />
              <path
                fill="#c4c4c4"
                d="M0 0h9v2H0zm0 3h12v2H0zm0 3h10v2H0zm0 3h13v2H0z"
              />
            </g>
          </g>
        </svg>
      </button>
    </li>
    <nav>
      <ul>
        <li><a href="#">Main</a></li>
        <li><a href="#">Demos</a></li>
        <li><a href="#">Portfolio</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Shortcodes</a></li>
      </ul>
    </nav>
    <li>
      <button class="search"><i class="fas fa-search"></i></button>
    </li>
  </menu>
</template>

<style lang="css">
.top {
  width: 100vw;
}

menu {
  display: flex;
  justify-content: space-around;
  align-items: center;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
  height: 80px;
  font-family: var(--page-font);
  font-size: 14px;
}

menu button {
  border: none;
  outline: none;
  background: none;
  cursor: pointer;
}

nav ul {
  display: flex;
  width: clamp(200px, 500px, 800px);
  justify-content: space-between;
  text-transform: uppercase;
  font-weight: 700;
}

nav ul li a {
  color: #4d4d4d;
}

nav ul li a:hover,
nav ul li a:focus {
  color: #22bb66;
}

.fa-search:hover {
  color: #31aae2;
}

.fa-search {
  color: #c4c4c4;
}

menu li {
  position: relative;
}

menu nav ul > li::after,
menu > li:first-child::after,
menu > li:last-child::before {
  content: "";
  background: url(/wrap.png);
  height: 15px;
  width: 1px;
  display: inline-block;
  position: absolute;
  top: 5%;
}

menu > li:first-child::after,
menu > li:last-child::before {
  height: 30px;
  position: absolute;
  top: -25%;
}

menu > li:first-child::after,
menu nav ul > li::after {
  left: calc(100% + 20px);
}

menu > li:last-child::before {
  right: calc(100% + 20px);
}

</style>