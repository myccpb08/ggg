<template>
    <div>
        <ImgBanner imgSrc="https://source.unsplash.com/random/1600x900">
        <div style="line-height:1.2em;font-size:1.2em;" slot="text">Portfolio</div>
        </ImgBanner>

        <v-container>
            <form>
                <v-text-field placeholder="제목을 입력해주세요."></v-text-field>
                <markdown-editor v-model="content" ref="markdownEditor"></markdown-editor>
                <v-btn @click="submit">submit</v-btn>
                <v-btn @click='$router.go(-1)'>back</v-btn>
            </form>
        </v-container>
    </div>
</template>

<script>
    import ImgBanner from '../components/ImgBanner'
    import markdownEditor from 'vue-simplemde/src/markdown-editor'

  export default {
    components: {
        ImgBanner,
        markdownEditor
    },
    name: 'Portfoliowriter',
  }
</script>
