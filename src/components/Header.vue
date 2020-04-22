<template>
    <div class="header">
      <div class="header__logo">
        <div class="header__container">
          <h5 class="logo__text"><span>Vincent</span> <span>Van</span> <span>Gogh</span></h5>
          <p class="logo__title">Amsterdam</p>
        </div>
      </div>
      <nav role="navigation" class="header__navigation">
        <div id="menuToggle">
          <input type="checkbox" />
          Menu
          <ul id="menu">
            <a href="#"><li>Home</li></a>
            <a href="#"><li>About</li></a>
            <a href="#"><li>Info</li></a>
            <a href="#"><li>Contact</li></a>
          </ul>
        </div>
      </nav>
    </div>
</template>

<script>
export default {

}
</script>

<style>

.header {
  height: 12vh;
  display: flex;
  background-color: #fef6f0;
}

.header__logo {
  width: 25%;
  background-color: #000;
}

.header__container {
  width: 70%;
  height: 100%;
  padding: 0 10px 0 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  color: #fff;
  text-align: end;
}

.logo__text {
  display: flex;
  flex-direction: column;
}

.logo__title {
  margin-top: 5px;
  font-size: 10px;
}

#menuToggle
{
  display: block;
  position: absolute;
  top: 20px;
  right: 20px;
  font-size: 20px;
  
  z-index: 1;
  
  user-select: none;
}

#menuToggle a
{
  text-decoration: none;
  color: #232323;
  
  transition: color 0.3s ease;
}

#menuToggle a:hover
{
  color: tomato;
}


#menuToggle input
{
  display: block;
  width: 40px;
  height: 32px;
  position: absolute;
  top: -7px;
  left: -5px;
  
  cursor: pointer;
  
  opacity: 0;
  z-index: 2;
  
  -webkit-touch-callout: none;
}

#menu
{
  position: absolute;
  width: 300px;
  margin: -100px 0 0 -50px;
  padding: 50px;
  padding-top: 125px;
  
  background: #ededed;
  list-style-type: none;
  -webkit-font-smoothing: antialiased;
  
  transform-origin: 0% 0%;
  transform: translate(50%, 0);
  
  transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0);
}

#menu li
{
  padding: 10px 0;
  font-size: 22px;
}

#menuToggle input:checked ~ ul
{
  transform: translate(-20%, 0);;
}
</style>