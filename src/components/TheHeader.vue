<template>
  <header>
    <FontAwesomeIcon :icon="icon('heart')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('laugh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('meh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('DO')"></FontAwesomeIcon>
  </header>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
  faHeart,
  faLaughBeam,
  faMeh,
  faFutbol as farFutbol
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
        meh: faMeh,
        DO: faDigitalOcean
      };
      return fa[`${i}`];
    }
  }
};
</script>
