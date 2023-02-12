<template>
  <div class="container">
  <div class="section_container">
    <div class="sections">
      <div class="section">
        BaseLine Topology
      </div>
    </div>
    <div class="settings">
      <div class="orange"></div>
      <span class="icon mdi mdi-cog"></span>
    </div>
  </div>
  <div class="table">

    <div class="thead">
      <div class="tr">
        <div class="th" v-for="sort in sortBy" :key="sort.name">
          <div class="sort">
            <span class="name">{{ sort.name }}</span>
            <span v-if="sort.sort !== null" class="arrow mdi mdi-arrow-up"></span>
          </div>
        </div>
      </div>
    </div>

    <div class="tbody">
      <div class="empty">
        <span class="icon mdi mdi-file-tree"></span>
        <div class="title">The Baseline Topology is empty</div>
        <div class="desc">Nodes will appear when they join the cluster</div>
      </div>
    </div>
  </div>
</div>

</template>
<script>
  export default({
    data: ()=> ({
      sortBy: [
        {name: 'Consistent ID', sort: null},
        {name: 'Node ID', sort: null},
        {name: 'Status', sort: null},
        {name: 'Node Type', sort: null},
        {name: 'Baseline', sort: null},
      ],
      items: [],
    }),
    methods: {

    }
  })
</script>
<style scoped>
.container {
  width: 100%;
  height: 100%;
  padding: 0;
}
.section_container {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}
.orange {
  position: absolute;
  top: 4px;
  right: 0;
  width: 8px;
  height: 8px;
  border-radius: 55%;
  background-color: orange;
}
.settings {
  position: relative;
  font-size: 22px;
  color: rgba(4, 4, 4, 0.7);
}
.settings .icon {
  margin-right: 4px;
}
.sections {
  width: 100%;
  border-bottom: 1px solid #ebebeb;
}
.section {
  font-size: 18px;
  width: 180px;
  text-align: center;
  border-bottom: 2px solid #0c5ca3;;
}
.empty {
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 1%;
}
.empty .icon {
  opacity: .7;
  font-size: 122px;
}
.empty .title {
  font-size: 22px;
}
.empty .desc {
  opacity: .7;
  font-size: 14px;
}
.table {
  width: 100%;
  height: 100%;
}
.tbody {
  width: 100%;
}
.thead {
  background-color: #89e1e0; 
  padding: 0 20px;
  height: 58px;
  border-radius: 6px;
  border-bottom-left-radius: 0px;
  border-bottom-right-radius: 0px;
}
.thead .tr {
  display: flex;
  align-items: center;
  height: 100%;
}
.tbody .tr {
  display: flex;
  border-bottom: 2px solid rgb(223, 223, 223);
}
.th {
  width: 20%;
  height: 100%;
}

.th .sort {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  height: 100%;
  color: rgba(4, 4, 4, 0.87);
  font-weight: bold;
  font-size: 15px;
}
.arrow {
  margin-left: 5px;
  font-size: 24px;
}
</style>