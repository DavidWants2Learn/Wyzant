<template>
    <div>
        <header class="module-header">
            <div class="container">
                <h1 class="title">
                    {{metadata.certificates}}
                </h1>
            </div>
        </header>
        <div class="panel certificates container">
            <header>
                <h2 class="panel-content">
                    {{metadata.certificatesHeadingParagraph}}
                </h2>
            </header>
        </div>
        <div id="certificateNav">
            <nav class="certificate-nav">
                <ul>
                    <li>
                        <a id="us2-cert-nav-menu" class="certificate-data-centers-active" onclick="toggleUs2CertTables();">US2 Data Center</a>
                    </li>
                    <li>
                        <a id="eu-cert-nav-menu" onclick="toggleEuCertTables();">EU Data Center</a>
                    </li>
                </ul>
            </nav>
        </div>
        <div id="us2-cert-tables" class="panel certificates container">
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesBlacklineCom}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">US2</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells"> {{metadata.certificatesUS2BlacklineComSubjectProd}} </td>
                        <td class="certificate-cells"> {{metadata.certificatesUS2BlacklineComSubjectSandbox}} </td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineComExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineComExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineComStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineComStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\wild-us2-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\wild-sbus2-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
            <br>
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesSso}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">US2</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2SsoSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2SsoSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2SsoExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2SsoExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2SsoStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2SsoStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\ssous2-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\sbssous2-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
            <br>
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesBlacklineOnDemandSso}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">US2</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2BlacklineOnDemandSsoSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2BlacklineOnDemandSsoSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineOnDemandSsoExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineOnDemandSsoExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineOnDemandSsoStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2BlacklineOnDemandSsoStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\blacklineondemandssous2-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\blacklineondemandssosbus2-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
            <br>
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesDataRelay2WaySsl}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">US2</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2DataRelay2WaySslSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesUS2DataRelay2WaySslSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2DataRelay2WaySslExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2DataRelay2WaySslExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesUS2DataRelay2WaySslStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesUS2DataRelay2WaySslStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\datarelay-us2-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\datarelay-sbus2-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
        </div>
        <div id="eu-cert-tables" class="panel certificates container">
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesBlacklineCom}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">EU</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUBlacklineComSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUBlacklineComSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesEUBlacklineComExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUBlacklineComExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesEUBlacklineComStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUBlacklineComStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\wild-eu1-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\wild-sbeu1-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
            <br>
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                        {{metadata.certificatesSso}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">EU</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUSsoSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUSsoSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesEUSsoExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUSsoExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesEUSsoStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUSsoStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\ssoeu-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\ssosbeu-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
            </div>
            <br>
            <div class="panel-content">
                <table class="certificate-table">
                    <caption>
                            {{metadata.certificatesDataRelay2WaySsl}}
                    </caption>
                    <tr>
                        <th class="certificate-cells-colhead-vertical" scope="col">EU</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Production</th>
                        <th class="certificate-cells-colhead-vertical" scope="col">Sandbox</th>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Subject</th>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUDataRelay2WaySslSubjectProd"></td>
                        <td class="certificate-cells" ng-bind-html="metadata.certificatesEUDataRelay2WaySslSubjectSandbox"></td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Expiration date</th>
                        <td class="certificate-cells">{{metadata.certificatesEUDataRelay2WaySslExpirationDateProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUDataRelay2WaySslExpirationDateSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Strength (key length)</th>
                        <td class="certificate-cells">{{metadata.certificatesEUDataRelay2WaySslStrengthProd}}</td>
                        <td class="certificate-cells">{{metadata.certificatesEUDataRelay2WaySslStrengthSandbox}}</td>
                    </tr>
                    <tr>
                        <th class="certificate-cells-colhead-horizontal" scope="row">Certificate download link</th>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\datarelay-eu1-blackline-com.crt">Certificate</a></td>
                        <td class="certificate-cells"><a href="..\..\..\..\cert-public-key\datarelay-sbeu1-blackline-com.crt">Certificate</a></td>
                    </tr>
                </table>
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
      title: 'Trust - Certificates' || '',
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

<style>

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
