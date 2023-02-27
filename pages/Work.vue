<template>
  <v-container>
    <v-card color="#f9fef6" elevation="0" style="margin-top: 150px">
      <v-row>
        <v-col cols="8">
          <v-card-title>
            <h1 class="page-title">Madrid, Spain, December 2022</h1>
          </v-card-title>
          <v-card-text>
            <p class="page-description">
              Photo by 
              <a href="https://unsplash.com/@wei0411?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Wei Hunag</a> 
              on <a href="https://unsplash.com/photos/qClP7kYfi08?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
            </p>
            <v-btn 
              href="https://unsplash.com/@wei0411?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText"
              color="primary"
              rounded
            ><b>Click to View</b></v-btn>
          </v-card-text>
        </v-col>
        <v-col cols="4">
          <v-avatar width="100%" height="90%">
            <img src="https://images.unsplash.com/photo-1675652426417-a7305afe7dbe?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80" />
          </v-avatar>
        </v-col>
      </v-row>
    </v-card>
    <v-card color="#f9fef6" elevation="0" style="margin-top: 100px">
      <v-card-title>
        <h1>Browse Images by Category</h1>
      </v-card-title>
      <v-card-text>
        <v-card-text>
          <v-row>
            <v-col v-for="item in items" :key="item.name" cols="12" md="6">
              <v-card color="#fbfcfa" height="220px">
                <v-card-title><h2>{{ item.name }}</h2></v-card-title>
                <v-card-subtitle>{{ item.type }}</v-card-subtitle>
                <v-card-text>
                  <p>{{ item.description }}</p>
                  <v-btn color="primary" :href="item.url" rounded><b>View More</b></v-btn>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-card-text>
      </v-card-text>
    </v-card>
    <v-card class="card-image-background">
      <v-card-title>
        <h1>For Clients</h1>
      </v-card-title>
      <v-card-subtitle style="max-width: 500px"><h2 class="subtitle">Find talent your way</h2></v-card-subtitle>
      <v-card-text style="max-width: 500px; font-size: 20px;font-weight: bold;margin-top: 75px;color: white;">Work with the largest network of independent professionals and get things done—from quick turnarounds to big transformations.</v-card-text>
      <v-card-text>
        <v-row>
          <v-col>
            <v-card color="#f9fef6">
              <v-card-title style="font-size: 40px;">Post a job and hire a pro</v-card-title>
              <v-card-text>
                <v-btn color="primary" rounded><b>View More</b></v-btn>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card color="#f9fef6">
              <v-card-title style="font-size: 40px;">Post a job and hire a pro</v-card-title>
              <v-card-text>
                <v-btn color="primary" rounded><b>View More</b></v-btn>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card color="#f9fef6">
              <v-card-title style="font-size: 40px;">Post a job and hire a pro</v-card-title>
              <v-card-text>
                <v-btn color="primary" rounded><b>View More</b></v-btn>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: 'Heather Wilde', description: 'Great outdoors photographer. Happiest getting lost in the wilderness with just a camera for company.', url: 'https://unsplash.com/@heather_wilde', type: 'Nature' },
        { name: 'Ricky', description: 'Download free, beautiful high-quality photos curated by Ricky.', url: 'https://unsplash.com/@tohriki', type: 'Street Photography' },
        { name: 'Harsh Raghavani', description: 'Photographer, Editor', url: 'https://unsplash.com/@justaclick_24', type: 'Experimental' },
        { name: 'Mitchell Orr', description: 'If you feel you would like to support my work, any donations no matter how small, would be extremely helpful.', url: 'https://unsplash.com/@mitchorr', type: 'Animals' },
        { name: 'Lance Reis', description: 'I\'m a published Portland based photographer who specializes in personal branding photography, business photography, & Product photography. Join me at Lancereis.com or Instagram and let me know you found me here :)', url: 'https://unsplash.com/@lancereis', type: 'Fashion & Beauty' },
        { name: 'Rodion Kutsaiev', description: 'Photographer and 3D designer', url: 'https://unsplash.com/@frostroomhead', type: 'Food & Drink' },
      ]
    }
  },
}
</script>

<style scoped>
.page-title {
  font-size: 75px;
  line-height: 1.2;
  max-width: 525px !important;
  color: rgb(0, 138, 88);
  /* white-space: break-spaces; */
}

.page-description {
  font-size: 30px;
  margin-top: 20px;
  margin-bottom: 40px !important;
}
.card-image-background {
  background-image: url('https://images.unsplash.com/photo-1598257006458-087169a1f08d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80');
  background-size: cover;
  font-family: 'Times New Roman', Times, serif;
}
.subtitle {
  margin-top: 50px;
  font-size: 90px;
  color: black;
  line-height: 1.2;
}
</style>