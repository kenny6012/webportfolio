<template>
  <div class="main_layout">
    <div class="side_layout">

      <div class="side_container">
        <!-- SIDE HEADER -->
        <div class="side_header">
          <div class="side_picture"></div>
          <div class="side_profile">
            <div class="profile_name">Fname M. Surname</div>
            <div class="profile_title">Main Profile Title</div>
          </div>
        </div>
        <!-- SIDE CONTENTS -->
        <div class="side_content">
          <!-- CONTACTS -->
          <div class="side_panel">
            <div class="display_B text_title"> Contacts: </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'envelope']"/> &ensp; sample@email.com </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'phone-square']"/> &ensp; +63 900 000 0000 </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'globe-asia']"/> &ensp; Sample City 0000, Country </div>
          </div>
          <!-- SKILLS -->
          <div class="side_panel scroller">
            <div class="display_B text_title"> Specializations: </div>
            <div class="skill_set" v-for="(skills, s) in skills" :key="'s'+s">
              <div class="display_B text_title2">{{ skills.skill }}</div>
              <div class="display_B prog_bar">
                <div class="prog" :style="'width:'+skills.lvl+'%;'"></div>
              </div>
            </div>
          </div>
        </div>

      </div>

    </div>
    <div :style="'height:'+computedHeight+'px;'" class="content_layout" >
      Contents Here
    </div>
  </div>
</template>

<script>
export default {
name: 'IndexPage',
data() {
  return {
    computedHeight: "",
    skills: [
      { skill: "Adobe Photoshop", lvl: 80 },
      { skill: "Adobe Illustrator", lvl: 60 },
      { skill: "Vue JS", lvl: 80 },
      { skill: "React JS", lvl: 10 },
      { skill: "HTML", lvl: 95 },
      { skill: "CSS", lvl: 95 },
      { skill: "Javascript", lvl: 70 },
    ]
  }
},
components: {

},
created() {
  var sh = screen.height;
  this.computedHeight = parseInt(sh) - 111; //111 is the chrome tabs + address bar heights
},
computed: {
  
}
}
</script>
