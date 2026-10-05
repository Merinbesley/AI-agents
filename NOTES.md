# Engineering Notes

## Chapter 2: Delegation Exercise

### 1. Task I Would Delegate
- **Task:** Validate CLI input in add command to reject negative/zero amounts and empty categories.
- **Bounded:** [Fact] Touches only src/ledgerlite/cli.py and 	ests/test_cli.py.
- **Verifiable:** [Fact] Verified with python scripts/verify.py and checking exit code 2 on invalid input.
- **Reversible:** [Fact] Reversible via git checkout -- ..
- **Understood:** [Fact] Strip whitespace, parse amount with Decimal, print to stderr and return exit code 2 if invalid.

### 2. Task I Would NOT Delegate
- **Task:** Redesign data storage format and implement third-party cloud sync with encryption.
- **Failing Question:** Understood and Bounded.
- **Reason:** [Inference] Security architecture requires human judgment; an agent might introduce unpinned dependencies or leak secrets.

### Reflection
- **Habit missing in student projects:** Code reviewing agent diffs and least-privilege permissions.
- **Reason:** [Inference] Students often focus only on whether an assignment passes tests, not on security or clean git history.
