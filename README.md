# AmazonLinux2-Hardening-Ansible

# Why Would I Use This Role?

If you are attempting to obtain compliance against an industry-accepted security standard, like PCI DSS, HIPAA or ISO 27001, then you need to demonstrate that you have applied documented hardening standards against all systems within scope of assessment.

If you are running Amazon Linux, then this role attempts to provide one piece of the solution to the compliance puzzle.

# How to use this role?

If you are considering applying this role to any servers, you should have a basic familiarity with the CIS Benchmark (or other similar benchmarks) and an appreciation for the impact that it may have on a system.

Please take the time to familarise yourself with the standard and with the configurable default values, and exclude any items before applying to a system.

An examples of items that should be immediately considered for exclusion (or at least, for modification of the related default values) include:

3.3.2 and 3.3.3, which by default effectively limit access to the host (including via ssh) to localhost only.



# Options
Tags (and combinations thereof) can be used to run a particular level of the CIS standard, a section, or an individual recommendation. For example:

Run only Level 1 tasks:  ansible-playbook playbook.yml -t level-1

Run only Section 3 tasks: ansible-playbook playbook.yml -t section-3

Run tasks 1.3.1 and 2.2.10 only:  ansible-playbook playbook.yml -t 1.3.1,2.2.10
Run scored tasks only: ansible-playbook playbook.yml -t scored
