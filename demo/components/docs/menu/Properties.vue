<template>
  <div>
    <base-title title="[Menu] Properties" />
    <base-table
      :columns="columns"
      :rows="rows"
    />
  </div>
</template>

<script>
import BaseTable from '../../base/Table'
import BaseTitle from '../../BaseTitle'

export default {
  components: {
    BaseTable, BaseTitle
  },
  data () {
    return {
      columns: [
        { attr: 'name', name: 'Name' },
        { attr: 'description', name: 'Description' },
        { attr: 'return', name: 'Return' }
      ],
      rows: [
        {
          name: 'hasDropdownEls',
          description: 'List of HTML elements that have dropdown content',
          return: 'Array<HTMLDivElement>'
        },
        {
          name: '$refs.links',
          description: 'List of HTML elements obtained from menu props',
          return: 'Array<HTMLDivElement>'
        }
      ]
    }
  }
}
</script>
