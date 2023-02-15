<template>

  <router-view />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600;800&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #fff;
  font-family: 'Montserrat', sans-serif;

}

.container {
  padding: 0 30px;
}

.accordeon {
  background: #FFFFFF;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.02), 0px 4px 17px rgba(0, 0, 0, 0.14), 0px 4px 22px rgba(0, 0, 0, 0.12);
  border-radius: 8px;
  max-width: 600px;
  margin: 0 auto;
  margin-top: 100px;
  overflow: hidden;
}

.arrow {
  transition: all .2s linear;
}

.question {
  position: relative;
  color: #3c3c3c;
  font-size: 16px;
  transition: all 0.2s linear;
  font-weight: 800;
  display: flex;
  justify-content: space-between;
}

.answer {
  color: #3c3c3c;
  font-size: 14px;
  opacity: 0;
  font-weight: 600;
  max-height: 0px;
  overflow-y: hidden;
}

.faq {
  padding: 24px;
  border-top: 1px solid #D0DBF1;

  &.open {
    background: #FAF8F6;

    .question {
      color: #2B41B7;
      margin-bottom: 8px;
    }

    .arrow {
      transform: rotate(180deg);
    }

    .answer {
      opacity: 1;
      max-height: 1000px;
    }
  }

  @media (max-width:400px) {
    padding: 10px;
  }
}
</style>
