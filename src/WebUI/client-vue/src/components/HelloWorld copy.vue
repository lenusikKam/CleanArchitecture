<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

  <p>Welcome to your new single-page application, built with:</p>
  <ul>
    <li><a href='https://get.asp.net/' target="_blank" rel="noopener">ASP.NET Core</a> and <a href='https://msdn.microsoft.com/en-us/library/67ef8sbd.aspx' target="_blank" rel="noopener">C#</a> for cross-platform server-side code</li>

    <li><a href='https://cli.vuejs.org' target="_blank" rel="noopener">Vue.js</a> and <a target="_blank" rel="noopener" href='http://www.typescriptlang.org/'>TypeScript</a> for client-side code</li>
    <li><a href='http://getbootstrap.com/' target="_blank" rel="noopener">Bootstrap</a> for layout and styling</li>
  </ul>
  <p>To help you get started, we've also set up:</p>
  <ul>
    <li><strong>Client-side navigation</strong>. For example, click <em>Counter</em> then <em>Back</em> to return here.</li>
    <li><strong>Angular CLI integration</strong>. In development mode, there's no need to run <code>ng serve</code>. It runs in the background automatically, so your client-side resources are dynamically built on demand and the page refreshes when you modify any file.</li>
    <li><strong>Efficient production builds</strong>. In production mode, development-time features are disabled, and your <code>dotnet publish</code> configuration automatically invokes <code>ng build</code> to produce minified, ahead-of-time compiled JavaScript files.</li>
  </ul>
  <p>The <code>ClientApp</code> subdirectory is a standard Angular CLI application. If you open a command prompt in that directory, you can run any <code>ng</code> command (e.g., <code>ng test</code>), or use <code>npm</code> to install extra packages into it.</p>




  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String
  }
})
export default class HelloWorld extends Vue {
  msg!: string
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 2.5rem;
  margin-bottom: .5rem;
  font-weight: 500;
  line-height: 1.2;
}
h3 {
  margin: 40px 0 0;
}
#hello{
  text-align: left;
}
li {
  line-height: 1.5;
}
a {
  color: #42b983;
  text-decoration: none;
}
code {
  color: #e01a76;
}

</style>
