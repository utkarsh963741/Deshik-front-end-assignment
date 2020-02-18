<template>
  <div class="container">
    
  <v-card class="mx-auto" max-width="450">
    <v-card dark flat >
      
      <v-toolbar color="white" dark  style="height:60px">
      
      <v-toolbar-title style="color:black">Recent Activities</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon color="black">mdi-dots-horizontal</v-icon>
      </v-btn>
    </v-toolbar>
     
    </v-card>
    <v-card-text class="py-0">
      <v-timeline
        align-top
        dense
      >
        <v-timeline-item class="item"
          color="pink"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>5pm</strong>
            </v-col>
            <v-col class="item">
              <strong>New Icon</strong>
              <div class="caption">Mobile App</div>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="teal lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>3-4pm</strong>
            </v-col>
            <v-col class="item">
              <strong>Design Stand Up</strong>
              <div class="caption mb-2">Hangouts</div>
              <v-avatar>
                <v-img
                  src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairFrida&accessoriesType=Kurt&hairColor=Red&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Gray01&graphicType=Skull&eyeType=Wink&eyebrowType=RaisedExcitedNatural&mouthType=Disbelief&skinColor=Brown"
                ></v-img>
              </v-avatar>
              <v-avatar>

                <v-img
                  src="https://avataaars.io/?avatarStyle=Circle&topType=ShortHairFrizzle&accessoriesType=Prescription02&hairColor=Black&facialHairType=MoustacheMagnum&facialHairColor=BrownDark&clotheType=BlazerSweater&clotheColor=Black&eyeType=Default&eyebrowType=FlatNatural&mouthType=Default&skinColor=Tanned"
                ></v-img>
              </v-avatar>
              <v-avatar>
                <v-img
                  src="https://avataaars.io/?avatarStyle=Circle&topType=LongHairMiaWallace&accessoriesType=Sunglasses&hairColor=BlondeGolden&facialHairType=Blank&clotheType=BlazerSweater&eyeType=Surprised&eyebrowType=RaisedExcited&mouthType=Smile&skinColor=Pale"
                ></v-img>
              </v-avatar>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="pink"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>12pm</strong>
            </v-col>
            <v-col class="item">
              <strong>Lunch break</strong>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="teal lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>9-11am</strong>
            </v-col>
            <v-col class="item">
              <strong>Finish Home Screen</strong>
              <div class="caption">Web App</div>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="green lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>11am</strong>
            </v-col>
            <v-col class="item">
              <strong>Work on IOT project</strong>
              
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="yellow lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>2pm</strong>
            </v-col>
            <v-col class="item">
              <strong>Work on Deshik Assignment</strong>
              
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="purple lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>5pm</strong>
            </v-col>
            <v-col class="item">
              <strong>Study for Exams</strong>
              
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item class="item"
          color="black lighten-3"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3" class="item">
              <strong>11pm</strong>
            </v-col>
            <v-col class="item">
              <strong>sleep</strong>
              
            </v-col>
          </v-row>
        </v-timeline-item>


      </v-timeline>
    </v-card-text>
  </v-card>

  </div>
</template>

<script>
export default {
  name:'RecentActivities'
}
</script>

<style scoped>
.container{
    background-color: #e3e3e3;
    height: 200px;
    overflow-x: hidden;
    width: max-content;
    
  }



.item{
  padding:1px
}
</style>