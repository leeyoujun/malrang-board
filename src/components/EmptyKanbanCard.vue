<template>
  <div class="emptyKanbanCard" @click="handleClickToAdd">
    <div class="emptyKanbanCard__body">
      <div class="emptyKanbanCard__icon">
        <el-icon class="kanban-menu menu-icon">
          <Plus />
        </el-icon>
      </div>
      <div class="emptyKanbanCard__text">카드를 추가하세요.</div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineEmits } from "vue";
import { ElIcon } from "element-plus";

const emit = defineEmits(["add"]);

const handleClickToAdd = () => {
  emit("add");
};

</script>

<style scoped lang="scss">
.emptyKanbanCard {
  width: 100%;
  height: 100%;
  border: 1px dashed #c0c4cc;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 20px;
  padding-bottom: 20px;

  .emptyKanbanCard__body {
    display: flex;
    flex-direction: column;
    align-items: center;

    .emptyKanbanCard__icon {
      font-size: 40px;
      color: #c0c4cc;
    }

    .emptyKanbanCard__text {
      font-size: 14px;
      color: #c0c4cc;
      margin-top: 10px;
    }
  }
}

/* -------------------------------- Hover 스타일 ------------------------------- */
.emptyKanbanCard:hover {
  border: 1px dashed #409eff;
  cursor: pointer;
}
</style>