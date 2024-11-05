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
import Avatar1 from '../assets/images/avatar-1.jpg';
import Avatar2 from '../assets/images/avatar-2.jpg';
import Avatar3 from '../assets/images/avatar-3.jpg';
import Avatar4 from '../assets/images/avatar-4.jpg';

import Story1 from '../assets/images/story-1.jpg';
import Story2 from '../assets/images/story-2.jpg';
import Story3 from '../assets/images/story-3.jpg';
import Story4 from '../assets/images/story-4.jpg';
import Story5 from '../assets/images/story-5.jpg';
import Story6 from '../assets/images/story-6.jpg';

import StoryAvatar1 from '../assets/images/story-avatar-1.jpg';
import StoryAvatar2 from '../assets/images/story-avatar-2.jpg';
import StoryAvatar3 from '../assets/images/story-avatar-3.jpg';
import StoryAvatar4 from '../assets/images/story-avatar-4.jpg';
import StoryAvatar5 from '../assets/images/story-avatar-5.jpg';
import StoryAvatar6 from '../assets/images/story-avatar-6.jpg';

export default {
  name: 'StorySection',
  data() {
    return {
      avatars: [
        { image: Avatar1, alt: "John smith" },
        { image: Avatar2, alt: "Jane smith" },
        { image: Avatar3, alt: "John smith" },
        { image: Avatar4, alt: "Jane smith", overlay: "99+" }
      ],
      stories: [
        {
          name: "Chris Traeger",
          rating: "5.0",
          background: Story1,
          avatar: StoryAvatar1
        },
        {
          name: "Duke Silver",
          rating: "5.0",
          background: Story2,
          avatar: StoryAvatar2
        },
        {
          name: "Tsukasa Aoi",
          rating: "5.0",
          background: Story3,
          avatar: StoryAvatar3
        },
        {
          name: "Freida Varnes",
          rating: "5.0",
          background: Story4,
          avatar: StoryAvatar4
        },
        {
          name: "Carl Lorthner",
          rating: "5.0",
          background: Story5,
          avatar: StoryAvatar5
        },
        {
          name: "Marci Senter",
          rating: "5.0",
          background: Story6,
          avatar: StoryAvatar6
        }
      ]
    };
  }
};
</script>


<style scoped>
/* Додайте стилі для StorySection тут або залиште їх у загальному файлі стилів */
</style>
