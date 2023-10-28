# Database Documentation

## Table of Contents
- [access_levels](#access_levels)
- [restaurants](#restaurants)
- [checklist_groups](#checklist_groups)
- [hidden_plates](#hidden_plates)
- [plates](#plates)
- [build_sheet_plate](#build_sheet_plate)
- [build_sheets](#build_sheets)
- [build_sheet_meal_period](#build_sheet_meal_period)
- [meal_periods](#meal_periods)
- [build_sheet_diet_type](#build_sheet_diet_type)
- [diet_types](#diet_types)
- [unknown_types](#unknown_types)
- [users](#users)
- [partners](#partners)
- [partner_companies](#partner_companies)
- [adjustments](#adjustments)
- [communication_preferences](#communication_preferences)
- [ontraport_audits](#ontraport_audits)
- [document_logs](#document_logs)
- [documents](#documents)
- [document_files](#document_files)
- [document_notes](#document_notes)
- [restaurant_accesses](#restaurant_accesses)
- [logs](#logs)
- [quickbooks_accounts](#quickbooks_accounts)
- [quick_books_accounts_matches](#quick_books_accounts_matches)
- [pause_salaries](#pause_salaries)
- [jobs](#jobs)
- [labor_categories](#labor_categories)
- [labor_jobs](#labor_jobs)
- [labors](#labors)
- [labor_entries](#labor_entries)
- [labor_employees](#labor_employees)
- [upload_counts](#upload_counts)
- [departments](#departments)
- [department_sales](#department_sales)
- [sales_notes](#sales_notes)
- [reason_sales](#reason_sales)
- [budget_daily_sales](#budget_daily_sales)
- [indirect_labor_settings](#indirect_labor_settings)
- [actions](#actions)
- [notifications](#notifications)
- [triggers](#triggers)
- [notification_schedules](#notification_schedules)
- [recipe_categories](#recipe_categories)
- [settings](#settings)
- [labor_settings](#labor_settings)
- [recipe_directions](#recipe_directions)
- [recipes](#recipes)
- [recipe_ingredients](#recipe_ingredients)
- [purchase_files](#purchase_files)
- [checklists](#checklists)
- [checklistsitems](#checklistsitems)
- [checklist_items](#checklist_items)
- [notification_states](#notification_states)
- [inventory_sheets](#inventory_sheets)
- [inventory_sheet_items](#inventory_sheet_items)
- [purchases](#purchases)
- [categories](#categories)
- [sales](#sales)
- [transfer_items](#transfer_items)
- [transfers](#transfers)
- [budget_categories](#budget_categories)
- [budgets](#budgets)
- [budget_comps](#budget_comps)
- [comp_categories](#comp_categories)
- [monthly_inventories](#monthly_inventories)
- [weekly_inventories](#weekly_inventories)
- [category_vendor](#category_vendor)
- [vendors](#vendors)
- [non_expense_category_vendor](#non_expense_category_vendor)
- [non_expense_categories](#non_expense_categories)
- [menus](#menus)
- [menu_items](#menu_items)
- [restaurant_tours](#restaurant_tours)
- [expense_schedules](#expense_schedules)
- [schedules](#schedules)
- [purchase_schedules](#purchase_schedules)
- [caterings](#caterings)
- [catering_items](#catering_items)
- [batch_recipes](#batch_recipes)
- [batch_recipe_items](#batch_recipe_items)
- [daily_imports](#daily_imports)
- [sale_guests](#sale_guests)
- [labor_budgets](#labor_budgets)
- [labor_budget_categories](#labor_budget_categories)
- [quick_books_toggle_accounts](#quick_books_toggle_accounts)
- [checklist_positions](#checklist_positions)
- [checklist_settings](#checklist_settings)
- [recently_imported_reports](#recently_imported_reports)
- [checklist_wizard_items](#checklist_wizard_items)
- [checklist_wizard_services](#checklist_wizard_services)
- [inventories](#inventories)
- [inventory_locations](#inventory_locations)
- [projects](#projects)
- [sub_locations](#sub_locations)
- [report_suggestions](#report_suggestions)
- [api_poster_matches](#api_poster_matches)
- [job_descriptions](#job_descriptions)
- [quasar_settings](#quasar_settings)
- [api_poster_transactions](#api_poster_transactions)
- [employees](#employees)
- [quick_books_fetch_datas](#quick_books_fetch_datas)
- [batch_recipe_locations](#batch_recipe_locations)
- [hidden_units](#hidden_units)
- [units](#units)
- [import_matches](#import_matches)
- [intuits](#intuits)
- [posters](#posters)
- [api_clover_merchants](#api_clover_merchants)
- [non_expense_items](#non_expense_items)
- [stations](#stations)
- [checklists_unit](#checklists_unit)
- [api_clovers](#api_clovers)
- [document_pending_statuses](#document_pending_statuses)
- [api_links](#api_links)
- [invoices](#invoices)
- [comps](#comps)
- [order_guides](#order_guides)
- [account_logs](#account_logs)
- [apis](#apis)
- [api_clovers_matches](#api_clovers_matches)
- [api_clover_webhooks](#api_clover_webhooks)
- [api_poster_products](#api_poster_products)
- [backup_files](#backup_files)
- [bugs](#bugs)
- [build_sheet_restaurant](#build_sheet_restaurant)
- [cache](#cache)
- [cancelled_archives](#cancelled_archives)
- [checklist_group_restaurants](#checklist_group_restaurants)
- [checklist_restaurant](#checklist_restaurant)
- [checklist_types](#checklist_types)
- [checklist_types_archives](#checklist_types_archives)
- [common_passwords](#common_passwords)
- [communication_preference_types](#communication_preference_types)
- [companies](#companies)
- [company_partner_company](#company_partner_company)
- [count_units](#count_units)
- [currencies](#currencies)
- [document_send_mail_logs](#document_send_mail_logs)
- [document_tags](#document_tags)
- [document_trees](#document_trees)
- [dropbox_backups](#dropbox_backups)
- [email_sched_logs](#email_sched_logs)
- [failed_jobs](#failed_jobs)
- [import_report_types](#import_report_types)
- [pos](#pos)
- [job_description_restaurant](#job_description_restaurant)
- [login_tokens](#login_tokens)
- [mailbox_inbound_emails](#mailbox_inbound_emails)
- [messages](#messages)
- [mf_logs](#mf_logs)
- [migrations](#migrations)
- [model_has_permissions](#model_has_permissions)
- [permissions](#permissions)
- [role_has_permissions](#role_has_permissions)
- [roles](#roles)
- [model_has_roles](#model_has_roles)
- [oauth_access_tokens](#oauth_access_tokens)
- [oauth_auth_codes](#oauth_auth_codes)
- [oauth_clients](#oauth_clients)
- [oauth_personal_access_clients](#oauth_personal_access_clients)
- [oauth_refresh_tokens](#oauth_refresh_tokens)
- [partner_company_user](#partner_company_user)
- [partner_restaurant_views](#partner_restaurant_views)
- [partner_user_restaurant_accesses](#partner_user_restaurant_accesses)
- [password_resets](#password_resets)
- [push_logs](#push_logs)
- [quasar_page_accesses](#quasar_page_accesses)
- [queue](#queue)
- [quickbooks_options](#quickbooks_options)
- [recipe_restaurant](#recipe_restaurant)
- [scripts](#scripts)
- [sessions](#sessions)
- [telescope_entries](#telescope_entries)
- [telescope_entries_tags](#telescope_entries_tags)
- [telescope_monitoring](#telescope_monitoring)
- [tours](#tours)
- [unit_archives](#unit_archives)
- [user_restaurant_modules](#user_restaurant_modules)

## access_levels

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| access_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- user_id references [users](#users) (id)

---

## restaurants

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| name | `varchar(255)` |
| categories | `text` |
| operating_expenses | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| logo | `varchar(255)` |
| logo_filename | `varchar(255)` |
| crop_values | `text` |
| welcome | `tinyint(1)` |
| setup_wizard | `int(11)` |
| setup_wizard_notify | `int(11)` |
| last_module | `text` |
| wizard_position | `varchar(255)` |
| agree_date | `datetime` |
| multi_migrate | `tinyint(1)` |
| pos | `varchar(255)` |
| company_id | `int(11)` |
| bill_internally | `tinyint(1)` |
| bill_immediately | `tinyint(1)` |
| document_tags_updated | `tinyint(1)` |
| has_qb_totals | `tinyint(1)` |
| last_document_folder | `int(11)` |
| qbo_tags_updated | `tinyint(1)` |
| deleted_by | `int(11)` |

### Relationships
- user_id references [users](#users) (id)

---

## checklist_groups

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## hidden_plates

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| plate_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- plate_id references [plates](#plates) (id)

---

## plates

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| restaurant_id | `int(11)` |
| order | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## build_sheet_plate

### Columns

| Name | Type |
|------|------|
| build_sheet_id | `int(10) unsigned` |
| plate_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- plate_id references [plates](#plates) (id)
- build_sheet_id references [build_sheets](#build_sheets) (id)

---

## build_sheets

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| description | `text` |
| plate | `text` |
| period | `text` |
| ingredients | `text` |
| directions | `text` |
| standards | `text` |
| allergies | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| photo | `varchar(255)` |
| crop_values | `text` |
| photo_filename | `text` |
| extension | `varchar(255)` |
| server_description | `text` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## build_sheet_meal_period

### Columns

| Name | Type |
|------|------|
| build_sheet_id | `int(10) unsigned` |
| meal_period_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- build_sheet_id references [build_sheets](#build_sheets) (id)
- meal_period_id references [meal_periods](#meal_periods) (id)

---

## meal_periods

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| restaurant_id | `int(11)` |
| order | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## build_sheet_diet_type

### Columns

| Name | Type |
|------|------|
| build_sheet_id | `int(10) unsigned` |
| diet_type_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- build_sheet_id references [build_sheets](#build_sheets) (id)
- diet_type_id references [diet_types](#diet_types) (id)

---

## diet_types

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| restaurant_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## unknown_types

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| email | `text` |
| file | `text` |
| filename | `text` |
| sent | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- user_id references [users](#users) (id)

---

## users

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| first_name | `varchar(255)` |
| last_name | `varchar(255)` |
| email | `varchar(255)` |
| password | `varchar(255)` |
| company | `varchar(255)` |
| contact_id | `int(11)` |
| status | `int(11)` |
| api_token | `varchar(255)` |
| reset_token | `varchar(255)` |
| role | `int(11)` |
| remember_token | `varchar(100)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| last_logged_in | `date` |
| parent_id | `int(10) unsigned` |
| multi_unit | `int(10) unsigned` |
| software_accounts | `int(11)` |
| ip_address | `varchar(255)` |
| from_demo | `int(11)` |
| partner_id | `int(11)` |
| agree | `tinyint(1)` |
| agree_date | `datetime` |
| timezone | `varchar(255)` |
| reset_token_date | `datetime` |
| free_to_standard | `tinyint(1)` |
| owner_id | `int(10) unsigned` |
| activation_code | `varchar(255)` |
| last_restaurant | `int(10) unsigned` |
| email_change | `varchar(255)` |
| multi_unit_date | `date` |
| profile_pic | `varchar(255)` |
| profile_pic_filename | `varchar(255)` |
| crop_values | `text` |
| visit_welcome_page | `int(11)` |
| email_transactional_emails | `tinyint(1)` |
| email_marketing | `tinyint(1)` |
| email_account_updates | `tinyint(1)` |
| email_reports | `tinyint(1)` |
| license_no | `varchar(255)` |
| steps | `text` |
| op_foodCost | `int(11)` |
| op_experienceLevel | `int(11)` |
| op_motivationLevel | `int(11)` |
| op_avgSales | `int(11)` |
| op_timeDedicate | `int(11)` |
| op_goal | `text` |
| op_this_time | `text` |
| license_no_used | `datetime` |
| cancelled_date | `datetime` |
| cancel_reason | `text` |
| login_attempts | `int(11)` |
| lock_date | `datetime` |
| notes | `text` |
| is_partner | `tinyint(1)` |
| last_active_date | `datetime` |
| admin_notes | `text` |
| document_email_notification | `tinyint(1)` |
| document_push_notification | `tinyint(1)` |
| pagination_records_per_page | `int(11)` |
| document_access | `tinyint(1)` |
| document_daily_activity | `tinyint(1)` |
| switch_users | `text` |
| restaurant_summary_report | `tinyint(1)` |
| partner_admin | `tinyint(1)` |

### Relationships
- owner_id references [users](#users) (id)

---

## partners

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| partner_company_id | `int(10) unsigned` |

### Relationships
- user_id references [users](#users) (id)
- partner_company_id references [partner_companies](#partner_companies) (id)

---

## partner_companies

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## adjustments

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| budget_id | `int(10) unsigned` |
| name | `varchar(255)` |
| amount | `double(15,2)` |
| old_amount | `double(15,2)` |
| reason | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| type | `int(11)` |

### Relationships
- user_id references [users](#users) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## communication_preferences

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| communication_preferences | `text` |
| emails | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- user_id references [users](#users) (id)

---

## ontraport_audits

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| op_id | `int(10) unsigned` |
| status | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- user_id references [users](#users) (id)

---

## document_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| document_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| email_from | `varchar(191)` |
| type | `int(11)` |
| method | `int(11)` |
| filename | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- user_id references [users](#users) (id)
- document_id references [documents](#documents) (id)

---

## documents

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(11)` |
| filename | `varchar(191)` |
| file | `varchar(191)` |
| document_tree_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| document_type_id | `int(11)` |
| vendor_id | `int(11)` |
| invoice_no | `varchar(191)` |
| check_no | `varchar(191)` |
| date | `date` |
| tags | `text` |
| customer | `varchar(191)` |
| original_document_id | `int(11)` |
| restore_document_tree_id | `int(11)` |
| ocr_result | `longtext` |
| ocr_status | `tinyint(1)` |
| ocr_created_at | `datetime` |
| ocr_updated_at | `datetime` |
| quickbooks | `int(11)` |
| quickbooks_data | `text` |
| share_id | `text` |
| vendor_qb_id | `int(11)` |
| is_email | `tinyint(1)` |
| email_content | `text` |
| qb_ref_id | `int(11)` |
| customer_qb_id | `int(11)` |
| notified_user_ids | `text` |
| seen_by | `text` |
| extra_chef | `tinyint(1)` |
| margin_edge | `tinyint(1)` |
| xtra_chef_failed | `tinyint(1)` |
| margin_edge_failed | `tinyint(1)` |
| total | `int(11)` |
| download_link | `varchar(191)` |
| pending | `int(11)` |

### Relationships
No relationships.

---

## document_files

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| document_id | `int(10) unsigned` |
| filename | `varchar(191)` |
| file | `varchar(191)` |
| order | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| mime_type | `varchar(191)` |
| file_hash | `text` |
| duplicate_ids | `longtext` |
| rotation_value | `int(11)` |

### Relationships
- document_id references [documents](#documents) (id)

---

## document_notes

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| document_id | `int(10) unsigned` |
| user_id | `int(11)` |
| notes | `text` |
| tags | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| from_name | `varchar(191)` |
| from_email | `varchar(191)` |
| seen_by | `text` |

### Relationships
- document_id references [documents](#documents) (id)

---

## restaurant_accesses

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| full_access | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- user_id references [users](#users) (id)

---

## logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| ip_address | `varchar(255)` |
| browser | `varchar(255)` |
| browser_version | `varchar(255)` |
| platform | `varchar(255)` |
| platform_version | `varchar(255)` |
| action | `varchar(255)` |
| notes | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- user_id references [users](#users) (id)

---

## quickbooks_accounts

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| quickbooks_id | `int(11)` |
| name | `varchar(255)` |
| type | `varchar(255)` |
| sub_account | `tinyint(1)` |
| data | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| QBORealmID | `varchar(191)` |
| account_no | `varchar(191)` |
| parent_id | `varchar(191)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## quick_books_accounts_matches

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| quickbooks_account_id | `int(10) unsigned` |
| account_type | `int(11)` |
| type | `int(11)` |
| category_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- quickbooks_account_id references [quickbooks_accounts](#quickbooks_accounts) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## pause_salaries

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| job_id | `int(10) unsigned` |
| start_date | `date` |
| end_date | `date` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| permanent | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- job_id references [jobs](#jobs) (id)

---

## jobs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| category_id | `int(10) unsigned` |
| use_fixed | `tinyint(1)` |
| fixed_amount | `double(10,2)` |
| restaurant_id | `int(10) unsigned` |
| order | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| entry_type | `int(10) unsigned` |
| last_day | `date` |
| effective_date | `date` |
| account_no | `varchar(255)` |

### Relationships
- category_id references [labor_categories](#labor_categories) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## labor_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| account_no | `varchar(255)` |
| indirect_labor | `tinyint(1)` |

### Relationships
No relationships.

---

## labor_jobs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| labor_id | `int(10) unsigned` |
| job_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| cost | `double(15,2)` |
| hours | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| is_fixed | `tinyint(1)` |
| cash | `double(15,2)` |
| deleted_at | `timestamp` |
| qbo_type | `varchar(191)` |
| qbo_num | `varchar(191)` |
| qbo_name | `varchar(191)` |

### Relationships
- labor_id references [labors](#labors) (id)
- restaurant_id references [restaurants](#restaurants) (id)
- job_id references [jobs](#jobs) (id)

---

## labors

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| fixed_cost | `double(15,2)` |
| percentage | `double(15,2)` |
| period_cost | `double(10,2)` |
| indirect_labor | `double(15,2)` |
| indirect_labor_source | `int(11)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## labor_entries

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| labor_id | `int(10) unsigned` |
| job_id | `int(10) unsigned` |
| hours | `double(15,2)` |
| cost | `double(15,2)` |
| cash | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- labor_id references [labors](#labors) (id)

---

## labor_employees

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| employee_id | `int(10) unsigned` |
| cash | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| employee_rate | `double(15,2)` |
| employee_type | `int(11)` |
| hours | `double(15,2)` |
| cost | `double(15,2)` |
| payroll_cash | `tinyint(1)` |
| labor_id | `int(10) unsigned` |
| pay_daily_rate | `tinyint(1) unsigned` |

### Relationships
- labor_id references [labors](#labors) (id)

---

## upload_counts

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| filename | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## departments

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| order | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## department_sales

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| department_id | `int(10) unsigned` |
| date | `date` |
| amount | `double(15,2)` |
| guest_count | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- department_id references [departments](#departments) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## sales_notes

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| date | `date` |
| traffic | `int(10) unsigned` |
| comment | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## reason_sales

### Columns

| Name | Type |
|------|------|
| sales_note_id | `int(10) unsigned` |
| reason | `int(10) unsigned` |

### Relationships
- sales_note_id references [sales_notes](#sales_notes) (id)

---

## budget_daily_sales

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| amount | `double(15,2)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## indirect_labor_settings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| from | `date` |
| to | `date` |
| actual_expense | `double(15,2)` |
| estimated_expense | `double(15,2)` |
| difference | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## actions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| notification_id | `int(10) unsigned` |
| item_id | `int(11)` |
| notes | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- notification_id references [notifications](#notifications) (id)

---

## notifications

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| title | `varchar(191)` |
| last_run | `datetime` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| status | `int(11)` |
| user_id | `int(11)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## triggers

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| notification_id | `int(10) unsigned` |
| item_id | `int(11)` |
| option_id | `int(11)` |
| compare_id | `int(11)` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- notification_id references [notifications](#notifications) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## notification_schedules

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| notification_id | `int(10) unsigned` |
| interval | `int(11)` |
| day | `int(11)` |
| day_no | `int(11)` |
| month | `int(11)` |
| month_no | `int(11)` |
| quarter | `int(11)` |
| time | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| server_time | `datetime` |

### Relationships
- notification_id references [notifications](#notifications) (id)

---

## recipe_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## settings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| guest_count | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| operating_expense | `tinyint(1)` |
| labor | `tinyint(1)` |
| inventory | `int(11)` |
| pdf_footer_line_1 | `varchar(255)` |
| pdf_footer_line_2 | `varchar(255)` |
| pdf_logo | `tinyint(1)` |
| department | `tinyint(1)` |
| job_description | `tinyint(1)` |
| job_description_signature | `text` |
| job_description_message | `text` |
| currency_id | `int(10) unsigned` |
| labor_calculator | `tinyint(1)` |
| job_sheet | `tinyint(1)` |
| sheet_package | `tinyint(1)` |
| ninja_interest | `tinyint(1)` |
| nesting | `tinyint(1)` |
| ninja_not_interested | `tinyint(1)` |
| nesting_date | `datetime` |
| nesting_flag | `tinyint(1)` |
| cash | `tinyint(1)` |
| getting_started | `tinyint(1)` |
| start_week | `int(11)` |
| accounts_module | `tinyint(1)` |
| account_module | `tinyint(1)` |
| checklist_wizard | `tinyint(1)` |
| comps | `tinyint(1)` |
| video_report_suggestion | `tinyint(1)` |
| tag_downloaded | `tinyint(1)` |
| new_feature | `tinyint(1)` |
| dont_show_profile_pic | `tinyint(1)` |
| dont_show_pos | `tinyint(1)` |
| show_integration | `tinyint(1)` |
| date_format | `tinyint(1)` |
| discount_type | `int(11)` |
| daily_budget | `tinyint(1)` |
| info_box | `tinyint(1)` |
| hide_new_dashboard_banner | `tinyint(1)` |
| budget_spreadsheet_view | `int(11)` |
| doe_detailed | `tinyint(1)` |
| documents | `tinyint(1)` |
| document_email | `varchar(191)` |
| splitter_width | `double` |
| document_one_click_forwarding | `tinyint(1)` |
| document_extra_chef_email | `varchar(191)` |
| document_margin_edge_email | `varchar(191)` |
| document_extra_chef_email_toggle | `tinyint(1)` |
| document_margin_edge_email_toggle | `tinyint(1)` |
| quickbooks_priority | `tinyint(1)` |
| document_write_to_parent | `tinyint(1)` |
| qb_class_id | `varchar(191)` |
| document_required_vendor | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## labor_settings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| frequency | `int(11)` |
| fixed_cost | `double(15,2)` |
| percentage | `double(15,2)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| show_hours | `tinyint(1)` |
| period_cost | `double(10,2)` |
| auto_post | `tinyint(1)` |
| auto_post_date | `date` |
| fed | `double(15,2)` |
| fmed | `double(15,2)` |
| fsoc | `double(15,2)` |
| futa | `double(15,2)` |
| state | `double(15,2)` |
| state_940 | `double(15,2)` |
| payroll_processing_fee | `double(15,2)` |
| workmans_compensation | `double(15,2)` |
| others | `double(15,2)` |
| fixed_payroll_processing_fees | `double(15,2)` |
| period_process_fee | `int(11)` |
| fixed_workmans_compensation | `double(15,2)` |
| period_workmans_compensation | `int(11)` |
| fixed_other | `double(15,2)` |
| period_other | `int(11)` |
| indirect_labor | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## recipe_directions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| recipe_id | `int(10) unsigned` |
| direction | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- recipe_id references [recipes](#recipes) (id)

---

## recipes

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| recipe_category_id | `int(10) unsigned` |
| yield | `varchar(255)` |
| unit_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| portion | `varchar(255)` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## recipe_ingredients

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| recipe_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| item | `varchar(255)` |
| quantity | `varchar(255)` |
| unit_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- recipe_id references [recipes](#recipes) (id)

---

## purchase_files

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| restaurant_id | `int(10) unsigned` |
| filename | `varchar(255)` |
| ext | `varchar(255)` |
| original_filename | `varchar(255)` |
| invoice_id | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklists

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| days | `varchar(255)` |
| months | `varchar(255)` |
| date | `tinyint(1)` |
| par | `tinyint(1)` |
| unit | `tinyint(1)` |
| low_high | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| checklist_type_id | `int(11)` |
| checklist_position_id | `int(11)` |
| checklist_group_id | `int(10) unsigned` |
| vendor_id | `int(10) unsigned` |
| type | `varchar(255)` |
| group | `varchar(255)` |
| position | `varchar(255)` |
| copy_status | `int(11)` |
| split | `tinyint(1)` |
| weekly_monthly | `tinyint(1)` |
| header_days | `text` |
| header_months | `text` |
| days_temp | `text` |
| deleted_at | `timestamp` |
| header_weeks | `text` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklistsitems

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| checklists_id | `int(10) unsigned` |
| desc | `varchar(255)` |
| low | `varchar(255)` |
| high | `varchar(255)` |
| unit | `varchar(255)` |
| days | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| station_id | `int(10) unsigned` |

### Relationships
- checklists_id references [checklists](#checklists) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklist_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| checklist_id | `int(10) unsigned` |
| station_id | `int(11)` |
| items | `text` |
| days | `text` |
| months | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| location | `varchar(255)` |
| deleted_at | `timestamp` |

### Relationships
- checklist_id references [checklists](#checklists) (id)

---

## notification_states

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| health | `varchar(191)` |
| prime_cost | `double(15,2)` |
| cogs | `double(15,2)` |
| health_rolling | `varchar(191)` |
| prime_cost_rolling | `double(15,2)` |
| cogs_rolling | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## inventory_sheets

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| category_id | `int(10) unsigned` |
| date | `date` |
| status | `int(11)` |
| inventory_period | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| total | `double(15,2)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## inventory_sheet_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| inventory_sheet_id | `int(10) unsigned` |
| inventory_id | `int(10) unsigned` |
| batch_recipe_id | `int(10) unsigned` |
| location_id | `int(10) unsigned` |
| sub_location_id | `int(10) unsigned` |
| unit_id | `int(10) unsigned` |
| cost | `double(15,2)` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- inventory_sheet_id references [inventory_sheets](#inventory_sheets) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## purchases

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| amount | `double(15,2)` |
| vendor_id | `int(11)` |
| category_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| invoice_id | `int(11)` |
| credit | `double(15,2)` |
| description | `varchar(255)` |
| order | `int(11)` |
| comps | `tinyint(1)` |
| qbo_type | `varchar(191)` |
| qbo_num | `varchar(191)` |
| qbo_name | `varchar(191)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- category_id references [categories](#categories) (id)

---

## categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| tag | `varchar(255)` |
| type | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| order | `int(10) unsigned` |
| inventory | `int(10) unsigned` |
| inventory_period | `int(11)` |
| _lft | `int(10) unsigned` |
| _rgt | `int(10) unsigned` |
| parent_id | `int(10) unsigned` |
| sort_after | `int(11)` |
| sorting | `int(11)` |
| quickbooks_account_id | `int(11)` |
| account_no | `varchar(255)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## sales

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| category_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| date | `date` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| api | `tinyint(1)` |
| deposit | `double(15,2)` |
| qbo_type | `varchar(191)` |
| qbo_num | `varchar(191)` |
| qbo_name | `varchar(191)` |

### Relationships
- category_id references [categories](#categories) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## transfer_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| transfer_id | `int(10) unsigned` |
| from_category | `int(10) unsigned` |
| to_category | `int(10) unsigned` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- to_category references [categories](#categories) (id)
- from_category references [categories](#categories) (id)
- transfer_id references [transfers](#transfers) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## transfers

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| description | `varchar(255)` |
| restaurant_id | `int(10) unsigned` |
| transfer_to | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- transfer_to references [restaurants](#restaurants) (id)

---

## budget_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| sale | `double(15,2)` |
| cost | `double(15,2)` |
| category_id | `int(10) unsigned` |
| budget_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| sale_amount | `double(15,2)` |
| cost_amount | `double(15,2)` |

### Relationships
- budget_id references [budgets](#budgets) (id)
- category_id references [categories](#categories) (id)

---

## budgets

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| amount | `double(15,2)` |
| date | `date` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| actual | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## budget_comps

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| budget_id | `int(10) unsigned` |
| comp_category_id | `int(10) unsigned` |
| sale | `double(15,2)` |
| cost | `double(15,2)` |
| sale_amount | `double(15,2)` |
| cost_amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- budget_id references [budgets](#budgets) (id)
- comp_category_id references [comp_categories](#comp_categories) (id)

---

## comp_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| account_type | `int(11)` |
| account_id | `int(10) unsigned` |
| show | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| parent_id | `int(11)` |
| account_no | `varchar(255)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## monthly_inventories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| month | `int(11)` |
| year | `int(11)` |
| category_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| inventory_sheet_id | `int(10) unsigned` |
| deleted_at | `timestamp` |

### Relationships
- category_id references [categories](#categories) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## weekly_inventories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| week | `int(11)` |
| year | `int(11)` |
| category_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| inventory_sheet_id | `int(10) unsigned` |
| deleted_at | `timestamp` |

### Relationships
- category_id references [categories](#categories) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## category_vendor

### Columns

| Name | Type |
|------|------|
| category_id | `int(10) unsigned` |
| vendor_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- category_id references [categories](#categories) (id)
- vendor_id references [vendors](#vendors) (id)

---

## vendors

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| order | `varchar(255)` |
| is_cogs | `tinyint(1)` |
| is_expense | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## non_expense_category_vendor

### Columns

| Name | Type |
|------|------|
| non_expense_category_id | `int(10) unsigned` |
| vendor_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- vendor_id references [vendors](#vendors) (id)
- non_expense_category_id references [non_expense_categories](#non_expense_categories) (id)

---

## non_expense_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| parent_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| hide | `text` |
| account_no | `varchar(255)` |
| type | `int(11)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## menus

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| food_cost | `double(15,2)` |
| gross_profit | `double(15,2)` |
| total_cost | `double(15,2)` |
| menu_price | `double(15,2)` |
| recipe_category_id | `int(10) unsigned` |
| directions | `text` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## menu_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| menu_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| quantity | `double(15,2)` |
| recipe_unit | `int(11)` |
| ru_units | `double(15,2)` |
| cost | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| inventory_id | `int(10) unsigned` |
| unit_cost | `double(15,2)` |
| unit_id | `int(10) unsigned` |
| batch_recipe_id | `int(11)` |

### Relationships
- menu_id references [menus](#menus) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## restaurant_tours

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| tour_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## expense_schedules

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| schedule_id | `int(10) unsigned` |
| non_expense_category_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| description | `varchar(255)` |
| order | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)
- schedule_id references [schedules](#schedules) (id)

---

## schedules

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| interval | `int(11)` |
| day | `int(11)` |
| date | `int(11)` |
| month | `int(11)` |
| month_date | `int(11)` |
| start_date | `date` |
| end_date | `date` |
| end_type | `int(11)` |
| vendor_id | `int(11)` |
| notes | `text` |
| end_interval | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| name | `varchar(255)` |
| last_run | `date` |
| run_count | `int(11)` |
| deleted_at | `timestamp` |
| users | `varchar(255)` |
| method | `varchar(255)` |
| data | `text` |
| type | `tinyint(1)` |
| quarter | `int(11)` |
| token | `varchar(255)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## purchase_schedules

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| schedule_id | `int(10) unsigned` |
| category_id | `int(11)` |
| amount | `double(15,2)` |
| description | `varchar(255)` |
| order | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- schedule_id references [schedules](#schedules) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## caterings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| received_date | `date` |
| event_date | `date` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| status | `int(11)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## catering_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| catering_id | `int(10) unsigned` |
| category_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- catering_id references [caterings](#caterings) (id)

---

## batch_recipes

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| count_unit_id | `int(10) unsigned` |
| total_cost | `double(15,2)` |
| total_yield | `double(15,2)` |
| cost | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| recipe_category_id | `int(10) unsigned` |
| directions | `text` |
| category_id | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## batch_recipe_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| batch_recipe_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| inventory_id | `int(10) unsigned` |
| quantity | `double(15,2)` |
| unit_cost | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| ru_units | `double(15,2)` |
| cost | `double(15,2)` |
| recipe_unit | `int(10) unsigned` |
| unit_id | `int(10) unsigned` |

### Relationships
- batch_recipe_id references [batch_recipes](#batch_recipes) (id)

---

## daily_imports

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| filename | `varchar(255)` |
| hash | `varchar(255)` |
| date | `date` |
| cogs | `text` |
| departments | `text` |
| labors | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| date_from | `date` |
| gift_cards | `double(15,2)` |
| discounts | `text` |
| pos_id | `int(10) unsigned` |
| import_report_type_id | `int(10) unsigned` |
| employees | `text` |
| guest_count | `double(15,2)` |
| next | `int(11)` |
| purchases | `text` |
| staff | `text` |
| reference_id | `varchar(255)` |
| expenses | `text` |
| invoice_no | `varchar(255)` |
| admin | `tinyint(1)` |
| department_discounts | `text` |
| vendor | `text` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## sale_guests

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| date | `date` |
| count | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## labor_budgets

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| percent | `double(10,2)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## labor_budget_categories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| labor_budget_id | `int(10) unsigned` |
| category_id | `int(10) unsigned` |
| percent | `double(10,2)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| amount | `double(15,2)` |

### Relationships
- labor_budget_id references [labor_budgets](#labor_budgets) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## quick_books_toggle_accounts

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(191)` |
| hide | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklist_positions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklist_settings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| days | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## recently_imported_reports

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| report_type_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| pos_id | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklist_wizard_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| ordered_from | `int(11)` |
| ordered_station | `int(11)` |
| prepared_position | `int(11)` |
| prepared_station | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklist_wizard_services

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| checklist_wizard_item_id | `int(10) unsigned` |
| checklist_position_id | `int(10) unsigned` |
| station_id | `int(10) unsigned` |
| am | `tinyint(1)` |
| pm | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- checklist_wizard_item_id references [checklist_wizard_items](#checklist_wizard_items) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## inventories

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| ingredient | `varchar(255)` |
| brand | `varchar(255)` |
| category | `varchar(255)` |
| category_id | `int(11)` |
| vendor_code | `varchar(255)` |
| purchase_price | `double(15,2)` |
| purchase_unit_id | `int(10) unsigned` |
| pack_type_measure | `varchar(255)` |
| ptm_per_ipt | `double(15,2)` |
| ipt_per_pu | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| recipe_unit | `int(11)` |
| ru_ptm | `double(15,2)` |
| yield | `double(15,2)` |
| recipe_unit_measure | `int(11)` |
| ru_ptm_measure | `double(15,2)` |
| yield_measure | `double(15,2)` |
| location | `varchar(255)` |
| sub_location | `varchar(255)` |
| sub_location_2 | `varchar(255)` |
| storage | `int(10) unsigned` |
| internal_pack_type | `int(10) unsigned` |
| random | `tinyint(1)` |
| price_per | `double(15,2)` |
| cost_per_ru | `double(15,2)` |
| cost_per_ru_measure | `double(15,2)` |
| price_per_ipt | `double(15,2)` |
| vendor_id | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## inventory_locations

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| inventory_id | `int(10) unsigned` |
| storage | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| location | `int(11)` |
| sub_location | `int(11)` |
| order_guide | `tinyint(1)` |

### Relationships
- inventory_id references [inventories](#inventories) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## projects

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| project | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## sub_locations

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## report_suggestions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| filename | `varchar(255)` |
| hash | `varchar(255)` |
| pos | `varchar(255)` |
| type | `varchar(255)` |
| notes | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| email | `text` |
| status | `int(11)` |
| deleted_at | `timestamp` |
| last_sent | `timestamp` |
| message | `text` |
| sent_count | `int(11)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## api_poster_matches

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| poster_category_id | `int(11)` |
| category_id | `int(11)` |
| deleted_at | `timestamp` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## job_descriptions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| title | `varchar(255)` |
| reports_to | `varchar(255)` |
| description | `text` |
| category_id | `int(10) unsigned` |
| tasks | `text` |
| skills | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## quasar_settings

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| dashboard | `longtext` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## api_poster_transactions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| from | `date` |
| to | `date` |
| transaction | `longtext` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## employees

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| first_name | `varchar(255)` |
| last_name | `varchar(255)` |
| job_id | `int(10) unsigned` |
| type | `int(11)` |
| rate | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| default_pay | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## quick_books_fetch_datas

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| from | `date` |
| to | `date` |
| data | `longtext` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## batch_recipe_locations

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| batch_recipe_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| location_id | `int(10) unsigned` |
| sub_location_id | `int(10) unsigned` |
| item_storage_id | `int(10) unsigned` |
| cost_per_storage_unit | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| cost | `double(15,2)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## hidden_units

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| unit_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- unit_id references [units](#units) (id)
- restaurant_id references [restaurants](#restaurants) (id)

---

## units

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(11)` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| default | `int(11)` |

### Relationships
No relationships.

---

## import_matches

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `text` |
| type | `int(11)` |
| account_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| pos_id | `int(10) unsigned` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## intuits

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| accessTokenKey | `text` |
| refreshTokenKey | `text` |
| QBORealmID | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| company_name | `varchar(191)` |
| last_import | `datetime` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## posters

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| restaurant_id | `int(10) unsigned` |
| access_token | `varchar(255)` |
| expiry | `datetime` |
| account | `varchar(255)` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## api_clover_merchants

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| merchant_id | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## non_expense_items

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| non_expense_id | `int(11)` |
| non_expense_category_id | `int(11)` |
| description | `text` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| invoice_id | `int(10) unsigned` |
| order | `int(11)` |
| credit | `double(15,2)` |
| comps | `tinyint(1)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## stations

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| description | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## checklists_unit

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| name | `varchar(255)` |
| description | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## api_clovers

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| merchant_id | `varchar(255)` |
| employee_id | `varchar(255)` |
| client_id | `varchar(255)` |
| code | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| access_token | `varchar(255)` |
| access_token_created_at | `timestamp` |
| api_token | `varchar(255)` |
| items | `text` |
| map | `text` |
| jobs | `text` |
| employees | `text` |
| company | `varchar(255)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## document_pending_statuses

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## api_links

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| pos_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## invoices

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| invoice_no | `varchar(255)` |
| vendor_id | `int(11)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| sales_tax | `double(15,2)` |
| freight | `double(15,2)` |
| fuel_charge | `double(15,2)` |
| credit | `tinyint(1)` |
| sales_tax_credit | `double(15,2)` |
| freight_credit | `double(15,2)` |
| fuel_charge_credit | `double(15,2)` |
| notes | `text` |
| schedule_id | `int(10) unsigned` |
| comps | `tinyint(1)` |
| deleted_at | `timestamp` |
| sum | `double(15,2)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## comps

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| date | `date` |
| restaurant_id | `int(10) unsigned` |
| comp_category_id | `int(10) unsigned` |
| account_id | `int(10) unsigned` |
| amount | `double(15,2)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| invoice_id | `int(10) unsigned` |
| qbo_type | `varchar(191)` |
| qbo_num | `varchar(191)` |
| qbo_name | `varchar(191)` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## order_guides

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| vendor_id | `int(10) unsigned` |
| days | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
- restaurant_id references [restaurants](#restaurants) (id)

---

## account_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user | `varchar(191)` |
| email | `varchar(191)` |
| type | `int(11)` |
| status | `int(11)` |
| description | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| operator | `int(11)` |
| restaurant_id | `int(11)` |
| notes | `text` |

### Relationships
No relationships.

---

## apis

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| notes | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## api_clovers_matches

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| item_name | `varchar(255)` |
| category_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| type | `int(11)` |

### Relationships
No relationships.

---

## api_clover_webhooks

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| response | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## api_poster_products

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| product_id | `int(11)` |
| poster_category_id | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## backup_files

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| path | `varchar(255)` |
| path_name | `varchar(255)` |
| filename | `varchar(255)` |
| size | `int(11)` |
| backed_up | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| restaurant_id | `int(11)` |

### Relationships
No relationships.

---

## bugs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(11)` |
| user_id | `int(11)` |
| url | `varchar(255)` |
| line | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| method | `varchar(255)` |
| file | `text` |
| message | `text` |

### Relationships
No relationships.

---

## build_sheet_restaurant

### Columns

| Name | Type |
|------|------|
| build_sheet_id | `int(11)` |
| restaurant_id | `int(11)` |

### Relationships
No relationships.

---

## cache

### Columns

| Name | Type |
|------|------|
| key | `varchar(255)` |
| value | `mediumtext` |
| expiration | `int(11)` |

### Relationships
No relationships.

---

## cancelled_archives

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| email | `text` |

### Relationships
No relationships.

---

## checklist_group_restaurants

### Columns

| Name | Type |
|------|------|
| restaurant_id | `int(11)` |
| checklist_id | `int(11)` |
| checklist_group_id | `int(11)` |

### Relationships
No relationships.

---

## checklist_restaurant

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| checklist_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |

### Relationships
No relationships.

---

## checklist_types

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(11)` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| setting | `varchar(255)` |
| default | `int(11)` |

### Relationships
No relationships.

---

## checklist_types_archives

### Columns

| Name | Type |
|------|------|
| id | `int(11)` |
| restaurant_id | `int(11)` |
| name | `varchar(255)` |
| setting | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## common_passwords

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| password | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## communication_preference_types

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| description | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## companies

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| user_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## company_partner_company

### Columns

| Name | Type |
|------|------|
| company_id | `int(10) unsigned` |
| partner_company_id | `int(10) unsigned` |

### Relationships
No relationships.

---

## count_units

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| dry | `tinyint(1)` |
| random | `tinyint(1)` |
| random_weight | `varchar(255)` |
| type | `int(11)` |

### Relationships
No relationships.

---

## currencies

### Columns

| Name | Type |
|------|------|
| id | `int(11)` |
| country | `varchar(100)` |
| currency | `varchar(100)` |
| code | `varchar(25)` |
| symbol | `varchar(25)` |

### Relationships
No relationships.

---

## document_send_mail_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| document_id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| type | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## document_tags

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## document_trees

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(191)` |
| _lft | `int(10) unsigned` |
| _rgt | `int(10) unsigned` |
| parent_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| permanent | `tinyint(1)` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## dropbox_backups

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| folder | `varchar(255)` |
| file | `varchar(255)` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## email_sched_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| schedule_id | `int(10) unsigned` |
| name | `varchar(255)` |
| email | `varchar(255)` |
| timezone | `varchar(255)` |
| date_sent_timezone | `timestamp` |
| date_sent | `timestamp` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## failed_jobs

### Columns

| Name | Type |
|------|------|
| id | `bigint(20) unsigned` |
| connection | `text` |
| queue | `text` |
| payload | `longtext` |
| exception | `longtext` |
| failed_at | `timestamp` |

### Relationships
No relationships.

---

## import_report_types

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| pos_id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| ext | `varchar(255)` |

### Relationships
- pos_id references [pos](#pos) (id)

---

## pos

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| title | `varchar(255)` |

### Relationships
No relationships.

---

## job_description_restaurant

### Columns

| Name | Type |
|------|------|
| job_description_id | `int(11)` |
| restaurant_id | `int(11)` |

### Relationships
No relationships.

---

## login_tokens

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(11)` |
| code | `text` |
| access_token | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## mailbox_inbound_emails

### Columns

| Name | Type |
|------|------|
| id | `bigint(20) unsigned` |
| message_id | `varchar(191)` |
| message | `longtext` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## messages

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| subject | `varchar(255)` |
| type | `int(11)` |
| send_from | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| group | `int(11)` |

### Relationships
No relationships.

---

## mf_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(11)` |
| loggable_id | `int(11)` |
| loggable_type | `varchar(255)` |
| action | `varchar(255)` |
| before | `text` |
| after | `text` |
| created_at | `datetime` |

### Relationships
No relationships.

---

## migrations

### Columns

| Name | Type |
|------|------|
| migration | `varchar(255)` |
| batch | `int(11)` |

### Relationships
No relationships.

---

## model_has_permissions

### Columns

| Name | Type |
|------|------|
| permission_id | `int(10) unsigned` |
| model_type | `varchar(191)` |
| model_id | `bigint(20) unsigned` |

### Relationships
- permission_id references [permissions](#permissions) (id)

---

## permissions

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| guard_name | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## role_has_permissions

### Columns

| Name | Type |
|------|------|
| permission_id | `int(10) unsigned` |
| role_id | `int(10) unsigned` |

### Relationships
- role_id references [roles](#roles) (id)
- permission_id references [permissions](#permissions) (id)

---

## roles

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(191)` |
| guard_name | `varchar(191)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## model_has_roles

### Columns

| Name | Type |
|------|------|
| role_id | `int(10) unsigned` |
| model_type | `varchar(191)` |
| model_id | `bigint(20) unsigned` |

### Relationships
- role_id references [roles](#roles) (id)

---

## oauth_access_tokens

### Columns

| Name | Type |
|------|------|
| id | `varchar(100)` |
| user_id | `bigint(20)` |
| client_id | `int(10) unsigned` |
| name | `varchar(255)` |
| scopes | `text` |
| revoked | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| expires_at | `datetime` |

### Relationships
No relationships.

---

## oauth_auth_codes

### Columns

| Name | Type |
|------|------|
| id | `varchar(100)` |
| user_id | `bigint(20)` |
| client_id | `int(10) unsigned` |
| scopes | `text` |
| revoked | `tinyint(1)` |
| expires_at | `datetime` |

### Relationships
No relationships.

---

## oauth_clients

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `bigint(20)` |
| name | `varchar(255)` |
| secret | `varchar(100)` |
| redirect | `text` |
| personal_access_client | `tinyint(1)` |
| password_client | `tinyint(1)` |
| revoked | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## oauth_personal_access_clients

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| client_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## oauth_refresh_tokens

### Columns

| Name | Type |
|------|------|
| id | `varchar(100)` |
| access_token_id | `varchar(100)` |
| revoked | `tinyint(1)` |
| expires_at | `datetime` |

### Relationships
No relationships.

---

## partner_company_user

### Columns

| Name | Type |
|------|------|
| partner_company_id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |

### Relationships
No relationships.

---

## partner_restaurant_views

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## partner_user_restaurant_accesses

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `bigint(20) unsigned` |
| user_id | `bigint(20) unsigned` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---

## password_resets

### Columns

| Name | Type |
|------|------|
| email | `varchar(255)` |
| token | `varchar(255)` |
| created_at | `timestamp` |

### Relationships
No relationships.

---

## push_logs

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| title | `varchar(191)` |
| body | `text` |
| status | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| read | `tinyint(1)` |
| deleted_at | `timestamp` |
| restaurant_id | `int(11)` |
| user_id | `int(11)` |
| params | `text` |

### Relationships
No relationships.

---

## quasar_page_accesses

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(11)` |
| sales_page_access | `tinyint(1)` |
| purchase_page_access | `tinyint(1)` |
| labor_page_access | `tinyint(1)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## queue

### Columns

| Name | Type |
|------|------|
| id | `bigint(20) unsigned` |
| queue | `varchar(255)` |
| payload | `longtext` |
| attempts | `tinyint(3) unsigned` |
| reserved_at | `int(10) unsigned` |
| available_at | `int(10) unsigned` |
| created_at | `int(10) unsigned` |

### Relationships
No relationships.

---

## quickbooks_options

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| QBORealmID | `varchar(191)` |
| vendors | `text` |
| expense_accounts | `text` |
| terms | `text` |
| customers | `text` |
| taxes | `text` |
| products | `text` |
| payment_accounts | `text` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |
| vendors_expenses | `text` |

### Relationships
No relationships.

---

## recipe_restaurant

### Columns

| Name | Type |
|------|------|
| recipe_id | `int(11)` |
| restaurant_id | `int(11)` |

### Relationships
No relationships.

---

## scripts

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## sessions

### Columns

| Name | Type |
|------|------|
| id | `varchar(255)` |
| user_id | `int(11)` |
| ip_address | `varchar(45)` |
| user_agent | `text` |
| payload | `text` |
| last_activity | `int(11)` |

### Relationships
No relationships.

---

## telescope_entries

### Columns

| Name | Type |
|------|------|
| sequence | `bigint(20) unsigned` |
| uuid | `char(36)` |
| batch_id | `char(36)` |
| family_hash | `varchar(255)` |
| should_display_on_index | `tinyint(1)` |
| type | `varchar(20)` |
| content | `longtext` |
| created_at | `datetime` |

### Relationships
No relationships.

---

## telescope_entries_tags

### Columns

| Name | Type |
|------|------|
| entry_uuid | `char(36)` |
| tag | `varchar(255)` |

### Relationships
- entry_uuid references [telescope_entries](#telescope_entries) (uuid)

---

## telescope_monitoring

### Columns

| Name | Type |
|------|------|
| tag | `varchar(255)` |

### Relationships
No relationships.

---

## tours

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| name | `varchar(255)` |
| code | `varchar(255)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## unit_archives

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| name | `varchar(255)` |
| default | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |

### Relationships
No relationships.

---

## user_restaurant_modules

### Columns

| Name | Type |
|------|------|
| id | `int(10) unsigned` |
| user_id | `int(10) unsigned` |
| restaurant_id | `int(10) unsigned` |
| module_id | `int(11)` |
| created_at | `timestamp` |
| updated_at | `timestamp` |
| deleted_at | `timestamp` |

### Relationships
No relationships.

---
