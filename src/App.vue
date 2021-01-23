<template>
  <ion-app>
    <ion-router-outlet />

    <ion-div>

      
      <ion-item>
        <ion-label for='nom'>Name : </ion-label>
        <ion-input type='text' name='name' v-model='name' ></ion-input>
      </ion-item>

      <ion-item>
        <ion-list>
          <ion-radio-group name="state" value="Non">
            <ion-list-header>
              <ion-label>State  </ion-label>
            </ion-list-header>
            <ion-item>
              <ion-label>Non</ion-label>
              <ion-radio value="non"></ion-radio>
            </ion-item>
            <ion-item>
              <ion-label>Oui</ion-label>
              <ion-radio value="oui"></ion-radio>
            </ion-item>
          </ion-radio-group>
        </ion-list>
      </ion-item>

      <ion-item>
        <ion-button >Add Task  + </ion-button>
      </ion-item>

    </ion-div>

  <i-div>
    
  <ion-list >
    <h2> {{ todos.name }} </h2>
    
  </ion-list>

  </i-div>


  </ion-app>
</template>

<script lang="ts">
import { IonApp, IonRouterOutlet } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  data() {
    return{
      todos: [
                {
                  id: 1,
                  name : 'tache 1',
                  completed : false
                },
                {
                  id: 2,
                  name : 'tache 2',
                  completed: true
                }
              ]
                ,
                newTodo: '',
                filter: 'all',

                }  },
      components: {
        IonApp,
        IonRouterOutlet
        },
      methods : {

        },
      props : {

      },
      computed : {

      }

});
</script>