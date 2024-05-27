<template>
  <div class="app-container">
    <el-card>
      <div class="main-box-one">
        <div class="box box-1">
          <span class="item" />
        </div>
        <div class="box box-2">
          <span class="item" />
        </div>
        <div class="box box-3">
          <span class="item" />
        </div>
        <div class="box box-4">
          <span class="item" />
        </div>
        <div class="box box-5">
          <span class="item" />
        </div>
        <div class="box box-6">
          <span class="item" />
        </div>
        <div class="box box-7">
          <span class="item" />
        </div>
      </div>
      <div class="main-box-two">
        <div class="box box-8">
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-9">
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-10">
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-11">
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-12">
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-13">
          <span class="item" />
          <span class="item" />
        </div>
      </div>
      <div class="main-box-three">
        <div class="box box-14">
          <span class="item" />
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-15">
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-16">
          <div class="column">
            <span class="item" />
            <span class="item" />
          </div>
          <div class="column">
            <span class="item" />
            <span class="item" />
          </div>
        </div>
        <div class="box box-17">
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-18">
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
        </div>
        <div class="box box-19">
          <div class="column">
            <span class="item" />
            <span class="item" />
            <span class="item" />
          </div>
          <div class="column">
            <span class="item item3" />
          </div>
          <div class="column">
            <span class="item" />
            <span class="item" />
          </div>
        </div>
        <div class="box box-20">
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
          <span class="item" />
        </div>
      </div>
    </el-card>
  </div>
</template>

<style lang="scss" scoped>
.main-box-one {
  display: flex;
}
.main-box-two {
  display: flex;
}
.main-box-three {
  display: flex;
}
.box {
  height: 110px;
  width: 110px;
  background-color: grey;
  border-radius: 5px;
  margin: 10px;
  .item {
    height: 30px;
    width: 30px;
    border-radius: 50%;
    margin: 3px;
    background-color: black;
  }
}
.box-1 {
  display: flex;
}
.box-2 {
  display: flex;
  justify-content: center;
}
.box-3 {
  display: flex;
  justify-content: end;
}
.box-4 {
  display: flex;
  align-items: center;
}
.box-5 {
  display: flex;
  align-items: center;
  justify-content: center;
}
.box-6 {
  display: flex;
  justify-content: center;
  align-items: end;
}
.box-7 {
  display: flex;
  justify-content: end;
  align-items: end;
}
.box-8 {
  display: flex;
  justify-content: space-between;
}
.box-9 {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.box-10 {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
.box-11 {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: end;
}
.box-12 {
  display: flex;
  .item:nth-child(2) {
    align-self: center;
  }
}
.box-13 {
  display: flex;
  justify-content: space-between;
  .item:nth-child(2) {
    align-self: flex-end;
  }
}
.box-14 {
  display: flex;
  .item:nth-child(2) {
    align-self: center;
  }
  .item:nth-child(3) {
    align-self: end;
  }
}
.box-15 {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  align-content: space-between;
}
.box-16 {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  .column {
    display: flex;
    justify-content: space-between;
    flex-basis: 100%;
  }
}
.box-17 {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
}
.box-18 {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  align-content: space-between;
}
.box-19 {
  display: flex;
  flex-wrap: wrap;
  .column {
    display: flex;
    flex-basis: 100%;
  }
  .column:nth-child(2) {
    justify-content: center;
  }
  .column:nth-child(3) {
    justify-content: space-between;
  }
}
.box-20 {
  display: flex;
  flex-wrap: wrap;
}
</style>
