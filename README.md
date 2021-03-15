# Prevent Duplicate Inherited Membership

Use-case: User having a single "Family" relationship type to join all family members.

- Membership type is created with "Family" rel type.
- Father is connected to Child with this rel type.
- Similarly, Mother is connected to Child with the same relationship type.
- When a membership is created on father's contact, this is inherited to Mother and Child's contact.
- Now, when a relationship is created between Mother and Father (same rel type), the membership is duplicated on Mother and Child.
- This extension is to prevent such duplciates to be created.
- Before creating the inherited membership, it avoid the creation if the contact already has an inherited membership with the same type.

The extension is licensed under [AGPL-3.0](LICENSE.txt).

## Requirements

* PHP v7.0+
* CiviCRM

## Installation (Web UI)

This extension has not yet been published for installation via the web UI.

## Installation (CLI, Zip)

Sysadmins and developers may download the `.zip` file for this extension and
install it with the command-line tool [cv](https://github.com/civicrm/cv).

```bash
cd <extension-dir>
cv dl nz.co.fuzion.duplicatemembership@https://github.com/fuzionnz/nz.co.fuzion.duplicatemembership/archive/master.zip
```

## Installation (CLI, Git)

Sysadmins and developers may clone the [Git](https://en.wikipedia.org/wiki/Git) repo for this extension and
install it with the command-line tool [cv](https://github.com/civicrm/cv).

```bash
git clone https://github.com/fuzionnz/nz.co.fuzion.duplicatemembership.git
cv en duplicatemembership
```

## Known Issues

It works on all membership types. A possible improvement will be to configure this on Membership type form.