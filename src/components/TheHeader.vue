<template>
  <header>
    <FontAwesomeIcon :icon="icon('heart')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('laugh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('meh')"></FontAwesomeIcon>
  </header>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
  faHeart,
  faLaughBeam,
  faMeh
} from "@fortawesome/free-regular-svg-icons";
import { faDigitalOcean } from "@fortawesome/free-brands-svg-icons";

export default {
  components: {
    FontAwesomeIcon
  },
  methods: {
    icon(i) {
      const fa = {
        heart: faHeart,
        laugh: faLaughBeam,
        meh: faMeh
      };
      return fa[`${i}`];
    }
  }
};
</script>
