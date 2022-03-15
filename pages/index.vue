<template>
  <div class="main_layout">
    <div class="side_layout">

      <div class="side_container">
        <!-- SIDE HEADER -->
        <div class="side_header">
          <div class="side_picture"></div>
          <div class="side_profile">
            <div class="profile_name">{{ name }}</div>
            <div class="profile_title">{{ title }}</div>
          </div>
        </div>
        <!-- SIDE CONTENTS -->
        <div class="side_content">
          <!-- CONTACTS -->
          <div class="side_panel">
            <div class="display_B text_title"> Contacts: </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'envelope']"/> &ensp; {{ email }} </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'phone-square']"/> &ensp; {{ mobile }} </div>
            <div class="display_B text_sub"> <fa :icon="['fa', 'globe-asia']"/> &ensp; {{ address }} </div>
          </div>
          <!-- SKILLS -->
          <div class="side_panel">
            <div class="display_B text_title"> Skills: </div>
            <div class="skill_set" v-for="(skills, s) in skills" :key="'s'+s">
              <div class="display_B text_title2">{{ skills.skill }}</div>
              <div class="display_B prog_bar">
                <div class="prog" :style="'width:'+skills.lvl+'%;'"></div>
              </div>
            </div>
          </div>
           <!-- KNOWLEDGE -->
          <div class="side_panel scroller">
            <div class="display_B text_title"> Knowledgable in: </div>
            <div class="display_B text_sub" v-for="(know, k) in knowledge" :key="'k'+k"> <fa :icon="['fa', 'check-circle']"/> &ensp; {{ know.skill }} </div>
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
    name: "Kenn Brian Nillama",
    title: "UX Designer/Artist",
    computedHeight: "",
    email: "sample@email.com",
    mobile: "+63 (900) 000 0000",
    address: "Sample City 0000, Country",
    skills: [
      { skill: "Adobe Photoshop", lvl: 85 },
      { skill: "Adobe Illustrator", lvl: 85 },
      { skill: "Vue JS", lvl: 75 },
      { skill: "Bootstrap", lvl: 70 },
    ],
    knowledge: [
      { skill: "Graphic Designing", lvl: 70 },
      { skill: "Web Designing", lvl: 70 },
      { skill: "UX Designing", lvl: 80 },
      { skill: "Traditional Illustrating", lvl: 10 },
      { skill: "Digital Illustrating", lvl: 10 }
    ],
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
