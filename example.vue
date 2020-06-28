<template>
    <bv-grdview-component
        :slots="slots"
        :id="id"
        :primary-key="primaryKey"
        :api-url="apiUrl"
        :filter-on="filterOn"
        :sort-by="sortBy"
        :sort-desc="sortDesc"
        :page="page"
        :per-page="perPage"
        :fields="fields"
    >
        <template #abstract="props">
            {{ props.row.item.abstract }}
        </template>
    </bv-grdview-component>
</template>

<script>
    export default {
        data() {
            return {
                slots: [
                    {
                        name: 'abstract',
                        field: 'abstract'
                    }
                ],
                id: 'admin-foo-table',
                primaryKey: '_id',

                apiUrl: '/url/to/endpoint',
                apiData: {},

                filterOn: ['title'],

                sortBy: '_id',
                sortDesc: true,
                page: 1,
                perPage: 2,
                fields: [
                    {
                        key: '_id',
                        label: '#',
                        sortable: true,
                        filterable: true
                    },
                    {
                        key: 'title',
                        label: 'Title',
                        sortable: true,
                        filterable: true
                    },
                    {
                        key: 'abstract',
                        label: 'Abstract',
                        sortable: true,
                        filterable: true
                    },
                    {
                        key: 'n',
                        label: 'N',
                        sortable: false,
                    },
                    {
                        key: 'created_at',
                        label: 'Created At',
                        sortable: true
                    },
                    {
                        key: 'updated_at',
                        label: 'Updated At',
                        sortable: true
                    },
                    {
                        key: 'actions',
                        label: ''
                    },
                ],
            }
        },
        mounted() {
        },
    }
</script>
