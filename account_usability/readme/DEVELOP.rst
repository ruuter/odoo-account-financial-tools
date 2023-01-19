Detailled Module Category Changes (ir.module.category)
======================================================

1) base.module_category_accounting_accounting
---------------------------------------------

*CE Without that module*
-> Complete Name : Invoicing

*CE With that module / EE*
-> Complete Name: **Accounting**


Detailled Groups Changes (res.groups)
=====================================

1) account.group_account_invoice
--------------------------------

*CE Without that module*
-> Complete Name : Invoicing / Billing
-> Parent Category : base.module_category_accounting_accounting
-> Implies : base.group_user

*CE With that module / EE*
-> Complete Name: **Accounting** / Billing


2) account.group_account_readonly
---------------------------------

*CE Without that module*
-> Complete Name : Technical / Show Accounting Features - Readonly
-> Parent : base.module_category_hidden
-> Implies : base.group_user

*CE With that module / EE*
-> name: **Accounting / Read-only**
-> Parent Category: **base.module_category_accounting_accounting**


3) account.group_account_user
-----------------------------

*CE Without that module*
-> Complete Name : Technical / Show Full Accounting Features
-> Parent : base.module_category_hidden
-> Implies : account.group_account_invoice, account.group_account_readonly

*CE With that module / EE*
-> name: **Accounting / Bookkeeper**
-> Parent Category: **base.module_category_accounting_accounting**


4) account.group_account_manager
--------------------------------

*CE Without that module*
-> Complete Name : Invoicing / Billing Administrator
-> Parent : base.module_category_accounting_accounting
-> Implies : account.group_account_invoice

*CE With that module / EE*
-> name: **Accounting / Accountant**
-> Implies : **account.group_account_user**
