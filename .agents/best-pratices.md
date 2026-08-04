# SuiteScript best pratices

[refrences](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_N3361037.html)

## Naming conventions

Variables and Constants:

- Avoid using a single character as a variable name.

- Name your variables to identify the data type and describe the data stored in the variable. For example,
  - String variables - prefix with "st", such as stTitle

  - Integer variables - prefix with "int", such as intTotalCount

  - Float variables - prefix with "fl", such as flPrice

  - Boolean variables - prefix with "b", such as bIsDone

  - Array variables - prefix with "arr", such as arrPhoneCalls

  - Object variables - prefix with "Obj", such as ObjNewPet

  - Record variables - prefix with "rec", such as recCustomer

  - Date variables - prefix with "dt", such as dtFirstBillingDate

- Local variable scope is only within the function. Use standard camelCase naming.

- Global variable scope is within the whole file or more files if declared under included library. Use a variable in upper case spaced by underscore.

- To represent a pseudo constant, use a variable in upper case spaced by underscore. Constants are to be used to make code more readable.

IDs:

- For IDs, enter all record, field, sublist, tab, and subtab IDs in lower case. Prefix all custom script IDs and deployment IDs with an underscore (\_).

## File names

- If you write SuiteScript code for multiple accounts, consider using the following file name convention: `<Company Name/Abbreviation>_<Script Type>_<Requirement Description>.js`.

For example, MyCompany_CS_SetTaxable.js.The following are suggested Script Types:

- CS - client scripts

- UE - user events

- SL - Suitelet

- RL - RESTlet

- PL - Portlet

- SC - Scheduled

- MR - Map/Reduce

- Gl - SuiteGL

- WA - Workflow Action

- MU - Mass Update

- BI - Bundle Installation
