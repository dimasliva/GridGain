<template>
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
      <div class="tr" v-for="item in items" :key="item">
        <div class="td checkbox">
          <div class="content">
            <input type="checkbox"/>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="name">{{ item.name }}</div>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="icon status">
              <span class="mdi mdi-close-circle"></span>
            </div>
            <div class="name">{{ item.status }}</div>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="name">{{ item.client }}</div>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="name">{{ item.server }}</div>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="name">{{ item.cluster }}</div>
          </div>
        </div>
        <div class="td">
          <div class="content">
            <div class="name">{{ item.version }}</div>
          </div>
        </div>

        <div class="td">
          <div class="content">
            <div class="name" v-if="!item.secure">
              <span class="lock mdi mdi-lock-open"></span>
            </div>
          </div>
        </div>

        <div class="td dots">
          <div class="content">
            <div class="name">
              <span class="mdi mdi-dots-horizontal"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default({
    data: ()=> ({
      sortBy: [
        {name: 'Name', sort: true},
        {name: 'Status', sort: null},
        {name: 'Client Nodes', sort: null},
        {name: 'Server Nodes', sort: null},
        {name: 'Cluster Type', sort: null},
        {name: 'Version', sort: null},
        {name: 'Secure', sort: null},
      ],
      items: [
        {name: "hardcore_chaplygin", status: 'Disconnected', client: '0', server: '2', cluster: 'Attached', version: '2.14.0', secure: false},
        {name: "dazilling_burnell", status: 'Disconnected', client: '0', server: '2', cluster: 'Attached', version: '2.14.0', secure: false},
        {name: "zen_benz", status: 'Disconnected', client: '0', server: '2', cluster: 'Attached', version: '2.14.0', secure: false},
      ],
    }),
    methods: {

    }
  })
</script>
<style scoped>
.table {
  width: 100%;
  height: 100%;
}
.tbody {
  width: 100%;
}
.thead {
  background-color: #89e1e0; 
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
.tbody {
  display: flex;
  flex-direction: column;
} 
.th, .td {
  width: 14%;
  height: 100%;
  text-align: center;
}
.td {
  font-size: 16px;
  padding: 0 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
}
.tbody .tr:nth-child(even) {
  background-color: rgb(235, 235, 235);
}
.th .sort {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  color: rgba(4, 4, 4, 0.87);
  font-weight: bold;
  font-size: 15px;
}
.arrow {
  margin-left: 5px;
  font-size: 24px;
}
.lock, .dots {
  font-size: 26px;
}
.dots {
  width: 10px;
  transform: rotate(90deg);
}
.checkbox {
  width: 10px;
}
.content {
  display: flex; 
  align-items: center;
}
.status {
  margin-right: 4px;
  color: red;
  font-size: 26px;
}
</style>