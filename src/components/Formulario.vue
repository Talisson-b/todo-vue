<script setup>
    const props = defineProps(['cadastrar', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>


<template>
    <form @submit.prevent="props.cadastrar">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="editaTarefaTemp" required
                    type="text" placeholder="Digite aqui a descrição da tarefa" class="form-control">
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col-md-2">
                <select @change="trocarFiltro" class="form-control">
                    <option value="todas">Todas tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas </option>

                </select>
            </div>
        </div>
    </form>
</template>