<template>
  <header>
    <FontAwesomeIcon :icon="icon('bomb')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('bong')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('heart')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('laugh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('meh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('DO')"></FontAwesomeIcon>
  </header>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faBomb, faBong } from "@fortawesome/pro-light-svg-icons";
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
        bomb: faBomb,
        bong: faBong,
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
