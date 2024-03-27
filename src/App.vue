<template>
  <org-chart
    :datasource="ds"
    @node-click="selectNode"
  ></org-chart>
</template>

<script>
/* eslint-disable */
import OrgChart from "./components/OrganizationChartContainer.vue";

export default {
  name: "App",
  components: {
    OrgChart,
  },
  data() {
    return {
      ds: {
        id: "1",
        name: "Augustin Ribreau",
        title: "director",
        birth_date: "01-01-2003",
        date_of_death: "01-01-2003",
        age: "1 Years",
        image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png",
        children: [
          { id: "2", name: "Bo Miao", title: "department manager", image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png" },
          {
            id: "3",
            name: "Su Miao",
            title: "department manager",
            image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png",
            children: [
              { id: "4", name: "Tie Hua", title: "senior engineer", image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png" },
              {
                id: "5",
                name: "Hei Hei",
                title: "senior engineer",
                image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png",
                children: [
                  { id: "6", name: "Pang Pang", title: "engineer" , image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png"},
                  { id: "7", name: "Xiang Xiang", title: "UE engineer" , image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png"},
                ],
              },
            ],
          },
          { id: "8", name: "Hong Miao", title: "department manager" , image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png"},
          { id: "9", name: "Chun Miao", title: "department manager" , image: "https://cdn-icons-png.flaticon.com/512/3135/3135715.png" },
        ],
      },
    };
  },
  methods: {
    selectNode(nodeData) {
      alert("node " + nodeData.name + " is selected");
    },
  },
};
</script>
