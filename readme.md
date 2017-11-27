## Following Reports and the Queries they are based on

1. Report 1 - information about all the suppliers who are employees and are currently active
    
SELECT AS1.*
FROM ap_suppliers AS1
WHERE AS1.enabled_flag = 'Y'
AND NVL(AS1.end_date_active,SYSDATE+1) > SYSDATE
AND AS1.employee_id IS NOT NULL
