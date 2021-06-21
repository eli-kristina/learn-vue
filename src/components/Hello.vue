<template>
  <div class="hello">
    <div class="dual-list col-md-6">
      <div class="well">
        <div class="row">
          <div class="col-md-12">
            <div class="input-group">
              <form @submit.prevent="addSkill" class="col-md-12">
                <input type="text" name="search" class="form-control" placeholder="Adding skill..." v-model="search" />
              </form>
            </div>
            <p>{{ search }}</p>
          </div>
        </div>
        <ul class="list-group">
          <li class="list-group-item" v-for="(data, idx) in skills" :key="idx">{{ data.skill }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      search: '',
      skills: [
        {'skill': 'PHP'},
        {'skill': 'MySQL'},
        {'skill': 'HTML'}
      ]
    }
  },
  methods: {
    addSkill () {
      this.skills.push({skill: this.search})
      this.search = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dual-list .list-group {
  margin-top: 8px;
}
</style>
