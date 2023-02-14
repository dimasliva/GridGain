<template>
  <div class="container">
    <AdminClustersHeader/>
    <div class="table_container">
      <AdminClustersTable/>
    </div>
    <div class="second_table_container">
      <SectionTable/>
    </div>
  </div>
</template>
<script>
import SectionTable from '~~/components/Admin/Clusters/SectionTable.vue';

export default {
    layout: "default",
    components: { SectionTable }
}
</script>
<style scoped>
.container {
  padding: 20px;
  width: 100%;
  height: 100%;
}
.table_container {
  margin-top: 20px;
  height: 370px;
  border: 1px solid rgb(228, 228, 228);
  border-radius: 6px;
  border-bottom-left-radius: 0px;
  border-bottom-right-radius: 0px;
  border-bottom: 2px solid rgb(197, 197, 197);
}
.second_table_container {
  margin-top: 20px;
  height: 445px;
  border-bottom: 2px solid rgb(197, 197, 197);
  border: 1px solid rgb(228, 228, 228);
  border-radius: 6px;
  padding: 20px 0px;
}
</style>