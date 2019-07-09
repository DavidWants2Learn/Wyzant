<template>
<div>
    <header class="module-header">
        <div class="container">
            <h1 class="title">
                {{metadata.learn}}
            </h1>
        </div>
    </header>

    <div class="container accordion">
        <div class="panel">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.bestPractices}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content">
                {{metadata.bestPracticesText}}
            </div>
        </div>

        <div class="panel collapse">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.physicalSecurity}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content" >
                {{metadata.physicalSecurityText}}
            </div>
        </div>

        <div class="panel collapse">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.protection}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content">
                {{metadata.protectionText}}
            </div>
        </div>

        <div class="panel collapse">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.compliance}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content">
                {{metadata.complianceText}}
            </div>
        </div>

        <div class="panel collapse">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.privacyPolicy}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content">{{
                metadata.privacyPolicyText | parseContent}}
            </div>
        </div>
        <div class="panel collapse">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.apiTermsofService}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content">
                {{metadata.apiTermsofServiceText | parseContent }}
            </div>
        </div>
        <div id="gdpr"></div>
        <div class="panel">
            <header class="toggler">
                <h1 class="title">
                    {{metadata.gdpr}}
                </h1>
                <div class="panel-content-toggle">
                </div>
            </header>
            <div class="panel-content"> 
                {{metadata.gdprText | parseContent}}
            </div>
        </div>
    </div>
</div>
</template>

<script>
import axios from 'axios'
import metadata from '~/app/metadata/resource/en-US/resource.json'

export default {
  head() {
    return {
      title: 'Trust - Learn' || '',
      meta: [
        { hid: 'description', name: 'description', content: process.env.npm_package_description || '' }
      ]
    }
  },
  asyncData ({ params }) {
      return {metadata}
  },
  components: {
  }
}

</script>
