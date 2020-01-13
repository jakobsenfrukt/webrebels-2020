<template>
  <main class="simple-page helpers">
    <div class="hero">
      <h1 class="page-title">Sponsors</h1>
      <p class="lead">The Web Rebels Conference is run by a team of voulenteers and we run our organization as a non-profit. Without the help of our team of sponsors there would be no conference. Show them some love!
      <br /><br/>Want to join the team for 2017? <a href="mailto:sponsor@webrebels.org" target="blank">email us</a> to be first in line for the most awesome packages ;)</p>
    </div>
    <h2>Become a sponsor</h2>
    <p>We are looking for sponsors to our developer conference Web Rebels. We have over 300 attendees of people interested in web development and the conference goes over two days. There will be workshops as well!<br /><br />This year we are offering 3 different sponsorship packages, Bronze, Silver and Gold. See below for more details.</p>
    <div class="package-list">
      <div class="package gold">
        <h2>Gold</h2>
        <p>We are looking for sponsors to our developer conference Web Rebels. We have over 300 attendees of people interested in web development and the conference goes over two days. There will be workshops as well!</p>
        <div class="diamond gold"></div>
      </div>
      <div class="package silver">
        <h2>Silver</h2>
        <p>We are looking for sponsors to our developer conference Web Rebels. We have over 300 attendees of people interested in web development and the conference goes over two days. There will be workshops as well!.</p>
        <div class="diamond silver"></div>
      </div>
      <div class="package bronze">
        <h2>Bronze</h2>
        <p>We are looking for sponsors to our developer conference Web Rebels. We have over 300 attendees of people interested in web development and the conference goes over two days. There will be workshops as well!.</p>
        <div class="diamond bronze"></div>
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
@import '../css/variables.scss';
.package-list {
  display: flex;
  flex-wrap: wrap;
  align-content: flex-start;
  justify-content: space-between;
  margin: 5rem auto;
}
.package {
  width: 49%;
  min-width: 20rem;
  background: $color-white;
  color: $color-black;
  padding: 3rem 5rem;
  margin: 1rem 0;
  position: relative;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);

  h2, p {
    margin: 0;
  }
  h2 {
    text-align: center;
    margin-bottom: 1rem;
  }
}
.diamond {
  width: 0;
  height: 0;
  border: 50px solid transparent;
  border-bottom: 70px solid $color-yellow;
  position: absolute;
  top: -6rem;
  left: .5rem;

  &:after {
    content: '';
    position: absolute;
    left: -50px;
    top: 70px;
    width: 0;
    height: 0;
    border: 50px solid transparent;
    border-top: 70px solid darken($color-yellow, 24%);
  }

  &.silver {
    border-bottom: 70px solid #ccc;
    &:after {
      border-top: 70px solid darken(#ccc, 24%);
    }
  }

  &.bronze {
    border-bottom: 70px solid $color-orange;
    &:after {
      border-top: 70px solid darken($color-orange, 24%);
    }
  }
}
</style>