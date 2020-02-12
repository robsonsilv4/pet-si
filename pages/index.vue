<template>
  <div>
    <section class="hero is-medium is-bold is-info">
      <div class="hero-body">
        <div class="container">
          <p class="title is-2">PET-SI</p>
          <p class="subtitle is-3">PET - Sistemas de Informação</p>
        </div>
      </div>
    </section>

    <div class="hero-body">
      <section class="section">
        <div class="container">
          <div class="columns is-multiline is-centered">
            <div
              v-for="(pilar, key) in pilares"
              :key="key"
              class="column is-4 has-text-centered"
            >
              <p class="title is-5">{{ pilar.titulo }}</p>
              <p class="subtitle is-5">
                {{ pilar.descricao }}
              </p>
            </div>
          </div>
        </div>
      </section>

      <section class="section">
        <div class="container has-text-centered">
          <h2 class="title" data-config-id="header">Membros</h2>
          <p class="subtitle" data-config-id="description">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            Cupiditate, eaque.
          </p>
          <div class="columns is-centered is-multiline">
            <div
              v-for="(membro, key) in membros"
              :key="key"
              class="column is-3"
            >
              <div class="level">
                <div class="level-item">
                  <figure class="image is-128x128">
                    <img
                      class="is-rounded"
                      src="https://via.placeholder.com/150"
                      alt=""
                    />
                  </figure>
                </div>
              </div>
              <h5 class="title is-5">{{ membro.nome }}</h5>
              <p class="subtitle is-6">{{ membro.tipo }}</p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Inicio',
  data() {
    return {
      pilares: [
        {
          titulo: 'Ensino',
          descricao:
            'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iusto, perspiciatis!'
        },
        {
          titulo: 'Pesquisa',
          descricao:
            'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iusto, perspiciatis!'
        },
        {
          titulo: 'Extensão',
          descricao:
            'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iusto, perspiciatis!'
        }
      ],
      membros: [
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' },
        { nome: 'Nome do membro', foto: '', tipo: 'Bolsista' }
      ]
    }
  }
}
</script>

<style></style>
