# tecnica24_find_apex_id
Function to find an apex export id in apex schema tables

# why
In Oracle APEX #orclapex exports files we have calls to api like wwv_flow_api.create_page. APEX sometimes uses parameters like p_reference_id 
that we can not set its origin: we can not know if there is a reference to a template, to a theme, to an authentication scheme, and so on.

We are creating T24_CREATE_APPLICATION and need to understand certain 'p_reference_id' that are used in apex exports.

# method
Lets search in all tables and columns in schema APEX_nnnnnn for ID value.

# example
SELECT T24_FIND_APEX_ID( '210100', '1996914646461572319' ) APEX_ID FROM DUAL
