<template>
  <div>
    <app-hero
      title="'PET - SI'"
      subtitle="'PET - Sistemas de Informação'"
      :img-background="
        'https://www.quixada.ufc.br/wp-content/uploads/2018/05/2018-05-30-ufc-campus-quixad%C3%A1_prof-odorico.jpg'
      "
    />

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
                      class="is-rounded zoom"
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
import AppHero from '~/components/AppHero'

export default {
  name: 'Inicio',
  components: {
    AppHero
  },
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
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }
      ]
    }
  }
}
</script>

<style lang="scss">
.zoom {
  transition: transform 0.2s;

  &:hover {
    transform: scale(1.2);
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.1);
  }
}
</style>
