# Column Toggling
Below is a example that lets developers define the columns and the templates
expressively in markup. This is especially useful for complex situations
where you want rich controls within your grid.

{% gistrun id="d9beac09cb9c5429b4034b384264e4e0" %}
{% endgistrun %}

## Notes
Its important to note, in order for you to project your column/row/value
properties onto the template, you must define those using the `let-*` syntax.
You can also use variables from outside the scope of the parent component.

```javascript
<datatable
  class="material"
  [rows]="rows"
  [options]="options">
  <datatable-column name="Name">
    <template let-value="value" let-row="row" let-column="column">
      {{row}} / {{column}} / {{value}}
    </template>
  </datatable-column>
</datatable>
```
