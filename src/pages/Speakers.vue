<template>
  <q-page class="q-ma-none">

    <div class="row q-ma-xl">

      <div
        v-for="speaker in speakers"
        v-bind:key="speaker.id"
        class="col-6 q-pa-lg"
      >

        <q-card>
          <q-card-section horizontal>
            <q-img
              class="col-5"
              :src="speaker.photo"
            />

            <q-card-section>
              <div class="text-h5 q-mt-sm q-mb-xs">{{ speaker.name }}</div>
              <div class="text-caption text-grey">
                {{ speaker.bio }}
              </div>

              <div
                v-for="talk in speaker.talks"
                v-bind:key="talk.title"
                class="q-my-md"
              >
                <q-chip icon="event">{{ talk.date }}</q-chip>
                <span class="text-h6 q-mx-md">{{ talk.title }}</span>
              </div>

            </q-card-section>

          </q-card-section>

        </q-card>
      </div>

    </div>
  </q-page>
</template>

<style lang="scss">
  body {
    background-color: $grey-4;
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }
</style>

<script>

export default {
  name: 'Home',
  data () {
    return {
      speakers: [
        {
          id: 'JakobHatzl',
          name: 'Jakob Hatzl',
          bio: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam faucibus dictum metus, a ultricies nibh rhoncus sed. Morbi eget pulvinar tortor, fringilla mollis nisi. Etiam ornare elit lacus, id tincidunt enim pretium nec. Cras gravida augue non nunc malesuada, sit amet accumsan erat condimentum. Pellentesque blandit elit a mauris dapibus, et laoreet ex scelerisque. Nulla hendrerit sem ut interdum tempor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.',
          photo: 'https://www.kmlvision.com/wp-content/uploads/2018/11/foto-hatzl-bw-450x450.jpg',
          talks: [
            {
              date: 'Oct 1, 12:00',
              title: 'Bringing IKOSAⓇ Automated Image Analysis to the Cloud with Axon-powered Microservices'

            }
          ]
        },
        {
          id: 'AdamDymitruk',
          name: 'Adam Dymitruk',
          photo: 'https://media-exp1.licdn.com/dms/image/C5603AQHJwpA7NbH7kA/profile-displayphoto-shrink_200_200/0?e=1602115200&v=beta&t=nGTh68tYFCNwX6Grew8T5j0miDpyBaxcuuAQ1WZGIvg'
        }
      ]
    }
  }
}
</script>
