# vue-workshop
npm init vue@latest (with node >v16.0)
	- enter project name and add support for everything
cd project_name
npm install
npm run lint
npm run dev

remove everything in app.vue
empty script, empty style and header with two router links and a router view on the template root

remove display: grid from app on main.css
remove everything on main.css and base.css and add body with margin 0 and * with font family on main.css
delete everything on HomeView.vue and put div with hello world

import {defineComonent} from 'vue'

export default defineComponent({
	name: 'page',
	data () {
		return {	
			variable: ''
		}
	}

})