<template>
  <panel>
    <h5 slot="heading-left">Registered users</h5>

    <toggle-link slot="heading-right" text="Create new user" :state="state" state-key="newFormVisible" class="toggle-link-new-user"></toggle-link>

    <div slot="body">
      <users-table :users="users" :sortable="true" sort-by="username" :users-path="usersPath"></users-table>
    </div>
  </panel>
</template>

<script>
  import Panel from '~/shared/components/panel';
  import ToggleLink from '~/shared/components/toggle-link';

  import UsersTable from './table';

  export default {
    props: {
      users: Array,
      usersPath: String,
      state: Object,
    },

    components: {
      Panel,
      ToggleLink,
      UsersTable,
    },
  };
</script>
