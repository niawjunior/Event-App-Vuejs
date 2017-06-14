<template>
<div class="col-md-card">
    <h4 class="card-title">{{event.title}}</h4>
    <p class="card-text">{{event.description}}</p>
    <ul class="list-group list-group-flush">
        <li class="list-group">Date: {{event.date}}</li>
        <li class="list-group">Date: {{event.location}}</li>
        <li class="list-group">Date: {{event.email}}</li>
    </ul>
</div>
</template>

<script>
export default {
    props: ['event']
}
</script>