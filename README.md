# Administer user by role

Allows site builders to set up fine-grained permissions for editing and deleting
user accounts by role, and a separate permission for creating user accounts. It
is more specific than Backdrop Core's all-or-nothing 'administer users'
permission, so site builders can set up "sub-admins" with permission to specific
roles.

## Installation

- Install this module using the official [Backdrop CMS instructions](https://backdropcms.org/guide/modules).
- Update permissions on the [permission page](/admin/config/people/permissions).

## Configuration

### Core permissions

**Administer users**
  DO NOT set this for sub-admins. This permission bypasses all of the
  permissions in "Administer Users by Role".

**View user profiles**
  Sub-admins should probably have this permission. Most things work
  without it, but for example with a View showing users, the user name
  will only become a link if this permission is not set.

### Permissions provided by this module

**Access the users overview page**
  See the list of users at `admin/people`.  Only users that can be edited are
  shown.

**Create new users**
  Create users, at `admin/people/create`.

**Edit users with no custom roles**
  Allows editing of any authenticated user that has no custom roles set.

**Edit users with role XXX**
  Allows editing of any authenticated user with the specified role.
  To edit a user with multiple roles, the sub-admin must have permission to
  edit ALL of those roles.  ("Edit users with no custom roles" is NOT needed.)

The permission for cancel work exactly the same as those for edit.

## License

This project is GPL v2 software. See the LICENSE.txt file in this
directory for complete text.

## Maintainers

- [Herb v/d Dool](https://github.com/herbdool)
- Other maintainers are encouraged and welcome.

## Credits

Ported to Backdrop by Herb v/d Dool from [Drupal 7](https://www.drupal.org/project/administerusersbyrole).

Drupal maintainers:

- [AdamPS](https://www.drupal.org/u/adamps)
- [mrfelton](https://www.drupal.org/u/mrfelton)
- [smokris](https://www.drupal.org/u/smokris)
- [joelpittet](https://www.drupal.org/u/joelpittet)
