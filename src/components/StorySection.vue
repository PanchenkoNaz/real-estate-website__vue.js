<template>
  <section class="section story">
    <div class="container">
      <div class="title-wrapper">
        <div>
          <p class="section-subtitle title-medium">Our Customers</p>
          <h2 class="section-title headline-medium">We Help 1000+ Family Find Their True Home</h2>
          <ul class="avatar-list">
            <li class="avatar" v-for="(avatar, index) in avatars" :key="index">
              <img :src="avatar.image" :alt="avatar.alt" width="120" height="80" loading="lazy" class="img-cover" />
              <div v-if="avatar.overlay" class="overlay-content">
                <span class="label-medium">{{ avatar.overlay }}</span>
              </div>
            </li>
          </ul>
        </div>
        <a href="#" class="btn btn-outline">
          <span class="label-medium">View All Stories</span>
          <span class="material-symbols-rounded" aria-hidden="true">arrow_outward</span>
        </a>
      </div>

      <ul class="story-list">
        <li class="story-card" v-for="(story, index) in stories" :key="index" :style="{ backgroundImage: 'url(' + story.background + ')' }">
          <a href="#" class="overlay-content">
            <div>
              <h3 class="title-small">{{ story.name }}</h3>
              <div class="rating-wrapper">
                <span class="material-symbols-rounded" aria-hidden="true" v-for="star in 5" :key="star">star</span>
                <data class="title-small rating-text" :value="story.rating">{{ story.rating }}</data>
              </div>
            </div>
            <figure class="card-avatar">
              <img :src="story.avatar" :alt="story.name" width="56" height="56" loading="lazy" class="img-cover" />
            </figure>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'StorySection',
  data() {
    return {
      avatars: [
        { image: "@/assets/images/avatar-1.jpg", alt: "John smith" },
        { image: "@/assets/images/avatar-2.jpg", alt: "Jane smith" },
        { image: "@/assets/images/avatar-3.jpg", alt: "John smith" },
        { image: "@/assets/images/avatar-4.jpg", alt: "Jane smith", overlay: "99+" }
      ],
      stories: [
        {
          name: "Chris Traeger",
          rating: "5.0",
          background: "@/assets/images/story-1.jpg",
          avatar: "@/assets/images/story-avatar-1.jpg"
        },
        {
          name: "Duke Silver",
          rating: "5.0",
          background: "@/assets/images/story-2.jpg",
          avatar: "@/assets/images/story-avatar-2.jpg"
        },
        {
          name: "Tsukasa Aoi",
          rating: "5.0",
          background: "@/assets/images/story-3.jpg",
          avatar: "@/assets/images/story-avatar-3.jpg"
        },
        {
          name: "Freida Varnes",
          rating: "5.0",
          background: "@/assets/images/story-4.jpg",
          avatar: "@/assets/images/story-avatar-4.jpg"
        },
        {
          name: "Carl Lorthner",
          rating: "5.0",
          background: "@/assets/images/story-5.jpg",
          avatar: "@/assets/images/story-avatar-5.jpg"
        },
        {
          name: "Marci Senter",
          rating: "5.0",
          background: "@/assets/images/story-6.jpg",
          avatar: "@/assets/images/story-avatar-6.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
/* Додайте стилі для StorySection тут або залиште їх у загальному файлі стилів */
</style>
