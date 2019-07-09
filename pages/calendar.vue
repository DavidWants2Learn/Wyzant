<template> 
<div>
    <div ng-hide="invalidReleaseData">
    <header>
        <h1 class="title">
            {{metadata.viewCalendarTitle}}
            <span>{{metadata.timesInUTC}}</span>
        </h1>
        <div class="actions" ng-class="{'disable': invalidReleaseData}">
            <div class="toggle">
                <button class="calendar" ng-disabled="canDoPrev"
                        ng-click="toggle = 'calendar'"
                        ng-class="{'selected': toggle == 'calendar'}">{{metadata.calendar}}</button>
                <button class="calendar"
                        ng-click="toggle = 'list'"
                        ng-class="{'selected': toggle == 'list'}">{{metadata.list}}</button>
            </div>

            <div class="month-picker">
                <button class="arrow prev" ng-click="prevMonth()" ng-disabled="!canDoPrevious"></button>
                <div class="current">{{range}}</div>
                <button class="arrow next" ng-click="nextMonth()" ng-disabled="!canDoNext"></button>
            </div>

            <button class="current-month" ng-click="resetRange()">{{metadata.currentMonth}}</button>
        </div>
    </header>

    <!-- Calendar -->
    <div class="calendar-section trust--animation-fade ng-cloak" ng-if="toggle == 'calendar'" ng-include="'/app/tmpl/modules/calendar/calendar.html'"></div>

    <!-- List -->
    <div class="list-view trust--animation-fade ng-cloak" ng-if="toggle == 'list'" ng-include="'/app/tmpl/modules/calendar/listview.html'"></div>
</div>

<!-- Error message -->
<div class="error" ng-show="invalidReleaseData">
    {{metadata.errorCalendarData}}
</div>
</div>
</template>

<script>
import axios from 'axios'
import metadata from '~/app/metadata/resource/en-US/resource.json'

export default {
  head() {
    return {
      title: 'Trust - Calendar' || '',
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