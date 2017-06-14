<template>
<div class="col-md-4">
  <div class="form-group">
    <div class="event-card">
      <h4 class="card-title">{{event.title}}</h4>
      <p class="card-text">{{event.description}}</p>
      <p>Date: {{event.date}}</p>
      <p>Location: {{event.location}}</p>
      <p>Email: {{event.email}}</p>
    </div>
  </div>
</div>
</template>
<script>
export default {
  props: ['event']
}
</script>
