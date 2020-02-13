<template>
  <div>
    <app-hero
      title="Blog"
      subtitle="Lorem ipsum dolor sit amet."
      :img-background="
        'https://www.buenosaireseducacional.com.br/wp-content/uploads/2019/06/qual-a-diferenca-entre-o-cbc-e-o-ubaxxi-da-uba-1024x410.jpg'
      "
    />
    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-8">
            <div class="columns is-multiline">
              <div class="column is-12">
                <nav class="pagination is-centered">
                  <p class="pagination-previous" disabled="">Anterior</p>

                  <p class="pagination-next" disabled="">Próximo</p>

                  <ul class="pagination-list">
                    <li>
                      <a
                        class="pagination-link pagination-is-primary is-primary is-current"
                        >1</a
                      >
                    </li>
                  </ul>
                </nav>
              </div>

              <div v-for="post in posts" :key="post.id" class="column is-12">
                <div class="card">
                  <div class="card-image">
                    <img
                      src="https://via.placeholder.com/1366x768"
                      alt="Introducing some new layouts to Bulma Clean Theme"
                    />
                  </div>

                  <div class="card-content">
                    <div class="content">
                      <a class="title is-4" href="#">{{ post.title }}</a>

                      <p></p>
                      <p>
                        {{ post.body }}
                      </p>

                      <p></p>
                    </div>
                    <div class="has-text-centered">
                      <a href="#" class="button is-primary">Continuar lendo</a>
                    </div>
                  </div>
                  <footer class="card-footer">
                    <p class="card-footer-item">
                      Publicado em: {{ post.id }} Fev, 2020
                    </p>
                  </footer>
                </div>
              </div>

              <div class="column is-12">
                <nav class="pagination is-centered">
                  <p class="pagination-previous" disabled="">Anteriror</p>

                  <p class="pagination-next" disabled="">Próximo</p>

                  <ul class="pagination-list">
                    <li><a class="pagination-link is-current">1</a></li>
                  </ul>
                </nav>
              </div>
            </div>
          </div>

          <div class="column is-4-desktop is-12-tablet">
            <p class="title is-4">Últimas postagens</p>

            <div class="columns is-multiline">
              <div
                v-for="post in lastPosts"
                :key="post.id"
                class="column is-12"
              >
                <div class="card">
                  <div class="card-image">
                    <img src="#" alt="" />
                  </div>

                  <div class="card-content">
                    <div class="content">
                      <a class="title is-4" href="#">{{ post.title }}</a>

                      <p></p>
                      <p>
                        {{ post.body }}
                      </p>

                      <p></p>
                    </div>
                    <div class="has-text-centered">
                      <a href="#" class="button is-primary">Continuar lendo</a>
                    </div>
                  </div>
                  <footer class="card-footer">
                    <p class="card-footer-item">
                      Publicado em: {{ post.id }} Fev, 2020
                    </p>
                  </footer>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import axios from 'axios'

import AppHero from '~/components/AppHero'

export default {
  components: { AppHero },
  data() {
    return {
      posts: []
    }
  },
  computed: {
    lastPosts() {
      return this.posts.slice(0, 5)
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json'
      }
    }

    try {
      const response = await axios.get(
        'https://jsonplaceholder.typicode.com/posts',
        config
      )
      this.posts = response.data
    } catch (error) {
      // console.log(error)
    }
  }
}
</script>

<style></style>
