<!-- https://www.youtube.com/watch?v=yo2bMGnIKE8 -->
<!-- git subtree push --prefix dist origin gh-pages -->
<script setup>
  import Foo from '/src/components/Foo.vue'
  const node_key = import.meta.env.VITE_NODE_KEY;
  </script>
  
  <template>
    <div class="container">
  
      <div class="item">
        {{node_key}}
      </div>
    </div>
sljsclkj  
    <div>
      <Foo />
    </div>
  
  </template>
  
  <style scoped>
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  
  .item {
    font-size: 20px;
    font-weight: 800;
    color: red;
  }
  </style>
  
  <!-- //////////// github host process //////////// -->
  <!-- 1. 
   import { fileURLToPath, URL } from 'node:url'
  import { defineConfig } from 'vite'
  import vue from '@vitejs/plugin-vue'
  // https://vitejs.dev/config/
  export default defineConfig({
    plugins: [vue()],
    base: '/<site name here>/', <-------------------------------
    resolve: {
      alias: {
        '@': fileURLToPath(new URL('./src', import.meta.url))
      },
    
    }
  }) -->
  
  <!-- 2. create stite -->
  <!-- 3. push to main branch -->
  <!-- 4. npm run build -->
  
  <!-- 5. npm run build -->
  <!-- 6. git add ./dist/ -f  -->
  <!-- 7. git commit -m '<some message>' -->
  
  <!-- 8. git push -->
  <!-- 9. git subtree push --prefix dist origin gh-pages -->
  
  <!-- //////////// REMOVE SENSITIVE DATA //////////// -->
  <!-- 10. git rm -r ./src/ -->
  <!-- 11. git rm -r .env -->
  <!-- 11. git commit -m '<some message>' -->
  <!-- 12. git reset --hard <last commit id> -->
  <!-- 13. git push --force -->
  

  <!-- https://stephenlee.info/version%20control/2021/01/13/git-force-push-subtree.html -->
  <!-- Just note to use the last_working_commit_id, when reverting a non-working commit
  
  git reset --hard <last_working_commit_id>
  So we must not reset to the commit_id that we don't want.
  
  Then sure, we must push to remote branch:
  
  git push --force -->

  <!-- git subtree split --prefix dist -b gh-pages 
  git push -f origin gh-pages:gh-pages  -->