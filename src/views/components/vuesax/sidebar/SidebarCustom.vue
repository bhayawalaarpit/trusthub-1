<!-- =========================================================================================
    File Name: SidebarCustom.vue
    Description: Rendering of custom sidebar with vx-sidebar(replaces vs-sidebar-item) and vx-sidebar-group(vs-sidebar-group)
    ----------------------------------------------------------------------------------------
    Item Name: Vuexy - Vuejs, HTML & Laravel Admin Dashboard Template
      Author: Pixinvent
    Author URL: http://www.themeforest.net/user/pixinvent
========================================================================================== -->


<template>
    <vx-card title="Custom Sidebar" code-toggler>

        <p>With custom sidebar you can create sidebar items and groups using <strong> list of object</strong>.</p>
        <p>You can also use feather icons in sidebar group and sidebar items using icon property. Check out all feather icons <a href="https://vue-feather-icons.netlify.com/" target="_blank" rel="nofollow">here</a></p>

        <p class="mt-3">Main sidebar on left side is demo of Custom Sidebar. You can check full code by clicking on code-toggler icon of this card.</p>

        <!-- <template slot="codeContainer"><template> -->
       <v-nav-menu
        :sidebarItems= 'sidebarItems'
        title= 'Custom'
        :logo= 'navMenuLogo'/>
    </vx-card>
</template>

<script>
import VNavMenu from '@/layouts/components/vertical-nav-menu/VerticalNavMenu.vue';

export default {
  data: () => ({
    showSidebar: false,
    navMenuLogo: require('@/assets/images/logo/logo.png'),
    sidebarItems: [
      {
        url: '/',
        name: 'Dashboard',
        slug: 'dashboardAnalytics',
        icon: 'HomeIcon',
        i18n: 'Dashboard',
      },
      {
        url: '/ui-elements/colors',
        name: 'Colors',
        slug: 'colors',
        icon: 'DropletIcon',
        i18n: 'Colors',
      },
      {
        header: 'Extensions',
        i18n: 'Extensions',
      },
      {
        url: '/extensions/select',
        name: 'Select',
        icon: 'PocketIcon',
        slug: 'extraComponentSelect',
        i18n: 'Select',
      },
      {
        url: '/extensions/quill-editor',
        name: 'Quill Editor',
        icon: 'EditIcon',
        slug: 'extraComponentQuillEditor',
        i18n: 'QuillEditor',
      },
      {
        url: '/extensions/drag-and-drop',
        name: 'Drag & Drop',
        icon: 'DropletIcon',
        slug: 'extraComponentDragAndDrop',
        i18n: 'DragAndDrop',
      },
      {
        url: '/extensions/datepicker',
        name: 'Datepicker',
        icon: 'CalendarIcon',
        slug: 'extraComponentDatepicker',
        i18n: 'Datepicker',
      },
    ]
  }),
  components: {
    VNavMenu
  }
}
</script>
