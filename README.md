# mmezcal-II
Cuando las segundas partes son mejores que las anteriores!


# full parameters:
params = {
  "q": "coffee",
  "location": "Location Requested", 
  "device": "desktop|mobile|tablet",
  "hl": "Google UI Language",
  "gl": "Google Country",
  "safe": "Safe Search Flag",
  "num": "Number of Results",
  "start": "Pagination Offset",
  "api_key": "Your SERP API Key", 
  # To be match
  "tbm": "nws|isch|shop", 
  # To be search
  "tbs": "custom to be search criteria",
  # allow async request
  "async": "true|false",
  # output format
  "output": "json|html"
}

# define the search search
search = GoogleSearch(params)

# override an existing parameter
search.params_dict["location"] = "Portland"

# parse results
#  as python Dictionary
	dict_results = search.get_dict()
#  as JSON using json package
	json_results = search.get_json()
#  as dynamic Python object
	object_result = search.get_object()
