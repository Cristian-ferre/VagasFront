<script setup>


</script>

<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <h4>A Presente a sua vaga para milhares de profissionais e de graças</h4>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Título da vaga</label>
        <input type="text" class="form-control">
        <div class="form-text">Por esxemplo: Programador C#</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Descrição</label>
        <textarea type="text" class="form-control"></textarea>
        <div class="form-text">Informe detalhes da vaga</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Salario</label>
        <input type="number" class="form-control">
        <div class="form-text">Informe o sálario.</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Modalidades</label>
        <select class="form-select">
          <option value="1">Home Office</option>
          <option value="2">Presencial</option>

        </select>
        <div class="form-text">Informe serão as atividades.</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Tipo</label>
        <select class="form-select">
          <option value="1">CLT</option>
          <option value="2">PJ</option>

        </select>
        <div class="form-text">Informe A modalidade de contratação.</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <button type="submit" class="btn btn-primary">Cadastrar</button>
      </div>
    </div>

  </div>
</template>

<style scoped></style>
