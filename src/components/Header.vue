<template>
    <div>
      
        
        
          <div class="topbar">
          <div class="topbar">
          <div class="searchBarContainer">
                <form class="searchBar" action="">
                <input class="input" type="text" placeholder="Search Products" >            
                <button type="submit" class="btn"><i class="fa fa-search"></i></button>
                </form>
          </div>

          <div class="language searchBarContainer" style="width:110px">
                <i class="fa fa-globe" style="padding:3px"></i>
                <select class="input" style="width:80px;border-radius:1px" placeholder="English">
                  <option>English</option>
                  <option>Hindi</option>
                  <option>Spanish</option>
                </select>
          </div>
        </div>
          

          
          <div class="notificationIcons">
              <nav class="navbarRight">
                    <ul>
                        <li><a href=""><i class="fa fa-shopping-cart"></i></a></li>
                        <li ><a href=""><i class="fa fa-envelope"></i></a></li>
                        <li ><a href=""><i class="fa fa-bell"></i></a></li>
                    </ul>
                </nav>

          </div>

          <div class="userIcon">
            <i class="fa fa-user-circle user" style="font-size:30px"></i>
            <p class="user" style="font-size:20px">{{name}}</p> 
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
    
    }
  }
  
}
</script>


<style scoped>




  .topbar{
    display: flex;
    width:100%;
    height: 55px;
    background-color:#f9f9f9 ;
    align-items: center;
    justify-content:flex-start ;
    position: top;
    padding-top: 0
  }

  .searchBarContainer{
    display: flex;
    background-color:white;
    border-radius: 5rem;
    height: 22px;
    width:auto;
    margin-left: 20px;
  
}
.searchBar{
    display: flex;
    flex-direction: row;
    width: auto;
    padding: 5px;
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
.user{
  display: flex;
  margin-right: 15px;
}

</style>