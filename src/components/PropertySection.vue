<template>
  <section class="section property" aria-labelledby="property-label">
    <div class="container">
      <div class="title-wrapper">
        <div>
          <h2 class="section-title headline-small">Best home in your city</h2>
          <p class="section-text body-large">
            Lorem ipsum dolor sit amet consectetur. In quisque scelerisque eget id facilisis. Aliquam in libero egestas at.
          </p>
        </div>
        <a href="#" class="btn btn-outline">
          <span class="label-medium">Explore more</span>
          <span class="material-symbols-rounded" aria-hidden="true">arrow_outward</span>
        </a>
      </div>

      <div class="property-list">
        <div class="card" v-for="(property, index) in properties" :key="index">
          <div class="card-banner">
            <figure class="img-holder" :style="{ '--width': '585', '--height': '390' }">
              <img :src="property.image" :alt="property.title" class="img-cover" />
            </figure>
            <span class="badge label-medium" v-if="property.isNew">New</span>
            <button class="icon-btn fav-btn" aria-label="add to favorite" data-toggle-btn>
              <span class="material-symbols-rounded" aria-hidden="true">favorite</span>
            </button>
          </div>

          <div class="card-content">
            <span class="title-large">{{ property.price }}</span>
            <h3>
              <a href="#" class="title-small card-title">{{ property.title }}</a>
            </h3>
            <address class="body-medium card-text">{{ property.address }}</address>
            <div class="card-meta-list">
              <div class="meta-item" v-for="(meta, i) in property.meta" :key="i">
                <span class="material-symbols-rounded meta-icon" aria-hidden="true">{{ meta.icon }}</span>
                <span class="meta-text label-medium">{{ meta.text }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PropertySection',
  data() {
    return {
      properties: [
        {
          image: "/src/assets/images/property-1.jpg",
          title: "COVA Home Realty",
          price: "$710.68",
          address: "1901 Thornridge Cir. Shiloh, Hawaii 81063",
          isNew: true,
          meta: [
            { icon: "bed", text: "3 Bed" },
            { icon: "bathtub", text: "2 Bath" },
            { icon: "straighten", text: "1430 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-2.jpg",
          title: "Exit Realty",
          price: "$630.44",
          address: "2972 Westheimer Rd. Santa Ana, Illinois 85486",
          isNew: false,
          meta: [
            { icon: "bed", text: "5 Bed" },
            { icon: "bathtub", text: "4 Bath" },
            { icon: "straighten", text: "1630 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-3.jpg",
          title: "The Real Estate Group",
          price: "$475.22",
          address: "2118 Thornridge Cir. Syracuse, Connecticut 35624",
          isNew: false,
          meta: [
            { icon: "bed", text: "8 Bed" },
            { icon: "bathtub", text: "5 Bath" },
            { icon: "straighten", text: "1240 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-4.jpg",
          title: "757 Realty",
          price: "$576.28",
          address: "4140 Parker Rd. Allentown, New Mexico 31134",
          isNew: false,
          meta: [
            { icon: "bed", text: "6 Bed" },
            { icon: "bathtub", text: "6 Bath" },
            { icon: "straighten", text: "1260 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-5.jpg",
          title: "Beach Pros Realty Inc.",
          price: "$473.85",
          address: "2715 Ash Dr. San Jose, South Dakota 83475",
          isNew: false,
          meta: [
            { icon: "bed", text: "10 Bed" },
            { icon: "bathtub", text: "8 Bath" },
            { icon: "straighten", text: "2350 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-6.jpg",
          title: "Keller Williams Elite Town Center",
          price: "$105.55",
          address: "3517 W. Gray St. Utica, Pennsylvania 57867",
          isNew: false,
          meta: [
            { icon: "bed", text: "8 Bed" },
            { icon: "bathtub", text: "8 Bath" },
            { icon: "straighten", text: "1950 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-7.jpg",
          title: "All Pros Real Estate",
          price: "$739.65",
          address: "8502 Preston Rd. Inglewood, Maine 98380",
          isNew: false,
          meta: [
            { icon: "bed", text: "4 Bed" },
            { icon: "bathtub", text: "4 Bath" },
            { icon: "straighten", text: "1580 sqft" }
          ]
        },
        {
          image: "/src/assets/images/property-8.jpg",
          title: "FIT Realty",
          price: "$948.55",
          address: "4517 Washington Ave. Manchester, Kentucky 39495",
          isNew: false,
          meta: [
            { icon: "bed", text: "3 Bed" },
            { icon: "bathtub", text: "2 Bath" },
            { icon: "straighten", text: "1120 sqft" }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
/* Додайте стилі для PropertySection тут */
</style>
