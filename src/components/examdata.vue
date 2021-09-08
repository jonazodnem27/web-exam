<template>
 <section class="section-1 bg">
      <div class="container">
        <div class="inner-section-1">
          <h1 class="header1">Hello Developer!</h1>
          <p class="paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
        </div>
      </div>
    </section>
    <section class="section-2">
      <div class="container">
        <div class="row">
          <div class="col-md-4 col-xs-12" v-for="Content in Contents.slice(0, 3)" :key="Content.title">
            <div class="card">
              <img src="https://via.placeholder.com/400x300.png" class="image-round">
              <div class="inside-loop" v-html="Content.content"></div>
              <a href="" class="button button-outline">READ MORE</a>
            </div>
          </div>
          <!-- <div class="col-md-4 col-xs-12">
            <div class="card">
              <img src="https://via.placeholder.com/400x300.png" class="image-round">
              <p class="paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
              <a href="" class="btn btn-outline">READ MORE</a>
            </div>
          </div>
          <div class="col-md-4 col-xs-12">
            <div class="card">
              <img src="https://via.placeholder.com/400x300.png" class="image-round">
              <p class="paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
              <a href="" class="btn btn-outline">READ MORE</a>
            </div>
          </div> -->
        </div>
      </div>
    </section>
</template>

<script>
import DataContent from './data.json';
export default{
    data(){
        return{
            Contents: DataContent
        }
    }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.bg{
  background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.header1{
  font-weight: 800;
  color: white;
  text-align: center;
    margin: 0;
    letter-spacing: 1.1px;
    font-size: 34px;
}

*{
  font-family: 'Roboto', sans-serif;
}

.section-1{
  padding: 115px 0 110px;
  position: relative;
  background-image: url(https://via.placeholder.com/1920x650/8f8f8f/696969.png);
}

.paragraph{
    color: white;
  text-align: center;
}

.section-1 .paragraph{
  margin: 0;
    font-size: 20px;
}

.image-round{
  border-radius: 5px;
}

.section-2 .card{
  border-color: #eeeeee;
  box-shadow: 0 1px 3px rgb(164 164 164 / 12%), 0 1px 2px rgb(163 163 163 / 22%);
  border-radius: 7px;
  overflow: hidden;
  height: 500px;
  padding: 15px;
  margin-bottom: 35px;
}

.section-2{
  padding: 35px 0 0;
}

.section-2 .inside-loop p, .section-2 .inside-loop li{
    font-size: 13px;
    color: black;
    margin: 10px 0 5px;
}

.section-2 .inside-loop li{
    margin: 5px 0;
}

.button{
    background: black;
    color: white;
    font-weight: 800;
    border-radius: 100px;
    display: inline-block;
    margin: auto;
    font-size: 14px;
    letter-spacing: 1.2px;
    transition: .4s;
    margin-top: 10px;
    display: inline-block;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: center;
    text-decoration: none;
    vertical-align: middle;
    cursor: pointer;
    -webkit-user-select: none;
    -moz-user-select: none;
    user-select: none;
    background-color: transparent;
    border: 1px solid transparent;
    padding: .375rem .75rem;
}

.button-outline{
  background: transparent;
  color: black;
  font-weight: 900;
  border: 2px solid #323232;
}

.section-2 .button{
    margin-bottom: unset;
    margin-top: auto;
}

.button-outline:hover{
  background: black;
  color: white;
}

@media screen and (max-width:  767px){
  .header1 {
      line-height: 48px;
      font-size: 36px;
  }

  .section-2 .card{
    height: unset;
  }

  .section-1{
    background-image: url(https://via.placeholder.com/600x800/8f8f8f/696969.png);
  }
}
</style>
