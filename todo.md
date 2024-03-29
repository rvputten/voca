Complete tests
==============
None.
    Entry::get_by_name()
    main::add_numbers()
    Db::add_entry()
    Db::add_or_modify_entry()

Ideas for vocabulary
====================
runs stats() at end of program
allow editing and adding words with translations
for stats, count words - not translations
add regular conjugations
show conjugations for a verb
    c tener
shorter prompt with more functionality
    "press <h> for help"
have several date columns
  create date
  history of "remembered" and "don't know" answers
    rerun after one day
    another rerun after 5 days
    another rerun after 30 days
automatically detect more inflections
  pollito -> pollo
add search term to every word and show all previous search terms
create lock file to prevent running multiple instances
make db own project
monitor clipboard and search for words in personal or vocabulary dictionary
    present a list of words found in the clipboard
search English results if no Spanish results are found (or are very few)
    with 'e search_term'
make naming of searches more consistent
    find by <p> and return <r> where
	<p> can be row_id, row_ids, name, name+value, single predicate or multiple predicates
	<r> can be
	    row_id (first entry)
		use later for performance reasons. discard now.
	    row_ids (all entries)
	    data (single)
	    data (multiple)
	    entry (first entry)
	    entries (all entries)
	    bool (true/false - test for existance)
		replace with Option<row_id>
    proposed names
	find_first_row_id_by_name
	find_entries_by_name
	find_entries_by_row_id
	find_row_id_by_predicates
	find_row_ids_by_predicates
	find_entry_by_predicates
	find_entries_by_predicates
	check_by_name_value

remove "set" = "en-es"
check for existance before inserting
store in hashmap by row\_id
    lookup of row\_ids is the slowest operation at the moment
guess inflexions
    cubren -> cubrir
    vuelve -> volver (come back)
    empieza -> empezar (begin, start)
    consiguen -> consegir (etwas erlangen)
    cierran -> cerrar (abschließen, sperren)
    pide -> pedir (jmd. um etw. bitten)
    pasaban -> pasar (vorübergehen)
    fue -> ir/ser/irse (gehen, sein, weggehen)
    contó -> contar (zählen)
    tienden -> tender (to tend to)
    predice -> predecir (to predict)
    haría -> hacer
    retuvieron -> retener (to retain)
make useful browsable documentation of source code

Done
====
exclude more granular results from broader results
show recent searches
    hand pick search results and store in personal dictionary
    implementation
	every row shown gets a line number
	line numbers are overwritten on subsequent searches
	when the user types a line number, the word is saved in the dictionary
if search unsuccessful, remove last letter until a result is found
count number of words in dictionary
when limiting search results, count multiple translations
count how often a word has been added to the dictionary
record last addition date to the dictionary
    and sort by date addition
search personal db
    to list all words beginning with 'ca', enter: 'p ca'
add conjugations to personal db
replace "name" and "value" with "word" and "translation" in main.rs where appropriate
