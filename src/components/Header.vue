<template>
    <div>
      <div class="topbar">
        <div class="topbar">
          <div class="field is-grouped">
          <div class="control has-icons-left is-expanded">
            <input class="input is-small is-rounded" type="text" placeholder="SearchProducts">
            <p class="icon is-small is-left">
                <i class="fa fa-search " ></i>
              </p>           
          </div>
          <div class="control ">
                <a class="button is-info is-small is-rounded">Search</a>
          </div>  
          </div>
        </div>  

          <div class="field" style="margin-top:9px">
            <div class="control has-icons-left">
              <div class="select is-small is-rounded">
                <select>
                  <option selected>English</option>
                  <option>Hindi</option>
                  <option>Spanish</option>
                </select>
              </div>
              
            </div>
          </div>

          
          <div class="notificationIcons">
              <nav class="navbarRight">
                    <ul>
                      
                        <li><a href="">
                          <v-badge
                          :content="shop"
                          :value="shop"
                             color="blue"
                              overlap
                              >
                            <v-icon medium>mdi-basket</v-icon>
                          </v-badge>
                        </a></li>
                        <li><a href="">
                          <v-badge
                          :content="messages"
                          :value="messages"
                             color="green"
                              overlap
                              >
                            <v-icon medium>mdi-email</v-icon>
                          </v-badge>
                        </a></li>
                        <li><a href="">
                          <v-badge
                          :content="notific"
                          :value="notific"
                             color="red"
                              overlap
                              >
                            <v-icon medium>mdi-bell</v-icon>
                          </v-badge>
                          
                          
                        </a></li>
                    </ul>
                </nav>

          </div>

          <div class="userIcon">
            <v-avatar>
                <v-img
                  src="https://avataaars.io/?avatarStyle=Circle&topType=ShortHairFrizzle&accessoriesType=Kurt&hairColor=Red&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Gray01&eyeType=Surprised&eyebrowType=RaisedExcitedNatural&mouthType=Smile&skinColor=Brown"
                ></v-img>
              </v-avatar>
            <div style="height:20;margin:5px;padding-top:5px">
            <p  style="font-size:20px;margin-left:5px;margin-right:5px;margin-bottom:0px">{{name}}</p>    
            </div>
            
            
           
            <a href="" style="list-style:none"><i class="fa fa-chevron-down user" style="font-size:10px"></i></a>
          </div>
          </div>
    </div>
</template>

<script>
export default {
  name:'Header',
  data() {
    return{
    name:'Utkarsh',
        messages: 5,
        shop:10,
        notific:16,
        show: false,
      
    }
  }
  
}
</script>


<style scoped>




  .topbar{
    display: flex;
    width:100%;
    height: 50px;
    background-color:#f9f9f9 ;
    align-items: center;
    justify-content:space-around;
    position: top;
    padding-top: 0;
    
  }

  .searchBarContainer{
    display: flex;
    background-color:white;
    border-radius: 5rem;
    width:370px;
    margin-left: 20px;
  
  
}
.searchBar{
    display: flex;
    flex-direction: row;
    width: auto;
    padding: 5px;
    margin-left: 10px;
    
}

.input{
    border-style: hidden;
    width: 300px;
    
}

.btn{
    width: 30px;
    border-style: hidden;
    background-color: white;
    color: black;
}

.navbarRight{
    display: flex;
    height: 35px;
    align-items: center;
    padding-right: 0.2%;
    
}

.navbarRight ul{
    display: flex;
    list-style: none;
   
}

.navbarRight ul li{
   margin:17px;
    transition: transform 0.5s;
}
.navbarRight ul li:hover{
    transform: scale(1.2);
}

.notificationIcons{
  
  padding-right: 10px;
  margin-right: 30px;
  
}
.userIcon{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-right: 50px;
  
}


</style>