<template>
  <div>
    <vo-basic
      draggable="true"
      exportButton="true"
      pan="true"
      zoom="true"
      toggleSiblingsResp="true"
      toggleCollapse="true"
      parentNodeSymbol="♦"
      :data="ds"
    ></vo-basic>
    <!-- <organization-chart
      pan="true"
      zoom="true"
      :datasource="ds"
    ></organization-chart> -->
  </div>
</template>
 
<script>
import OrganizationChart from "vue-organization-chart";
// import "vue-organization-chart/dist/orgchart.css";
import "vue-orgchart/dist/style.min.css";
import { VoBasic } from "vue-orgchart";
import { VoEdit } from "vue-orgchart";
export default {
  components: {
    OrganizationChart,
    VoBasic,
    VoEdit,
  },
  data() {
    return {
      ds: {
        id: "1",
        name: "Lao Lao",
        title: "general manager",
        children: [
          { id: "2", name: "Bo Miao", title: "department manager" },
          {
            id: "3",
            name: "Su Miao",
            title: "department manager",
            children: [
              { id: "4", name: "Tie Hua", title: "senior engineer" },
              {
                id: "5",
                name: "Hei Hei",
                title: "senior engineer",
                children: [
                  { id: "6", name: "Pang Pang", title: "engineer" },
                  { id: "7", name: "Xiang Xiang", title: "UE engineer" },
                ],
              },
            ],
          },
          { id: "8", name: "Hong Miao", title: "department manager" },
          { id: "9", name: "Chun Miao", title: "department manager" },
        ],
      },
    };
  },
};
</script> 