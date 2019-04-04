<template>
  <header>
    <FontAwesomeIcon :icon="icon('futbolL')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('futbolR')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('slice')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('heart')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('laugh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('meh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('DO')"></FontAwesomeIcon>
  </header>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
  faFutbol as falFutbol,
  faPizzaSlice
} from "@fortawesome/pro-light-svg-icons";
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
        futbolL: falFutbol,
        futbolR: farFutbol,
        slice: faPizzaSlice,
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
