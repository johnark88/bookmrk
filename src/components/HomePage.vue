<template>
  <div class="HomePage">
    <b-container fluid> 
    </b-container>
  </div>
</template>

<script>
  import draggable from 'vuedraggable'
  export default {
    name: 'HomePage',
    components: {
      draggable,
    },
    data() {
      return {
        editable: true,
        isDragging: false,
        delayedDragging: false
      }
    },
    methods: {
      onMove({
        relatedContext,
        draggedContext
      }) {
        const relatedElement = relatedContext.element;
        const draggedElement = draggedContext.element;
        return (
          (!relatedElement || !relatedElement.fixed) && !draggedElement.fixed
        );
      }
    },
    computed: {
      dragOptions() {
        return {};
      },
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.column {
  padding: 1rem;
  background-color: #33b5e5;
  border: 2px solid #fff;
  color: #fff;
  text-align: center;
}
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>