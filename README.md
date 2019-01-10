# Arch-US-Reflector-Hook
A reflector hook file for sorting US mirrors

Hook file for Arch Linux's package manager, pacman.
Hooks run at certain points of package installation.  This will run when the pacman-mirrorlist package is installed/updated.
For more on hooks, go to https://wiki.archlinux.org/index.php/Pacman#Hooks.

Requires the reflector package, which allows for sorting your mirror list

Breakdown of flags used:
  | Flag                       | Description                                                          |
  |----------------------------|----------------------------------------------------------------------|
  | --protocol "<protocol>"    | which protocol the mirror uses, usually http or https                |
  | --country "<country name>" | which country the mirrors are based in                               |
  | --latest n                 | n mirrors that were most recently synchronized                       |
  | --age n                    | only return mirrors that have synchronized in the last n hours       |
  | --threads n                | use n threads in sorting mirrors                                     |
  | --sort                     | sort mirrors based on criteria: age, rate, country, score, delay     |
  | --completion-percent n     | use only mirrors that have n% or greater of the total archive synced |
  | --score n                  | sort the top n mirrors based on the mirror score                     |
  | --fastest n                | sort the top n mirrors based on speed                                |
  | --save                     | file to save the mirrorlist to (usually /etc/pacman.d/mirrorlist)    |
