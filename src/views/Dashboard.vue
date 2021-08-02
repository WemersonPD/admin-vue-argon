<template>
  <div>

    <base-header class="pb-6 pb-8 pt-5 pt-md-8 bg-gradient-success">
      <b-row>
        <b-col v-for="card in cards" :key="card.title" xl="3" md="6">
          <stats-card 
            :title="card.title"
            :type="card.color"
            :sub-title="card.description"
            :icon="card.icon"
            class="mb-4">
          </stats-card>
        </b-col>
      </b-row>
    </base-header>
    <b-container fluid class="mt--7">
      <b-card >
          <b-card-header class="border-0">
              <h3 class="mb-0">Table teste</h3>
          </b-card-header>

          <el-table responsive class="table-responsive table-flush"
                    header-row-class-name="thead-light"
                    :data="projects">

              <el-table-column label="Veterinários"
                              min-width="310px"
                              prop="name"
                              sortable>
                  <template v-slot="{row}">
                      <b-media no-body class="align-items-center">
                          <a href="#" class="avatar rounded-circle mr-3">
                              <img alt="Image placeholder" :src="row.img">
                          </a>
                          <b-media-body>
                              <span class="font-weight-600 name mb-0 text-sm"></span>
                          </b-media-body>
                      </b-media>
                  </template>
              </el-table-column>

              <el-table-column label="Caixa"
                              prop="budget"
                              min-width="140px"
                              sortable>
              </el-table-column>

              <el-table-column label="Status"
                              min-width="170px"
                              prop="status"
                              sortable>
                  <template v-slot="{row}">
                    <b-badge variant="success" v-if="row.statusType == 'success'">Ativo</b-badge>
                    <b-badge v-else variant="danger">Desativado</b-badge>
                  </template>
              </el-table-column>

              <el-table-column label="Clientes" min-width="190px">
                  <div class="avatar-group">
                      <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip"
                        data-original-title="Ryan Tompson">
                          <img alt="Image placeholder" src="img/theme/team-1.jpg">
                      </a>
                      <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip"
                        data-original-title="Romina Hadid">
                          <img alt="Image placeholder" src="img/theme/team-2.jpg">
                      </a>
                      <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip"
                        data-original-title="Alexander Smith">
                          <img alt="Image placeholder" src="img/theme/team-3.jpg">
                      </a>
                      <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip"
                        data-original-title="Jessica Doe">
                          <img alt="Image placeholder" src="img/theme/team-4.jpg">
                      </a>
                  </div>
              </el-table-column>

              <el-table-column min-width="180px">
                  <template v-slot="{row}">
                      <el-dropdown trigger="click" class="dropdown">
                      <span class="btn btn-sm btn-icon-only text-light">
                        <i class="fas fa-ellipsis-v mt-2"></i>
                      </span>
                          <el-dropdown-menu class="dropdown-menu dropdown-menu-arrow show" slot="dropdown">
                              <b-dropdown-item>
                                <base-button type="primary">
                                  Edit
                                </base-button>
                              </b-dropdown-item>
                              <b-dropdown-item>
                                 <base-button v-if="row.statusType == 'success'" type="danger">
                                    Desativar
                                </base-button>
                                 <base-button v-else  type="success">
                                   Ativar
                                </base-button>
                              </b-dropdown-item>
                              <b-dropdown-item>
                                 <base-button icon type="danger">
                                    <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
                                    <span>Deletear</span>
                                </base-button>
                              </b-dropdown-item>
                          </el-dropdown-menu>
                      </el-dropdown>
                  </template>
              </el-table-column>
          </el-table>

          <!-- <b-card-footer class="py-4 d-flex justify-content-end">
              <base-pagination v-model="currentPage" :per-page="5" :total="10"></base-pagination>
          </b-card-footer> -->
      </b-card>
    </b-container>




  </div>
</template>
<script>
  // Components
  import BaseProgress from '@/components/BaseProgress';
  import StatsCard from '@/components/Cards/StatsCard';
  import { Table, TableColumn, DropdownMenu, DropdownItem, Dropdown} from 'element-ui';
  import project from './../views/Tables/projects'

  export default {
    components: {
      BaseProgress,
      StatsCard,
      [Table.name]: Table,
      [TableColumn.name]: TableColumn,
      [Dropdown.name]: Dropdown,
      [DropdownItem.name]: DropdownItem,
      [DropdownMenu.name]: DropdownMenu,
    },
    data() {
      return {
        cards: [
          {
            title: 'Veterinários',
            color: "gradient-red",
            description: "1000",
            icon: "ni ni-active-40",
          },
          {
            title: 'Clientes',
            color: "gradient-orange",
            description: "7000",
            icon: "ni ni-chart-pie-35",
          },

        ],
        projects: project,
        currentPage: 1
      };
    },
    methods: {
     
    },
    mounted() {
    }
  };
</script>
<style>
.el-table .cell{
  padding-left: 0px;
  padding-right: 0px;
}
</style>
