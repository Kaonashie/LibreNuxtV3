<template>
  <div>
    <button
      class="rounded-md"
      id="SOIBTN_JoelSavoie"
      style="
        background: #1192a4;
        color: #ffffff;
        padding: 0.75rem 2rem;
        border: 1px solid #c8c8c8;
        font: 16px;
        cursor: pointer;
      "
      data-height="580"
      data-psz="00"
      data-so-page="JoelSavoie"
      data-delay="1"
    >
      Prendre Rendez-vous
    </button>
  </div>
</template>

<script>
export default {
  mounted() {
    const plugin = document.createElement("script");
    plugin.setAttribute(
      "src",
      "https://cdn.oncehub.com/mergedjs/so.js",
      "type",
      "module" 
    );
    plugin.async = false;
    document.head.appendChild(plugin);
  },
};
</script>
