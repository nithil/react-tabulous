# Syook-Table 🎉

```js
import Table from 'syook-table-v5';

...

tableConfig = [
  {
    heading: 'Name',
    column: 'name',
    cell: ({ row }) => row.name,
    isSortable: true,
    isSearchable: true,
  },
  {
    heading: 'Description',
    column: 'description',
    cell: ({ row }) => row.description,
    isSortable: true,
    isSearchable: true,
  },
  {
    heading: 'Availability',
    column: 'availability',
    cell: ({ row }) => row.availability ? 'true' : 'false',
    isSortable: true,
    isSearchable: true,
  }
];

actionConfig = [
  {
    action: 'Edit',
    show: row => true,
    function: this.onShow,
  },
  {
    action: 'Delete',
    show: row => true,
    function: this.onShow,
  },
];

...

<Table
  data={this.props.objects}
  records={tableConfig}
  mandatoryFields={['Name']}
  includeAction={true}
  actionConfig={actionConfig}
  bulkActions={[{ action: 'delete', function: onDelete }]}
  name='MenuItems'
/>

...
```