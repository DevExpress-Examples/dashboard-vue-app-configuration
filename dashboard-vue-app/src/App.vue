<template>
    <div>
        <DxButton 
            @click="switchWorkingMode" 
            :text="buttonText"
        />   
        <DxSelectBox            
            :data-source="data"
            v-model:value="dashboardIdProp"
            display-expr="name"
            value-expr="id"
            width="200px"
        />
        <DxDashboardControl 
            style="height:900px; display: 'block'; width: '100%';"
            endpoint="http://localhost:5000/api/dashboard"
            :workingMode="workingModeProp"
            :dashboardId="dashboardIdProp"
            @beforeRender="onBeforeRender"
        />
    </div>  
</template>

<script>
import DxButton from 'devextreme-vue/button';
import DxSelectBox from 'devextreme-vue/select-box';
import ArrayStore from 'devextreme/data/array_store';
import { DxDashboardControl } from 'devexpress-dashboard-vue';
import {TextBoxItemEditorExtension} from 'devexpress-dashboard/designer/text-box-item-editor-extension';

export default {
    components: {
        DxDashboardControl,
        DxButton,
        DxSelectBox
    },
    data: function() {
        const dashboards = [
            {"id": "support", "name": "Support"},
            {"id": "products", "name": "Products"},
        ];
        return {
            dashboardIdProp: dashboards[0].id,
            workingModeProp: "Designer",            
            data: new ArrayStore({
                data: dashboards,
                key: 'id'
            })
        };
    },
    methods: {
        switchWorkingMode() {
            this.workingModeProp =  this.workingModeProp === "Designer" ? "Viewer": "Designer"            
        },
        onBeforeRender(e) {
            e.component.registerExtension(new TextBoxItemEditorExtension(e.component));
        }
    },
    computed: {
      buttonText() {
        return `Switch to ${this.workingModeProp === "Designer" ? "Viewer": "Designer"}`; 
      }
    }
}
</script>