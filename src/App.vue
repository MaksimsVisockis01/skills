<template>
  <h1 class="Roadmap">Roadmap</h1> 
  <a href="https://www.isaacnc.com/" target="_blank" class="isaac">By Isaac N.C. Visit website</a>
  
  <div 
    class="Backlog"
    @drop="onDrop($event, 1)"
    @dragender.prevent
    @dragover.prevent
  >
    <a class="TitleBacklog">Backlog</a>
    
    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket1"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader1">Twilio integration</p>
      <p class="BoxText1">Create new note via SMS. Support text, audio, links, and media.</p>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket2"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader2">Markdown support</p>
      <p class="BoxText2">Markdown shorthand converts to formatting</p>
        <button class="BoxButton1">Formatting</button>
    </div>
  </div>


  <div 
    class="ToDo"
    @drop="onDrop($event, 2)"
    @dragender.prevent
    @dragover.prevent
  >
  <a class="TitleToDo">To do</a>
    
    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket3"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader3">Tablet view</p>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket4"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader4">Audio recording in note</p>
                    <p class="BoxText3">Show audio in a note and playback UI</p>
                        <button class="BoxButton2">Note interface</button>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket5"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader5">Bookmark in note</p>
                    <p class="BoxText4">Show rich link UI in a note, and feature to render website screenshot.</p>
                        <button class="BoxButton3">Note interface</button>
    </div>


    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket6"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader6">Image viewer</p>
    <p class="BoxText5">Opens when clicking on the thumbnail in the list or on the image in the note</p>
    </div>
    
  </div>



  <div 
    class="InProgress"
    @drop="onDrop($event, 2)"
    @dragender.prevent
    @dragover.prevent
  >
  <a class="TitleInProgress">In progress</a>
    
    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket7"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader7">Mobile view</p>
                    <p class="BoxText6">Functions for both web responsive and native apps. Note: Android and iOS will need unique share icons.</p>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket8"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader8">Desktop view</p>
                    <p class="BoxText7">PWA for website and native apps. Note: Windows and Mac will need unique share icons.</p>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket9"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader9">Formatting options</p>
                    <p class="BoxText8">Mobile formatting bar expands and collapses when tapping the format icon.</p>
    </div>


    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket10"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader10">Media in note</p>
                    <p class="BoxText9">Image & video with player UI</p>
                        <button class="BoxButton4">Note interface</button>
    </div>
    
  </div>



  <div 
    class="Designed"
    @drop="onDrop($event, 1)"
    @dragender.prevent
    @dragover.prevent
  >
  <a class="TitleDesigned">Designed</a>
    
    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket11"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader11">Audio recording</p>
                    <p class="BoxText10">Interface for when recording a new audio note</p>
                        <button class="BoxButton5">New note</button>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket12"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader12">Bookmarking</p>
                    <p class="BoxText11">Interface for when creating a new link note.</p>
                        <button class="BoxButton6">New note</button>
    </div>

    <div 
    v-for="item in getList(1)" 
    :key="item.id" 
    class="ticket13"
    draggable="true"
    @dragstart="startDrag($event, item)"
    >     
    <p class="Boxheader13">Mobile home screen</p>
                    <p class="BoxText12">Folders, tags, and notes lists are sorted by recent.</p>
    </div>
  </div>

  

</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const items = ref([
      //1st box
      { id: 0, list: 1 },
      { id: 1, list: 2 },

       //2st box
      { id: 2, list: 3 },
      { id: 3, list: 4 },
      { id: 4, list: 5 },
      { id: 5, list: 6 },

       //3st box
      { id: 6, list: 7 },
      { id: 7, list: 8 },
      { id: 8, list: 9 },
      { id: 9, list: 10 },

       //5st box
      { id: 10, list: 11 },
      { id: 11, list: 12 },
      { id: 12, list: 13 },
      
    ])

    const getList = (list) => {
      return items.value.filter((item) => item.list == list)
    }

    const startDrag = (event, item) => {
      console.log(item)
      event.dataTransfer.dropEffect = 'move'
      event.dataTransfer.effectAllowed = 'move'
      event.dataTransfer.setData('itemID', item.id)
    }

    const onDrop = (event, list) => {
      const itemID = event.dataTransfer.getData('itemID')
      const item = items. value.find((item) => item.id == itemID)
      item.list = list
    } 


    return{
      getList,
      onDrop,
      startDrag,
      
    }
  },
} 
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.drag-el {
  background-color: #3498db;
  color: white;
  padding: 5px;
  margin-bottom: 10px;
}
body{
    background-color: #000000;
    max-width: 1920px;
    max-height: 1080px;
    font-style: normal;
}
.Roadmap{

    position: absolute;
    width: 218px;
    height: 60px;

    top: 89px;
    left: 224px;


    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 700;
    font-size: 50px;
    line-height: 60px;


    color: #FFFFFF;
}

.isaac{

    /* By Isaac N.C. Visit website */

    position: absolute;
    width: 200px;
    height: 24px;

    top: 190px;
    left: 224px;

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */

    text-decoration-line: underline;

    /* gray / 9 white */

    color: #FFFFFF;
}


/* div plates*/


.Backlog{

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px;
    gap: 16px;

    position: absolute;
    width: 368px;
    max-height: 455px;

    left: 200px;
    top: 240px;
    /* gray / 2 */

    background: #262626;
    border-radius: 16px;
}

.ToDo{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px;
    gap: 16px;

    position: absolute;
    width: 368px;
    height: 795px;

    left: 650px;
    top: 240px;

    /* gray / 2 */

    background: #262626;
    border-radius: 16px;
}

.InProgress{
    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px;
    gap: 16px;

    position: absolute;
    width: 368px;
    height: 840px;

    left: 1100px;
    top: 240px;

    /* gray / 2 */

    background: #262626;
    border-radius: 16px;
}

.Designed{
    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px;
    gap: 16px;

    position: absolute;
    width: 368px;
    height: 680px;

    left: 1550px;
    top: 240px;

    /* gray / 2 */

    background: #262626;
    border-radius: 16px;
}

/* Plates title header*/

.TitleBacklog{
    /* Backlog */


    width: 320px;
    height: 44px;

    /* heading / 37 */

    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 700;
    font-size: 37px;
    line-height: 44px;
    /* identical to box height, or 119% */


    /* gray / 9 white */

    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}


.TitleToDo{
    /* To do */


    width: 320px;
    height: 44px;

    /* heading / 37 */

    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 700;
    font-size: 37px;
    line-height: 44px;
    /* identical to box height, or 119% */


    /* gray / 9 white */

    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.TitleInProgress{
    /* In progress */


    width: 320px;
    height: 44px;

    /* heading / 37 */

    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 700;
    font-size: 37px;
    line-height: 44px;
    /* identical to box height, or 119% */


    /* gray / 9 white */

    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}

.TitleDesigned{
    /* Designed */


    width: 320px;
    height: 44px;

    /* heading / 37 */

    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 700;
    font-size: 37px;
    line-height: 44px;
    /* identical to box height, or 119% */


    /* gray / 9 white */

    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}


/* Tickets BackLog*/

.ticket1{
    /* 
    ticket menu overlay modal popup popover alert
    */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 110px;

    /* core/pink */

    background: #C440A1;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 1;
    flex-grow: 0;
}

.ticket2{
    /* ticket menu overlay modal popup popover alert */
    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 160px;

    /* core/periwinkle */

    background: #6A6DCD;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 2;
    flex-grow: 0;
}

/* Tickets To do */


.ticket3{
    /* ticket menu overlay modal popup popover alert*/

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 72px;

    /* core/red */

    background: #D93535;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 1;
    flex-grow: 0;
}
.ticket4{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 140px;

    /* core/periwinkle */

    background: #6A6DCD;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 2;
    flex-grow: 0;
}
.ticket5{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 160px;

    /* core/periwinkle */

    background: #6A6DCD;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 3;
    flex-grow: 0;
}
.ticket6{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 120px;

    /* core/periwinkle */

    background: #6A6DCD;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 4;
    flex-grow: 0;
}

/* Tickets In progress */

.ticket7{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 140px;

    /* core/red */

    background: #D93535;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 1;
    flex-grow: 0;
}
.ticket8{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 140px;

    /* core/red */

    background: #D93535;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 2;
    flex-grow: 0;
}
.ticket9{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 120px;

    /* core/blue */

    background: #307FE2;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 3;
    flex-grow: 0;
}
.ticket10{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 140px;

    /* core/periwinkle */

    background: #6A6DCD;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 4;
    flex-grow: 0;
}


/* Tickets Designed */

.ticket11{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 160px;

    /* core/mint */

    background: #00A88B;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 1;
    flex-grow: 0;
}
.ticket12{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 160px;

    /* core/mint */

    background: #00A88B;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 2;
    flex-grow: 0;
}
.ticket13{
    /* ticket menu overlay modal popup popover alert */

    /* Auto layout */

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px;
    gap: 8px;

    width: 320px;
    height: 120px;

    /* core/blue */

    background: #307FE2;
    /* shadow/level 3 */

    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.12), 0px 16px 32px rgba(0, 0, 0, 0.08);
    border-radius: 8px;

    /* Inside auto layout */

    flex: none;
    order: 3;
    flex-grow: 0;
}



/* Box headers: */
/* ---------------------------------------------- */
/* Backlog: */
.Boxheader1{
    /* title */

    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}

.Boxheader2{
    /* title */

    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}

/* ---------------------------------------------- */
/* To do: */
.Boxheader3{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader4{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader5{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader6{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
/* ---------------------------------------------- */
/* In progress: */
.Boxheader7{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader8{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader9{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader10{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
/* ---------------------------------------------- */
/* Designed: */
.Boxheader11{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader12{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
.Boxheader13{
    /* title */


    width: 272px;
    height: 24px;

    /* body / bold */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 150%;
    /* identical to box height, or 24px */


    color: #FFFFFF;


    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
}
/* ---------------------------------------------- */


/* ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ */




/* Boxes text: */

/* Backlog: */

.BoxText1{
    /* description */
    

    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
    
}
.BoxText2{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}

/* ---------------------------------------------- */

/* To do: */
.BoxText3{
    /* description */


    width: 272px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText4{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText5{
   /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
/* ---------------------------------------------- */

/* In progress: */
.BoxText6{
    /* description */


    width: 272px;
    height: 60px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText7{
    /* description */


    width: 272px;
    height: 60px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText8{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText9{
    /* description */


    width: 272px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}

/* ---------------------------------------------- */

/* Designed: */
.BoxText10{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText11{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}
.BoxText12{
    /* description */


    width: 272px;
    height: 40px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);


    /* Inside auto layout */

    flex: none;
    order: 1;
    align-self: stretch;
    flex-grow: 0;
}


/* ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ */



/* Box button: */
/* Backlog: */
.BoxButton1{
    /* badge */
    position: absolute;

    background-color: transparent;
    text-align: center;
    

    width: 80px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75); 
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    cursor: pointer;

    margin-top: 130px;
}

/* ---------------------------------------------- */

/* To do: */
.BoxButton2{
    /* badge */
    background-color: transparent;
    text-align: center;
    position: absolute;

    width: 95px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin-top: 130px;
}
.BoxButton3{
    /* badge */
    background-color: transparent;
    text-align: center;
    position: absolute;

    width: 95px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin-top: 130px;
}
/* ---------------------------------------------- */

/* In progress: */
.BoxButton4{
    /* badge */
    background-color: transparent;
    text-align: center;
    position: absolute;

    width: 95px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin-top: 130px;
}
/* ---------------------------------------------- */

/* Designed: */
.BoxButton5{
    /* badge */
    position: absolute;
    background-color: transparent;
    text-align: center;

    width: 95px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin-top: 130px;
}
.BoxButton6{
    /* badge */
    position: absolute;
    background-color: transparent;
    text-align: center;

    width: 95px;
    height: 20px;

    /* caption / regular */

    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    /* identical to box height, or 20px */


    /* overlay/white */

    color: rgba(255, 255, 255, 0.75);
    border: 1px solid white;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin-top: 130px;
}
/* ---------------------------------------------- */


/* ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ */


</style>
