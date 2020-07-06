# dt-oracleebs-config
BizOpsConfigurator for Oracle EBS

## Custom Service Detection
### customService_oracleformslistenerservlet.json
Creates a custom service to monitor the Oracle Forms ListenerServlet calls on the Java tier.  This represents the passing of forms data between the Java tier and the native forms runtime engine.

## Request Attributes
### requestAttribute_OAFunc.json
Captures the OAFunc query parameter on web request services.  The OAFunc can be used to identify context of calls to OA.jsp requests.

### requestAttribute_functionid.json
Captures the function_id query parameter on web request services.  The function_id can be used to identify context of calls to RF.jsp requests.

### requestAttribute_page.json
Captures the page query parameter on web request services.  The page query parameter can be used to identify context of calls to OA.jsp requests.

### requestAttribute_username.json
Captures the username HTTP POST parameter on web request services.  The username parameter can be used to identify the user of web requests.  This parameter is not useful when using SSO, as SSO will pass the SSO token in this field instead of the actual user name.

## Global Request Naming Rules
### serviceRequestNamingRule_OA.jsp.json
Request naming rule to change the request name of calls to /OA.jsp to include the value of OAFunc (when detected).  This is useful for identifying performance and establishing baselines for each unique value of OAFunc on the /OA.jsp page.

### serviceRequestNamingRule_RF.jsp.json
Request naming rule to change the request name of calls to /RF.jsp to include the value of function_id (when detected).  This is useful for identifying performance and establishing baselines for each unique value of function_id on the /RF.jsp page.
