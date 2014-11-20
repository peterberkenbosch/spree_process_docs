# PR rejection and discussion rules:

This document will describe the rules and guidelines we use to either accept or
deny a pull request. Some rules warrant more discussion from the core team before
it get's accepted.

## 1. Don’t decorate the state machine.
## 2. No callbacks.
## 3. Public API changes will need justification.
## 4. Limit (avoid) adding actions to controllers & models.
## 5. Performance can’t take a hit.
## 6. No additional queries.
## 7. Breaking other specs.
## 8. Use of non-localized strings.
## 9. Destruction or change data.
## 10. Adding new gem dependencies.
## 11. API endpoints need to proper authentication/authorization

# Measure code quality and performance

Before you send a pull request, there are a few things that you can do yourself
to make sure that the above rules are not broken.

You can run the HoundCI checks manually before sending the PR by running `rubocop`
locally. For details on how to use Rubocop see their [readme](https://github.com/bbatsov/rubocop)

Also, we added the [Bullet](https://github.com/flyerhzm/bullet) gem to the sandbox. That way you can test if your changes
introduce performance problems. To use it generate a sandbox and run it on your
localmachine. You will see the bullet reporting on screen, including suggestions
on how to improve the performance issue detected.
