# v0.0.1

- Projects
	- name, string (30)
	- user, int, foreignkey(Users.id)
	- description, text
	- summary (70)
	- code_name, string(45), unique # Le code du projet n'est pas unique appliqué de petite variation pour le rendre unique si necessaire. Exemple : logizar.app ou logizar.Les caractères autorisé sont les lettres, chiffres, - .
	- status, # ENUM in_progress, pause, ended, abort
	- is_opensource, default(false)
	- site_url, string(100), default(null)
	- repository_url, string(100), default(null)
	- type_id, int, foreignkey(ProjectTypes.id)
	- deliverable_id, int, foreignkey(ProjectDeliverable.id)

	
- Category
	- name, string(25)
	- type, string(10), default ('system')
	- slug, string(255)

- ProjectTypes
	- name, unique, string (25)
	- shortname, string (25)
	- description, text (100)

- ProjectDeliverable
	- name, unique, string (30)
	- shortname, string (30)
	- description, text (100)

- [new] Tags
	- name (100)
	- project_id

